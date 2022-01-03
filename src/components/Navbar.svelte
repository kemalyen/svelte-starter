  <script lang="ts">
    import {
      Collapse,
      Navbar,
      NavbarToggler,
      NavbarBrand,
      Nav,
      NavItem,
      NavLink,
      Dropdown,
      DropdownToggle,
      DropdownMenu,
      DropdownItem
    } from 'sveltestrap';

    let isOpen = false;

    function handleUpdate(event) {
      isOpen = event.detail.isOpen;
    }
  </script>

  <Navbar color="dark" dark expand="md">
    <NavbarBrand href="/">sveltestrap</NavbarBrand>
    <NavbarToggler on:click={() => (isOpen = !isOpen)} />
    <Collapse {isOpen} navbar expand="md" on:update={handleUpdate}>
      <Nav class="ms-auto" navbar>
        <NavItem>
          <NavLink href="/events">Events</NavLink>
        </NavItem>
        <NavItem>
          <NavLink href="/tasks">Tasks</NavLink>
        </NavItem>
        <NavItem>
          <NavLink href="/schedules">Schedules</NavLink>
        </NavItem>
        <NavItem>
          <NavLink href="/users">Users</NavLink>
        </NavItem>
        <NavItem>
          <NavLink href="/settings">Settings</NavLink>
        </NavItem>
        <NavItem>
          <NavLink href="/profile">Profile</NavLink>
        </NavItem>
        <NavItem>
          <NavLink href="/logout">Log Out</NavLink>
        </NavItem>
      </Nav>
    </Collapse>
  </Navbar>