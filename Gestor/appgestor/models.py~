from django.db import models

class Proyecto(models.Model):
    nombre_proyecto = models.CharField(max_length=200)
    tiempo_Inicio = models.DateTimeField('Inicio Proyecto')
    tiempo_fin = models.DateTimeField('Fin Proyecto')
    def __str__(self):  
        return self.nombre_proyecto
        
class Tarea(models.Model):
    nombre_tarea = models.CharField(max_length=200)
    tiempo_Inicio = models.DateTimeField('Inicio Tarea')
    tiempo_fin = models.DateTimeField('Fin Tarea')
    proyecto = models.ForeignKey(Proyecto)
    def __str__(self):  
        return self.nombre_tarea


