---
title: funzione glClearIndex (GL. h)
description: La funzione glClearIndex specifica il valore Clear per i buffer di indice dei colori.
ms.assetid: 87983d93-c5a1-445f-8621-1c2952d93a0f
keywords:
- funzione glClearIndex OpenGL
topic_type:
- apiref
api_name:
- glClearIndex
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85b1ed90b017828e13d387e1e6db440c1d781cb5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477242"
---
# <a name="glclearindex-function"></a>glClearIndex (funzione)

La funzione **glClearIndex** specifica il valore Clear per i buffer di indice dei colori.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glClearIndex(
   GLfloat c
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*c* 
</dt> <dd>

Indice utilizzato quando i buffer dell'indice dei colori vengono cancellati. Il valore predefinito è zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significato                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_operazione GL non valida \_**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Commenti

La funzione **glClearIndex** specifica l'indice usato da [**glClear**](glclear.md) per cancellare i buffer dell'indice dei colori. Il parametro *c* non è stato bloccato. Il linguaggio *c* viene invece convertito in un valore a virgola fissa con una precisione non specificata a destra del punto binario. La parte intera di questo valore viene quindi mascherata con 2 <sup>m</sup>  -1, dove *m* è il numero di bit in un indice dei colori archiviato nel framebuffer.

Le funzioni seguenti consentono di recuperare informazioni correlate a **glClearIndex**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con valore di \_ cancellazione dell'indice GL dell'argomento \_ \_

**glGet** con bit di indice GL dell'argomento \_ \_

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

 

 





