---
title: test with siteleaf
date: 2018-02-04 09:06:00 Z
---

### testing with siteleaf

{% highlight ruby %}
def show
@widget = Widget(params\[:id\])
respond_to do |format|
format.html # show.html.erb
format.json { render json: @widget }
end
end
{% endhighlight %}