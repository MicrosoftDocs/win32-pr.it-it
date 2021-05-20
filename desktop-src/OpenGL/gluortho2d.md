---
title: Funzione gluOrtho2D (Glu.h)
description: La funzione gluOrtho2D definisce una matrice di proiezione ortogonale 2D.
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
ms.openlocfilehash: 1bf07fea583c5ae46680d888f6bf6c0a9c5aa9a0
ms.sourcegitcommit: 88049609e29f91a42442235885abf56f598b06b3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/19/2021
ms.locfileid: "110153554"
---
# <a name="gluortho2d-function"></a>Funzione gluOrtho2D

La **funzione gluOrtho2D** definisce una matrice di proiezione ortogonale 2D.

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

La **funzione gluOrtho2D** configura un'area di visualizzazione ortografica bidimensionale. Equivale a chiamare [**glOrtho con**](glortho.md) zNear = -1 e zFar = 1.

## <a name="requirements"></a>Requisiti



| Requisito | valore |
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

 

 





