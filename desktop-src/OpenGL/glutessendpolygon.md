---
title: funzione gluTessEndPolygon (Glu. h)
description: Le funzioni gluTessBeginPolygon e gluTessEndPolygon delimitano una descrizione del poligono. | funzione gluTessEndPolygon (Glu. h)
ms.assetid: c9ae2075-59d7-4c1a-b720-0aa05954525c
keywords:
- funzione gluTessEndPolygon OpenGL
topic_type:
- apiref
api_name:
- gluTessEndPolygon
api_location:
- Glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8353f9176e5bdb64dc0e3cd21bd42735e57b541b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321445"
---
# <a name="glutessendpolygon-function"></a>gluTessEndPolygon (funzione)

Le funzioni [**gluTessBeginPolygon**](glutessbeginpolygon.md) e **gluTessEndPolygon** delimitano una descrizione del poligono.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI gluTessEndPolygon(
   GLUtesselator *tess
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Tess* 
</dt> <dd>

Oggetto a mosaico creato con [**gluNewTess**](glunewtess.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

Le funzioni [**gluTessBeginPolygon**](glutessbeginpolygon.md) e **gluTessEndPolygon** delimitano la definizione di un poligono non convesso. All'interno di ogni coppia **gluTessBeginPolygon**  /  **gluTessEndPolygon** , includere una o più chiamate a [**gluTessBeginContour**](glutessbegincontour.md). All'interno di ogni contorno sono presenti zero o più chiamate a [**gluTessVertex**](glutessvertex.md). I vertici specificano un contorno chiuso (l'ultimo vertice di ogni contorno viene automaticamente collegato al primo).

Il parametro di *\_ dati Polygon* è un puntatore a una struttura di dati definita dal programmatore. Se vengono specificati i callback appropriati (vedere [*gluTessCallback*](glutess.md)), questo puntatore viene restituito alla funzione o alle funzioni di callback, rendendolo un modo pratico per archiviare le informazioni per poligono.

Quando si chiama **gluTessEndPolygon**, il poligono è tassellati e i triangoli risultanti vengono descritti tramite callback. Per le descrizioni delle funzioni di callback, vedere [*gluTessCallback*](glutess.md).

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
| Intestazione<br/>                   | <dl> <dt>Glu. h</dt> </dl>     |
| Libreria<br/>                  | <dl> <dt>Glu32. lib</dt> </dl> |
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

[**gluTessProperty**](glutessproperty.md)
</dt> <dt>

[**gluTessVertex**](glutessvertex.md)
</dt> </dl>

 

 





