### Example 0
[permalink](#example-0)

{% highlight clojure %}
{% raw %}
;; Prevent namespace conflicts like:

;; `WARNING: time already refers to: #'clojure.core/time in namespace:
;; time, being replaced by: #'time/time`

user=> (ns time
         (:refer-clojure :exclude [time]))

(defn time []
  (System/nanoTime))
{% endraw %}
{% endhighlight %}


