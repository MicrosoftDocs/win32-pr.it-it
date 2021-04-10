---
title: Criteri di gestione degli errori Direct2D
description: 'In questo argomento vengono descritti i criteri di gestione degli errori Direct2D. Include le sezioni seguenti:'
ms.assetid: b5fa327a-a315-46fa-aa78-8a5733faae01
keywords:
- Direct2D, gestione degli errori
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fc930e7ee9e5b73b5f676103f45ffe25e4d4e61
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103963367"
---
# <a name="direct2d-error-handling-policies"></a>Criteri di gestione degli errori Direct2D

In questo argomento vengono descritti i criteri di gestione degli errori Direct2D. Include le sezioni seguenti:

-   [Utilizzo di HRESULT](#use-of-hresult)
-   [Valore restituito delle funzioni in batch](#return-value-of-batched-functions)
-   [Input non valido](#invalid-input)
    -   [Puntatore di output](#output-pointer)
    -   [Parametro obbligatorio](#required-parameter)
-   [RECTs di input NaN e ordinato male](#nan-and-poorly-ordered-input-rects)
    -   [NaN come input](#nan-as-input)
    -   [RETTANGOLi di input ordinati in modo non corretto](#poorly-ordered-input-rects)

## <a name="use-of-hresult"></a>Utilizzo di HRESULT

Se una funzione non è in batch e può avere un errore di run-time, deve restituire **HRESULT** per indicare un errore. Un errore in fase di esecuzione è un errore che non può essere evitato in fase di progettazione, ad esempio memoria insufficiente.

## <a name="return-value-of-batched-functions"></a>Valore restituito delle funzioni in batch

Le funzioni in batch in Direct2D sono le funzioni elaborate come una singola unità quando viene chiamato [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) o [**Close**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-close) . Sono i comandi di disegno tra [**BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) e **EndDraw** o i comandi su [**GeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink). Per queste funzioni, gli errori vengono segnalati nel momento in cui il batch viene completato. L'errore viene restituito dopo **EndDraw** per il disegno dei comandi e dopo la **chiusura** di **GeometrySink**.

RenderTargets arresta il disegno se è stato impostato uno stato di errore, ma un'applicazione può chiamare [**Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) per reimpostare lo stato di errore e riprendere il disegno.

Le funzioni **Get** e **set** non restituiscono alcun valore. Tuttavia, se una funzione **set** ha un input non valido, il livello di debug genera un messaggio. In questo caso non viene impostato alcuno stato di errore e la funzione **set** non esegue alcuna operazione.

## <a name="invalid-input"></a>Input non valido

Direct2D consente di dereferenziare i puntatori di output e i parametri obbligatori che generano violazioni di accesso quando i puntatori non sono validi o sono **null**.

### <a name="output-pointer"></a>Puntatore di output

Direct2D dereferenzia un puntatore di output e lo assegna a **null** immediatamente dopo l'immissione della funzione. Ciò provoca una violazione di accesso se un chiamante passa **null** come puntatore al valore restituito. Questo criterio si applica anche a matrici di puntatori. Per altri parametri di output, ad esempio uno struct, la dereferenziazione viene eseguita in un secondo momento e comporta anche una violazione di accesso. Tuttavia, esistono alcuni metodi che dispongono di puntatori di output facoltativi (ovvero [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw), [**Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush)) che non provocheranno una violazione di accesso.

### <a name="required-parameter"></a>Parametro obbligatorio

Se **null** viene passato a una funzione che richiede un valore valido, la funzione dereferenzia il puntatore errato in anticipo, causando una violazione di accesso. Per i parametri di input facoltativi, **null** è un valore valido che restituisce un valore predefinito ragionevole.

## <a name="nan-and-poorly-ordered-input-rects"></a>RECTs di input NaN e ordinato male

In Direct2D, NaN è considerato un input valido e i RETTANGOLi di input non ordinati sono ordinati.

### <a name="nan-as-input"></a>NaN come input

NaN è considerato un input valido, sebbene in genere il risultato della primitiva che contiene il valore NaN non viene disegnato. L'API Direct2D non fornisce il filtro esplicito di NaN per convalidare l'input.

### <a name="poorly-ordered-input-rects"></a>RETTANGOLi di input ordinati in modo non corretto

I RETTANGOLi di input poco ordinati vengono ordinati in modo che gli angoli superiore, sinistro e inferiore siano specificati correttamente. Per l'output, i rettangoli vuoti hanno un aspetto simile al seguente: {Infinity, Infinity, FloatMax, FloatMax}.

 

 