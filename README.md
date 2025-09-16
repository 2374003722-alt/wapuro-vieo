[测试.html](https://github.com/user-attachments/files/22354595/default.html)
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>WAPURO与创作者业务合作平台</title>
    <style>
        /* 基础样式 */
        body {
            font-family: "Noto Sans JP", "sans-serif";
            margin: 0;
            padding: 0;
            background-color: #F5F5DC;
            color: #333;
            line-height: 1.6;
        }
        
        .container {
            width: 90%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 15px;
        }
        
        /* 头部样式 */
        header {
            background-color: #8B5A2B;
            color: white;
            padding: 20px 0;
            box-shadow: 0 2px 5px rgba(0,0,0,0.2);
        }
        
        header h1 {
            text-align: center;
            margin: 0 0 20px 0;
            font-size: 2em;
        }
        
        nav ul {
            list-style: none;
            padding: 0;
            margin: 0;
            text-align: center;
            flex-wrap: wrap;
            display: flex;
            justify-content: center;
        }
        
        nav li {
            margin: 0 10px 10px;
        }
        
        nav a {
            color: white;
            text-decoration: none;
            padding: 5px 10px;
            transition: color 0.3s;
            display: inline-block;
        }
        
        nav a:hover {
            color: #D2B48C;
        }
        
        /* 主要内容样式 */
        main {
            padding: 30px 0;
        }
        
        .section-title {
            text-align: center;
            color: #8B5A2B;
            margin: 40px 0 20px;
            padding-bottom: 10px;
            border-bottom: 2px solid #D2B48C;
        }
        
        section {
            margin-bottom: 40px;
            background-color: white;
            border-radius: 8px;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
            overflow: hidden;
            transition: transform 0.3s, box-shadow 0.3s;
        }
        
        section:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 20px rgba(0,0,0,0.1);
        }
        
        .section-header {
            background-color: rgba(139, 90, 43, 0.1);
            padding: 15px 20px;
            border-bottom: 1px solid rgba(139, 90, 43, 0.2);
        }
        
        .section-header h2 {
            margin: 0;
            color: #8B5A2B;
            font-size: 1.5em;
        }
        
        .section-content {
            padding: 20px;
        }
        
        .content-wrapper {
            display: flex;
            flex-direction: column;
        }
        
        @media (min-width: 768px) {
            .content-wrapper {
                flex-direction: row;
                gap: 30px;
            }
            
            .features {
                flex: 1;
            }
            
            .video-section {
                flex: 1;
            }
        }
        
        .features h3, .video-section h3 {
            color: #3E2723;
            border-bottom: 2px solid #D2B48C;
            padding-bottom: 10px;
            margin-top: 0;
        }
        
        .features ul {
            list-style: none;
            padding: 0;
        }
        
        .features li {
            margin-bottom: 10px;
            padding-left: 25px;
            position: relative;
        }
        
        .features li:before {
            content: "✓";
            color: #8B5A2B;
            position: absolute;
            left: 0;
            font-weight: bold;
        }
        
        /* 合作细则样式 */
        .rules-section {
            padding: 30px;
            background-color: white;
            border-radius: 8px;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
            margin-bottom: 40px;
        }
        
        .rules-section h2 {
            color: #8B5A2B;
            border-bottom: 2px solid #D2B48C;
            padding-bottom: 10px;
            margin-top: 0;
        }
        
        .rules-section h3 {
            color: #3E2723;
            margin-top: 25px;
        }
        
        .rules-section p, .rules-section li {
            margin-bottom: 10px;
        }
        
        .rules-section ul {
            padding-left: 20px;
        }
        
        .table-wrapper {
            overflow-x: auto;
            margin: 15px 0;
        }
        
        .rules-table {
            width: 100%;
            border-collapse: collapse;
            margin: 15px 0;
        }
        
        .rules-table th, .rules-table td {
            border: 1px solid #ddd;
            padding: 12px;
            text-align: left;
        }
        
        .rules-table th {
            background-color: rgba(139, 90, 43, 0.1);
            color: #8B5A2B;
        }
        
        /* 视频容器样式 */
        .video-container {
            position: relative;
            padding-bottom: 56.25%;
            height: 0;
            overflow: hidden;
            background-color: #f0f0f0;
            border-radius: 5px;
            margin-bottom: 15px;
        }
        
        .video-container iframe {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            border: 0;
        }
        
        .video-links {
            margin-top: 15px;
        }
        
        .video-links h4 {
            margin-bottom: 10px;
            color: #3E2723;
        }
        
        .video-links a {
            display: block;
            color: #8B5A2B;
            text-decoration: none;
            margin-bottom: 8px;
            padding-left: 15px;
            position: relative;
        }
        
        .video-links a:before {
            content: "→";
            position: absolute;
            left: 0;
            color: #8B5A2B;
        }
        
        .video-links a:hover {
            color: #6d4421;
            text-decoration: underline;
        }
        
        .video-caption {
            text-align: center;
            color: #666;
            font-size: 0.9em;
            margin-top: 10px;
        }
        
        /* 页脚样式 */
        footer {
            background-color: #3E2723;
            color: white;
            text-align: center;
            padding: 20px 0;
            margin-top: 50px;
        }
        
        /* 返回顶部按钮 */
        #backToTop {
            position: fixed;
            bottom: 20px;
            right: 20px;
            background-color: #8B5A2B;
            color: white;
            width: 50px;
            height: 50px;
            border-radius: 50%;
            border: none;
            cursor: pointer;
            display: none;
            justify-content: center;
            align-items: center;
            box-shadow: 0 2px 10px rgba(0,0,0,0.3);
            font-size: 1.2em;
            transition: background-color 0.3s;
        }
        
        #backToTop:hover {
            background-color: #6d4421;
        }
        
        /* 平滑滚动 */
        html {
            scroll-behavior: smooth;
        }
    </style>
