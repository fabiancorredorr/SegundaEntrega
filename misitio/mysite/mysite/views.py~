#from django.template.loader import get_template
#from django.template import Context
#Para la funcion current_datetime no es necesaria la importacion de HttpResponse porque se utuiliza la funcion render, para las demas funciones si es necesario importarla
#from django.http import HttpResponse
from django.shortcuts import render
import datetime

def hello(request):
    return HttpResponse("Hello world")
    
def current_datetime(request):
    """
    now=datetime.datetime.now()
    html="<html><body>It is now %s.</body></html>" % now
    return HttpResponse(html)
    """
    """
    now=datetime.datetime.now()
    t=get_template('current_datetime.html')
    html= t.render(Context({'current_date': now}))
    return HttpResponse(html)
    """
    now=datetime.datetime.now()
    return render(request, 'current_datetime.html', {'current_date':now})
    

def hours_ahead(request, offset):
    try:
        offset=int(offset)
    except ValueError:
        raise Http404()
    dt= datetime.datetime.now() + datetime.timedelta(hours=offset)
    #assert False
    #html="<html><body> In %s hour(s), it will be %s. </body></html>" % (offset, dt)
    #return HttpResponse(html)
    return render(request, 'hours_ahead.html', {'hour_offset':offset, 'next_time':dt})
    
    
    
    
    
