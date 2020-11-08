# SASL-Timer-Library
timer_library.lua
    Jeffory J. Beckers
    Jemma Studios
    MIT License
    25 October 2020
    ver 1.0.0

    Looking-For-A-Handout-Ware https://paypal.me/JemmaStudios

    Sets up xLua style function timer for SASL 3.  Makes life a little simpler when converting a project from xLua to SASL

    LIBARY SETUP.
    Drop this script in the "plugins\sasl\data\modules\Custom Module" folder
    add it as a component in "plugins\sasl\data\modules\main.lua"
    add the line "timer_lib = {}" anywhere in your main.lua script

    USAGE:
    After completing the setup above, the following functions can be called from any other subcomponent in your project.

    (If the following function documentation looks familiar it's because I plagarized from JGregory's xLua post)
    You can create a timer out of any function. Timer functions take no arguments. 

    timer_lib.run_at_interval(func, interval)
    Runs func every interval seconds, starting interval seconds from the call.

    timer_lib.run_after_time(func, delay)
    Runs func once after delay seconds, then timer stops.

    timer_lib.run_timer(func, delay, interval)
    Runs func after delay seconds, then every interval seconds after that.

    timer_lib.stop_timer(func)
    This ensures that func does not run again until you re­schedule it; any scheduled runs from previous calls are canceled.

    timer_lib.is_timer_scheduled(func)
    This returns true if the timer function will run at any time in the future. It returns false if the timer isn’t 
    scheduled or if func has never been used as a timer.

    BONUS features!
    timer_lib.SIM_PERIOD
    contains the duration of the current frame in seconds (so it is always a fraction). Use this to normalize rates, 
    e.g. to add 3 units of fuel per second in a per­frame callback you’d do fuel = fuel + 3 * SIM_PERIOD

    timer_lib.RUN_TIME_SEC
    contains the elapsed running time of the X-plane session in seconds

    timer_lib.FLIGHT_TIME_SEC
    contains the elapsed time of the current flight in seconds.