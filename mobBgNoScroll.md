# 移动端禁止蒙层底部页面跟随滚动
    // 设置 body fixed
    let bodyEl = document.body
    let top = 0

    function stopBodyScroll (isFixed) {
        if (isFixed) {
            top = window.scrollY

            bodyEl.style.position = 'fixed'
            bodyEl.style.top = -top + 'px'
        } else {
            bodyEl.style.position = ''
            bodyEl.style.top = ''

            window.scrollTo(0, top) // 回到原先的top
        }
    }