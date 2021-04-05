---
title: funzione gluDeleteNurbsRenderer (Glu. h)
description: La funzione gluDeleteNurbsRenderer Elimina un oggetto di logica B-spline (NURBS) non uniforme.
ms.assetid: 77063dcb-90b8-47e4-8b00-e1c46cf4f712
keywords:
- funzione gluDeleteNurbsRenderer OpenGL
topic_type:
- apiref
api_name:
- gluDeleteNurbsRenderer
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3fb6ecf0bbb7076d4d6292676d3d358586d0986c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741418"
---
# <a name="gludeletenurbsrenderer-function"></a>gluDeleteNurbsRenderer (funzione)

La funzione **gluDeleteNurbsRenderer** Elimina un oggetto di logica B-spline ([NURBS](using-nurbs-curves-and-surfaces.md)) non uniforme.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI gluDeleteNurbsRenderer(
   GLUnurbs *nobj
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*juje* 
</dt> <dd>

Oggetto NURBS da eliminare definitivamente (creato con **gluNewNurbsRenderer**).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

La funzione **gluDeleteNurbsRenderer** Elimina l'oggetto NURBS e libera la memoria usata. Dopo aver chiamato **gluDeleteNurbsRenderer**, non è più possibile usare *juje* .

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

[**gluNewNurbsRenderer**](glunewnurbsrenderer.md)
</dt> </dl>

 

 





