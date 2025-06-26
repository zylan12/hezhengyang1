<!DOCTYPE html>
<html lang="zh-CN">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>HOME家庭 - 我们的温馨港湾</title>
  <script src="https://cdn.tailwindcss.com"></script>
  <link href="https://cdn.jsdelivr.net/npm/font-awesome@4.7.0/css/font-awesome.min.css" rel="stylesheet">
  <script>
    tailwind.config = {
      theme: {
        extend: {
          colors: {
            primary: '#D2691E', // 温暖的橙棕色主色调
            secondary: '#FFD700', // 金色辅助色
            accent: '#8B4513', // 深棕色强调色
            neutral: '#FFF8DC', // 米白色背景
          },
          fontFamily: {
            sans: ['Inter', 'system-ui', 'sans-serif'],
            display: ['"Ma Shan Zheng"', 'cursive'],
          },
        },
      }
    }
  </script>
  <style type="text/tailwindcss">
    @layer utilities {
      .content-auto {
        content-visibility: auto;
      }
      .text-shadow {
        text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.2);
      }
      .card-hover {
        @apply transition-all duration-300 hover:shadow-xl hover:-translate-y-1;
      }
      .section-padding {
        @apply py-16 md:py-24;
      }
    }
  </style>
</head>
<body class="bg-neutral text-gray-800 min-h-screen flex flex-col">
  <!-- 导航栏 -->
  <header class="bg-primary/95 text-white sticky top-0 z-50 backdrop-blur-md shadow-md">
    <div class="container mx-auto px-4 py-3">
      <div class="flex justify-between items-center">
        <a href="#" class="flex items-center space-x-2">
          <i class="fa fa-home text-2xl"></i>
          <span class="text-xl font-bold">HOME家庭</span>
        </a>
        
        <!-- 桌面导航 -->
        <nav class="hidden md:flex space-x-8">
          <a href="#home" class="hover:text-secondary transition-colors duration-300">首页</a>
          <a href="#family" class="hover:text-secondary transition-colors duration-300">家庭成员</a>
          <a href="#gallery" class="hover:text-secondary transition-colors duration-300">家庭相册</a>
          <a href="#events" class="hover:text-secondary transition-colors duration-300">活动日历</a>
          <a href="#stories" class="hover:text-secondary transition-colors duration-300">家庭故事</a>
          <a href="#contact" class="hover:text-secondary transition-colors duration-300">联系我们</a>
        </nav>
        
        <!-- 移动端菜单按钮 -->
        <button class="md:hidden text-2xl" id="menuBtn">
          <i class="fa fa-bars"></i>
        </button>
      </div>
    </div>
    
    <!-- 移动端导航菜单 -->
    <div class="md:hidden bg-primary/98 hidden transition-all duration-300" id="mobileMenu">
      <div class="container mx-auto px-4 py-3 flex flex-col space-y-4">
        <a href="#home" class="hover:text-secondary transition-colors duration-300 py-2 border-b border-gray-700">首页</a>
        <a href="#family" class="hover:text-secondary transition-colors duration-300 py-2 border-b border-gray-700">家庭成员</a>
        <a href="#gallery" class="hover:text-secondary transition-colors duration-300 py-2 border-b border-gray-700">家庭相册</a>
        <a href="#events" class="hover:text-secondary transition-colors duration-300 py-2 border-b border-gray-700">活动日历</a>
        <a href="#stories" class="hover:text-secondary transition-colors duration-300 py-2 border-b border-gray-700">家庭故事</a>
        <a href="#contact" class="hover:text-secondary transition-colors duration-300 py-2">联系我们</a>
      </div>
    </div>
  </header>

  <!-- 主内容区 -->
  <main class="flex-grow">
    <!-- 首页/欢迎区 -->
    <section id="home" class="relative min-h-[80vh] flex items-center justify-center bg-cover bg-center" style="background-image: url('https://picsum.photos/id/1067/1920/1080');">
      <div class="absolute inset-0 bg-black/40"></div>
      <div class="container mx-auto px-4 relative z-10 text-center">
        <h1 class="text-[clamp(2.5rem,5vw,4rem)] font-bold text-white mb-6 text-shadow">欢迎来到HOME家庭</h1>
        <p class="text-[clamp(1rem,2vw,1.5rem)] text-white/90 mb-10 max-w-3xl mx-auto text-shadow">这里记录着我们的生活点滴，分享爱与温暖的家庭故事</p>
        <a href="#family" class="bg-secondary hover:bg-secondary/80 text-accent font-bold py-3 px-8 rounded-full inline-block transition-all duration-300 shadow-lg hover:shadow-xl transform hover:-translate-y-1">
          认识我们的家人 <i class="fa fa-arrow-down ml-2"></i>
        </a>
      </div>
      <div class="absolute bottom-10 left-1/2 transform -translate-x-1/2 animate-bounce">
        <a href="#family" class="text-white text-3xl opacity-80 hover:opacity-100 transition-opacity">
          <i class="fa fa-angle-down"></i>
        </a>
      </div>
    </section>

    <!-- 家庭成员介绍 -->
    <section id="family" class="section-padding bg-white">
      <div class="container mx-auto px-4">
        <div class="text-center mb-16">
          <h2 class="text-[clamp(2rem,4vw,3rem)] font-bold text-primary mb-4">家庭成员</h2>
          <div class="w-24 h-1 bg-accent mx-auto mb-6"></div>
          <p class="text-gray-600 max-w-2xl mx-auto">我们是相亲相爱的一家人，每个人都有独特的故事</p>
        </div>

        <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
          <!-- 爷爷 - 何文强 -->
          <div class="bg-neutral rounded-xl overflow-hidden shadow-lg card-hover">
            <div class="relative h-64 overflow-hidden">
              <img src="https://picsum.photos/id/1074/600/400" alt="爷爷 何文强" class="w-full h-full object-cover">
              <div class="absolute bottom-0 left-0 right-0 bg-gradient-to-t from-black/70 to-transparent p-4">
                <h3 class="text-xl font-bold text-white">何文强</h3>
                <p class="text-white/90">爷爷</p>
              </div>
            </div>
            <div class="p-6">
              <p class="text-gray-700 mb-4">退休，喜欢书法和园艺，每天清晨都会在阳台侍弄花草，书法作品多次在社区展览。</p>
              <div class="flex space-x-3 text-accent">
                <a href="#" class="hover:text-primary transition-colors"><i class="fa fa-wechat"></i></a>
                <a href="#" class="hover:text-primary transition-colors"><i class="fa fa-book"></i></a>
              </div>
            </div>
          </div>

          <!-- 奶奶 - 姚伍成 -->
          <div class="bg-neutral rounded-xl overflow-hidden shadow-lg card-hover">
            <div class="relative h-64 overflow-hidden">
              <img src="https://picsum.photos/id/1062/600/400" alt="奶奶 姚伍成" class="w-full h-full object-cover">
              <div class="absolute bottom-0 left-0 right-0 bg-gradient-to-t from-black/70 to-transparent p-4">
                <h3 class="text-xl font-bold text-white">姚伍成</h3>
                <p class="text-white/90">奶奶</p>
              </div>
            </div>
            <div class="p-6">
              <p class="text-gray-700 mb-4">家庭主妇，擅长传统刺绣和烹饪，尤其是手工水饺和腌菜，是家庭聚会的美食担当。</p>
              <div class="flex space-x-3 text-accent">
                <a href="#" class="hover:text-primary transition-colors"><i class="fa fa-wechat"></i></a>
                <a href="#" class="hover:text-primary transition-colors"><i class="fa fa-cutlery"></i></a>
              </div>
            </div>
          </div>

          <!-- 外婆 - 龙吉满 -->
          <div class="bg-neutral rounded-xl overflow-hidden shadow-lg card-hover">
            <div class="relative h-64 overflow-hidden">
              <img src="https://picsum.photos/id/1069/600/400" alt="外婆 龙吉满" class="w-full h-full object-cover">
              <div class="absolute bottom-0 left-0 right-0 bg-gradient-to-t from-black/70 to-transparent p-4">
                <h3 class="text-xl font-bold text-white">龙吉满</h3>
                <p class="text-white/90">外婆</p>
              </div>
            </div>
            <div class="p-6">
              <p class="text-gray-700 mb-4">退休，热爱戏曲和剪纸艺术，经常教孙子孙女们制作传统剪纸作品。</p>
              <div class="flex space-x-3 text-accent">
                <a href="#" class="hover:text-primary transition-colors"><i class="fa fa-video-camera"></i></a>
                <a href="#" class="hover:text-primary transition-colors"><i class="fa fa-scissors"></i></a>
              </div>
            </div>
          </div>

          <!-- 外公 - 张文华 -->
          <div class="bg-neutral rounded-xl overflow-hidden shadow-lg card-hover">
            <div class="relative h-64 overflow-hidden">
              <img src="https://picsum.photos/id/1076/600/400" alt="外公 张文华" class="w-full h-full object-cover">
              <div class="absolute bottom-0 left-0 right-0 bg-gradient-to-t from-black/70 to-transparent p-4">
                <h3 class="text-xl font-bold text-white">张文华</h3>
                <p class="text-white/90">外公</p>
              </div>
            </div>
            <div class="p-6">
              <p class="text-gray-700 mb-4">退休，喜欢钓鱼和中医养生，每周都会去公园练习太极，是家庭的健康顾问。</p>
              <div class="flex space-x-3 text-accent">
                <a href="#" class="hover:text-primary transition-colors"><i class="fa fa-fish"></i></a>
                <a href="#" class="hover:text-primary transition-colors"><i class="fa fa-medkit"></i></a>
              </div>
            </div>
          </div>

          <!-- 丈夫 - 何正阳 -->
          <div class="bg-neutral rounded-xl overflow-hidden shadow-lg card-hover">
            <div class="relative h-64 overflow-hidden">
              <img src="https://picsum.photos/id/1012/600/400" alt="丈夫 何正阳" class="w-full h-full object-cover">
              <div class="absolute bottom-0 left-0 right-0 bg-gradient-to-t from-black/70 to-transparent p-4">
                <h3 class="text-xl font-bold text-white">何正阳</h3>
                <p class="text-white/90">丈夫 / 工业设计师</p>
              </div>
            </div>
            <div class="p-6">
              <p class="text-gray-700 mb-4">工业设计师专家，热爱户外徒步和摄影，擅长将自然元素融入设计，产品广受市场认可。</p>
              <div class="flex space-x-3 text-accent">
                <a href="#" class="hover:text-primary transition-colors"><i class="fa fa-camera"></i></a>
                <a href="#" class="hover:text-primary transition-colors"><i class="fa fa-mountain"></i></a>
              </div>
            </div>
          </div>

          <!-- 妻子 - 张正 -->
          <div class="bg-neutral rounded-xl overflow-hidden shadow-lg card-hover">
            <div class="relative h-64 overflow-hidden">
              <img src="https://picsum.photos/id/1000/600/400" alt="妻子 张正" class="w-full h-full object-cover">
              <div class="absolute bottom-0 left-0 right-0 bg-gradient-to-t from-black/70 to-transparent p-4">
                <h3 class="text-xl font-bold text-white">张正</h3>
                <p class="text-white/90">妻子 / 小学数学老师</p>
              </div>
            </div>
            <div class="p-6">
              <p class="text-gray-700 mb-4">充满爱心的小学数学老师，喜欢烘焙和亲子阅读，擅长用游戏化教学激发孩子的学习兴趣。</p>
              <div class="flex space-x-3 text-accent">
                <a href="#" class="hover:text-primary transition-colors"><i class="fa fa-book"></i></a>
                <a href="#" class="hover:text-primary transition-colors"><i class="fa fa-cutlery"></i></a>
              </div>
            </div>
          </div>

          <!-- 儿子 - 何乐章 -->
          <div class="bg-neutral rounded-xl overflow-hidden shadow-lg card-hover">
            <div class="relative h-64 overflow-hidden">
              <img src="https://picsum.photos/id/1062/600/400" alt="儿子 何乐章" class="w-full h-full object-cover">
              <div class="absolute bottom-0 left-0 right-0 bg-gradient-to-t from-black/70 to-transparent p-4">
                <h3 class="text-xl font-bold text-white">何乐章</h3>
                <p class="text-white/90">儿子 / 3岁</p>
              </div>
            </div>
            <div class="p-6">
              <p class="text-gray-700 mb-4">活泼可爱的3岁宝宝，喜欢搭积木、听故事和奥特曼，是家庭的开心果。</p>
              <div class="flex space-x-3 text-accent">
                <a href="#" class="hover:text-primary transition-colors"><i class="fa fa-child"></i></a>
                <a href="#" class="hover:text-primary transition-colors"><i class="fa fa-cube"></i></a>
              </div>
            </div>
          </div>

          <!-- 兄弟姐妹扩展端口 -->
          <div class="bg-neutral rounded-xl overflow-hidden shadow-lg border-2 border-dashed border-gray-300 flex items-center justify-center h-64">
            <div class="text-center p-4">
              <i class="fa fa-user-plus text-4xl text-gray-400 mb-2"></i>
              <p class="text-gray-500">兄弟姐妹端口</p>
              <p class="text-sm text-gray-400">点击添加更多家庭成员</p>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- 家庭相册 -->
    <section id="gallery" class="section-padding bg-gray-50">
      <div class="container mx-auto px-4">
        <div class="text-center mb-16">
          <h2 class="text-[clamp(2rem,4vw,3rem)] font-bold text-primary mb-4">家庭相册</h2>
          <div class="w-24 h-1 bg-accent mx-auto mb-6"></div>
          <p class="text-gray-600 max-w-2xl mx-auto">记录生活中的美好瞬间，每一张照片都承载着珍贵回忆</p>
        </div>

        <!-- 相册过滤 -->
        <div class="flex flex-wrap justify-center gap-4 mb-12">
          <button class="gallery-filter-btn active bg-primary text-white py-2 px-6 rounded-full hover:bg-primary/90 transition-colors" data-filter="all">全部</button>
          <button class="gallery-filter-btn bg-gray-200 text-gray-700 py-2 px-6 rounded-full hover:bg-gray-300 transition-colors" data-filter="family">全家福</button>
          <button class="gallery-filter-btn bg-gray-200 text-gray-700 py-2 px-6 rounded-full hover:bg-gray-300 transition-colors" data-filter="outdoor">户外活动</button>
          <button class="gallery-filter-btn bg-gray-200 text-gray-700 py-2 px-6 rounded-full hover:bg-gray-300 transition-colors" data-filter="holiday">节日</button>
          <button class="gallery-filter-btn bg-gray-200 text-gray-700 py-2 px-6 rounded-full hover:bg-gray-300 transition-colors" data-filter="kids">孩子成长</button>
        </div>

        <!-- 相册网格 -->
        <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-6" id="gallery-grid">
          <!-- 全家福照片 -->
          <div class="gallery-item family" data-category="family">
            <div class="relative overflow-hidden rounded-xl shadow-md group">
              <img src="https://picsum.photos/id/1058/800/600" alt="全家福" class="w-full h-80 object-cover transition-transform duration-700 group-hover:scale-110">
              <div class="absolute inset-0 bg-black/60 opacity-0 group-hover:opacity-100 transition-opacity duration-300 flex items-center justify-center">
                <div class="text-center p-4 transform translate-y-4 group-hover:translate-y-0 transition-transform duration-300">
                  <h3 class="text-white text-xl font-bold mb-2">春节全家福</h3>
                  <p class="text-white/80 mb-4">2025年春节全家合影</p>
                  <button class="view-photo-btn bg-secondary hover:bg-secondary/80 text-accent font-bold py-2 px-4 rounded-full transition-colors">
                    <i class="fa fa-search-plus mr-2"></i>查看大图
                  </button>
                </div>
              </div>
            </div>
          </div>

          <!-- 户外活动照片 -->
          <div class="gallery-item outdoor" data-category="outdoor">
            <div class="relative overflow-hidden rounded-xl shadow-md group">
              <img src="https://picsum.photos/id/1036/800/600" alt="郊外野餐" class="w-full h-80 object-cover transition-transform duration-700 group-hover:scale-110">
              <div class="absolute inset-0 bg-black/60 opacity-0 group-hover:opacity-100 transition-opacity duration-300 flex items-center justify-center">
                <div class="text-center p-4 transform translate-y-4 group-hover:translate-y-0 transition-transform duration-300">
                  <h3 class="text-white text-xl font-bold mb-2">郊外野餐</h3>
                  <p class="text-white/80 mb-4">2025年5月家庭户外活动</p>
                  <button class="view-photo-btn bg-secondary hover:bg-secondary/80 text-accent font-bold py-2 px-4 rounded-full transition-colors">
                    <i class="fa fa-search-plus mr-2"></i>查看大图
                  </button>
                </div>
              </div>
            </div>
          </div>

          <!-- 节日照片 -->
          <div class="gallery-item holiday" data-category="holiday">
            <div class="relative overflow-hidden rounded-xl shadow-md group">
              <img src="https://picsum.photos/id/1068/800/600" alt="中秋团圆饭" class="w-full h-80 object-cover transition-transform duration-700 group-hover:scale-110">
              <div class="absolute inset-0 bg-black/60 opacity-0 group-hover:opacity-100 transition-opacity duration-300 flex items-center justify-center">
                <div class="text-center p-4 transform translate-y-4 group-hover:translate-y-0 transition-transform duration-300">
                  <h3 class="text-white text-xl font-bold mb-2">中秋团圆饭</h3>
                  <p class="text-white/80 mb-4">2024年中秋节家庭聚餐</p>
                  <button class="view-photo-btn bg-secondary hover:bg-secondary/80 text-accent font-bold py-2 px-4 rounded-full transition-colors">
                    <i class="fa fa-search-plus mr-2"></i>查看大图
                  </button>
                </div>
              </div>
            </div>
          </div>

          <!-- 孩子成长照片 -->
          <div class="gallery-item kids" data-category="kids">
            <div class="relative overflow-hidden rounded-xl shadow-md group">
              <img src="https://picsum.photos/id/1070/800/600" alt="何乐章生日" class="w-full h-80 object-cover transition-transform duration-700 group-hover:scale-110">
              <div class="absolute inset-0 bg-black/60 opacity-0 group-hover:opacity-100 transition-opacity duration-300 flex items-center justify-center">
                <div class="text-center p-4 transform translate-y-4 group-hover:translate-y-0 transition-transform duration-300">
                  <h3 class="text-white text-xl font-bold mb-2">何乐章3岁生日</h3>
                  <p class="text-white/80 mb-4">2024年12月生日派对</p>
                  <button class="view-photo-btn bg-secondary hover:bg-secondary/80 text-accent font-bold py-2 px-4 rounded-full transition-colors">
                    <i class="fa fa-search-plus mr-2"></i>查看大图
                  </button>
                </div>
              </div>
            </div>
          </div>

          <!-- 户外活动照片2 -->
          <div class="gallery-item outdoor" data-category="outdoor">
            <div class="relative overflow-hidden rounded-xl shadow-md group">
              <img src="https://picsum.photos/id/1043/800/600" alt="公园游玩" class="w-full h-80 object-cover transition-transform duration-700 group-hover:scale-110">
              <div class="absolute inset-0 bg-black/60 opacity-0 group-hover:opacity-100 transition-opacity duration-300 flex items-center justify-center">
                <div class="text-center p-4 transform translate-y-4 group-hover:translate-y-0 transition-transform duration-300">
                  <h3 class="text-white text-xl font-bold mb-2">公园游玩</h3>
                  <p class="text-white/80 mb-4">2025年4月家庭公园日</p>
                  <button class="view-photo-btn bg-secondary hover:bg-secondary/80 text-accent font-bold py-2 px-4 rounded-full transition-colors">
                    <i class="fa fa-search-plus mr-2"></i>查看大图
                  </button>
                </div>
              </div>
            </div>
          </div>

          <!-- 节日照片2 -->
          <div class="gallery-item holiday" data-category="holiday">
            <div class="relative overflow-hidden rounded-xl shadow-md group">
              <img src="https://picsum.photos/id/1060/800/600" alt="端午包粽子" class="w-full h-80 object-cover transition-transform duration-700 group-hover:scale-110">
              <div class="absolute inset-0 bg-black/60 opacity-0 group-hover:opacity-100 transition-opacity duration-300 flex items-center justify-center">
                <div class="text-center p-4 transform translate-y-4 group-hover:translate-y-0 transition-transform duration-300">
                  <h3 class="text-white text-xl font-bold mb-2">端午包粽子</h3>
                  <p class="text-white/80 mb-4">2025年端午节家庭活动</p>
                  <button class="view-photo-btn bg-secondary hover:bg-secondary/80 text-accent font-bold py-2 px-4 rounded-full transition-colors">
                    <i class="fa fa-search-plus mr-2"></i>查看大图
                  </button>
                </div>
              </div>
            </div>
          </div>
        </div>

        <!-- 加载更多按钮 -->
        <div class="text-center mt-12">
          <button id="load-more" class="bg-primary hover:bg-primary/90 text-white font-bold py-3 px-8 rounded-full transition-all duration-300 shadow-md hover:shadow-lg transform hover:-translate-y-1">
            加载更多照片 <i class="fa fa-refresh ml-2"></i>
          </button>
        </div>
      </div>
    </section>

    <!-- 活动日历 -->
    <section id="events" class="section-padding bg-white">
      <div class="container mx-auto px-4">
        <div class="text-center mb-16">
          <h2 class="text-[clamp(2rem,4vw,3rem)] font-bold text-primary mb-4">活动日历</h2>
          <div class="w-24 h-1 bg-accent mx-auto mb-6"></div>
          <p class="text-gray-600 max-w-2xl mx-auto">记录家庭重要活动，不错过每一个温馨时刻</p>
        </div>

        <div class="grid grid-cols-1 lg:grid-cols-3 gap-10">
          <!-- 左侧日历 -->
          <div class="lg:col-span-2 bg-neutral rounded-xl shadow-lg p-6">
            <div class="flex justify-between items-center mb-6">
              <h3 class="text-xl font-bold text-primary" id="current-month">2025年6月</h3>
              <div class="flex space-x-2">
                <button id="prev-month" class="bg-gray-200 hover:bg-gray-300 text-gray-700 p-2 rounded-full transition-colors">
                  <i class="fa fa-chevron-left"></i>
                </button>
                <button id="next-month" class="bg-gray-200 hover:bg-gray-300 text-gray-700 p-2 rounded-full transition-colors">
                  <i class="fa fa-chevron-right"></i>
                </button>
              </div>
            </div>

            <!-- 日历网格 -->
            <div class="grid grid-cols-7 gap-1">
              <!-- 星期标题 -->
              <div class="text-center font-bold text-gray-500 py-2">周日</div>
              <div class="text-center font-bold text-gray-500 py-2">周一</div>
              <div class="text-center font-bold text-gray-500 py-2">周二</div>
              <div class="text-center font-bold text-gray-500 py-2">周三</div>
              <div class="text-center font-bold text-gray-500 py-2">周四</div>
              <div class="text-center font-bold text-gray-500 py-2">周五</div>
              <div class="text-center font-bold text-gray-500 py-2">周六</div>

              <!-- 上个月的日期 -->
              <div class="text-center text-gray-400 py-3">28</div>
              <div class="text-center text-gray-400 py-3">29</div>
              <div class="text-center text-gray-400 py-3">30</div>
              <div class="text-center text-gray-400 py-3">31</div>

              <!-- 当月的日期 -->
              <div class="text-center py-3">1</div>
              <div class="text-center py-3">2</div>
              <div class="text-center py-3">3</div>
              <div class="text-center py-3">4</div>
              <div class="text-center py-3">5</div>
              <div class="text-center py-3">6</div>
              <div class="text-center py-3">7</div>
              <div class="text-center py-3">8</div>
              <div class="text-center py-3">9</div>
              <div class="text-center py-3">10</div>
              <div class="text-center py-3">11</div>
              <div class="text-center py-3">12</div>
              <div class="text-center py-3">13</div>
              <div class="text-center py-3">14</div>
              <div class="text-center py-3">15</div>
              <div class="text-center py-3">16</div>
              <div class="text-center py-3">17</div>
              <div class="text-center py-3">18</div>
              <div class="text-center py-3">19</div>
              <div class="text-center py-3">20</div>
              <div class="text-center py-3">21</div>
              <div class="text-center py-3">22</div>
              <div class="text-center py-3">23</div>
              <div class="text-center py-3">24</div>
              <div class="text-center bg-accent text-white rounded-full w-10 h-10 mx-auto flex items-center justify-center font-bold">25</div>
              <div class="text-center py-3 relative group">
                26
                <div class="absolute bottom-full left-1/2 transform -translate-x-1/2 mb-2 w-64 bg-black text-white p-2 rounded opacity-0 invisible group-hover:opacity-100 group-hover:visible transition-all z-10">
                  <p class="text-sm font-medium">何乐章生日派对</p>
                </div>
              </div>
              <div class="text-center py-3 relative group">
                27
                <div class="absolute bottom-full left-1/2 transform -translate-x-1/2 mb-2 w-64 bg-black text-white p-2 rounded opacity-0 invisible group-hover:opacity-100 group-hover:visible transition-all z-10">
                  <p class="text-sm font-medium">家庭徒步活动</p>
                </div>
              </div>
              <div class="text-center py-3">28</div>
              <div class="text-center py-3">29</div>
              <div class="text-center py-3">30</div>

              <!-- 下个月的日期 -->
              <div class="text-center text-gray-400 py-3">1</div>
              <div class="text-center text-gray-400 py-3">2</div>
              <div class="text-center text-gray-400 py-3">3</div>
              <div class="text-center text-gray-400 py-3">4</div>
              <div class="text-center text-gray-400 py-3">5</div>
            </div>
          </div>

          <!-- 右侧即将到来的活动 -->
          <div class="bg-neutral rounded-xl shadow-lg p-6">
            <h3 class="text-xl font-bold text-primary mb-6">即将到来的活动</h3>
            
            <div class="space-y-6">
              <!-- 活动1 -->
              <div class="bg-white rounded-lg shadow-sm p-4 border-l-4 border-accent">
                <div class="flex items-center mb-2">
                  <div class="bg-accent text-white rounded-full w-10 h-10 flex items-center justify-center mr-3">
                    <i class="fa fa-birthday-cake"></i>
                  </div>
                  <div>
                    <h4 class="font-bold">何乐章4岁生日</h4>
                    <p class="text-sm text-gray-500">12月21日 (还有几个月)</p>
                  </div>
                </div>
                <p class="text-gray-700 text-sm">家庭生日派对，邀请亲朋好友共同庆祝</p>
              </div>

              <!-- 活动2 -->
              <div class="bg-white rounded-lg shadow-sm p-4 border-l-4 border-primary">
                <div class="flex items-center mb-2">
                  <div class="bg-primary text-white rounded-full w-10 h-10 flex items-center justify-center mr-3">
                    <i class="fa fa-mountain"></i>
                  </div>
                  <div>
                    <h4 class="font-bold">家庭徒步活动</h4>
                    <p class="text-sm text-gray-500">6月27日 (下周五)</p>
                  </div>
                </div>
                <p class="text-gray-700 text-sm">前往郊外森林公园徒步，野餐午餐</p>
              </div>

              <!-- 活动3 -->
              <div class="bg-white rounded-lg shadow-sm p-4 border-l-4 border-secondary">
                <div class="flex items-center mb-2">
                  <div class="bg-secondary text-accent rounded-full w-10 h-10 flex items-center justify-center mr-3">
                    <i class="fa fa-users"></i>
                  </div>
                  <div>
                    <h4 class="font-bold"> grandparents 探访</h4>
                    <p class="text-sm text-gray-500">7月5日 (下下周六)</p>
                  </div>
                </div>
                <p class="text-gray-700 text-sm">爷爷奶奶外公外婆来访，家庭聚餐</p>
              </div>

              <!-- 活动4 -->
              <div class="bg-white rounded-lg shadow-sm p-4 border-l-4 border-gray-500">
                <div class="flex items-center mb-2">
                  <div class="bg-gray-500 text-white rounded-full w-10 h-10 flex items-center justify-center mr-3">
                    <i class="fa fa-calendar-check-o"></i>
                  </div>
                  <div>
                    <h4 class="font-bold">张正教师节庆祝</h4>
                    <p class="text-sm text-gray-500">9月10日 (周三)</p>
                  </div>
                </div>
                <p class="text-gray-700 text-sm">庆祝张正老师的教师节，孩子手工制作礼物</p>
              </div>
            </div>

            <!-- 添加新活动按钮 -->
            <button id="add-event" class="mt-8 w-full bg-primary hover:bg-primary/90 text-white font-bold py-3 px-4 rounded-lg transition-colors flex items-center justify-center">
              <i class="fa fa-plus-circle mr-2"></i> 添加新活动
            </button>
          </div>
        </div>
      </div>
    </section>

    <!-- 家庭故事 -->
    <section id="stories" class="section-padding bg-gray-50">
      <div class="container mx-auto px-4">
        <div class="text-center mb-16">
          <h2 class="text-[clamp(2rem,4vw,3rem)] font-bold text-primary mb-4">家庭故事</h2>
          <div class="w-24 h-1 bg-accent mx-auto mb-6"></div>
          <p class="text-gray-600 max-w-2xl mx-auto">记录那些值得永远珍藏的家庭回忆与感动时刻</p>
        </div>

        <div class="grid grid-cols-1 lg:grid-cols-2 gap-10">
          <!-- 故事1 -->
          <div class="bg-white rounded-xl shadow-lg overflow-hidden group">
            <div class="relative h-64">
              <img src="https://picsum.photos/id/1067/800/400" alt="何乐章出生" class="w-full h-full object-cover transition-transform duration-700 group-hover:scale-105">
              <div class="absolute inset-0 bg-gradient-to-t from-black/70 via-black/20 to-transparent"></div>
              <div class="absolute bottom-0 left-0 p-6">
                <span class="bg-accent text-white text-xs font-bold px-3 py-1 rounded-full">2022年6月</span>
                <h3 class="text-white text-xl font-bold mt-2">何乐章的诞生</h3>
              </div>
            </div>
            <div class="p-6">
              <p class="text-gray-700 mb-4">2021年12月21日，我们迎来了家庭的新成员何乐章。从那天起，家里充满了欢声笑语，初为父母的我们虽然忙碌，但每一天都充满了幸福。爷爷奶奶外公外婆轮流来照顾宝宝，家庭的纽带更加紧密。</p>
              <div class="flex items-center justify-between">
                <div class="flex items-center">
                  <img src="https://picsum.photos/id/1012/100/100" alt="何正阳" class="w-10 h-10 rounded-full object-cover mr-3">
                  <span class="text-gray-600">何正阳</span>
                </div>
                <div class="flex space-x-3">
                  <button class="text-gray-400 hover:text-primary transition-colors">
                    <i class="fa fa-heart-o"></i> 24
                  </button>
                  <button class="text-gray-400 hover:text-primary transition-colors">
                    <i class="fa fa-comment-o"></i> 8
                  </button>
                </div>
              </div>
            </div>
          </div>

          <!-- 故事2 -->
          <div class="bg-white rounded-xl shadow-lg overflow-hidden group">
            <div class="relative h-64">
              <img src="https://picsum.photos/id/1055/800/400" alt="家庭旅行" class="w-full h-full object-cover transition-transform duration-700 group-hover:scale-105">
              <div class="absolute inset-0 bg-gradient-to-t from-black/70 via-black/20 to-transparent"></div>
              <div class="absolute bottom-0 left-0 p-6">
                <span class="bg-accent text-white text-xs font-bold px-3 py-1 rounded-full">2024年08月</span>
                <h3 class="text-white text-xl font-bold mt-2">第一次全家旅行</h3>
              </div>
            </div>
            <div class="p-6">
              <p class="text-gray-700 mb-4">2024年暑假，我们带着2岁多的乐章进行了第一次全家旅行，目的地是西北。我们在沙滩草地湖边玩耍，参观博物馆景点，乐章第一次看到沙漠时兴奋的样子至今记忆犹新。这次旅行让我们感受到了一家人旅行的幸福。</p>
              <div class="flex items-center justify-between">
                <div class="flex items-center">
                  <img src="https://picsum.photos/id/1000/100/100" alt="张正" class="w-10 h-10 rounded-full object-cover mr-3">
                  <span class="text-gray-600">张正</span>
                </div>
                <div class="flex space-x-3">
                  <button class="text-gray-400 hover:text-primary transition-colors">
                    <i class="fa fa-heart-o"></i> 32
                  </button>
                  <button class="text-gray-400 hover:text-primary transition-colors">
                    <i class="fa fa-comment-o"></i> 12
                  </button>
                </div>
              </div>
            </div>
          </div>

          <!-- 故事3 -->
          <div class="bg-white rounded-xl shadow-lg overflow-hidden group">
            <div class="relative h-64">
              <img src="https://picsum.photos/id/1071/800/400" alt="爷爷的书法课" class="w-full h-full object-cover transition-transform duration-700 group-hover:scale-105">
              <div class="absolute inset-0 bg-gradient-to-t from-black/70 via-black/20 to-transparent"></div>
              <div class="absolute bottom-0 left-0 p-6">
                <span class="bg-accent text-white text-xs font-bold px-3 py-1 rounded-full">2025年3月</span>
                <h3 class="text-white text-xl font-bold mt-2">爷爷的书法课</h3>
              </div>
            </div>
            <div class="p-6">
              <p class="text-gray-700 mb-4">爷爷何文强开始教乐章学习书法，虽然乐章还很小，但已经能拿着毛笔有模有样地涂鸦。爷爷总是耐心地指导，这不仅是书法的启蒙，更是传统文化的传承。看着爷孙俩一起在书桌前的样子，全家人都感到无比温馨。</p>
              <div class="flex items-center justify-between">
                <div class="flex items-center">
                  <img src="https://picsum.photos/id/1074/100/100" alt="何文强" class="w-10 h-10 rounded-full object-cover mr-3">
                  <span class="text-gray-600">何文强</span>
                </div>
                <div class="flex space-x-3">
                  <button class="text-gray-400 hover:text-primary transition-colors">
                    <i class="fa fa-heart-o"></i> 18
                  </button>
                  <button class="text-gray-400 hover:text-primary transition-colors">
                    <i class="fa fa-comment-o"></i> 6
                  </button>
                </div>
              </div>
            </div>
          </div>

          <!-- 故事4 -->
          <div class="bg-white rounded-xl shadow-lg overflow-hidden group">
            <div class="relative h-64">
              <img src="https://picsum.photos/id/1060/800/400" alt="外婆的剪纸" class="w-full h-full object-cover transition-transform duration-700 group-hover:scale-105">
              <div class="absolute inset-0 bg-gradient-to-t from-black/70 via-black/20 to-transparent"></div>
              <div class="absolute bottom-0 left-0 p-6">
                <span class="bg-accent text-white text-xs font-bold px-3 py-1 rounded-full">2025年5月</span>
                <h3 class="text-white text-xl font-bold mt-2">外婆的剪纸课</h3>
              </div>
            </div>
            <div class="p-6">
              <p class="text-gray-700 mb-4">外婆龙吉满教乐章学习传统剪纸，第一张作品是一只简单的小兔子。虽然线条还不流畅，但乐章拿着自己的作品兴奋地展示给每个人看。这样的亲子互动不仅培养了孩子的动手能力，更让传统文化在家庭中得以延续。</p>
              <div class="flex items-center justify-between">
                <div class="flex items-center">
                  <img src="https://picsum.photos/id/1069/100/100" alt="龙吉满" class="w-10 h-10 rounded-full object-cover mr-3">
                  <span class="text-gray-600">龙吉满</span>
                </div>
                <div class="flex space-x-3">
                  <button class="text-gray-400 hover:text-primary transition-colors">
                    <i class="fa fa-heart-o"></i> 22
                  </button>
                  <button class="text-gray-400 hover:text-primary transition-colors">
                    <i class="fa fa-comment-o"></i> 7
                  </button>
                </div>
              </div>
            </div>
          </div>
        </div>

        <!-- 查看更多故事按钮 -->
        <div class="text-center mt-12">
          <button class="bg-primary hover:bg-primary/90 text-white font-bold py-3 px-8 rounded-full transition-all duration-300 shadow-md hover:shadow-lg transform hover:-translate-y-1">
            查看更多故事 <i class="fa fa-arrow-right ml-2"></i>
          </button>
        </div>
      </div>
    </section>

    <!-- 联系我们 -->
    <section id="contact" class="section-padding bg-white">
      <div class="container mx-auto px-4">
        <div class="text-center mb-16">
          <h2 class="text-[clamp(2rem,4vw,3rem)] font-bold text-primary mb-4">联系我们</h2>
          <div class="w-24 h-1 bg-accent mx-auto mb-6"></div>
          <p class="text-gray-600 max-w-2xl mx-auto">有什么想分享的？填写下面的表单，给我们留言吧</p>
        </div>

        <div class="grid grid-cols-1 lg:grid-cols-2 gap-10">
          <!-- 联系表单 -->
          <div class="bg-neutral rounded-xl shadow-lg p-8">
            <h3 class="text-xl font-bold text-primary mb-6">发送消息</h3>
            
            <form id="contact-form" class="space-y-6">
              <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
                <div>
                  <label for="name" class="block text-gray-700 font-medium mb-2">姓名</label>
                  <input type="text" id="name" class="w-full px-4 py-3 rounded-lg border border-gray-300 focus:border-primary focus:ring focus:ring-primary/20 outline-none transition-all" placeholder="请输入您的姓名">
                </div>
                <div>
                  <label for="email" class="block text-gray-700 font-medium mb-2">邮箱</label>
                  <input type="email" id="email" class="w-full px-4 py-3 rounded-lg border border-gray-300 focus:border-primary focus:ring focus:ring-primary/20 outline-none transition-all" placeholder="请输入您的邮箱">
                </div>
              </div>
              
              <div>
                <label for="subject" class="block text-gray-700 font-medium mb-2">主题</label>
                <input type="text" id="subject" class="w-full px-4 py-3 rounded-lg border border-gray-300 focus:border-primary focus:ring focus:ring-primary/20 outline-none transition-all" placeholder="请输入消息主题">
              </div>
              
              <div>
                <label for="message" class="block text-gray-700 font-medium mb-2">消息</label>
                <textarea id="message" rows="5" class="w-full px-4 py-3 rounded-lg border border-gray-300 focus:border-primary focus:ring focus:ring-primary/20 outline-none transition-all resize-none" placeholder="请输入您的消息内容"></textarea>
              </div>
              
              <div>
                <button type="submit" class="w-full bg-primary hover:bg-primary/90 text-white font-bold py-3 px-6 rounded-lg transition-colors flex items-center justify-center">
                  <i class="fa fa-paper-plane mr-2"></i> 发送消息
                </button>
              </div>
            </form>
          </div>
          
          <!-- 联系信息和地图 -->
          <div class="flex flex-col space-y-10">
            <!-- 联系信息 -->
            <div class="bg-neutral rounded-xl shadow-lg p-8">
              <h3 class="text-xl font-bold text-primary mb-6">联系方式</h3>
              
              <div class="space-y-6">
                <div class="flex items-start">
                  <div class="bg-primary/10 text-primary rounded-full w-12 h-12 flex items-center justify-center mr-4 shrink-0">
                    <i class="fa fa-map-marker"></i>
                  </div>
                  <div>
                    <h4 class="font-bold text-gray-800 mb-1">家庭住址</h4>
                    <p class="text-gray-600">东莞市横沥镇松湖明珠13502号 HOME家园</p>
                  </div>
                </div>
                
                <div class="flex items-start">
                  <div class="bg-primary/10 text-primary rounded-full w-12 h-12 flex items-center justify-center mr-4 shrink-0">
                    <i class="fa fa-phone"></i>
                  </div>
                  <div>
                    <h4 class="font-bold text-gray-800 mb-1">电话联系</h4>
                    <p class="text-gray-600">何正阳: 151-1335-7640</p>
                    <p class="text-gray-600">张正: 1479-8951-4962</p>
                  </div>
                </div>
                
                <div class="flex items-start">
                  <div class="bg-primary/10 text-primary rounded-full w-12 h-12 flex items-center justify-center mr-4 shrink-0">
                    <i class="fa fa-envelope"></i>
                  </div>
                  <div>
                    <h4 class="font-bold text-gray-800 mb-1">电子邮箱</h4>
                    <p class="text-gray-600">hefamily@example.com</p>
                  </div>
                </div>
                
                <div class="flex items-start">
                  <div class="bg-primary/10 text-primary rounded-full w-12 h-12 flex items-center justify-center mr-4 shrink-0">
                    <i class="fa fa-clock-o"></i>
                  </div>
                  <div>
                    <h4 class="font-bold text-gray-800 mb-1">家庭开放时间</h4>
                    <p class="text-gray-600">每周日下午2:00-5:00 欢迎来访</p>
                  </div>
                </div>
              </div>
              
              <!-- 社交媒体 -->
              <div class="mt-8">
                <h4 class="font-bold text-gray-800 mb-4">关注我们</h4>
                <div class="flex space-x-4">
                  <a href="#" class="bg-primary hover:bg-primary/90 text-white w-10 h-10 rounded-full flex items-center justify-center transition-colors">
                    <i class="fa fa-weixin"></i>
                  </a>
                  <a href="#" class="bg-primary hover:bg-primary/90 text-white w-10 h-10 rounded-full flex items-center justify-center transition-colors">
                    <i class="fa fa-weibo"></i>
                  </a>
                  <a href="#" class="bg-primary hover:bg-primary/90 text-white w-10 h-10 rounded-full flex items-center justify-center transition-colors">
                    <i class="fa fa-instagram"></i>
                  </a>
                  <a href="#" class="bg-primary hover:bg-primary/90 text-white w-10 h-10 rounded-full flex items-center justify-center transition-colors">
                    <i class="fa fa-youtube-play"></i>
                  </a>
                </div>
              </div>
            </div>
            
            <!-- 地图占位 -->
            <div class="bg-neutral rounded-xl shadow-lg overflow-hidden h-80">
              <div class="w-full h-full bg-gray-200 flex items-center justify-center">
                <div class="text-center p-4">
                  <i class="fa fa-map-o text-4xl text-gray-400 mb-2"></i>
                  <p class="text-gray-500">家庭位置地图将在这里显示</p>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>
  </main>

  <!-- 页脚 -->
  <footer class="bg-primary text-white py-12">
    <div class="container mx-auto px-4">
      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-10">
        <!-- 关于我们 -->
        <div>
          <h3 class="text-xl font-bold mb-6">关于我们</h3>
          <p class="text-white/80 mb-6">HOME家庭是一个充满爱与温暖的大家庭，三代同堂，其乐融融。这个网站记录着我们的生活点滴，分享家庭的幸福与感动。</p>
          <div class="flex space-x-4">
            <a href="#" class="text-white/80 hover:text-white transition-colors">
              <i class="fa fa-weixin"></i>
            </a>
            <a href="#" class="text-white/80 hover:text-white transition-colors">
              <i class="fa fa-weibo"></i>
            </a>
            <a href="#" class="text-white/80 hover:text-white transition-colors">
              <i class="fa fa-instagram"></i>
            </a>
            <a href="#" class="text-white/80 hover:text-white transition-colors">
              <i class="fa fa-youtube-play"></i>
            </a>
          </div>
        </div>
        
        <!-- 快速链接 -->
        <div>
          <h3 class="text-xl font-bold mb-6">快速链接</h3>
          <ul class="space-y-3">
            <li><a href="#home" class="text-white/80 hover:text-white transition-colors">首页</a></li>
            <li><a href="#family" class="text-white/80 hover:text-white transition-colors">家庭成员</a></li>
            <li><a href="#gallery" class="text-white/80 hover:text-white transition-colors">家庭相册</a></li>
            <li><a href="#events" class="text-white/80 hover:text-white transition-colors">活动日历</a></li>
            <li><a href="#stories" class="text-white/80 hover:text-white transition-colors">家庭故事</a></li>
            <li><a href="#contact" class="text-white/80 hover:text-white transition-colors">联系我们</a></li>
          </ul>
        </div>
        
        <!-- 最新动态 -->
        <div>
          <h3 class="text-xl font-bold mb-6">最新动态</h3>
          <ul class="space-y-4">
            <li class="flex">
              <div class="bg-secondary/20 text-accent rounded-full w-10 h-10 flex items-center justify-center mr-3 shrink-0">
                <i class="fa fa-calendar"></i>
              </div>
              <div>
                <p class="text-white/80">何乐章即将庆祝3岁生日</p>
                <p class="text-white/60 text-sm">2024-12-20</p>
              </div>
            </li>
            <li class="flex">
              <div class="bg-secondary/20 text-accent rounded-full w-10 h-10 flex items-center justify-center mr-3 shrink-0">
                <i class="fa fa-trophy"></i>
              </div>
              <div>
                <p class="text-white/80">何正阳设计作品展示</p>
                <p class="text-white/60 text-sm">2025-06-15</p>
              </div>
            </li>
          </ul>
        </div>
        
        <!-- 订阅 -->
        <div>
          <h3 class="text-xl font-bold mb-6">订阅更新</h3>
          <p class="text-white/80 mb-4">订阅我们的家庭动态，第一时间获取最新消息</p>
          <form class="space-y-3">
            <div>
              <input type="email" placeholder="您的邮箱地址" class="w-full px-4 py-3 rounded-lg bg-white/10 border border-white/20 text-white placeholder-white/40 focus:outline-none focus:ring-2 focus:ring-secondary">
            </div>
            <button type="submit" class="w-full bg-secondary hover:bg-secondary/90 text-accent font-bold py-3 px-6 rounded-lg transition-colors">
              订阅更新
            </button>
          </form>
        </div>
      </div>
      
      <div class="border-t border-white/20 mt-12 pt-8 text-center">
        <p class="text-white/70">&copy; 2025 HOME家庭网站 - 保留所有权利</p>
      </div>
    </div>
  </footer>

  <!-- 照片查看模态框 -->
  <div id="photo-modal" class="fixed inset-0 bg-black/90 z-50 flex items-center justify-center opacity-0 invisible transition-all duration-300">
    <button id="close-modal" class="absolute top-6 right-6 text-white text-3xl hover:text-secondary transition-colors">
      <i class="fa fa-times"></i>
    </button>
    <div class="max-w-4xl w-full mx-4">
      <img id="modal-image" src="" alt="大图预览" class="w-full h-auto max-h-[80vh] object-contain">
      <div class="mt-4 text-center">
        <h3 id="modal-title" class="text-white text-xl font-bold"></h3>
        <p id="modal-description" class="text-white/80"></p>
      </div>
    </div>
  </div>

  <!-- 返回顶部按钮 -->
  <button id="back-to-top" class="fixed bottom-6 right-6 bg-primary hover:bg-primary/90 text-white w-12 h-12 rounded-full flex items-center justify-center shadow-lg transform translate-y-20 opacity-0 transition-all duration-300 z-40">
    <i class="fa fa-chevron-up"></i>
  </button>

  <!-- JavaScript -->
  <script>
    // 导航栏滚动效果
    const navbar = document.getElementById('navbar');
    window.addEventListener('scroll', () => {
      if (window.scrollY > 50) {
        navbar.classList.add('py-2', 'shadow-md');
        navbar.classList.remove('py-3');
      } else {
        navbar.classList.add('py-3');
        navbar.classList.remove('py-2', 'shadow-md');
      }
    });

    // 移动端菜单
    const menuBtn = document.getElementById('menuBtn');
    const mobileMenu = document.getElementById('mobileMenu');
    
    menuBtn.addEventListener('click', () => {
      mobileMenu.classList.toggle('hidden');
      if (mobileMenu.classList.contains('hidden')) {
        menuBtn.innerHTML = '<i class="fa fa-bars"></i>';
      } else {
        menuBtn.innerHTML = '<i class="fa fa-times"></i>';
      }
    });

    // 平滑滚动
    document.querySelectorAll('a[href^="#"]').forEach(anchor => {
      anchor.addEventListener('click', function (e) {
        e.preventDefault();
        
        // 关闭移动菜单
        if (!mobileMenu.classList.contains('hidden')) {
          mobileMenu.classList.add('hidden');
          menuBtn.innerHTML = '<i class="fa fa-bars"></i>';
        }
        
        const targetId = this.getAttribute('href');
        const targetElement = document.querySelector(targetId);
        
        if (targetElement) {
          window.scrollTo({
            top: targetElement.offsetTop - 80,
            behavior: 'smooth'
          });
        }
      });
    });

    // 返回顶部按钮
    const backToTopBtn = document.getElementById('back-to-top');
    
    window.addEventListener('scroll', () => {
      if (window.scrollY > 300) {
        backToTopBtn.classList.remove('translate-y-20', 'opacity-0');
        backToTopBtn.classList.add('translate-y-0', 'opacity-100');
      } else {
        backToTopBtn.classList.add('translate-y-20', 'opacity-0');
        backToTopBtn.classList.remove('translate-y-0', 'opacity-100');
      }
    });
    
    backToTopBtn.addEventListener('click', () => {
      window.scrollTo({
        top: 0,
        behavior: 'smooth'
      });
    });

    // 相册过滤
    const filterBtns = document.querySelectorAll('.gallery-filter-btn');
    const galleryItems = document.querySelectorAll('.gallery-item');
    
    filterBtns.forEach(btn => {
      btn.addEventListener('click', () => {
        // 更新按钮样式
        filterBtns.forEach(b => {
          b.classList.remove('active', 'bg-primary', 'text-white');
          b.classList.add('bg-gray-200', 'text-gray-700');
        });
        btn.classList.add('active', 'bg-primary', 'text-white');
        btn.classList.remove('bg-gray-200', 'text-gray-700');
        
        // 过滤项目
        const filter = btn.getAttribute('data-filter');
        
        galleryItems.forEach(item => {
          if (filter === 'all' || item.getAttribute('data-category') === filter) {
            item.style.display = 'block';
          } else {
            item.style.display = 'none';
          }
        });
      });
    });

    // 照片查看模态框
    const photoModal = document.getElementById('photo-modal');
    const modalImage = document.getElementById('modal-image');
    const modalTitle = document.getElementById('modal-title');
    const modalDescription = document.getElementById('modal-description');
    const closeModal = document.getElementById('close-modal');
    const viewPhotoBtns = document.querySelectorAll('.view-photo-btn');
    
    viewPhotoBtns.forEach(btn => {
      btn.addEventListener('click', () => {
        const galleryItem = btn.closest('.gallery-item');
        const image = galleryItem.querySelector('img');
        const title = galleryItem.querySelector('h3').textContent;
        const description = galleryItem.querySelector('p').textContent;
        
        modalImage.src = image.src;
        modalImage.alt = image.alt;
        modalTitle.textContent = title;
        modalDescription.textContent = description;
        
        photoModal.classList.remove('opacity-0', 'invisible');
        document.body.style.overflow = 'hidden';
      });
    });
    
    closeModal.addEventListener('click', () => {
      photoModal.classList.add('opacity-0', 'invisible');
      document.body.style.overflow = 'auto';
    });
    
    // 点击模态框背景关闭
    photoModal.addEventListener('click', (e) => {
      if (e.target === photoModal) {
        photoModal.classList.add('opacity-0', 'invisible');
        document.body.style.overflow = 'auto';
      }
    });

    // 联系表单
    const contactForm = document.getElementById('contact-form');
    
    contactForm.addEventListener('submit', (e) => {
      e.preventDefault();
      
      // 简单验证
      const name = document.getElementById('name').value;
      const email = document.getElementById('email').value;
      const subject = document.getElementById('subject').value;
      const message = document.getElementById('message').value;
      
      if (!name || !email || !subject || !message) {
        alert('请填写所有字段');
        return;
      }
      
      // 模拟提交成功
      alert('消息已发送！我们会尽快回复您。');
      contactForm.reset();
    });

    // 日历月份切换
    const currentMonthEl = document.getElementById('current-month');
    const prevMonthBtn = document.getElementById('prev-month');
    const nextMonthBtn = document.getElementById('next-month');
    
    let currentMonth = 6;
    let currentYear = 2025;
    
    prevMonthBtn.addEventListener('click', () => {
      currentMonth--;
      if (currentMonth < 1) {
        currentMonth = 12;
        currentYear--;
      }
      currentMonthEl.textContent = `${currentYear}年${currentMonth}月`;
    });
    
    nextMonthBtn.addEventListener('click', () => {
      currentMonth++;
      if (currentMonth > 12) {
        currentMonth = 1;
        currentYear++;
      }
      currentMonthEl.textContent = `${currentYear}年${currentMonth}月`;
    });

    // 添加新活动按钮
    const addEventBtn = document.getElementById('add-event');
    
    addEventBtn.addEventListener('click', () => {
      alert('活动添加功能将在未来版本中实现');
    });

    // 加载更多照片按钮
    const loadMoreBtn = document.getElementById('load-more');
    
    loadMoreBtn.addEventListener('click', () => {
      alert('更多照片将在未来版本中加载');
    });
  </script>
</body>
</html>
