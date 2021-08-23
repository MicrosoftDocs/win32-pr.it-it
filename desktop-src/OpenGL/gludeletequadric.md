---
title: Funzione gluDeleteQuadric (Glu.h)
description: La funzione gluDeleteQuadric elimina un oggetto quadric.
ms.assetid: 09efd887-0fe8-4a56-bc6f-2177a4930035
keywords:
- Funzione gluDeleteQuadric OpenGL
topic_type:
- apiref
api_name:
- gluDeleteQuadric
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad0c12bd77d3d8b7f7de641671916bb8a901d29d812dfa4e9af6ef116984a128
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119519621"
---
# <a name="gludeletequadric-function"></a>Funzione gluDeleteQuadric

La **funzione gluDeleteQuadric** elimina un oggetto quadric.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI gluDeleteQuadric(
   GLUquadricObj *state
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*state* 
</dt> <dd>

Oggetto quadric da eliminare (creato con [**gluNewQuadric).**](glunewquadric.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

La **funzione gluDeleteQuadric** elimina l'oggetto quadric e libera la memoria usata. Dopo aver chiamato **gluDeleteQuadric**, non è possibile usare *nuovamente lo* stato.

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

[**gluNewQuadric**](glunewquadric.md)
</dt> </dl>

 

 





