---
title: Funzione glClearStencil (Gl.h)
description: La funzione glClearStencil specifica il valore non crittografato per il buffer di stencil.
ms.assetid: bbde8fa8-78f3-45bd-bac3-5d03839acc52
keywords:
- Funzione glClearStencil OpenGL
topic_type:
- apiref
api_name:
- glClearStencil
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4749a8d9c4844bd95181a7353bb0ce4559001fa47164fec3dbab5c188de8d994
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118618031"
---
# <a name="glclearstencil-function"></a>Funzione glClearStencil

La **funzione glClearStencil** specifica il valore non crittografato per il buffer di stencil.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glClearStencil(
   GLint s
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*s* 
</dt> <dd>

Indice utilizzato quando il buffer dello stencil viene cancellato. Il valore predefinito è zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

Il codice di errore seguente può essere recuperato dalla [**funzione glGetError.**](glgeterror.md)



| Nome                                                                                                  | Significato                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**OPERAZIONE GL \_ NON \_ VALIDA**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Commenti

La **funzione glClearStencil** specifica l'indice usato da [**glClear**](glclear.md) per cancellare il buffer degli stencil. Il *parametro s* viene mascherato con 2 <sup>m</sup>  - 1, dove *m* è il numero di bit nel buffer dello stencil.

Le funzioni seguenti recuperano informazioni correlate alla **funzione glClearStencil:**

[**glGet con**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) argomento GL \_ STENCIL CLEAR \_ \_ VALUE

**glGet con** argomento GL \_ STENCIL \_ BITS

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                              |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>Gl.h</dt> </dl>         |
| Libreria<br/>                  | <dl> <dt>Opengl32.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Opengl32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**glBegin**](glbegin.md)
</dt> <dt>

[**glClear**](glclear.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> </dl>

 

 





