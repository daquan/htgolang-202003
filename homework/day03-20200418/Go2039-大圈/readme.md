1. 知识整理
2. "我有一个梦想" 中出现次数最多的top 10 字符及出现
3. 统计
    a.每个IP出现次数
    b.每个状态码出现次数
    c.每个IP在每个URL上产生的流量 IP, URL key
    d. a, b, c top 10
    int[][4]string {
        // ip   url  状态码  字节大小(B)
        {"1.1.1.1", "/index.html", "200", "1000"},
        {"1.1.1.2", "/index.html", "200", "10000"},
        {"1.1.1.1", "/index.html", "200", "10000"},
    }

    key: map 必须是可以使用==进行比较的数据类型
    key 数据类型, ip+url => string key
                 []string{ip, url}
                 [2]string{ip, url}

4. todo管理
    a. 编辑
        请输入编辑的ID:
        通过ID查找 => Task => 显示
        用户确认是否进行编辑(y/yes): 编辑
        用户输入: 任务名称, 开始时间，状态
        // 状态如果是已完成, 初始化完成时间
        // time.Now().Format("2006-01-02 15:04:05")

    b. 删除
        请输入编辑的ID:
        通过ID查找 => Task => 显示
        用户确认是否进行删除(y/yes): 删除

    c. 数据验证（用户输入数据检查）
        任务名称: 不能重复 (新增，编辑)
        编辑：
            a. 任务名称不变
            b. 任务名称改成其他已存在的
        任务状态:
            新创建, 开始执行, 已完成, 暂停

            xxx