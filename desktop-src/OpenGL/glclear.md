---
title: funzione glClear (GL. h)
description: La funzione glClear Cancella i buffer sui valori predefiniti.
ms.assetid: 9818f969-3145-45ea-aa9c-2abed953a8e0
keywords:
- funzione glClear OpenGL
topic_type:
- apiref
api_name:
- glClear
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0db935e46c65c42976024a8afbb98028294710c7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301800"
---
# <a name="glclear-function"></a>glClear (funzione)

La funzione **glClear** Cancella i buffer sui valori predefiniti.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glClear(
   GLbitfield mask
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*maschera* 
</dt> <dd>

Operatori OR bit per bit delle maschere che indicano i buffer da cancellare. Le quattro maschere sono le seguenti:



| Valore                                                                                                                                                                                   | Significato                                                     |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <span id="GL_COLOR_BUFFER_BIT"></span><span id="gl_color_buffer_bit"></span><dl> <dt>**\_bit del \_ buffer dei colori GL \_**</dt> </dl>       | Buffer attualmente abilitati per la scrittura di colori.<br/> |
| <span id="GL_DEPTH_BUFFER_BIT"></span><span id="gl_depth_buffer_bit"></span><dl> <dt>**\_ \_ bit buffer di profondità GL \_**</dt> </dl>       | Buffer di profondità.<br/>                                |
| <span id="GL_ACCUM_BUFFER_BIT"></span><span id="gl_accum_buffer_bit"></span><dl> <dt>**\_bit del buffer di accut GL \_ \_**</dt> </dl>       | Buffer di accumulo.<br/>                         |
| <span id="GL_STENCIL_BUFFER_BIT"></span><span id="gl_stencil_buffer_bit"></span><dl> <dt>**\_ \_ bit buffer dello stencil GL \_**</dt> </dl> | Buffer dello stencil.<br/>                              |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significato                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_valore GL non valido \_**</dt> </dl>     | Un bit diverso dai quattro bit definiti è stato impostato nella *maschera*.<br/>                                                                |
| <dl> <dt>**\_operazione GL non valida \_**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Commenti

La funzione **glClear** imposta l'area bitplane della finestra sui valori selezionati in precedenza da [**glClearColor**](glclearcolor.md), [**glClearIndex**](glclearindex.md), [**glClearDepth**](glcleardepth.md), [**glClearStencil**](glclearstencil.md)e [**glClearAccum**](glclearaccum.md). È possibile cancellare contemporaneamente più buffer di colori selezionando più di un buffer alla volta usando [**glDrawBuffer**](gldrawbuffer.md).

Il test di proprietà dei pixel, il test a forbice, il dithering e il buffer writemasks influiscono sul funzionamento di **glClear**. La casella a forbice delimita l'area deselezionata. La funzione **glClear** ignora la funzione Alpha, la funzione Blend, l'operazione logica, lo stencil, il mapping della trama e il buffer *z*.

La funzione **glClear** accetta un solo argomento (*maschera*) che rappresenta l'operatore OR bit per bit di diversi valori che indicano il buffer da cancellare.

Il valore a cui viene cancellato ogni buffer dipende dall'impostazione del valore Clear per il buffer.

Se non è presente un buffer, una chiamata **glClear** indirizzata a tale buffer non ha alcun effetto.

Le funzioni seguenti consentono di recuperare informazioni correlate a **glClear**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con l'argomento contabilità GL \_ \_ Clear \_ value

**glGet** con \_ \_ valore Clear Depth Depth \_

**glGet** con valore di \_ cancellazione dell'indice GL dell'argomento \_ \_

**glGet** con valore di \_ cancellazione del colore GL argomento \_ \_

**glGet** con il \_ \_ valore Clear dello stencil GL degli argomenti \_

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

[**glClearAccum**](glclearaccum.md)
</dt> <dt>

[**glClearColor**](glclearcolor.md)
</dt> <dt>

[**glClearDepth**](glcleardepth.md)
</dt> <dt>

[**glClearIndex**](glclearindex.md)
</dt> <dt>

[**glClearStencil**](glclearstencil.md)
</dt> <dt>

[**glDrawBuffer**](gldrawbuffer.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glScissor**](glscissor.md)
</dt> </dl>

 

 





