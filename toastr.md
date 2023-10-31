toastr.options = {
        "closeButton": true,
        "debug": false,
        "newestOnTop": false,
        "progressBar": true,
        "positionClass": "toast-top-right",
        "preventDuplicates": false,
        "onclick": null,
        "showDuration": "300",
        "hideDuration": "1000",
        "timeOut": "5000",
        "extendedTimeOut": "1000",
        "showEasing": "swing",
        "hideEasing": "linear",
        "showMethod": "fadeIn",
        "hideMethod": "fadeOut"
    }

  in Django 
{% if messages %}
    {% for message in messages %}
    {% if message.tags == 'error' %}
    <script>
        toastr.error('{{ message }}', 'Error', {
            closeButton: true,
            progressBar: true,
            positionClass: 'toast-top-right',
            timeOut: 5000
        });
    </script>
    {% elif message.tags == 'success' %}
    <script>
        toastr.success('{{ message }}', 'Success', {
            closeButton: true,
            progressBar: true,
            positionClass: 'toast-top-right',
            timeOut: 5000
        });
    </script>
    {% elif message.tags == 'warning' %}
    <script>
        toastr.warning('{{ message }}', 'Warning', {
            closeButton: true,
            progressBar: true,
            positionClass: 'toast-top-right',
            timeOut: 5000
        });
    </script>
    {% elif message.tags == 'info' %}
    <script>
        toastr.info('{{ message }}', 'Info', {
            closeButton: true,
            progressBar: true,
            positionClass: 'toast-top-right',
            timeOut: 5000
        });
    </script>
    {% endif %}
    {% endfor %}
    {% endif %}
