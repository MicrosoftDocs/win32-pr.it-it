---
title: Funzione glDrawBuffer (Gl.h)
description: La funzione glDrawBuffer specifica in quali buffer di colore devono essere disegnati.
ms.assetid: ea625699-303b-4e60-b9aa-771949a8d52d
keywords:
- Funzione glDrawBuffer OpenGL
topic_type:
- apiref
api_name:
- glDrawBuffer
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc5bc715aad24198031ed096d53f1a468b6672532e4df4ae1ef66b416002a65b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120081611"
---
# <a name="gldrawbuffer-function"></a>Funzione glDrawBuffer

La **funzione glDrawBuffer** specifica in quali buffer di colore devono essere disegnati.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glDrawBuffer(
   GLenum mode
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*mode* 
</dt> <dd>

Specifica fino a quattro buffer di colore da disegnare con le costanti simboliche accettabili seguenti.



| Valore                                                                                                                                                                       | Significato                                                                                                                                                                                                                                                                                                                                                                                                      |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_NONE"></span><span id="gl_none"></span><dl> <dt>**GL \_ NONE**</dt> </dl>                                 | Non vengono scritti buffer di colore.<br/>                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="GL_FRONT_LEFT"></span><span id="gl_front_left"></span><dl> <dt>**GL \_ FRONT \_ LEFT**</dt> </dl>              | Viene scritto solo il buffer colori anteriore sinistro.<br/>                                                                                                                                                                                                                                                                                                                                                      |
| <span id="GL_FRONT_RIGHT"></span><span id="gl_front_right"></span><dl> <dt>**GL \_ FRONT \_ RIGHT**</dt> </dl>           | Viene scritto solo il buffer dei colori anteriore destro.<br/>                                                                                                                                                                                                                                                                                                                                                     |
| <span id="GL_BACK_LEFT"></span><span id="gl_back_left"></span><dl> <dt>**GL \_ INDIETRO \_ A SINISTRA**</dt> </dl>                 | Viene scritto solo il buffer dei colori back-left.<br/>                                                                                                                                                                                                                                                                                                                                                       |
| <span id="GL_BACK_RIGHT"></span><span id="gl_back_right"></span><dl> <dt>**GL \_ BACK \_ RIGHT**</dt> </dl>              | Viene scritto solo il buffer dei colori back-right.<br/>                                                                                                                                                                                                                                                                                                                                                      |
| <span id="GL_FRONT"></span><span id="gl_front"></span><dl> <dt>**GL \_ FRONT**</dt> </dl>                              | Vengono scritti solo i buffer dei colori front-left e front-right. Se non è presente alcun buffer colore anteriore destro, viene scritto solo il buffer di colore a sinistra anteriore.<br/>                                                                                                                                                                                                                                              |
| <span id="GL_BACK"></span><span id="gl_back"></span><dl> <dt>**GL \_ BACK**</dt> </dl>                                 | Vengono scritti solo i buffer di colore back-left e back-right. Se non è presente alcun buffer di colore back-right, viene scritto solo il buffer dei colori back-left.<br/>                                                                                                                                                                                                                                                  |
| <span id="GL_LEFT"></span><span id="gl_left"></span><dl> <dt>**GL \_ A SINISTRA**</dt> </dl>                                 | Vengono scritti solo i buffer dei colori anteriore sinistro e posteriore sinistro. Se non è presente alcun buffer colore back-left, viene scritto solo il buffer colori anteriore sinistro.<br/>                                                                                                                                                                                                                                                  |
| <span id="GL_RIGHT"></span><span id="gl_right"></span><dl> <dt>**GL \_ RIGHT**</dt> </dl>                              | Vengono scritti solo i buffer dei colori front-right e back-right. Se non è presente alcun buffer colore back-right, viene scritto solo il buffer colori anteriore destro.<br/>                                                                                                                                                                                                                                              |
| <span id="GL_FRONT_AND_BACK"></span><span id="gl_front_and_back"></span><dl> <dt>**GL \_ FRONT \_ AND \_ BACK**</dt> </dl> | Vengono scritti tutti i buffer di colore anteriore e posteriore (front-left, front-right, back-left, back-right). Se non sono presenti buffer di colore nascosto, vengono scritti solo i buffer colore anteriore sinistro e anteriore destro. Se non sono presenti buffer colori a destra, vengono scritti solo i buffer di colore anteriore sinistro e posteriore sinistro. Se non sono presenti buffer di colore destro o posteriore, viene scritto solo il buffer colori anteriore sinistro.<br/> |
| <span id="GL_AUXi"></span><span id="gl_auxi"></span><span id="GL_AUXI"></span><dl> <dt>**GL \_ AUXi**</dt> </dl>       | Viene scritto solo il buffer colori ausiliario *i.* *i* è compreso tra 0 e GL \_ AUX \_ BUFFERS - 1. (Gl \_ AUX BUFFERS non è il limite massimo. Usare glGet per eseguire query sul numero di \_ buffer ausiliari [](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) disponibili.<br/>                                                                                                                            |



 

Il valore predefinito è GL FRONT per i contesti a buffer singolo e GL BACK per i \_ \_ contesti con doppio buffer.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

I codici di errore seguenti possono essere recuperati dalla [**funzione glGetError.**](glgeterror.md)



| Nome                                                                                                  | Significato                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ENUMERAZIONE GL \_ NON \_ VALIDA**</dt> </dl>      | *mode* non è un valore accettato.<br/>                                                                                          |
| <dl> <dt>**OPERAZIONE GL \_ NON \_ VALIDA**</dt> </dl> | Nessuno dei buffer indicati dalla *modalità* esisteva.<br/>                                                                           |
| <dl> <dt>**OPERAZIONE GL \_ NON \_ VALIDA**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/> |


## <a name="remarks"></a>Commenti

Quando i colori vengono scritti nel framebuffer, vengono scritti nei buffer dei colori specificati da **glDrawBuffer**.

Se per il disegno sono selezionati più buffer colori, le operazioni di fusione o logica vengono calcolate e applicate in modo indipendente per ogni buffer di colore e possono produrre risultati diversi in ogni buffer.

I contesti monoscopici includono solo buffer a sinistra e i contesti stereoscopici includono buffer sia a sinistra che a destra. Analogamente, i contesti a buffer singolo includono solo i front buffer e i contesti con doppio buffer includono sia i buffer front che back. Il contesto viene selezionato durante l'inizializzazione OpenGL.

È sempre il caso che GL \_ AUX *i* = GL \_ AUX0 + *i*.

Le funzioni seguenti recuperano informazioni correlate alla **funzione glDrawBuffer:**

[**glGet con**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) argomento GL \_ DRAW \_ BUFFER

**glGet con** l'argomento GL \_ AUX \_ BUFFERS

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

[**glBlendFunc**](glblendfunc.md)
</dt> <dt>

[**glColorMask**](glcolormask.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glIndexMask**](glindexmask.md)
</dt> <dt>

[**glLogicOp**](gllogicop.md)
</dt> <dt>

[**glReadBuffer**](glreadbuffer.md)
</dt> </dl>

 

 





