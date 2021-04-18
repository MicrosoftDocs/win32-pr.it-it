---
title: funzione glDrawBuffer (GL. h)
description: La funzione glDrawBuffer specifica i buffer dei colori da disegnare in.
ms.assetid: ea625699-303b-4e60-b9aa-771949a8d52d
keywords:
- funzione glDrawBuffer OpenGL
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
ms.openlocfilehash: 3a99bd2b184766f1621d89b2c8d642902d300e14
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301266"
---
# <a name="gldrawbuffer-function"></a>glDrawBuffer (funzione)

La funzione **glDrawBuffer** specifica i buffer dei colori da disegnare in.

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

Consente di specificare fino a quattro buffer di colore da disegnare con le costanti simboliche accettabili seguenti.



| Valore                                                                                                                                                                       | Significato                                                                                                                                                                                                                                                                                                                                                                                                      |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_NONE"></span><span id="gl_none"></span><dl> <dt>**GL \_ None**</dt> </dl>                                 | Non viene scritto alcun buffer dei colori.<br/>                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="GL_FRONT_LEFT"></span><span id="gl_front_left"></span><dl> <dt>**GL \_ anteriore \_ sinistra**</dt> </dl>              | Viene scritto solo il buffer dei colori in primo piano.<br/>                                                                                                                                                                                                                                                                                                                                                      |
| <span id="GL_FRONT_RIGHT"></span><span id="gl_front_right"></span><dl> <dt>**GL in \_ primo piano \_**</dt> </dl>           | Viene scritto solo il buffer dei colori front-right.<br/>                                                                                                                                                                                                                                                                                                                                                     |
| <span id="GL_BACK_LEFT"></span><span id="gl_back_left"></span><dl> <dt>**GL \_ a \_ sinistra**</dt> </dl>                 | Viene scritto solo il buffer dei colori Back-left.<br/>                                                                                                                                                                                                                                                                                                                                                       |
| <span id="GL_BACK_RIGHT"></span><span id="gl_back_right"></span><dl> <dt>**GL \_ a \_ destra**</dt> </dl>              | Viene scritto solo il buffer dei colori back-right.<br/>                                                                                                                                                                                                                                                                                                                                                      |
| <span id="GL_FRONT"></span><span id="gl_front"></span><dl> <dt>**\_primo piano GL**</dt> </dl>                              | Vengono scritti solo i buffer dei colori Front-Left e front-right. Se non è presente alcun buffer di colore front-right, viene scritto solo il buffer di colore anteriore sinistro.<br/>                                                                                                                                                                                                                                              |
| <span id="GL_BACK"></span><span id="gl_back"></span><dl> <dt>**indietro per GL \_**</dt> </dl>                                 | Vengono scritti solo i buffer dei colori Back-left e back-right. Se non è presente alcun buffer dei colori di back-right, viene scritto solo il buffer di colore Back-left.<br/>                                                                                                                                                                                                                                                  |
| <span id="GL_LEFT"></span><span id="gl_left"></span><dl> <dt>**GL a \_ sinistra**</dt> </dl>                                 | Vengono scritti solo i buffer dei colori Front-Left e back-left. Se non è presente alcun buffer dei colori Back-left, viene scritto solo il buffer di colore in primo piano.<br/>                                                                                                                                                                                                                                                  |
| <span id="GL_RIGHT"></span><span id="gl_right"></span><dl> <dt>**GL a \_ destra**</dt> </dl>                              | Vengono scritti solo i buffer dei colori Front-Right e back-right. Se non è presente alcun buffer dei colori back-right, viene scritto solo il buffer del colore front-right.<br/>                                                                                                                                                                                                                                              |
| <span id="GL_FRONT_AND_BACK"></span><span id="gl_front_and_back"></span><dl> <dt>**\_primo \_ e \_ indietro GL**</dt> </dl> | Vengono scritti tutti i buffer di colore anteriore e posteriore (in primo piano, a sinistra, in primo piano, a sinistra, a destra). Se non sono presenti buffer di colore di sfondo, vengono scritti solo i buffer dei colori Front-Left e front-right. Se non sono presenti buffer di colore corretti, vengono scritti solo i buffer dei colori in primo piano e a sinistra. Se non sono presenti buffer a destra o a sinistra, viene scritto solo il buffer dei colori in primo piano.<br/> |
| <span id="GL_AUXi"></span><span id="gl_auxi"></span><span id="GL_AUXI"></span><dl> <dt>**\_Auxi GL**</dt> </dl>       | *Viene scritto* solo il buffer dei colori ausiliario; *i* è compreso tra 0 e GL \_ aux \_ buffers-1. (GL \_ \_I buffer aux non corrispondono al limite massimo. utilizzare [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) per eseguire una query sul numero di buffer ausiliari disponibili.<br/>                                                                                                                            |



 

Il valore predefinito è GL \_ front per i contesti con buffer singolo e GL \_ indietro per i contesti con doppio buffer.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significato                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_enumerazione GL non valida \_**</dt> </dl>      | la *modalità* non è un valore accettato.<br/>                                                                                          |
| <dl> <dt>**\_operazione GL non valida \_**</dt> </dl> | Nessuno dei buffer indicati dalla *modalità* esisteva.<br/>                                                                           |
| <dl> <dt>**\_operazione GL non valida \_**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/> |


## <a name="remarks"></a>Commenti

Quando i colori vengono scritti nel framebuffer, vengono scritti nei buffer dei colori specificati da **glDrawBuffer**.

Se per il disegno è selezionato più di un buffer di colore, le operazioni di fusione o logiche vengono calcolate e applicate in modo indipendente per ogni buffer di colore e possono produrre risultati diversi in ogni buffer.

I contesti monoscopiche includono solo i buffer a sinistra e i contesti stereoscopici includono entrambi i buffer a sinistra e a destra. Analogamente, i contesti con buffer singolo includono solo i buffer di primo livello e i contesti a doppio buffer includono i buffer front e back. Il contesto è selezionato nell'inizializzazione di OpenGL.

È sempre il caso GL \_ aux *i* = GL \_ AUX0 + *i*.

Le funzioni seguenti consentono di recuperare informazioni correlate alla funzione **glDrawBuffer** :

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con il \_ buffer di disegnato GL argomento \_

**glGet** con gli argomenti GL \_ aux \_ buffers

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

[**glBlendFunc**](glblendfunc.md)
</dt> <dt>

[**glColorMask**](glcolormask.md)
</dt> <dt>

[**Remo**](glend.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glIndexMask**](glindexmask.md)
</dt> <dt>

[**glLogicOp**](gllogicop.md)
</dt> <dt>

[**glReadBuffer**](glreadbuffer.md)
</dt> </dl>

 

 