</head>
<body>
    <!-- 顶部导航 -->
    <header>
        <div class="container">
            <h1>WAPURO创作者合作平台</h1>
            <nav>
                <ul>
                    <li><a href="#rules">合作细则</a></li>
                    <li><a href="#one-price">一口价质量参考</a></li>
                    <li><a href="#japanese">日式风格</a></li>
                    <li><a href="#wabi-sabi">侘寂风格</a></li>
                    <li><a href="#log">原木风格</a></li>
                    <li><a href="#minimalist">极简风格</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <!-- 主要内容 -->
    <main class="container">
        <!-- 合作细则部分 -->
        <section id="rules" class="rules-section">
            <h2>《WAPURO与创作者业务合作细则》</h2>
            
            <h3>一、 合作总览</h3>
            <p><strong>合作基础：</strong>本次合作以单款产品试拍为起点，旨在建立长期合作关系。首期视频验收达标后，将开放多款产品同时拍摄的长期合作模式。</p>
            <p><strong>合作性质：</strong>诚邀素人创作者/大学生，无粉丝量要求，重在拍摄审美与内容质量。</p>
            <p><strong>核心流程：</strong>品牌直送样品 → 协商报价并确认接收档期情况（包裹签收即开始档期） → 拍摄制作 → 验收修改 → 费用结算。</p>
            
            <h3>二、 费用与结算</h3>
            <div class="table-wrapper">
                <table class="rules-table">
                    <tr>
                        <th>项目</th>
                        <th>说明</th>
                    </tr>
                    <tr>
                        <td>费用构成</td>
                        <td>基础费用 (30-80元) + 视频质量奖励 (20-50元)</td>
                    </tr>
                    <tr>
                        <td>一口价</td>
                        <td>拍摄质量优异者可协商一口价，若验收未达一口价标准，则按“基础+奖励”结算。（有一口价视频参考标准）</td>
                    </tr>
                    <tr>
                        <td>结算方式</td>
                        <td>品牌方验收通过后，全款打入指定账户（结算以公帐结算，需要提供银行账户以及银行账户持有人名字）。长期合作后，按款按条数单独结算。</td>
                    </tr>
                    <tr>
                        <td>超时扣款</td>
                        <td>从包裹签收后72小时内需提交初稿，超时按总费用1%/小时扣款，累计最高不超过30%。</td>
                    </tr>
                </table>
            </div>
            
            <h3>三、 产品、样品与版权</h3>
            <p><strong>样品政策：</strong>产品由品牌方免费直发送拍（包邮），样品无需退回，签收即视为合作生效。</p>
            <p><strong>版权买断：</strong>视频采用买断制，品牌方享有唯一发布权、使用权及完整著作权。产品主销外网，视频将用于海外社交媒体发布。</p>
            
            <h3>四、 视频要求与制作规范</h3>
            <div class="table-wrapper">
                <table class="rules-table">
                    <tr>
                        <th>类别</th>
                        <th>要求明细</th>
                    </tr>
                    <tr>
                        <td>内容要求</td>
                        <td>1条30秒至1分钟的精剪成品视频 + 全部原始未剪辑素材（多角度、多场景）</td>
                    </tr>
                    <tr>
                        <td>技术标准</td>
                        <td>
                            • 分辨率: 4K 或以上<br>
                            • 帧率: 60fps 或以上<br>
                            • 格式: MP4<br>
                            • 画质: 清晰不模糊，光线自然（不过曝、不压暗）
                        </td>
                    </tr>
                    <tr>
                        <td>风格与场景</td>
                        <td>
                            • 日式风格：整体简约，可参考侘寂、极简、原木风格（会提供参考视频）。<br>
                            • 拍摄多样化，但无需口播。<br>
                            • 场景中不出现任何中文元素（可出现英文或日文）。
                        </td>
                    </tr>
                    <tr>
                        <td>剪辑与文案</td>
                        <td>
                            • 精剪视频需添加日文字幕（可使用AI/机翻，但需保证基本语义通顺）。<br>
                            • 原素材必须提供，要求包含不少于8个片段，涵盖5-8个切换角度（如：俯拍、平拍、正拍、特写等）。<br>
                            • 成品禁止添加任何转场特效。
                        </td>
                    </tr>
                </table>
            </div>
            
            <h3>五、 验收与交付流程</h3>
            <p><strong>交付期限：</strong>创作者需在签收样品后72小时内提交第一版视频。</p>
            <p><strong>验收流程：</strong></p>
            <ul>
                <li>初稿需添加全屏水印供审核。</li>
                <li>品牌方提供修改意见，原则上支持1-2次修改。</li>
                <li>验收通过后，创作者需在24小时内交付无水印的最终成片及所有原素材。</li>
            </ul>
            <p><strong>交付格式：</strong>所有文件（成品视频 + 原始素材）需整合为一个压缩包发送。</p>
            
            <h3>六、 长期合作</h3>
            <p>首期合作效果达到双方预期后，可开启长期合作，合作模式包括：</p>
            <ul>
                <li>同时选择多款产品进行拍摄。</li>
                <li>费用和档期可具体详谈，提供更具竞争力的报价。</li>
            </ul>
            
            <h3>七、 拍摄质量无法支持结算情况</h3>
            <h4>一、 视为根本性违约，不予结算的情况：</h4>
            <p>若作品出现以下任何一项严重问题，则视为根本性违约，品牌方有权拒绝结算任何费用，且创作者需承担相应责任：</p>
            <ul>
                <li>技术规格严重不符：未能达到协议规定的硬性技术标准（如：分辨率过低、视频模糊不清晰，格式非MP4）。</li>
                <li>内容要求完全偏离：视频中出现任何中文元素（品牌方允许的除外），或出现了品牌方明确禁止的内容。</li>
                <li>版权与真实性缺陷：
                    <ul>
                        <li>视频非创作者原创，存在盗用、抄袭等版权纠纷。</li>
                        <li>未按约定提供原始未剪辑素材，或提供的原始素材与成片不符、数量严重不足（远少于8个片段）。</li>
                    </ul>
                </li>
                <li>严重超时且失联：严重超出约定交付时间（例如，超过约定时间24小时以上）且无法联系、未做出任何合理解释和沟通。</li>
            </ul>
            
            <h4>二、 可修改补救或部分结算的情况：</h4>
            <p>若作品基础质量达标，但存在以下可修改的问题，品牌方应提供明确的修改意见，创作者需配合完成修改：</p>
            <ul>
                <li>场景搭建问题：日式风格体现不足、场景杂乱、出现无关物品等。</li>
                <li>剪辑与文案问题：日文字幕机翻痕迹过重导致语义不通、节奏不佳、时长不符等。</li>
                <li>画质问题：光线略有过曝或压暗（经提醒后可重拍或调整）、画面稳定性不够等。</li>
            </ul>
            <p><strong>处理方式：</strong>创作者应在约定时间内完成修改（一般不超过48小时）。若经1-2次修改后仍无法验收通过，品牌方有权：</p>
            <ul>
                <li>方案A（推荐）：与创作者协商，按基础费用的50% 进行部分结算，品牌方获得当前作品有限的使用权。</li>
                <li>方案B：终止本项目合作，不予结算，但样品也无需退还。乙方提供2-3个无水印未剪辑原素材视频作为等价交换。</li>
            </ul>
            
            <h4>三、 样品处理</h4>
            <p>无论合作是否成功，为简化流程，所有寄出的样品均无需创作者退回。</p>
            
            <h4>四、 免责终止</h4>
            <p>若因不可抗力（如自然灾害、设备意外损坏等）导致无法完成拍摄，创作者需提供必要证明并及时告知，双方可协商免责终止合作，不产生违约金。</p>
            
            <p style="margin-top: 30px; font-weight: bold;">请确认以上协议细则，如无异议，即可开始首期合作。期待您的精彩创作！</p>
            <p>WAPURO 团队</p>
        </section>

        <!-- 一口价视频质量参考 -->
        <h2 class="section-title">视频参考标准</h2>
        <section id="one-price">
            <div class="section-header">
                <h2>一口价视频质量参考</h2>
            </div>
            <div class="section-content">
                <div class="content-wrapper">
                    <div class="features">
                        <h3>特点</h3>
                        <ul>
                            <li>分辨率达到4K及以上，画面清晰无模糊</li>
                            <li>帧率稳定在60fps以上，动态画面流畅</li>
                            <li>光线均匀，不曝不暗，色彩还原真实</li>
                            <li>多角度拍摄（不少于5-8个场景切换）</li>
                            <li>剪辑节奏得当，无多余转场，突出产品卖点</li>
                            <li>无中文元素，日文文案准确（可AI翻译）</li>
                        </ul>
                    </div>
                    <div class="video-section">
                        <h3>参考视频</h3>
                        <div class="video-container">
                            <iframe 
                                src="https://www.xiaohongshu.com/discovery/item/68c7b4c5000000001d007e0c?source=webshare&xhsshare=pc_web&xsec_token=YBzU-ikmnhWhWhwncytbEvPTkD2eLYikIccKEUdQjxSfE=&xsec_source=pc_share" 
                                allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" 
                                allowfullscreen>
                            </iframe>
                        </div>
                        <div class="video-links">
                            <h4>更多参考链接：</h4>
                            <a href="https://www.xiaohongshu.com/discovery/item/68c7ae40000000001d02cfec?source=webshare&xhsshare=pc_web&xsec_token=YBzU-ikmnhWhWhwncytbEvPVVr0OSgt1q1VD1tqXYacZ8=&xsec_source=pc_share" target="_blank">一口价标准视频示例1</a>
                            <a href="https://www.xiaohongshu.com/discovery/item/68c78a3c000000001c03c3c0?source=webshare&xhsshare=pc_web&xsec_token=GBgMnhbmByZzteDPitGZBMBfaamPZJkp1-pRsBbN2F1aI=&xsec_source=pc_share" target="_blank">一口价标准视频示例2</a>
                            <a href="https://www.xiaohongshu.com/discovery/item/68c7bccd000000001b032860?source=webshare&xhsshare=pc_web&xsec_token=YBzU-ikmnhWhWhwncytbEvPbKM2SClMAu0T0fyIw4Lqvs=&xsec_source=pc_share">产品多角度拍摄参考</a>
                        </div>
                        <p class="video-caption">示例视频：高质量产品拍摄参考</p>
                    </div>
                </div>
            </div>
        </section>

        <!-- 日式风格视频参考 -->
        <section id="japanese">
            <div class="section-header">
                <h2>日式风格视频参考</h2>
            </div>
            <div class="section-content">
                <div class="content-wrapper">
                    <div class="features">
                        <h3>特点</h3>
                        <ul>
                            <li>整体简约自然，注重留白和空间感</li>
                            <li>多使用原木色家具，线条简洁流畅</li>
                            <li>色调以米色、浅棕、白色为主，清新淡雅</li>
                            <li>可搭配日式传统元素（如榻榻米、障子门元素）</li>
                            <li>光线柔和，多采用自然光拍摄</li>
                            <li>场景整洁，无过多装饰，突出产品本身</li>
                        </ul>
                    </div>
                    <div class="video-section">
                        <h3>参考视频</h3>
                        <div class="video-container">
                            <iframe 
                                src="https://www.xiaohongshu.com/discovery/item/68c6ae99000000001c011f79?source=webshare&xhsshare=pc_web&xsec_token=ABQPTnAoZfx8OuP-97GoauhsilsJE_lpUNnth9KmwYPUc=&xsec_source=pc_share" 
                                allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" 
                                allowfullscreen>
                            </iframe>
                        </div>
                        <div class="video-links">
                            <h4>更多参考链接：</h4>
                            <a href=" https://www.xiaohongshu.com/discovery/item/687a3c7c0000000015023f78?source=webshare&xhsshare=pc_web&xsec_token=ABTjkb49ljUhHeA4srzpmwDo8ookdZeiTeEvcY5-b2bzg=&xsec_source=pc_share"_blank">日式家居空间展示1</a>
                            <a href=" https://www.xiaohongshu.com/discovery/item/680600b6000000001e004656?source=webshare&xhsshare=pc_web&xsec_token=ABw6BWe5zSUGmMUOK3w09LvXIM3UkUs97wlGGgQlewX0U=&xsec_source=pc_share">日式家居</a>
                            <a href=" https://www.xiaohongshu.com/discovery/item/65d848280000000007027c5d?source=webshare&xhsshare=pc_web&xsec_token=ABfBUC7hl-uiM1WRKFuBcJ-XnOJeNcq8gp3tQXSlWGprA=&xsec_source=pc_share" target="_blank">传统日式美学解析</a>
                        </div>
                        <p class="video-caption">示例视频：日式家居空间展示</p>
                    </div>
                </div>
            </div>
        </section>

        <!-- 侘寂风格视频参考 -->
        <section id="wabi-sabi">
            <div class="section-header">
                <h2>侘寂风格视频参考</h2>
            </div>
            <div class="section-content">
                <div class="content-wrapper">
                    <div class="features">
                        <h3>特点</h3>
                        <ul>
                            <li>呈现自然的残缺美，不追求完美无瑕</li>
                            <li>色调偏暗淡柔和，多为土色、棕色系</li>
                            <li>可使用做旧质感的道具，体现岁月痕迹</li>
                            <li>光线偏柔和昏暗，营造宁静氛围</li>
                            <li>装饰极简，多为天然材质物品</li>
                            <li>强调自然纹理，如木材的结疤、石材的纹路</li>
                        </ul>
                    </div>
                    <div class="video-section">
                        <h3>参考视频</h3>
                        <div class="video-container">
                            <iframe 
                                src="https://www.xiaohongshu.com/discovery/item/6739718d000000001d038e62?source=webshare&xhsshare=pc_web&xsec_token=ABXi71rSsycr6n_Pre70JDhzySsF-Jbu7WC7NHQXMziSg=&xsec_source=pc_share" 
                                allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" 
                                allowfullscreen>
                            </iframe>
                        </div>
                        <div class="video-links">
                            <h4>更多参考链接：</h4>
                            <a href="https://www.xiaohongshu.com/discovery/item/65d06aba000000000b01afc1?source=webshare&xhsshare=pc_web&xsec_token=ABusoNswFNXORLzPfz79xDh5CKyJU-_y1vzcUEXQ-TqWU=&xsec_source=pc_share" target="_blank">侘寂风1</a>
                            <a href="https://www.youtube.com/embed/wabi2" target="_blank">侘寂风格2</a>
                            <a href="https://www.xiaohongshu.com/discovery/item/67ab1e6a00000000290190ec?source=webshare&xhsshare=pc_web&xsec_token=ABDwmUJlabsm2M3Xsj5ck5DgaElNvBKC7Eu6nnR7ayZu0=&xsec_source=pc_share" target="_blank">自然质感场景搭建</a>
                        </div>
                        <p class="video-caption">示例视频：京都侘寂庭院景观</p>
                    </div>
                </div>
            </div>
        </section>

        <!-- 原木风格视频参考 -->
        <section id="log">
            <div class="section-header">
                <h2>原木风格视频参考</h2>
            </div>
            <div class="section-content">
                <div class="content-wrapper">
                    <div class="features">
                        <h3>特点</h3>
                        <ul>
                            <li>以天然木材为主要元素，展现木材自然纹理</li>
                            <li>色调以原木色为主，搭配白色、浅灰色等中性色</li>
                            <li>家具造型简洁，保留木材原始质感</li>
                            <li>可搭配绿植，营造自然清新氛围</li>
                            <li>光线充足，突出木材的自然光泽</li>
                            <li>整体风格温暖舒适，贴近自然</li>
                        </ul>
                    </div>
                    <div class="video-section">
                        <h3>参考视频</h3>
                        <div class="video-container">
                            <iframe 
                                src="https://www.xiaohongshu.com/discovery/item/67483ac60000000007036f90?source=webshare&xhsshare=pc_web&xsec_token=ABDE-zu5ahTYwEQIrhdE3cLvObncJAf917Hq8wbDE63s8=&xsec_source=pc_share" 
                                allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" 
                                allowfullscreen>
                            </iframe>
                        </div>
                        <div class="video-links">
                            <h4>更多参考链接：</h4>
                            <a href=" https://www.xiaohongshu.com/discovery/item/6822af1e000000002301e077?source=webshare&xhsshare=pc_web&xsec_token=ABQ56hmMOn7CL0Fmrc0c40sw9vVHyfMiCMfxmrPoFh930=&xsec_source=pc_share" target="_blank">原木材质</a>
                            <a href="https://www.xiaohongshu.com/discovery/item/67fcdf66000000001c02d51c?source=webshare&xhsshare=pc_web&xsec_token=ABzX1WYvy0TnHslJ_6UUZjMi3aqXqgIREQmJhQ995VVqk=&xsec_source=pc_share" target="_blank">原木产品</a>
                            <a href="https://www.xiaohongshu.com/discovery/item/656d4175000000000901ce7c?source=webshare&xhsshare=pc_web&xsec_token=AB7_1_xXEev3YeObMV9JIxBmJIWWAJ6X9TgzvJSBDpSfY=&xsec_source=pc_share" target="_blank">原木风场景布置</a>
                        </div>
                        <p class="video-caption">示例视频：原木家居设计展示</p>
                    </div>
                </div>
            </div>
        </section>

        <!-- 极简风格视频参考 -->
        <section id="minimalist">
            <div class="section-header">
                <h2>极简风格视频参考</h2>
            </div>
            <div class="section-content">
                <div class="content-wrapper">
                    <div class="features">
                        <h3>特点</h3>
                        <ul>
                            <li>去繁就简，仅保留必要元素，大量留白</li>
                            <li>色彩简洁，多为黑白灰或单色系</li>
                            <li>线条利落，几何感强，无多余装饰</li>
                            <li>场景整洁有序，无杂乱物品</li>
                            <li>光线均匀明亮，突出产品形态</li>
                            <li>强调产品本身的造型和功能美</li>
                        </ul>
                    </div>
                    <div class="video-section">
                        <h3>参考视频</h3>
                        <div class="video-container">
                            <iframe 
                                src=" https://www.xiaohongshu.com/discovery/item/6690dc80000000000a027782?source=webshare&xhsshare=pc_web&xsec_token=AB6CXO0nWBn9jfcfkto4pSUZ77-UNf5UlQiiq9pERmsUE=&xsec_source=pc_share" 
                                allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" 
                                allowfullscreen>
                            </iframe>
                        </div>
                        <div class="video-links">
                            <h4>更多参考链接：</h4>
                            <a href="https://www.xiaohongshu.com/discovery/item/6613c183000000001a0127ae?source=webshare&xhsshare=pc_web&xsec_token=AB0KWMlxucbM2eYylxu_X_uPGiuwhaNst_y_HAxMKSmv0=&xsec_source=pc_share">极简产品</a>
                            <a href="https://www.xiaohongshu.com/discovery/item/6577ad8c0000000009022ff2?source=webshare&xhsshare=pc_web&xsec_token=ABaVMrmIjvi8vM0uB_AIcILXzgJgx8ypjMxgwOQ-fh-lQ=&xsec_source=pc_share">产品极简拍摄案例</a>
                            <a href="https://www.xiaohongshu.com/discovery/item/663dfbc8000000001e019cbc?source=webshare&xhsshare=pc_web&xsec_token=ABJpqGT2cAVYEeUEwWfkPTlZXwVN3LBHNKUJgjdk30AqY=&xsec_source=pc_share">留白技巧与应用</a>
                        </div>
                        <p class="video-caption">示例视频：极简主义家居空间</p>
                    </div>
                </div>
            </div>
        </section>
    </main>

    <!-- 页脚 -->
    <footer>
        <div class="container">
            <p>WAPURO创作者合作平台 &copy; 2025</p>
            <p style="font-size: 0.9em; margin-top: 10px;">如有疑问，请联系我们</p>
        </div>
    </footer>

    <!-- 返回顶部按钮 -->
    <button id="backToTop">↑</button>

    <script>
        // 返回顶部按钮功能
        const backToTopBtn = document.getElementById('backToTop');
        
        window.addEventListener('scroll', () => {
            if (window.scrollY > 300) {
                backToTopBtn.style.display = 'flex';
            } else {
                backToTopBtn.style.display = 'none';
            }
        });
        
        backToTopBtn.addEventListener('click', () => {
            window.scrollTo({
                top: 0,
                behavior: 'smooth'
            });
        });

        // 视频懒加载
        document.addEventListener("DOMContentLoaded", function() {
            if ("IntersectionObserver" in window) {
                const videoObserver = new IntersectionObserver((entries, observer) => {
                    entries.forEach(entry => {
                        if (entry.isIntersecting) {
                            const iframe = entry.target.querySelector('iframe');
                            if (iframe) {
                                // 懒加载逻辑
                            }
                            observer.unobserve(entry.target);
                        }
                    });
                });

                document.querySelectorAll('.video-container').forEach(container => {
                    videoObserver.observe(container);
                });
            }
        });
    </script>
</body>
</html>
