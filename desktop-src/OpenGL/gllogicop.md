---
title: Funzione glLogicOp (Gl.h)
description: La funzione glLogicOp specifica un'operazione di pixel logica per il rendering dell'indice dei colori.
ms.assetid: 29edf9bd-f3b8-4de7-9afb-07714f4efd92
keywords:
- Funzione glLogicOp OpenGL
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
ms.openlocfilehash: 427bd338e416843418fa7551d4e1632dccaf268426ca2a910e164aeae50663dd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119492671"
---
# <a name="gllogicop-function"></a>Funzione glLogicOp

La **funzione glLogicOp** specifica un'operazione di pixel logica per il rendering dell'indice dei colori.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glLogicOp(
   GLenum opcode
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Opcode* 
</dt> <dd>

Costante simbolica che seleziona un'operazione logica. Vengono accettati i simboli seguenti, dove s è uguale al valore del bit di origine e d è il valore del bit di destinazione.



| Valore                                                                                                                                                                   | Significato              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------|
| <span id="GL_CLEAR"></span><span id="gl_clear"></span><dl> <dt>**GL \_ CLEAR**</dt> </dl>                          | 0<br/>         |
| <span id="GL_SET"></span><span id="gl_set"></span><dl> <dt>**GL \_ SET**</dt> </dl>                                | 1<br/>         |
| <span id="GL_COPY"></span><span id="gl_copy"></span><dl> <dt>**COPIA \_ GL**</dt> </dl>                             | s<br/>         |
| <span id="GL_COPY_INVERTED"></span><span id="gl_copy_inverted"></span><dl> <dt>**COPIA \_ GL \_ INVERTITA**</dt> </dl> | !s<br/>        |
| <span id="GL_NOOP"></span><span id="gl_noop"></span><dl> <dt>**GL \_ NOOP**</dt> </dl>                             | d<br/>         |
| <span id="GL_INVERT"></span><span id="gl_invert"></span><dl> <dt>**\_INVERTI GL**</dt> </dl>                       | !d<br/>        |
| <span id="GL_AND"></span><span id="gl_and"></span><dl> <dt>**GL \_ E**</dt> </dl>                                | s & d<br/>     |
| <span id="GL_NAND"></span><span id="gl_nand"></span><dl> <dt>**GL \_ NAND**</dt> </dl>                             | ! (s & d)<br/>  |
| <span id="GL_OR"></span><span id="gl_or"></span><dl> <dt>**GL \_ OR**</dt> </dl>                                   | s \| d<br/>    |
| <span id="GL_NOR"></span><span id="gl_nor"></span><dl> <dt>**GL \_ NOR**</dt> </dl>                                | ! (s \| d)<br/> |
| <span id="GL_XOR"></span><span id="gl_xor"></span><dl> <dt>**GL \_ XOR**</dt> </dl>                                | s ^ d<br/>     |
| <span id="GL_EQUIV"></span><span id="gl_equiv"></span><dl> <dt>**GL \_ EQUIV**</dt> </dl>                          | ! (s ^ d)<br/>  |
| <span id="GL_AND_REVERSE"></span><span id="gl_and_reverse"></span><dl> <dt>**GL \_ E \_ REVERSE**</dt> </dl>       | s & !d<br/>    |
| <span id="GL_AND_INVERTED"></span><span id="gl_and_inverted"></span><dl> <dt>**GL \_ E \_ INVERTED**</dt> </dl>    | !s & d<br/>    |
| <span id="GL_OR_REVERSE"></span><span id="gl_or_reverse"></span><dl> <dt>**GL \_ O \_ REVERSE**</dt> </dl>          | s \| !d<br/>   |
| <span id="GL_OR_INVERTED"></span><span id="gl_or_inverted"></span><dl> <dt>**GL \_ O \_ INVERTITO**</dt> </dl>       | !s \| d<br/>   |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

I codici di errore seguenti possono essere recuperati dalla [**funzione glGetError.**](glgeterror.md)



| Nome                                                                                                  | Significato                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ENUMERAZIONE GL \_ NON \_ VALIDA**</dt> </dl>      | *opcode* non è un valore accettato.<br/>                                                                                        |
| <dl> <dt>**OPERAZIONE GL \_ NON \_ VALIDA**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Commenti

La **funzione glLogicOp** specifica un'operazione logica che, se abilitata, viene applicata tra l'indice dei colori in ingresso e l'indice dei colori nella posizione corrispondente nel framebuffer. L'operazione logica è abilitata o disabilitata con [**glEnable**](glenable.md) **e glDisable** usando la costante simbolica GL \_ LOGIC \_ OP.

Il *parametro opcode* è una costante simbolica scelta dall'elenco seguente. Nella spiegazione delle operazioni logiche, *s* rappresenta l'indice dei colori in ingresso e *d* rappresenta l'indice nel framebuffer. Vengono usati gli operatori del linguaggio C standard. Come suggerito da questi operatori bit per bit, l'operazione logica viene applicata in modo indipendente a ogni coppia di bit degli indici di origine e di destinazione.

Le operazioni dei pixel logici non vengono applicate ai buffer di colore RGBA.

Quando sono abilitate più index buffer colori per il disegno, le operazioni logiche vengono eseguite separatamente per ogni buffer abilitato, usando il contenuto di tale buffer per l'indice di destinazione (vedere [**glDrawBuffer**](gldrawbuffer.md)).

Il *parametro opcode* deve essere uno dei 16 valori accettati. Altri valori comportano un errore.

Le funzioni seguenti recuperano informazioni correlate a **glLogicOp:**

[**glGet con**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) argomento GL \_ LOGIC OP \_ \_ MODE

[**glIsEnabled con**](glisenabled.md) argomento GL \_ LOGIC \_ OP

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

[**glEnd**](glend.md)
</dt> <dt>

[**glIsEnabled**](glisenabled.md)
</dt> <dt>

[**glStencilOp**](glstencilop.md)
</dt> </dl>

 

 





