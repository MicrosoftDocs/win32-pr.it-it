---
title: Funzione glClear (Gl.h)
description: La funzione glClear cancella i buffer in base ai valori preimpostati.
ms.assetid: 9818f969-3145-45ea-aa9c-2abed953a8e0
keywords:
- Funzione glClear OpenGL
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
ms.openlocfilehash: 0bb48a1b2832a5f9c046bb450b7cfba9ec4f83a759b093df91f3ec2064f23a3d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082101"
---
# <a name="glclear-function"></a>Funzione glClear

La **funzione glClear** cancella i buffer in base ai valori preimpostati.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glClear(
   GLbitfield mask
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Maschera* 
</dt> <dd>

Operatori OR bit per bit delle maschere che indicano i buffer da cancellare. Le quattro maschere sono le seguenti.



| Valore                                                                                                                                                                                   | Significato                                                     |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <span id="GL_COLOR_BUFFER_BIT"></span><span id="gl_color_buffer_bit"></span><dl> <dt>**BIT BUFFER COLORE GL \_ \_ \_**</dt> </dl>       | Buffer attualmente abilitati per la scrittura dei colori.<br/> |
| <span id="GL_DEPTH_BUFFER_BIT"></span><span id="gl_depth_buffer_bit"></span><dl> <dt>**BIT \_ BUFFER \_ DI PROFONDITÀ GL \_**</dt> </dl>       | Buffer di profondità.<br/>                                |
| <span id="GL_ACCUM_BUFFER_BIT"></span><span id="gl_accum_buffer_bit"></span><dl> <dt>**GL \_ ACCUM \_ BUFFER \_ BIT**</dt> </dl>       | Buffer di accumulo.<br/>                         |
| <span id="GL_STENCIL_BUFFER_BIT"></span><span id="gl_stencil_buffer_bit"></span><dl> <dt>**GL \_ STENCIL \_ BUFFER \_ BIT**</dt> </dl> | Buffer degli stencil.<br/>                              |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

I codici di errore seguenti possono essere recuperati dalla [**funzione glGetError.**](glgeterror.md)



| Nome                                                                                                  | Significato                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**VALORE GL \_ NON \_ VALIDO**</dt> </dl>     | Qualsiasi bit diverso da quattro bit definiti è stato impostato nella *maschera*.<br/>                                                                |
| <dl> <dt>**OPERAZIONE GL \_ NON \_ VALIDA**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Commenti

La **funzione glClear** imposta l'area di bitplane della finestra su valori selezionati in precedenza da [**glClearColor**](glclearcolor.md), [**glClearIndex**](glclearindex.md), [**glClearDepth**](glcleardepth.md), [**glClearStencil**](glclearstencil.md)e [**glClearAccum**](glclearaccum.md). È possibile cancellare più buffer di colore contemporaneamente selezionando più buffer alla volta usando [**glDrawBuffer.**](gldrawbuffer.md)

Il test di proprietà del pixel, il test di scissor, il dithering e le maschera di scrittura del buffer influiscono sul funzionamento di **glClear.** La casella di forbice delimita l'area cancellata. La **funzione glClear** ignora la funzione alfa, la funzione blend, l'operazione logica, lo stencil, il mapping della trama e *il buffering z.*

La **funzione glClear** accetta un singolo argomento (*mask*) che è l'OR bit per bit di diversi valori che indica quale buffer deve essere cancellato.

Il valore in base al quale viene cancellato ogni buffer dipende dall'impostazione del valore non crittografato per tale buffer.

Se non è presente un buffer, una **chiamata glClear** indirizzata a tale buffer non ha alcun effetto.

Le funzioni seguenti recuperano informazioni correlate **a glClear:**

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento GL \_ ACCUM \_ CLEAR \_ VALUE

**glGet** con argomento GL \_ DEPTH \_ CLEAR \_ VALUE

**glGet** con argomento GL \_ INDEX \_ CLEAR \_ VALUE

**glGet con** argomento GL \_ COLOR CLEAR \_ \_ VALUE

**glGet** con argomento GL \_ STENCIL \_ CLEAR \_ VALUE

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

 

 





