{% extends 'dashboard/base.html' %}

{% block content %}
<main class="flex-1 lg:ml-72 pt-16 lg:pt-0 p-4 md:p-7 transition-all mt-8">
    <div class="bg-white rounded-2xl border border-slate-200 shadow-sm overflow-hidden mb-6 md:mb-8">
        <div class="border-b border-slate-200 px-4 pt-4 pb-3 md:px-5 md:pt-5 md:pb-4">
            <h1 class="text-2xl font-bold text-slate-800">Редактирование фильма</h1>
        </div>
        <div class="p-4 md:p-5">
            <form method="post" enctype="multipart/form-data">
                {% csrf_token %}
                {{ form.as_p }}
                <div class="flex gap-3 mt-6">
                    <button type="submit" class="inline-flex items-center gap-2 bg-primary-600 hover:bg-primary-700 text-white px-4 py-2 rounded-lg transition shadow-sm text-sm font-medium">
                        <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 4v16m8-8H4"></path>
                        </svg>
                        Сохранить
                    </button>
                    <a href="{% url 'dashboard:movie_view_list' %}" class="inline-flex items-center gap-2 bg-slate-200 hover:bg-slate-300 text-slate-700 px-4 py-2 rounded-lg transition shadow-sm text-sm font-medium">
                        Отмена
                    </a>
                </div>
            </form>
        </div>
    </div>
</main>
{% endblock %}
movie_update

{% extends 'dashboard/base.html' %}

{% block content %}
<main class="flex-1 lg:ml-72 pt-16 lg:pt-0 p-4 md:p-7 transition-all mt-8">
    <div class="bg-white rounded-2xl border border-slate-200 shadow-sm overflow-hidden mb-6 md:mb-8">
        <div class="border-b border-slate-200 px-4 pt-4 pb-3 md:px-5 md:pt-5 md:pb-4">
            <h1 class="text-2xl font-bold text-slate-800">Редактирование жанра</h1>
        </div>
        <div class="p-4 md:p-5">
            <form method="post">
                {% csrf_token %}
                {{ form.as_p }}
                <div class="flex gap-3 mt-6">
                    <button type="submit" class="inline-flex items-center gap-2 bg-primary-600 hover:bg-primary-700 text-white px-4 py-2 rounded-lg transition shadow-sm text-sm font-medium">
                        <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 4v16m8-8H4"></path>
                        </svg>
                        Сохранить
                    </button>
                    <a href="{% url 'dashboard:genre_view_list' %}" class="inline-flex items-center gap-2 bg-slate-200 hover:bg-slate-300 text-slate-700 px-4 py-2 rounded-lg transition shadow-sm text-sm font-medium">
                        Отмена
                    </a>
                </div>
            </form>
        </div>
    </div>
</main>
{% endblock %}
genre_update


{% extends 'dashboard/base.html' %}

{% block content %}
<main class="flex-1 lg:ml-72 pt-16 lg:pt-0 p-4 md:p-7 transition-all mt-8">
    <div class="bg-white rounded-2xl border border-slate-200 shadow-sm overflow-hidden mb-6 md:mb-8">
        <div class="border-b border-slate-200 px-4 pt-4 pb-3 md:px-5 md:pt-5 md:pb-4">
            <h1 class="text-2xl font-bold text-slate-800">Удаление жанра</h1>
        </div>
        <div class="p-4 md:p-5">
            <p class="text-slate-700 mb-6">
                Вы уверены, что хотите удалить жанр <strong class="text-red-600">"{{ genre.name }}"</strong>?
            </p>
            <form method="POST">
                {% csrf_token %}
                <div class="flex gap-3">
                    <button type="submit" class="inline-flex items-center gap-2 bg-red-600 hover:bg-red-700 text-white px-4 py-2 rounded-lg transition shadow-sm text-sm font-medium">
                        <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 7l-.867 12.142A2 2 0 0116.138 21H7.862a2 2 0 01-1.995-1.858L5 7m5 4v6m4-6v6m1-10V4a1 1 0 00-1-1h-4a1 1 0 00-1 1v3M4 7h16"></path>
                        </svg>
                        Да, удалить
                    </button>
                    <a href="{% url 'dashboard:genre_view_list' %}" class="inline-flex items-center gap-2 bg-slate-200 hover:bg-slate-300 text-slate-700 px-4 py-2 rounded-lg transition shadow-sm text-sm font-medium">
                        Отмена
                    </a>
                </div>
            </form>
        </div>
    </div>
</main>
{% endblock %}
delete genre

{% extends 'dashboard/base.html' %}

{% block content %}
<main class="flex-1 lg:ml-72 pt-16 lg:pt-0 p-4 md:p-7 transition-all mt-8">
    <div class="bg-white rounded-2xl border border-slate-200 shadow-sm overflow-hidden mb-6 md:mb-8">
        <div class="border-b border-slate-200 px-4 pt-4 pb-3 md:px-5 md:pt-5 md:pb-4">
            <h1 class="text-2xl font-bold text-slate-800">Удаление фильма</h1>
        </div>
        <div class="p-4 md:p-5">
            <p class="text-slate-700 mb-6">
                Вы уверены, что хотите удалить фильм <strong class="text-red-600">"{{ movie.title }}"</strong>?
            </p>
            <form method="POST">
                {% csrf_token %}
                <div class="flex gap-3">
                    <button type="submit" class="inline-flex items-center gap-2 bg-red-600 hover:bg-red-700 text-white px-4 py-2 rounded-lg transition shadow-sm text-sm font-medium">
                        <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 7l-.867 12.142A2 2 0 0116.138 21H7.862a2 2 0 01-1.995-1.858L5 7m5 4v6m4-6v6m1-10V4a1 1 0 00-1-1h-4a1 1 0 00-1 1v3M4 7h16"></path>
                        </svg>
                        Да, удалить
                    </button>
                    <a href="{% url 'dashboard:movie_view_list' %}" class="inline-flex items-center gap-2 bg-slate-200 hover:bg-slate-300 text-slate-700 px-4 py-2 rounded-lg transition shadow-sm text-sm font-medium">
                        Отмена
                    </a>
                </div>
            </form>
        </div>
    </div>
</main>
{% endblock %}
delete movie
