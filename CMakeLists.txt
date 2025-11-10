cmake_minimum_required(VERSION 3.20.0)
find_package(Zephyr REQUIRED HINTS $ENV{ZEPHYR_BASE})
project(zmk_feature_charge_indicator)

if(CONFIG_CHARGE_INDICATOR)
  target_sources(app PRIVATE src/charge_indicator.c)
endif()