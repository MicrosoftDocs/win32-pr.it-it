---
title: Funzione gluGetNurbsProperty (Glu.h)
description: La funzione gluGetNurbsProperty ottiene una proprietà B-Spline razionale non uniforme (NURBS).
ms.assetid: 7dbc75a0-d04e-4794-b3dd-a602addf9dfa
keywords:
- Funzione gluGetNurbsProperty OpenGL
topic_type:
- apiref
api_name:
- gluGetNurbsProperty
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a68e91fbdaafc2a1857a95e059125bf62347777edfbcc764868ceea0a8fce578
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119519591"
---
# <a name="glugetnurbsproperty-function"></a>Funzione gluGetNurbsProperty

La **funzione gluGetNurbsProperty** ottiene una proprietà B-Spline razionale non uniforme ([NURBS).](using-nurbs-curves-and-surfaces.md)

## <a name="syntax"></a>Sintassi


```C++
void WINAPI gluGetNurbsProperty(
   GLUnurbs *nobj,
   GLenum   property,
   GLfloat  *value
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*nobj* 
</dt> <dd>

Oggetto NURBS (creato con [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)).

</dd> <dt>

*property* 
</dt> <dd>

Proprietà il cui valore deve essere recuperato. I valori seguenti sono validi: GLU \_ SAMPLING \_ TOLERANCE, GLU \_ DISPLAY \_ MODE, GLU \_ CULLING, GLU \_ AUTO LOAD \_ \_ MATRIX, GLU \_ PARAMETRIC \_ TOLERANCE, GLU SAMPLING \_ \_ METHOD, GLU U STEP e \_ GLU V \_ \_ \_ STEP.

</dd> <dt>

*value* 
</dt> <dd>

Puntatore alla posizione in cui viene scritto il valore della proprietà denominata.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

Usare **gluGetNurbsProperty** per recuperare le proprietà archiviate in un oggetto NURBS. Queste proprietà influiscono sul modo in cui viene eseguito il rendering di curve e superfici NURBS. Per informazioni sulle proprietà NURBS, vedere [**gluNurbsProperty**](glunurbsproperty.md).

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

[**gluNewNurbsRenderer**](glunewnurbsrenderer.md)
</dt> <dt>

[**GluNurbsProperty**](glunurbsproperty.md)
</dt> </dl>

 

 





