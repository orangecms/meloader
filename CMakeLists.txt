cmake_minimum_required(VERSION 3.13)
project(meloader C)

set(CMAKE_C_STANDARD 11)
set (CMAKE_C_FLAGS "-m32")
include_directories(include)

add_executable(meloader
        include/manifest.h
        user/loader/manifest.c
        user/loader/map.c
        include/user/meloader.h
        user/loader/me_abi.c
        user/kernel/threads.c
        user/romlib/mmio.c
        include/user/romlib.h
        include/printf.h
        include/numfmt.h
        user/romlib/thunks.c
        user/kernel/memory.c
        util/numfmt.c
        util/printf.c
        periph/tracehub/gth.c
        include/tracehub.h
        periph/tracehub/rs1.c
        periph/tracehub/ftmr.c
        util/trace.c
        include/mipitrace.h
        user/syslib/kernelcall.c
        include/user/syslib.h
        user/syslib/tls.c
        user/syslib/thunks.c
        periph/ocs/sks/sks.c
        periph/spi/spi.c
        user/kernel/snowball.c
        periph/ocs/hash/hash.c
        periph/ocs/aes/aes.c
        include/ocs/hash/sha256.h
        periph/ocs/hash/sha256.c
        include/ocs/hash/rotate-bits.h
        user/kernel/dma.c
        user/kernel/grant.c
        include/grant.h
        periph/ocs/dma/gpdma.c
        include/ocs/gpdma.h
        periph/sideband/sbdev.c
        include/sideband.h
        util/log.c
        include/log.h
        include/cfg_file.h
        config/cfgparser.c
        config/devreg.c
        include/devreg.h
        include/misa/regs.h
        include/misa/emu.h
        include/pci/bus.h
        include/pci/device.h
        include/pci/cfgspace.h
        periph/pci/master.c
        periph/pci/simplefunc.c
        periph/pci/config.c
        periph/misa/hunit.c
        periph/misa/aunit/upstream.c
        periph/misa/bunit.c
        periph/misa/aunit/bus_target.c
        periph/misa/aunit/iommu.c
        periph/misa/dev.c
        include/fsb.h
        periph/cpu/usercpu.c
        include/cpu/usercpu.h
        user/loader/meloader.c
        util/file.c
        include/file.h
        periph/gasket/prim2gasket/dev.c
        periph/gasket/att/prim_bus.c
        periph/gasket/att/prim_regs.c
        periph/gasket/att/sb_regs.c
        periph/gasket/att/sb_master.c
        periph/gasket/att/dev.c
        include/gasket/att/regs.h
        periph/spi/dev.c
        periph/ocs/dev.c include/ocs/dev.h include/ocs/sks.h include/ocs/hash/hash.h include/ocs/aes.h include/fastspi.h periph/fuse/fusectl.c include/fusectl.h user/kernel/select.c periph/pmc/dev.c include/pmc.h periph/dfxagg/dev.c include/dfxagg.h include/exi.h periph/exi/dev.c periph/gasket/heci/dev.c include/gasket/heci/heci.h periph/gasket/heci/status.c)
