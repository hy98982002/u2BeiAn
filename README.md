# UAI Education Platform

> A modern, full-stack online education platform built with Vue 3 and Django REST Framework

[![Vue 3](https://img.shields.io/badge/Vue-3.5.17-4FC08D?style=flat&logo=vue.js)](https://vuejs.org/)
[![Django](https://img.shields.io/badge/Django-5.2.4-092E20?style=flat&logo=django)](https://www.djangoproject.com/)
[![TypeScript](https://img.shields.io/badge/TypeScript-5.8.3-3178C6?style=flat&logo=typescript)](https://www.typescriptlang.org/)
[![Bootstrap](https://img.shields.io/badge/Bootstrap-5.3.6-7952B3?style=flat&logo=bootstrap)](https://getbootstrap.com/)

## ✨ Features

### 🎓 Course Management
- **Multi-stage Learning Path**: Structured courses from beginner to advanced levels
- **Interactive Content**: Rich multimedia lessons with video, images, and interactive elements
- **Progress Tracking**: Real-time learning progress monitoring
- **Course Reviews**: Student feedback and rating system

### 🛒 E-commerce Integration
- **Shopping Cart**: Add multiple courses to cart
- **Secure Payments**: Integrated payment processing
- **Order Management**: Complete order lifecycle management
- **User Dashboard**: Personal learning and purchase history

### 🔐 Authentication & Authorization
- **JWT Authentication**: Secure token-based authentication
- **RBAC System**: Role-based access control with fine-grained permissions
- **User Profiles**: Comprehensive user management system
- **Security Audit**: Complete operation logging and security monitoring

### 📱 Modern UI/UX
- **Responsive Design**: Mobile-first approach using Bootstrap 5
- **Interactive Components**: Star ratings, carousels, modals, and more
- **Accessibility**: WCAG compliant interface
- **Performance Optimized**: Fast loading with Vite build system

## 🚀 Quick Start

### Prerequisites
- **Node.js** >= 18.0.0
- **Python** >= 3.12
- **MySQL** >= 8.4.5 (SQLite for development)

### Installation

#### Frontend Setup

cd frontend
npm install
npm run dev

The frontend will be available at `http://localhost:5173`

#### Backend Setup

cd backend
python -m venv venv
source venv/bin/activate  # Windows: venv\Scriptsctivate
pip install -r requirements.txt
python manage.py migrate
python manage.py createsuperuser
python manage.py runserver

The backend API will be available at `http://localhost:8000`

## 🛠 Tech Stack

### Frontend
| Technology | Version | Purpose |
|------------|---------|---------|
| **Vue 3** | 3.5.17 | Progressive JavaScript framework |
| **TypeScript** | 5.8.3 | Type-safe JavaScript development |
| **Vite** | 7.0.0 | Fast build tool and dev server |
| **Pinia** | 3.0.3 | State management |
| **Vue Router** | 4.5.1 | Client-side routing |
| **Bootstrap** | 5.3.6 | UI framework and responsive design |
| **Vue I18n** | 11.1.9 | Internationalization |

### Backend
| Technology | Version | Purpose |
|------------|---------|---------|
| **Django** | 5.2.4 | Web framework |
| **Django REST Framework** | 3.16.0 | API development |
| **Django SimpleJWT** | 5.5.0 | JWT authentication |
| **MySQL Client** | 2.0.2 | Database connectivity |
| **Django CORS Headers** | 4.7.0 | Cross-origin resource sharing |
| **drf-yasg** | 1.21.10 | API documentation |

## 📁 Project Structure


UAI_project/
├── 📁 frontend/                    # Vue 3 Frontend Application
│   ├── 📁 src/
│   │   ├── 📁 assets/             # Static Assets
│   │   │   ├── 📁 icons/          # Logo and icon resources
│   │   │   └── 📁 images/         # Course covers and business images
│   │   ├── 📁 components/         # Reusable Vue Components
│   │   │   ├── 📁 cart/           # Shopping cart components
│   │   │   ├── 📁 order/          # Order processing components
│   │   │   └── 📁 personCenter/   # User profile components
│   │   ├── 📁 views/              # Page-level components
│   │   ├── 📁 store/              # Pinia state management
│   │   ├── 📁 router/             # Vue Router configuration
│   │   ├── 📁 types/              # TypeScript type definitions
│   │   └── 📁 utils/              # Utility functions
│   ├── 📄 package.json            # Dependencies and scripts
│   └── 📄 vite.config.ts          # Vite configuration
├── 📁 backend/                     # Django Backend Application
│   ├── 📁 apps/                   # Django application modules
│   │   ├── 📁 users/              # User management
│   │   ├── 📁 courses/            # Course system
│   │   ├── 📁 cart/               # Shopping cart
│   │   ├── 📁 orders/             # Order processing
│   │   ├── 📁 learning/           # Learning progress
│   │   ├── 📁 reviews/            # Review system
│   │   └── 📁 system/             # System functionality
│   ├── 📄 requirements.txt        # Python dependencies
│   └── 📁 uai_backend/            # Django project settings
└── 📁 docs/                       # Project documentation
    ├── 📄 PRD-Management.md         # PRD导航和管理文档
    ├── 📄 prd.md                    # SEO/AEO优化PRD v6.0
    ├── 📄 core-business-prd-v7.md   # 核心业务功能PRD v7.0
    └── 📄 UAI_Unified_PRD_v5.0.md   # 统一PRD v5.0 (历史文档)

## 📋 产品规划文档

### 🎯 PRD文档导航

本项目采用**模块化PRD管理**，不同领域的产品需求分别管理：

| PRD文档 | 版本 | 专注领域 | 状态 | 链接 |
|---------|------|----------|------|------|
| **SEO/AEO优化** | v6.0 | 搜索引擎优化和流量获取 | ✅ 完成 | [查看文档](docs/prd.md) |
| **核心业务功能** | v7.0 | 教育产品功能和用户体验 | ✅ 完成 | [查看文档](docs/core-business-prd-v7.md) |
| **统一PRD** | v5.0 | 整体产品框架 | 📋 历史版本 | [查看文档](docs/UAI_Unified_PRD_v5.0.md) |

### 📖 如何使用PRD文档

1. **开发团队**: 先查看 [PRD管理文档](docs/PRD-Management.md) 了解整体架构
2. **SEO优化**: 参考 [SEO/AEO优化PRD v6.0](docs/prd.md) 
3. **业务功能**: 参考 [核心业务功能PRD v7.0](docs/core-business-prd-v7.md)
4. **架构设计**: 基于PRD要求进行技术架构设计

### 🚀 实施建议

- **Phase 1**: 优先实施核心业务功能 (PRD v7.0)
- **Phase 2**: 基于稳定的核心功能实施SEO优化 (PRD v6.0)
- **并行开发**: 两个PRD可由不同团队并行开发

> 📝 **详细的PRD依赖关系、实施计划请查看**: [PRD管理文档](docs/PRD-Management.md)

## 🔧 Development Commands

### Frontend Commands

npm run dev           # Start development server
npm run build         # Production build
npm run build:check   # Build with TypeScript checking
npm run type-check    # TypeScript type checking only
npm run preview       # Preview production build


### Backend Commands

python manage.py runserver        # Start Django development server
python manage.py makemigrations   # Create database migrations
python manage.py migrate          # Apply database migrations
python manage.py createsuperuser  # Create admin user
python manage.py collectstatic    # Collect static files


## 🎨 Asset Management

### Image Organization
- **Icons**: `frontend/src/assets/icons/` - Logo and UI icons
- **Course Images**: `frontend/src/assets/images/` - Course covers and content

### Naming Convention
Course covers follow the pattern: `{stage}-{course}-cover.{ext}`
- **Stages**: `tiyan` (trial) | `rumen` (beginner) | `jingjin` (intermediate) | `shizhan` (practical) | `xiangmuluodi` (project)
- **Courses**: `python` | `photoshop` | `xuhuan` (loop) | etc.

### Usage Example

<script setup lang="ts">
import logoImg from '@/assets/icons/logo.png'
import courseImg from '@/assets/images/tiyan-python-cover.jpg'
</script>

<template>
  <img :src="logoImg" alt="UAI Logo" />
  <img :src="courseImg" alt="Python Trial Course" />
</template>


## 🌐 API Documentation

All API endpoints follow RESTful conventions and return responses in this format:

{
  "status": 200,
  "data": {},
  "msg": "Success"
}


### Base URL
- **Development**: `http://localhost:8000/api/`
- **Authentication**: JWT tokens via `/api/token/`

### Core Endpoints
- `GET /api/courses/` - List all courses
- `POST /api/cart/` - Add item to cart
- `GET /api/orders/` - User orders
- `POST /api/users/register/` - User registration
- `POST /api/token/` - JWT authentication

## 🧪 Testing & Quality

### Code Quality
- **TypeScript**: Full type safety for frontend
- **ESLint**: Code linting and formatting
- **Django Tests**: Comprehensive backend testing
- **Security**: OWASP security practices

### Development Workflow
1. **Development**: Local development with hot reload
2. **Type Checking**: Automated TypeScript validation
3. **Code Review**: Pull request workflow
4. **Testing**: Automated test suites
5. **Deployment**: Production-ready builds

## 🤝 Contributing

We welcome contributions! Please follow these steps:

1. **Fork** the repository
2. **Create** a feature branch (`git checkout -b feature/amazing-feature`)
3. **Commit** your changes (`git commit -m 'Add amazing feature'`)
4. **Push** to the branch (`git push origin feature/amazing-feature`)
5. **Open** a Pull Request

### Development Guidelines
- Follow **Vue 3 Composition API** patterns
- Use **TypeScript** for type safety
- Follow **Django REST** conventions
- Maintain **Bootstrap 5** styling consistency
- Write **meaningful commit messages**
- Add **comprehensive tests**

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- **Vue.js Team** - For the amazing Vue 3 framework
- **Django Software Foundation** - For the robust Django framework
- **Bootstrap Team** - For the comprehensive UI toolkit
- **Open Source Community** - For the countless libraries and tools

---

<div align="center">
  <p><strong>Built with ❤️ for modern online education</strong></p>
  <p>
    <a href="#uai-education-platform">⬆ Back to top</a>
  </p>
</div>
