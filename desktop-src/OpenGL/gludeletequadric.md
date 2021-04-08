---
title: funzione gluDeleteQuadric (Glu. h)
description: La funzione gluDeleteQuadric Elimina un oggetto quadrica.
ms.assetid: 09efd887-0fe8-4a56-bc6f-2177a4930035
keywords:
- funzione gluDeleteQuadric OpenGL
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
ms.openlocfilehash: 9b5ee85e943cd958e394efb191932393d228d948
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742231"
---
# <a name="gludeletequadric-function"></a>gluDeleteQuadric (funzione)

La funzione **gluDeleteQuadric** Elimina un oggetto quadrica.

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

Oggetto quadrica da eliminare definitivamente (creato con [**gluNewQuadric**](glunewquadric.md)).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

La funzione **gluDeleteQuadric** Elimina l'oggetto quadrica e libera la memoria usata. Dopo aver chiamato **gluDeleteQuadric**, non è possibile usare di nuovo *lo stato* .

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

[**gluNewQuadric**](glunewquadric.md)
</dt> </dl>

 

 





