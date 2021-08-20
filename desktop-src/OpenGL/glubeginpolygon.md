---
title: Funzione gluBeginPolygon (Glu.h)
description: Le funzioni gluBeginPolygon e gluEndPolygon delimitano una descrizione del poligono. | Funzione gluBeginPolygon (Glu.h)
ms.assetid: e4da731c-2082-4dbc-ae3a-8d6b30d50253
keywords:
- Funzione gluBeginPolygon OpenGL
topic_type:
- apiref
api_name:
- gluBeginPolygon
api_location:
- Glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98fe58a48a10d36a07e3a96bdfe612d8857f691233e19faac670eb6d987b42f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118937894"
---
# <a name="glubeginpolygon-function"></a>Funzione gluBeginPolygon

\[La **funzione gluBeginPolygon** è obsoleta e viene fornita solo per la compatibilità con le versioni precedenti. La **funzione gluBeginPolygon** viene mappata a [**gluTessBeginPolygon**](glutessbeginpolygon.md) seguita da [**gluTessBeginContour**](glutessbegincontour.md).\]

Le **funzioni gluBeginPolygon** [**e gluEndPolygon delimitano**](gluendpolygon.md) una descrizione del poligono.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI gluBeginPolygon(
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

Usare **gluBeginPolygon** e **gluEndPolygon** per delimitare la definizione di un poligono non convenzionale.

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

 

 





