---
title: Criteri di gestione degli errori Direct2D
description: 'Questo argomento descrive i criteri di gestione degli errori Direct2D. Include le sezioni seguenti:'
ms.assetid: b5fa327a-a315-46fa-aa78-8a5733faae01
keywords:
- Direct2D, gestione degli errori
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3be48c5d80cbbd971f63392efaf6b902ff6187e0a2687df25ccc728efafbfab
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119318031"
---
# <a name="direct2d-error-handling-policies"></a>Criteri di gestione degli errori Direct2D

Questo argomento descrive i criteri di gestione degli errori Direct2D. Include le sezioni seguenti:

-   [Uso di HRESULT](#use-of-hresult)
-   [Valore restituito delle funzioni in batch](#return-value-of-batched-functions)
-   [Input non valido](#invalid-input)
    -   [Puntatore di output](#output-pointer)
    -   [Parametro obbligatorio](#required-parameter)
-   [RECT di input nan e non ordinati in modo non valido](#nan-and-poorly-ordered-input-rects)
    -   [NaN come input](#nan-as-input)
    -   [RECT di input non ordinati in modo non valido](#poorly-ordered-input-rects)

## <a name="use-of-hresult"></a>Uso di HRESULT

Se una funzione non è in batch e può avere un errore di run-time, deve restituire **HRESULT** per indicare un errore. Un errore di run-time è qualsiasi errore che non può essere evitato in fase di progettazione, ad esempio memoria insufficiente.

## <a name="return-value-of-batched-functions"></a>Valore restituito delle funzioni in batch

Le funzioni in batch in Direct2D sono le funzioni elaborate come singola unità quando [**viene chiamato EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) [**o**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-close) Close. Sono i comandi di disegno tra [**BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) **ed EndDraw** o i comandi [**in GeometrySink.**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink) Per queste funzioni, gli errori vengono segnalati al completamento del batch. L'errore viene restituito dopo **EndDraw per** i comandi di disegno e **dopo Close** per **GeometrySink.**

RenderTargets interrompe il disegno se è impostato uno stato di errore, ma un'applicazione può chiamare [**Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) per reimpostare lo stato di errore e riprendere il disegno.

**Le funzioni Get** **e Set** non hanno alcun valore restituito. Tuttavia, se un **input di una funzione Set** non è valido, il livello di debug genera un messaggio. In questo caso, non viene impostato alcuno stato di errore e la **funzione Set** non esegue alcuna operazione.

## <a name="invalid-input"></a>Input non valido

Direct2D dereferenzia i puntatori di output e i parametri obbligatori che comportano violazioni di accesso quando i puntatori non sono validi o **NULL.**

### <a name="output-pointer"></a>Puntatore di output

Direct2D dereferenzia un puntatore di output e lo assegna **a NULL immediatamente** dopo l'immissione della funzione. Ciò causa una violazione di accesso se un chiamante passa **NULL** come puntatore al valore restituito. Questo criterio si applica anche alle matrici di puntatori. Per altri parametri di output, ad esempio uno struct, la dereferenziazione si verifica in un secondo momento e comporta anche una violazione di accesso. Esistono tuttavia alcuni metodi che hanno puntatori di output facoltativi [**(ovvero EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw), [**Flush)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush)che non causeranno una violazione di accesso.

### <a name="required-parameter"></a>Parametro obbligatorio

Se **NULL viene** passato a qualsiasi funzione che richiede un valore valido, la funzione dereferenzia il puntatore non valido in anticipo causando una violazione di accesso. Per i parametri di input **facoltativi, NULL** è un valore valido che restituisce un valore predefinito ragionevole.

## <a name="nan-and-poorly-ordered-input-rects"></a>RECT di input nan e non ordinati in modo non valido

In Direct2D, NaN è considerato un input valido e i RECT di input ordinati in modo non valido vengono ordinati.

### <a name="nan-as-input"></a>NaN come input

NaN è considerato un input valido, anche se in genere comporta la primitiva che contiene il valore NaN non di disegno. L'API Direct2D non fornisce filtri espliciti di NaN per convalidare l'input.

### <a name="poorly-ordered-input-rects"></a>RECT di input non ordinati in modo non valido

I RETT di input ordinati in modo non corretto vengono ordinati in modo che gli angoli superiore, sinistro e inferiore destro siano specificati correttamente. Per l'output, i rettangoli vuoti hanno un aspetto simile al seguente: {Infinity, Infinity, FloatMax, FloatMax}.

 

 