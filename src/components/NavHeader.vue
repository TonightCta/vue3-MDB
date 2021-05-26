<template lang="html">
  <div class="">
    <MDBNavbar expand="lg" light bg="light" container>
      <MDBNavbarBrand href="#">
        <img
          src="https://mdbootstrap.com/img/logo/mdb-transaprent-noshadows.png"
          height="30"
          alt=""
          loading="lazy"
        />
      </MDBNavbarBrand>
      <MDBNavbarToggler
        @click="collapse1 = !collapse1"
        target="#navbarSupportedContent"
      ></MDBNavbarToggler>
      <MDBCollapse v-model="collapse1" id="navbarSupportedContent">
        <MDBNavbarNav class="mb-2 mb-lg-0">
          <MDBNavbarItem to="#" active>
            首页
          </MDBNavbarItem>
          <MDBNavbarItem href="#">
            调研
          </MDBNavbarItem>
          <MDBNavbarItem>
            <!-- Navbar dropdown -->
            <MDBDropdown class="nav-item" v-model="dropdown1">
              <MDBDropdownToggle
                tag="a"
                class="nav-link"
                @click="dropdown1 = !dropdown1"
                >Dropdown</MDBDropdownToggle
              >
              <MDBDropdownMenu aria-labelledby="dropdownMenuButton">
                <MDBDropdownItem href="#">Action</MDBDropdownItem>
                <MDBDropdownItem href="#">Another Action</MDBDropdownItem>
                <MDBDropdownItem href="#"
                  >Something else here</MDBDropdownItem
                >
              </MDBDropdownMenu>
            </MDBDropdown>
          </MDBNavbarItem>
          <MDBNavbarItem to="#">
            月报
          </MDBNavbarItem>
        </MDBNavbarNav>
        <!-- Search form -->
        <form class="d-flex input-group w-auto">
          <input
            type="search"
            class="form-control"
            placeholder="请输入"
            aria-label="Search"
          />
          <MDBBtn outline="primary">
            搜索
          </MDBBtn>
        </form>
      </MDBCollapse>
    </MDBNavbar>
  </div>
</template>

<script>
import { defineComponent,ref } from 'vue';
import {
  MDBBtn,
  MDBNavbar,
  MDBNavbarToggler,
  MDBNavbarBrand,
  MDBNavbarNav,
  MDBNavbarItem,
  MDBCollapse,
  MDBDropdown,
  MDBDropdownToggle,
  MDBDropdownMenu,
  MDBDropdownItem
} from 'mdb-vue-ui-kit'
export default defineComponent({
  name:'NavHeader',
  components:{
    MDBBtn,
    MDBNavbar,
    MDBNavbarToggler,
    MDBNavbarBrand,
    MDBNavbarNav,
    MDBNavbarItem,
    MDBCollapse,
    MDBDropdown,
    MDBDropdownToggle,
    MDBDropdownMenu,
    MDBDropdownItem
  },
  setup(){
    const collapse1 = ref(false);
    const dropdown1 = ref(false);
    return{
      collapse1,
      dropdown1
    }
  }
})
</script>

<style lang="scss" scoped>

</style>
