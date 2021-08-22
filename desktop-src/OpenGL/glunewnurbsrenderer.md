---
title: Funzione gluNewNurbsRenderer (Glu.h)
description: La funzione gluNewNurbsRenderer crea un oggetto B-Spline razionale non uniforme (NURBS).
ms.assetid: f47badb0-6b75-4bfd-9771-516668d9e255
keywords:
- Funzione gluNewNurbsRenderer OpenGL
topic_type:
- apiref
api_name:
- gluNewNurbsRenderer
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 089c1a88ac0fe9ac246efd435ae941ba5e66e2412595e4f5f96dc73e85e90478
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118937796"
---
# <a name="glunewnurbsrenderer-function"></a>Funzione gluNewNurbsRenderer

La **funzione gluNewNurbsRenderer** crea un oggetto B-Spline razionale non uniforme ([NURBS).](using-nurbs-curves-and-surfaces.md)

## <a name="syntax"></a>Sintassi


```C++
GLUnurbs* WINAPI gluNewNurbsRenderer(void);
```



## <a name="parameters"></a>Parametri

Questa funzione non ha parametri.

## <a name="remarks"></a>Commenti

La **funzione gluNewNurbsRenderer** crea e restituisce un puntatore a un nuovo oggetto NURBS. Fare riferimento a questo oggetto quando si chiamano le funzioni di rendering e controllo NURBS. Un valore restituito pari a zero indica che la memoria da allocare all'oggetto non è sufficiente.

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

[**gluBeginCurve**](glubegincurve.md)
</dt> <dt>

[**gluBeginSurface**](glubeginsurface.md)
</dt> <dt>

[**gluBeginTrim**](glubegintrim.md)
</dt> <dt>

[**gluDeleteNurbsRenderer**](gludeletenurbsrenderer.md)
</dt> <dt>

[*gluNurbsCallback*](glunurbs.md)
</dt> <dt>

[**GluNurbsProperty**](glunurbsproperty.md)
</dt> </dl>

 

 





