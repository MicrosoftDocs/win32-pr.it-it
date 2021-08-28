---
title: Funzione glClearColor (Gl.h)
description: La funzione glClearColor specifica valori non crittografati per i buffer di colore.
ms.assetid: f938e3f4-9db3-4c24-97ae-531b6799224e
keywords:
- Funzione glClearColor OpenGL
topic_type:
- apiref
api_name:
- glClearColor
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1bd68590ab9221dd094265a54f3c69ca396f810fb1f716c194b627a675196edd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119061919"
---
# <a name="glclearcolor-function"></a>Funzione glClearColor

La **funzione glClearColor** specifica valori non crittografati per i buffer di colore.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glClearColor(
   GLclampf red,
   GLclampf green,
   GLclampf blue,
   GLclampf alpha
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Rosso* 
</dt> <dd>

Valore rosso utilizzato [**da glClear**](glclear.md) per cancellare i buffer di colore. Il valore predefinito è zero.

</dd> <dt>

*Verde* 
</dt> <dd>

Valore verde utilizzato [**da glClear**](glclear.md) per cancellare i buffer di colore. Il valore predefinito è zero.

</dd> <dt>

*Blu* 
</dt> <dd>

Valore blu utilizzato [**da glClear**](glclear.md) per cancellare i buffer di colore. Il valore predefinito è zero.

</dd> <dt>

*Alfa* 
</dt> <dd>

Valore alfa utilizzato [**da glClear**](glclear.md) per cancellare i buffer di colore. Il valore predefinito è zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

I codici di errore seguenti possono essere recuperati dalla [**funzione glGetError.**](glgeterror.md)



| Nome                                                                                                  | Significato                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**OPERAZIONE GL \_ NON \_ VALIDA**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Commenti

La **funzione glClearColor** specifica i valori rosso, verde, blu e alfa usati da [**glClear**](glclear.md) per cancellare i buffer dei colori. I valori specificati **da glClearColor** sono ancorati all'intervallo \[ 0,1. \]

Le funzioni seguenti recuperano informazioni correlate alla **funzione glClearColor:**

[**glGet con**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) argomento GL \_ ACCUM \_ CLEAR \_ VALUE

**glGet con** argomento GL \_ COLOR CLEAR \_ \_ VALUE

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

 

 





