---
title: funzione glGetClipPlane (GL. h)
description: La funzione glGetClipPlane restituisce i coefficienti del piano di ritaglio specificato.
ms.assetid: 8ff5ee0a-95c1-4321-8aa8-3d9d144d1ef6
keywords:
- funzione glGetClipPlane OpenGL
topic_type:
- apiref
api_name:
- glGetClipPlane
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b3e29d730c09bcc7c2b12082116e174cb39eb74
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302762"
---
# <a name="glgetclipplane-function"></a>glGetClipPlane (funzione)

La funzione **glGetClipPlane** restituisce i coefficienti del piano di ritaglio specificato.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glGetClipPlane(
   GLenum   plane,
   GLdouble *equation
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*aereo* 
</dt> <dd>

Un piano di ritaglio. Il numero di piani di ritaglio dipende dall'implementazione, ma sono supportati almeno sei piani di ritaglio. Sono identificati da nomi simbolici del formato GL \_ clip \_ plane *i* dove 0 = *i* < i \_ \_ piani di ritaglio GL Max \_ .

</dd> <dt>

*equazione* 
</dt> <dd>

Restituisce quattro valori a precisione doppia che corrispondono ai coefficienti *dell'equazione del piano delle coordinate* oculari.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significato                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_enumerazione GL non valida \_**</dt> </dl>      | il *piano* non è un valore accettato.<br/>                                                                                         |
| <dl> <dt>**\_operazione GL non valida \_**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Commenti

La funzione **glGetClipPlane** restituisce in *equazione* i quattro coefficienti dell'equazione del piano per il *piano*.

È sempre il caso GL \_ clip \_ plane *i* = GL \_ clip \_ PLANE0 + *i*.

Se viene generato un errore, non viene apportata alcuna modifica al contenuto dell' *equazione*.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                              |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>GL. h</dt> </dl>         |
| Libreria<br/>                  | <dl> <dt>Opengl32. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Opengl32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**glBegin**](glbegin.md)
</dt> <dt>

[**glClipPlane**](glclipplane.md)
</dt> <dt>

[**Remo**](glend.md)
</dt> </dl>

 

 





