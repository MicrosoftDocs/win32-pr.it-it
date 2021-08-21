---
title: Funzione gluEndCurve (Glu.h)
description: Le funzioni gluBeginCurve e gluEndCurve delimitano una definizione di curva B-Spline razionale non uniforme (NURBS). | Funzione gluEndCurve (Glu.h)
ms.assetid: b00ec687-6127-4585-b7b7-06e8dca78cfc
keywords:
- Funzione gluEndCurve OpenGL
topic_type:
- apiref
api_name:
- gluEndCurve
api_location:
- Glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20b6d8e9871b03286eebc285d2c3ad8834c8c354b196213c985626fc80cd02fc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119489521"
---
# <a name="gluendcurve-function"></a>Funzione gluEndCurve

Le [**funzioni gluBeginCurve**](glubegincurve.md) e **gluEndCurve** delimitano una definizione di curva B-Spline razionale non uniforme ([NURBS).](using-nurbs-curves-and-surfaces.md)

## <a name="syntax"></a>Sintassi


```C++
void WINAPI gluEndCurve(
   GLUnurbs *nobj
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*nobj* 
</dt> <dd>

Oggetto NURBS (creato con [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

Usare [**gluBeginCurve per**](glubegincurve.md) contrassegnare l'inizio di una definizione di curva NURBS. Dopo aver **chiamato gluBeginCurve,** effettuare una o più chiamate a [**gluNurbsCurve**](glunurbscurve.md) per definire gli attributi della curva. Esattamente una delle chiamate a **gluNurbsCurve** deve avere un tipo di curva GL \_ MAP1 \_ VERTEX \_ 3 o GL \_ MAP1 \_ VERTEX \_ 4. Per contrassegnare la fine della definizione della curva NURBS, chiamare **gluEndCurve**.

Gli analizzatori OpenGL vengono usati per eseguire il rendering della curva NURBS come una serie di segmenti di linea. Lo stato dell'analizzatore viene mantenuto durante il rendering con [**glPushAttrib**](glpushattrib.md) (GL \_ EVAL \_ BIT) e [**glPopAttrib**](glpopattrib.md). Per informazioni esattamente sullo stato che queste chiamate mantengono, vedere **glPushAttrib**.

## <a name="examples"></a>Esempio

Le funzioni seguenti eseguono il rendering di una curva NURBS con trama con normali. Le coordinate di trama e le normali vengono specificate anche come curve NURBS:

``` syntax
gluBeginCurve(nobj); 
gluNurbsCurve(nobj, . . ., GL_MAP1_TEXTURE_COORD_2); 
gluNurbsCurve(nobj, . . ., GL_MAP1_NORMAL); 
gluNurbsCurve(nobj, . . ., GL_MAP1_VERTEX_4);  
gluEndCurve(nobj);
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

[**glPushAttrib**](glpushattrib.md)
</dt> <dt>

[**gluBeginSurface**](glubeginsurface.md)
</dt> <dt>

[**gluBeginTrim**](glubegintrim.md)
</dt> <dt>

[**gluNewNurbsRenderer**](glunewnurbsrenderer.md)
</dt> <dt>

[**gluNurbsCurve**](glunurbscurve.md)
</dt> </dl>

 

 





