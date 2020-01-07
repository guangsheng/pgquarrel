./pgquarrel --source-dbname=bike_config --source-host=10.111.10.63 --source-port=3007 --source-username=bike_config --source-tablename=t_city_config --target-dbname=bike_config --target-host=10.111.40.139 --target-port=3007 --target-username=bike_config --target-tablename=yzb_t_city_config --table-compare=true

需要修改




编译方法：
cd pgquarrel
cmake -DCMAKE_INSTALL_PREFIX=/dbdir/shiguangsheng/temp/pgquarrel/bin/ -DCMAKE_PREFIX_PATH=/usr/pgsql-10/
make
make install

说明：如果pg_config的配置不对，可以直接改CMakeLists.txt，直接指定路径：set(PGCONFIG_PATH /usr/pgsql-10/bin/pg_config)


测试方法
./pgquarrel --source-dbname=bike_config --source-host=10.111.10.63 --source-port=3007 --source-username=bike_config --source-tablename=t_city_config --target-dbname=bike_config --target-host=10.111.40.139 --target-port=3007 --target-username=bike_config --target-tablename=yzb_t_city_config --table-compare=true



####
hellobike@normal.

export LD_LIBRARY_PATH=$HOME/pgquarrel/:$LD_LIBRARY_PATH
./pgquarrel --help

./pgquarrel --source-dbname=bike_config --source-host=10.111.10.63 --source-port=3007 --source-username=bike_config --source-tablename=t_city_config --target-dbname=bike_config --target-host=10.111.40.139 --target-port=3007 --target-username=bike_config --target-tablename=yzb_t_city_config --table-compare=true


gdb pgquarrel
set args --source-dbname=bike_config --source-host=10.111.10.63 --source-port=3007 --source-username=bike_config --target-dbname=bike_config --target-host=10.111.40.139 --target-port=3007 --target-username=bike_config
b main


./pgquarrel --source-dbname=bike_config --source-host=10.111.10.63 --source-port=3007 --source-username=bike_config --source-tablename=t_scenic_area_rule --target-dbname=bike_config --target-host=10.111.40.139 --target-port=3007 --target-username=bike_config --target-tablename=t_scenic_area_rule --table-compare=true
./pgquarrel --source-dbname=bike_config --source-host=10.111.10.63 --source-port=3007 --source-username=bike_config --source-tablename=t_ride_card --target-dbname=bike_config --target-host=10.111.40.139 --target-port=3007 --target-username=bike_config --target-tablename=t_ride_card --table-compare=true
./pgquarrel --source-dbname=bike_config --source-host=10.111.10.63 --source-port=3007 --source-username=bike_config --source-tablename=t_bike_area_sms_push_template --target-dbname=bike_config --target-host=10.111.40.139 --target-port=3007 --target-username=bike_config --target-tablename=t_bike_area_sms_push_template --table-compare=true


t_scenic_area_rule
t_ride_card
t_bike_area_sms_push_template