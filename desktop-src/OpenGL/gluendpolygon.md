---
title: Funzione gluEndPolygon (Glu.h)
description: Le funzioni gluBeginPolygon e gluEndPolygon delimitano una descrizione del poligono. | Funzione gluEndPolygon (Glu.h)
ms.assetid: fdb8cc73-c6c3-4377-aa5b-36a79791e7a9
keywords:
- Funzione gluEndPolygon OpenGL
topic_type:
- apiref
api_name:
- gluEndPolygon
api_location:
- Glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b12d3565938dbc963a720333bbbba23a42d0d2e775297af4de3c2f2c1362760e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119675391"
---
# <a name="gluendpolygon-function"></a>Funzione gluEndPolygon

\[La **funzione gluEndPolygon** è obsoleta e viene fornita solo per la compatibilità con le versioni precedenti. La **funzione gluEndPolygon** viene mappata a **gluTessEndPolygon** seguita da **gluTessEndContour**.\]

Le [**funzioni gluBeginPolygon**](glubeginpolygon.md) **e gluEndPolygon delimitano** una descrizione del poligono.

## <a name="syntax"></a>Sintassi


```C++
void gluEndPolygon(
   GLUtesselator *tess
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Tess* 
</dt> <dd>

Oggetto a tassellamento (creato con [**gluNewTess).**](glunewtess.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

Usare [**gluBeginPolygon**](glubeginpolygon.md) e **gluEndPolygon** per delimitare la definizione di un poligono non convenzionale.

1.  Chiamare **gluBeginPolygon**.
2.  Definire i contorni del poligono chiamando [**gluTessVertex**](glutessvertex.md) per ogni vertice e [**gluNextContour**](glunextcontour.md) per avviare ogni nuovo contorno.
3.  Chiamare **gluEndPolygon** per segnalare la fine della definizione.

    Dopo **aver chiamato gluEndPolygon,** il poligono viene a tessellato e i triangoli risultanti vengono descritti tramite callback. Per le descrizioni delle funzioni di callback, [*vedere gluTessCallback*](glutess.md).

## <a name="examples"></a>Esempio

L'esempio seguente descrive un quadrilatero con un foro triangolare:

``` syntax
gluBeginPolygon(tess); 
    gluTessVertex(tess, v1, v1); 
    gluTessVertex(tess, v2, v2); 
    gluTessVertex(tess, v3, v3); 
    gluTessVertex(tess, v4, v4); 
gluNextContour(tess, GLU_INTERIOR); 
    gluTessVertex(tess, v5, v5); 
    gluTessVertex(tess, v6, v6); 
    gluTessVertex(tess, v7, v7); 
gluEndPolygon(tess);
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

[**gluNextContour**](glunextcontour.md)
</dt> <dt>

[**gluTessBeginContour**](glutessbegincontour.md)
</dt> <dt>

[**gluTessBeginPolygon**](glutessbeginpolygon.md)
</dt> <dt>

[*gluTessCallback*](glutess.md)
</dt> <dt>

[**gluTessVertex**](glutessvertex.md)
</dt> </dl>

 

 





