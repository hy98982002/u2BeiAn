<template>
  <div class="home-page">
    <!-- 轮播图区域 -->
    <!-- 移除margin-top: 60px，让轮播图紧贴导航栏 -->
    <div class="hero-section d-none d-md-block">
      <HeroCarousel />
    </div>

    <!-- 课程专区 -->
    <!-- 桌面端：距离轮播图6px；手机端：从导航栏下方开始 -->
    <div class="course-section-wrapper" style="padding-top: 6px">
      <CampSection :show-popular-tags="true" :initial-display-count="8" />
    </div>

    <!-- 就业模块 -->
    <EmploymentSection />

    <!-- 作品展示模块 -->
    <!-- <WorksShowSection /> -->

    <!-- 页脚 -->
    <footer class="footer py-5" role="contentinfo">
      <div class="container">
        <div class="text-center">
          <p class="mb-2">DoviAI 是一家为就业者提供最新职场技术的在线交流平台。</p>
          <p>网站呈现内容之版权均归 小木偶（天津）文化科技有限公司所有 <a href="https://beian.miit.gov.cn/" target="_blank">津ICP备2024023837号-2</a></p>
        </div>
      </div>
    </footer>
  </div>
</template>

<script setup lang="ts">
import { onMounted } from 'vue'
import HeroCarousel from '../components/HeroCarousel.vue'
import CampSection from '../components/CampSection.vue'
import EmploymentSection from '../components/EmploymentSection.vue'
import WorksShowSection from '../components/WorksShowSection.vue'
import { useUIStore } from '../store/uiStore'

// 导入图片资源
import logoImg from '@/assets/icons/logo.png'

const uiStore = useUIStore()

onMounted(() => {
  // 设置当前导航项
  uiStore.setCurrentNavItem('home')

  // 初始化AOS动画库（如果需要的话）
  console.log('首页已加载')
})
</script>

<style scoped>
.home-page {
  position: relative;
}

/* 通用样式 */
.section-title {
  font-size: 3rem;
  font-weight: 700;
  margin-bottom: 1rem;
  position: relative;
}

.title-highlight {
  background: linear-gradient(135deg, #1e7f98, #2a9bb8);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
  display: block;
}

.title-subtitle {
  font-size: 1.2rem;
  color: #666;
  font-weight: 400;
  display: block;
  margin-top: 0.5rem;
}

.section-description {
  font-size: 1.1rem;
  color: #666;
  max-width: 600px;
  margin: 0 auto;
  line-height: 1.6;
}

/* 页脚样式 */
.footer {
  background: #1a1a1a;
  color: #ccc;
}

.footer-title {
  color: white;
  font-weight: 600;
  margin-bottom: 1rem;
}

.footer-text {
  line-height: 1.6;
  margin-bottom: 1.5rem;
}

.footer-links {
  list-style: none;
  padding: 0;
}

.footer-links li {
  margin-bottom: 0.5rem;
}

.footer-links a {
  color: #ccc;
  text-decoration: none;
  transition: color 0.3s ease;
}

.footer-links a:hover {
  color: #1e7f98;
}

.social-links {
  display: flex;
  gap: 1rem;
}

.social-links .social-link {
  width: 40px;
  height: 40px;
  background: rgba(255, 255, 255, 0.1);
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  color: #ccc;
  transition: all 0.3s ease;
}

.social-links .social-link:hover {
  background: #1e7f98;
  color: white;
  transform: translateY(-2px);
}

.contact-info p {
  margin-bottom: 0.5rem;
  color: #ccc;
}

.contact-info i {
  color: #1e7f98;
  margin-right: 0.5rem;
  width: 16px;
}

.footer-divider {
  border-color: rgba(255, 255, 255, 0.1);
  margin: 2rem 0;
}

.footer-copyright {
  color: #999;
  margin: 0;
}

.footer-links-inline {
  display: flex;
  gap: 1.5rem;
  justify-content: flex-end;
}

.footer-links-inline a {
  color: #999;
  text-decoration: none;
  font-size: 0.9rem;
}

.footer-links-inline a:hover {
  color: #1e7f98;
}

/* 响应式设计 */
@media (max-width: 768px) {
  .section-title {
    font-size: 2.2rem;
  }

  /* 手机端：轮播图隐藏时，课程区域需要顶部间距 */
  .course-section-wrapper {
    margin-top: 60px !important; /* 导航栏高度 */
    padding-top: 20px !important; /* 额外间距 */
  }

  .footer-links-inline {
    flex-direction: column;
    gap: 0.5rem;
    text-align: left;
  }
}

@media (max-width: 576px) {
  .section-title {
    font-size: 1.8rem;
  }

  .title-subtitle {
    font-size: 1rem;
  }
}

/* 按钮样式 */
.btn-tech-blue {
  background: linear-gradient(135deg, #1e7f98, #2a9bb8);
  border: none;
  border-radius: 50px;
  padding: 15px 40px;
  font-weight: 600;
  font-size: 1.1rem;
  letter-spacing: 0.5px;
  transition: all 0.3s ease;
  box-shadow: 0 8px 25px rgba(30, 127, 152, 0.3);
  color: white;
}

.btn-tech-blue:hover {
  background: linear-gradient(135deg, #166d84, #228ba1);
  transform: translateY(-3px);
  box-shadow: 0 12px 35px rgba(30, 127, 152, 0.4);
  color: white;
}

.btn-outline-tech-blue {
  border: 2px solid #1e7f98;
  color: #1e7f98;
  background: rgba(255, 255, 255, 0.8);
  border-radius: 50px;
  padding: 13px 38px;
  font-weight: 600;
  font-size: 1.1rem;
  letter-spacing: 0.5px;
  transition: all 0.3s ease;
  backdrop-filter: blur(10px);
  -webkit-backdrop-filter: blur(10px);
}

.btn-outline-tech-blue:hover {
  background: #1e7f98;
  border-color: #1e7f98;
  color: white;
  transform: translateY(-3px);
}
</style>
