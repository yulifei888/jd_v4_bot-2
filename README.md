#最后两行二选一，根据自己的平台，一键部署v4_bot

    docker run -dit \
    -v $PWD/jd_v4_bot/config:/jd/config \
    -v $PWD/jd_v4_bot/log:/jd/log \
    -v $PWD/jd_v4_bot/own:/jd/own \
    -v $PWD/jd_v4_bot/diy:/jd/jbot/diy \
    -v $PWD/jd_v4_bot/scripts:/jd/scripts \
    -p 5678:5678 \
    -e ENABLE_HANGUP=true \
    -e ENABLE_WEB_PANEL=true \
    -e ENABLE_WEB_TTYD=true \
    -e ENABLE_TG_BOT=true \
    --name jd_v4_bot \
    --hostname jd_v4_bot \
    --restart always \
    anyline/jd:v4_bot_amd64
    anyline/jd:v4_bot_arm
