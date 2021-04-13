---
title: funzione gluOrtho2D (Glu. h)
description: La funzione gluOrtho2D definisce una matrice di proiezione ortogonale 2D.
ms.assetid: ba83fb5c-e5c7-4486-a815-a1aff0469757
keywords:
- funzione gluOrtho2D OpenGL
topic_type:
- apiref
api_name:
- gluOrtho2D
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a36b321f312a074a5dd78340968f1c9b2b844c6c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400212"
---
# <a name="gluortho2d-function"></a>gluOrtho2D (funzione)

La funzione **gluOrtho2D** definisce una matrice di proiezione ortogonale 2D.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI gluOrtho2D(
   GLdouble left,
   GLdouble right,
   GLdouble top,
   GLdouble bottom
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*sinistra* 
</dt> <dd>

Coordinata per il piano di ritaglio verticale sinistro.

</dd> <dt>

*Ok* 
</dt> <dd>

Coordinata per il piano di ritaglio verticale destro.

</dd> <dt>

*top* 
</dt> <dd>

Coordinata per il piano di ritaglio orizzontale superiore.

</dd> <dt>

*parte inferiore* 
</dt> <dd>

Coordinata per il piano di ritaglio orizzontale inferiore.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

La funzione **gluOrtho2D** configura un'area di visualizzazione ortogonale bidimensionale. Equivale a chiamare [**glOrtho**](glortho.md) con near = 1 e lontano = 1.

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

[**glOrtho**](glortho.md)
</dt> <dt>

[**gluPerspective**](gluperspective.md)
</dt> </dl>

 

 





