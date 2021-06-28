# particles.js-demo
a Starry background demo of particles.js

> 官方给的例子有点复杂，项目中一般就引一个 JS 文件然后调用好了，简单粗暴，网上很少有想要的效果，而且都没有源码，这里分享一个


# 一、源码地址
 - 效果演示：https://zhichaosong.github.io/particles-js/
 - 官方地址：https://github.com/VincentGarreau/particles.js
 - demo地址：https://github.com/zhichaosong/particles.js-demo
 - CSDN下载：https://download.csdn.net/download/zhichaosong/11238470
# 二、实现效果
## 1. 电脑端
![在这里插入图片描述](https://img-blog.csdnimg.cn/20190613021042104.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3poaWNoYW9zb25n,size_16,color_FFFFFF,t_70)
## 2. 手机端
![手机端](https://img-blog.csdnimg.cn/20190613021003256.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3poaWNoYW9zb25n,size_16,color_FFFFFF,t_70)

# 三、源码
```html
<!DOCTYPE html>
<html>
<head>
<style>
	.diy-bg {
        position: fixed;
        width: 100%;
        height: 100%;
		background-image: url(loginbg.jpg);
		background-size: cover;
	}
</style>
</head>

<body style="margin: 0;">
<div id="particles-js" class="diy-bg">
    <canvas class="particles-js-canvas-el" width="980" height="1742" style="width: 100%; height: 100%;"></canvas>
</div>
<script src="particles.min.js"></script>
<script>
    particlesJS("particles-js", {
        particles: {
            number: {
                value: 120,
                density: {
                    enable: true,
                    value_area: 800
                }
            },
            color: {
                value: "#ffffff"
            },
            shape: {
                type: "circle",
                stroke: {
                    width: 0,
                    color: "#000000"
                },
                polygon: {
                    nb_sides: 5
                },
                image: {
                    src: "img/github.svg",
                    width: 100,
                    height: 100
                }
            },
            opacity: {
                value: .5,
                random: false,
                anim: {
                    enable: false,
                    speed: 1,
                    opacity_min: .1,
                    sync: false
                }
            },
            size: {
                value: 1,
                random: true,
                anim: {
                    enable: false,
                    speed: 20,
                    size_min: .1,
                    sync: false
                }
            },
            line_linked: {
                enable: true,
                distance: 40,
                color: "#fff",
                opacity: 1,
                width: 1
            },
            move: {
                enable: true,
                speed: 3,
                direction: "none",
                random: false,
                straight: false,
                out_mode: "out",
                attract: {
                    enable: false,
                    rotateX: 600,
                    rotateY: 1200
                }
            }
        },
        interactivity: {
            detect_on: "canvas",
            events: {
                onhover: {
                    enable: true,
                    mode: "grab"
                },
                onclick: {
                    enable: true,
                    mode: "push"
                },
                resize: true
            },
            modes: {
                grab: {
                    distance: 120,
                    line_linked: {
                        opacity: 1
                    }
                },
                bubble: {
                    distance: 400,
                    size: 40,
                    duration: 2,
                    opacity: 8,
                    speed: 3
                },
                repulse: {
                    distance: 300
                },
                push: {
                    particles_nb: 4
                },
                remove: {
                    particles_nb: 2
                }
            }
        },
        retina_detect: true,
        config_demo: {
            hide_card: false,
            background_color: "#b61924",
            background_image: "",
            background_position: "50% 50%",
            background_repeat: "no-repeat",
            background_size: "cover"
        }
    });
</script>

</body>
</html>
```
