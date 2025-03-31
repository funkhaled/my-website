<!DOCTYPE html>
<html lang="ar">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>الدعم النفسي - صفحتي الشخصية</title>
    <style>
        body {
            font-family: "Tajawal", Arial, sans-serif;
            direction: rtl;
            text-align: right;
            margin: 0;
            padding: 0;
            background-color: #eef2f3;
            color: #333;
        }

        header {
            background: #87CBB9;
            color: white;
            padding: 20px;
            text-align: center;
            font-size: 24px;
            font-weight: bold;
        }

        .container {
            width: 90%;
            max-width: 800px;
            margin: 20px auto;
            overflow: hidden;
        }

        .section {
            background: white;
            padding: 20px;
            margin: 15px 0;
            border-radius: 8px;
            box-shadow: 0px 2px 10px rgba(0, 0, 0, 0.1);
        }

        h2 {
            color: #005f73;
        }

        a {
            color: #008CBA;
            text-decoration: none;
        }

        a:hover {
            text-decoration: underline;
        }

        ul {
            padding-right: 20px;
        }

        footer {
            background: #87CBB9;
            color: white;
            text-align: center;
            padding: 15px;
            margin-top: 20px;
            font-size: 14px;
        }
    </style>
    <script>
        async function loadArticles() {
            try {
                const response = await fetch("articles.json");
                const articles = await response.json();
                const articlesContainer = document.getElementById("articles");

                articlesContainer.innerHTML = ""; 

                articles.forEach(article => {
                    const articleDiv = document.createElement("div");
                    articleDiv.innerHTML = `
                        <h3>${article.title}</h3>
                        <p>${article.summary} <a href="${article.link}" target="_blank">اقرأ المزيد</a></p>
                    `;
                    articlesContainer.appendChild(articleDiv);
                });
            } catch (error) {
                console.error("حدث خطأ أثناء تحميل المقالات:", error);
            }
        }

        window.onload = loadArticles;
    </script>
</head>
<body>

<header>
    الدعم النفسي - صفحتي الشخصية
</header>

<div class="container">
    <div class="section">
        <h2>من نحن؟</h2>
        <p>مرحبًا بك في صفحتي الشخصية، حيث أقدم مقالات ونصائح حول الدعم النفسي من مصادر موثوقة لمساعدتك على تحقيق التوازن النفسي والتغلب على التحديات.</p>
    </div>

    <div class="section">
        <h2>أحدث المقالات</h2>
        <div id="articles">
            <p>جاري تحميل المقالات...</p>
        </div>
    </div>

    <div class="section">
        <h2>نصائح نفسية سريعة</h2>
        <ul>
            <li>مارس التأمل لمدة 5 دقائق يوميًا.</li>
            <li>تحدث مع شخص تثق به عند الشعور بالضغط.</li>
            <li>احصل على قسط كافٍ من النوم يوميًا.</li>
            <li>خصص وقتًا لممارسة هواياتك المفضلة.</li>
        </ul>
    </div>
</div>

<footer>
    © 2025 صفحتي الشخصية - جميع الحقوق محفوظة
</footer>

</body>
</html> 
[
    {
        "title": "كيف تتعامل مع القلق والتوتر؟",
        "summary": "تعرف على طرق مثبتة علميًا لتقليل القلق وتحسين صحتك النفسية.",
        "link": "https://example.com/article1"
    },
    {
        "title": "أهمية النوم للصحة النفسية",
        "summary": "النوم الجيد ضروري للحفاظ على توازن نفسي وعاطفي. اكتشف كيف يمكنك تحسين نومك.",
        "link": "https://example.com/article2"
    },
    {
        "title": "تقنيات الاسترخاء لعلاج التوتر",
        "summary": "تعلم تقنيات الاسترخاء التي تساعد على تهدئة الأعصاب وتقليل الضغط النفسي.",
        "link": "https://example.com/article3"
    }
]
