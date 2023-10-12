# Template for Hugo+Reveal.js slides

Custom extension of `dzello/reveal-hugo.git` template, adding:
* Bootstrap
* Chart.js
* FontAwesome


### Download
```bash
git clone --recursive git@github.com:anitvam/slides-template-hugo-reveal.git
```

### Update
```bash
git pull --resurse-submodules
```

### Build
```bash
hugo
```

### Local serve
```
hugo server
```
and then available at `http://localhost:1313/slides-template-hugo-reveal/#/`.

---

### Configure a chart from chart.js
```
{{< chart >}}
{
    type: 'bar',
    data: {
        labels: ['Red', 'Blue', 'Yellow', 'Green', 'Purple', 'Orange'],
        datasets: [{
            label: 'Bar Chart',
            data: [12, 19, 18, 16, 13, 14],
            backgroundColor: [
                'rgba(255, 99, 132, 0.2)',
                'rgba(54, 162, 235, 0.2)',
                'rgba(255, 206, 86, 0.2)',
                'rgba(75, 192, 192, 0.2)',
                'rgba(153, 102, 255, 0.2)',
                'rgba(255, 159, 64, 0.2)'
            ],
            borderColor: [
                'rgba(255, 99, 132, 1)',
                'rgba(54, 162, 235, 1)',
                'rgba(255, 206, 86, 1)',
                'rgba(75, 192, 192, 1)',
                'rgba(153, 102, 255, 1)',
                'rgba(255, 159, 64, 1)'
            ],
            borderWidth: 1
        }]
    },
    options: {
        maintainAspectRatio: false,
        scales: {
            yAxes: [{
                ticks: {
                    beginAtZero: true
                }
            }]
        }
    }
}
{{< /chart >}}
```

---

### Use a multi-columns layout
```
{{< multicol >}}{{< col >}}
Left column     
{{< /col >}}{{< col >}}
Right column
{{< /col >}}{{< /multicol >}}
```
