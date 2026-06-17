<!DOCTYPE html>
<html lang="zh-TW">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>我的專屬足球現場直播台</title>
    <!-- 引入專業直播播放器核心 -->
    <link href="https://zencdn.net" rel="stylesheet" />
    <style>
        body { background-color: #0b0e14; color: #ffffff; font-family: sans-serif; margin: 0; padding: 20px; text-align: center; }
        .container { max-width: 900px; margin: 0 auto; }
        h1 { color: #00ff87; border-bottom: 2px solid #00ff87; padding-bottom: 15px; }
        .scoreboard { background: #1a1f2c; border-radius: 12px; padding: 20px; margin: 20px 0; display: flex; justify-content: space-around; align-items: center; }
        .score { font-size: 2.5rem; font-weight: bold; color: #00ff87; background: #0b0e14; padding: 5px 15px; border-radius: 8px; }
        /* 直播播放器外觀設定 */
        .video-box { margin-top: 20px; background: #000; border-radius: 12px; overflow: hidden; box-shadow: 0 10px 30px rgba(0,0,0,0.7); }
        .video-js { width: 100% !important; height: auto !important; aspect-ratio: 16/9; }
        .notice { background: #2a1a1a; border: 1px solid #ff4a4a; padding: 10px; border-radius: 8px; margin: 15px 0; color: #ff9999; font-size: 0.9rem; }
    </style>
</head>
<body>
<div class="container">
    <h1>⚽ 我的專屬足球現場直播台</h1>
    
    <div class="scoreboard">
        <h2>🇦🇷 阿根廷</h2>
        <div class="score">0 : 0</div>
        <h2>奧地利 🇦🇹</h2>
    </div>

    <div class="notice">
        💡 <b>直播觀看提示：</b>下方為獨立網路直播通道。如果開賽時畫面卡頓，可以在後台替換最新的 M3U8 直播訊號源。
    </div>

    <!-- 專業直播播放器 -->
    <div class="video-box">
        <video id="football-live" class="video-js vjs-default-skin vjs-big-play-centered" controls preload="auto" poster="https://unsplash.com">
            <!-- 這裡是網路免費足球直播的串流訊號源 (M3U8) -->
            <source src="https://mux.dev" type="application/x-mpegURL">
            <p class="vjs-no-js">您的瀏覽器不支援此播放器</p>
        </video>
    </div>
</div>

<!-- 引入播放器核心 JavaScript -->
<script src="https://zencdn.net"></script>
<script>
    var player = videojs('football-live');
</script>
</body>
</html>
# soccer-tv
