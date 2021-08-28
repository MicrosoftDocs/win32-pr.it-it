---
title: Funzione gluTessBeginPolygon (Glu.h)
description: Le funzioni gluTessBeginPolygon e gluTessEndPolygon delimitano una descrizione del poligono. | Funzione gluTessBeginPolygon (Glu.h)
ms.assetid: 3a04363a-c492-4fa5-b312-f2fa2a805782
keywords:
- Funzione gluTessBeginPolygon OpenGL
topic_type:
- apiref
api_name:
- gluTessBeginPolygon
api_location:
- Glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42566cf8a0674086883e6333a67ac2df03329f6a9bd3bb903ef558af3c430b9c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119777391"
---
# <a name="glutessbeginpolygon-function"></a>Funzione gluTessBeginPolygon

Le **funzioni gluTessBeginPolygon** e [**gluTessEndPolygon**](glutessendpolygon.md) delimitano una descrizione del poligono.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI gluTessBeginPolygon(
   GLUtesselator *tess,
   void          *polygon_data
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Tess* 
</dt> <dd>

Oggetto a tassellamento (creato con [**gluNewTess).**](glunewtess.md)

</dd> <dt>

*dati \_ poligono* 
</dt> <dd>

Puntatore a una struttura di dati poligono definita dal programmatore.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

Le **funzioni gluTessBeginPolygon** e [**gluTessEndPolygon**](glutessendpolygon.md) delimitano la definizione di un poligono non convenzionale. All'interno di ogni coppia **gluTessBeginPolygon**  /  **gluTessEndPolygon** includere una o più chiamate a [**gluTessBeginContour**](glutessbegincontour.md). All'interno di ogni contorno sono presenti zero o più chiamate a [**gluTessVertex.**](glutessvertex.md) I vertici specificano un contorno chiuso (l'ultimo vertice di ogni contorno viene collegato automaticamente al primo).

Il *parametro di dati \_ polygon* è un puntatore a una struttura di dati definita dal programmatore. Se vengono specificati i callback appropriati (vedere [*gluTessCallback),*](glutess.md)questo puntatore viene restituito alla funzione o alle funzioni di callback, rendendo così un modo pratico per archiviare le informazioni per poligono.

Quando si chiama [**gluTessEndPolygon,**](glutessendpolygon.md)il poligono viene a tessellato e i triangoli risultanti vengono descritti tramite callback. Per le descrizioni delle funzioni di callback, [*vedere gluTessCallback*](glutess.md).

## <a name="examples"></a>Esempio

Di seguito viene descritto un quadrilatero con un foro triangolare:

``` syntax
gluTessBeginPolygon(tobj, NULL); 
  gluTessBeginContour(tobj); 
    gluTessVertex(tobj, v1, v1); 
    gluTessVertex(tobj, v2, v2); 
    gluTessVertex(tobj, v3, v3); 
    gluTessVertex(tobj, v4, v4); 
  gluTessEndContour(tobj); 
  gluTessBeginContour(tobj); 
    gluTessVertex(tobj, v5, v5); 
    gluTessVertex(tobj, v6, v6); 
    gluTessVertex(tobj, v7, v7); 
  gluTessEndContour(tobj); 
gluTessEndPolygon(tobj);
```

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Glu.h</dt> </dl>     |
| Libreria<br/>                  | <dl> <dt>Glu32.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Glu32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**gluNewTess**](glunewtess.md)
</dt> <dt>

[**gluTessBeginContour**](glutessbegincontour.md)
</dt> <dt>

[*gluTessCallback*](glutess.md)
</dt> <dt>

[**gluTessEndContour**](glutessendcontour.md)
</dt> <dt>

[**gluTessNormal**](glutessnormal.md)
</dt> <dt>

[**GluTessProperty**](glutessproperty.md)
</dt> <dt>

[**gluTessVertex**](glutessvertex.md)
</dt> </dl>

 

 





