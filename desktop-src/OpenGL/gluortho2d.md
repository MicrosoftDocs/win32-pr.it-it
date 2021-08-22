---
title: Funzione gluOrtho2D (Glu.h)
description: La funzione gluOrtho2D definisce una matrice di proiezione ortografica 2D.
ms.assetid: ba83fb5c-e5c7-4486-a815-a1aff0469757
keywords:
- Funzione gluOrtho2D OpenGL
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
ms.openlocfilehash: b4a2f0d5fad1a2efb0df0c802dbb2cf51b54ff3e43402c3143bad982009f4f95
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119488861"
---
# <a name="gluortho2d-function"></a>Funzione gluOrtho2D

La **funzione gluOrtho2D** definisce una matrice di proiezione ortografica 2D.

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

*Sinistra* 
</dt> <dd>

Coordinata per il piano di ritaglio verticale sinistro.

</dd> <dt>

*va bene* 
</dt> <dd>

Coordinata per il piano di ritaglio verticale destro.

</dd> <dt>

*top* 
</dt> <dd>

Coordinata per il piano di ritaglio orizzontale superiore.

</dd> <dt>

*Fondoschiena* 
</dt> <dd>

Coordinata per il piano di ritaglio orizzontale inferiore.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

La **funzione gluOrtho2D** configura un'area di visualizzazione ortografica bidimensionale. Equivale a chiamare [**glOrtho**](glortho.md) con zNear = -1 e zFar = 1.

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

[**glOrtho**](glortho.md)
</dt> <dt>

[**gluPerspective**](gluperspective.md)
</dt> </dl>

 

 





