---
title: funzione glLogicOp (GL. h)
description: La funzione glLogicOp specifica un'operazione pixel logica per il rendering dell'indice dei colori.
ms.assetid: 29edf9bd-f3b8-4de7-9afb-07714f4efd92
keywords:
- funzione glLogicOp OpenGL
topic_type:
- apiref
api_name:
- glLogicOp
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb29e8f845e99f6d3c988dfd0c0201de129bee69
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519150"
---
# <a name="gllogicop-function"></a>glLogicOp (funzione)

La funzione **glLogicOp** specifica un'operazione pixel logica per il rendering dell'indice dei colori.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glLogicOp(
   GLenum opcode
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*codice operativo* 
</dt> <dd>

Costante simbolica che seleziona un'operazione logica. I simboli seguenti sono accettati, dove s è uguale al valore del bit di origine e d è il valore del bit di destinazione.



| Valore                                                                                                                                                                   | Significato              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------|
| <span id="GL_CLEAR"></span><span id="gl_clear"></span><dl> <dt>**\_cancellazione GL**</dt> </dl>                          | 0<br/>         |
| <span id="GL_SET"></span><span id="gl_set"></span><dl> <dt>**\_set GL**</dt> </dl>                                | 1<br/>         |
| <span id="GL_COPY"></span><span id="gl_copy"></span><dl> <dt>**\_copia GL**</dt> </dl>                             | s<br/>         |
| <span id="GL_COPY_INVERTED"></span><span id="gl_copy_inverted"></span><dl> <dt>**\_copia GL \_ invertita**</dt> </dl> | ! s<br/>        |
| <span id="GL_NOOP"></span><span id="gl_noop"></span><dl> <dt>**\_NoOp GL**</dt> </dl>                             | d<br/>         |
| <span id="GL_INVERT"></span><span id="gl_invert"></span><dl> <dt>**GL \_ invertiti**</dt> </dl>                       | ! d<br/>        |
| <span id="GL_AND"></span><span id="gl_and"></span><dl> <dt>**GL \_ e**</dt> </dl>                                | s & d<br/>     |
| <span id="GL_NAND"></span><span id="gl_nand"></span><dl> <dt>**\_NAND GL**</dt> </dl>                             | ! (s & d)<br/>  |
| <span id="GL_OR"></span><span id="gl_or"></span><dl> <dt>**GL \_ o**</dt> </dl>                                   | s \| d<br/>    |
| <span id="GL_NOR"></span><span id="gl_nor"></span><dl> <dt>**GL \_ e**</dt> </dl>                                | ! (s \| d)<br/> |
| <span id="GL_XOR"></span><span id="gl_xor"></span><dl> <dt>**\_Xor GL**</dt> </dl>                                | s ^ d<br/>     |
| <span id="GL_EQUIV"></span><span id="gl_equiv"></span><dl> <dt>**\_equiv GL**</dt> </dl>                          | ! (s ^ d)<br/>  |
| <span id="GL_AND_REVERSE"></span><span id="gl_and_reverse"></span><dl> <dt>**GL \_ e \_ Reverse**</dt> </dl>       | s &! d<br/>    |
| <span id="GL_AND_INVERTED"></span><span id="gl_and_inverted"></span><dl> <dt>**GL \_ e \_ invertiti**</dt> </dl>    | ! s & d<br/>    |
| <span id="GL_OR_REVERSE"></span><span id="gl_or_reverse"></span><dl> <dt>**GL \_ o \_ Reverse**</dt> </dl>          | s \| ! d<br/>   |
| <span id="GL_OR_INVERTED"></span><span id="gl_or_inverted"></span><dl> <dt>**GL \_ o \_ invertiti**</dt> </dl>       | ! s \| d<br/>   |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significato                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_enumerazione GL non valida \_**</dt> </dl>      | *OpCode* non è un valore accettato.<br/>                                                                                        |
| <dl> <dt>**\_operazione GL non valida \_**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Commenti

La funzione **glLogicOp** specifica un'operazione logica che, se abilitata, viene applicata tra l'indice dei colori in ingresso e l'indice dei colori nella posizione corrispondente nel framebuffer. L'operazione logica è abilitata o disabilitata con [**glEnable**](glenable.md) e **glDisable** usando la costante simbolica GL \_ logica \_ op.

Il parametro *OpCode* è una costante simbolica scelta nell'elenco seguente. Nella spiegazione delle operazioni logiche, *s* rappresenta l'indice dei colori in ingresso e *d* rappresenta l'indice nel framebuffer. Vengono utilizzati gli operatori di linguaggio C standard. Poiché gli operatori bit per bit suggeriscono, l'operazione logica viene applicata indipendentemente a ogni coppia di bit degli indici di origine e di destinazione.

Le operazioni di pixel logici non vengono applicate ai buffer dei colori RGBA.

Quando per il disegno è abilitato più di un buffer di indice dei colori, le operazioni logiche vengono eseguite separatamente per ogni buffer abilitato, usando il contenuto del buffer per l'indice di destinazione (vedere [**glDrawBuffer**](gldrawbuffer.md)).

Il parametro *OpCode* deve essere uno dei 16 valori accettati. Altri valori generano un errore.

Le funzioni seguenti consentono di recuperare informazioni correlate a **glLogicOp**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento \_ \_ modalità operativa logica \_

[**glIsEnabled**](glisenabled.md) con argomento GL \_ logica \_ op

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

[**glAlphaFunc**](glalphafunc.md)
</dt> <dt>

[**glBegin**](glbegin.md)
</dt> <dt>

[**glBlendFunc**](glblendfunc.md)
</dt> <dt>

[**glDrawBuffer**](gldrawbuffer.md)
</dt> <dt>

[**glEnable**](glenable.md)
</dt> <dt>

[**Remo**](glend.md)
</dt> <dt>

[**glIsEnabled**](glisenabled.md)
</dt> <dt>

[**glStencilOp**](glstencilop.md)
</dt> </dl>

 

 





