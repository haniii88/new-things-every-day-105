/* New Things Every Day — Da 105 */
/* Filters completed tasks and displays a summary */

function dailyLog105() {
    const tasks = [
        { name: "Read documentation", completed: true },
        { name: "Write code", completed: true },
        { name: "Review project", completed: false },
        { name: "Commit changes", completed: true }
    ];

    const completedTasks = tasks.filter(task => task.completed);
    const completionRate = (
        (completedTasks.length / tasks.length) * 100
    ).toFixed(0);

    console.log({
        day: 105,
        timestamp: new Date().toISOString(),
        completed: completedTasks.length,
        total: tasks.length,
        completionRate: `${completionRate}%`,
        completedTasks: completedTasks.map(task => task.name)
    });
}

dailyLog105();
