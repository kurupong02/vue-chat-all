<template>
  <div class="sidebars">
    <div class="sidebar-content">
      <div class="sidebar-logo" @click="showCheck = !showCheck">
        <font-awesome-icon icon="user-secret"></font-awesome-icon>
      </div>
      <div class="sidebar-menu">
        <div
          class="sidebar-item"
          :class="{ active: menuActive === index }"
          @click="menuActive = index"
          v-for="(menu, index) in menus"
          :key="menu.name"
        >
          <font-awesome-icon icon="user-secret" />
          <div class="sidebar-item-text-tooltip">{{ menu.name }}</div>
          <div :class="{ 'sidebar-item-line-active': menuActive === index }" />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Sidebar",
  data: function() {
    return {
      menuActive: 0,
      menus: [
        {
          name: "meun1",
          path: "/"
        },
        {
          name: "meun1",
          path: "/"
        },
        {
          name: "meun1",
          path: "/"
        },
        {
          name: "meun1",
          path: "/"
        }
      ]
    };
  }
};
</script>

<style scoped>
.sidebars {
  width: 60px;
}
.sidebar-content {
  color: #fff;
  width: 60px;
  position: absolute !important;
  z-index: 9001;
  height: 100%;
  left: 0;
  top: 0;
  background: #1c263d;
  box-shadow: 0 0 2px 0 rgba(0, 0, 0, 0.06);
  display: flex;
  align-items: flex-start;
  justify-content: space-between;
  flex-direction: column;
}
.sidebar-logo {
  display: -webkit-box;
  display: -ms-flexbox;
  display: flex;
  align-items: center;
  justify-content: center;
  width: 100%;
  padding: 25px 0;
  min-height: 80px;
}
.sidebar-menu {
  overflow-x: hidden;
  width: 100%;
  flex-grow: 1;
  display: -webkit-box;
  display: -ms-flexbox;
  display: flex;
  align-items: flex-start;
  justify-content: flex-start;
  flex-direction: column;
}

.sidebar-item-text-tooltip {
  position: fixed;
  left: 80px;
  opacity: 0;
  pointer-events: none;
  transition: all 0.25s ease;
  font-size: 0.85rem;
  white-space: nowrap;
  z-index: 1000;
}

.sidebar-item:hover .sidebar-item-text-tooltip {
  opacity: 1;
  left: 70px;
  color: #000;
  transition-delay: 0.7s;
}

.active:hover .sidebar-item-text-tooltip {
  opacity: 1;
  left: 70px;
  color: #3eaf7c;
  transition-delay: 0.7s;
}

.sidebar-menu .active {
  color: #3eaf7c;
}

.sidebar-item {
  height: 57px;
  width: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
  position: relative;
  cursor: pointer;
}

.sidebar-item-line-active {
  position: absolute;
  left: 0;
  top: 0;
  width: 10px;
  height: 100%;
  background: #3eaf7c;
  border-radius: 0 20px 20px 0;
  transform: translate(-6px);
  transition: all 0.25s ease;
  z-index: 60;
}
</style>
