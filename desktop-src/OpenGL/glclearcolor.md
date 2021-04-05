---
title: funzione glClearColor (GL. h)
description: La funzione glClearColor specifica i valori Clear per i buffer dei colori.
ms.assetid: f938e3f4-9db3-4c24-97ae-531b6799224e
keywords:
- funzione glClearColor OpenGL
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
ms.openlocfilehash: 34005ce34900f5fee8a4c9b2f1b963b7fe4bb6d0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741938"
---
# <a name="glclearcolor-function"></a>glClearColor (funzione)

La funzione **glClearColor** specifica i valori Clear per i buffer dei colori.

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

*Red* 
</dt> <dd>

Valore rosso utilizzato da [**glClear**](glclear.md) per cancellare i buffer dei colori. Il valore predefinito è zero.

</dd> <dt>

*verde* 
</dt> <dd>

Valore verde utilizzato da [**glClear**](glclear.md) per cancellare i buffer dei colori. Il valore predefinito è zero.

</dd> <dt>

*blu* 
</dt> <dd>

Valore blu usato da [**glClear**](glclear.md) per cancellare i buffer dei colori. Il valore predefinito è zero.

</dd> <dt>

*Alfa* 
</dt> <dd>

Valore alfa usato da [**glClear**](glclear.md) per cancellare i buffer dei colori. Il valore predefinito è zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significato                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_operazione GL non valida \_**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Commenti

La funzione **glClearColor** specifica i valori rosso, verde, blu e alfa usati da [**glClear**](glclear.md) per cancellare i buffer dei colori. I valori specificati da **glClearColor** vengono bloccati nell'intervallo compreso tra \[ 0 e 1 \] .

Le funzioni seguenti consentono di recuperare informazioni correlate alla funzione **glClearColor** :

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con l'argomento contabilità GL \_ \_ Clear \_ value

**glGet** con valore di \_ cancellazione del colore GL argomento \_ \_

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

[**glClear**](glclear.md)
</dt> <dt>

[**Remo**](glend.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> </dl>

 

 





