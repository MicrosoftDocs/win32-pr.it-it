---
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: 92438df1-afde-4038-853e-9b98f7e589ea
title: Opzioni con parametri rispetto alle opzioni non parametrizzate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3c1da2aba2515662be79da0c3831762de66463d
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "104351846"
---
# <a name="parameterized-options-versus-nonparameterized-options"></a>Opzioni con parametri rispetto alle opzioni non parametrizzate

Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

I provider PrintCapabilities e PrintTicket devono gestire correttamente le istanze di opzioni con parametri durante il processo di convalida PrintTicket. Come illustrato nelle [definizioni delle opzioni](option-definitions.md), un passaggio eseguito nella convalida PrintTicket consiste nel trovare l'opzione nel documento PrintCapabilities del dispositivo corrente (opzione candidata) che corrisponde maggiormente all'opzione specificata nell'oggetto PrintTicket (opzione di riferimento). Quando una o entrambe le istanze dell'opzione sono parametrizzate, esistono tre casi possibili che devono essere gestiti dal processo di assegnazione dei punteggi definito dal driver di dispositivo: il caso in cui entrambe le istanze di opzione sono parametrizzate e i due casi in cui un'opzione è parametrizzata e l'altra non lo è. Nei casi seguenti si presuppone che esista una corrispondenza tra le istanze ScoredProperty con parametri nell'opzione PrintTicket e un particolare ScoredProperty nell'opzione PrintCapabilities. Se non è presente alcuna corrispondenza, il processo di assegnazione dei punteggi può considerare queste istanze di ScoredProperty nello stesso modo in cui tratta qualsiasi altra istanza di ScoredProperty non corrispondente.

## <a name="case-1---parameterized-printticket-and-printcapabilities-document-options"></a>Caso 1: opzioni di documento PrintTicket e PrintCapabilities con parametri

In questo caso, sia l'opzione di riferimento (in PrintTicket) che l'opzione candidata (nel documento PrintCapabilities) sono parametrizzati. Accedere all'istanza di ParameterDef a cui fa riferimento l'opzione candidata (sia nel documento PrintCapabilities) che determinare se il valore ParameterInit specificato nell'oggetto PrintTicket rientra nell'intervallo consentito dall'istanza di ParameterDef. In caso affermativo, prendere in considerazione questo ScoredProperty per trovare una corrispondenza. In caso contrario, questo ScoredProperty non è una corrispondenza.

## <a name="case-2---parameterized-printticket-option-nonparameterized-printcapabilities-document-option"></a>Case 2-opzione PrintTicket con parametri, opzione del documento PrintCapabilities senza parametri

In questo caso, l'oggetto PrintTicket contiene una funzionalità con un'opzione con parametri, mentre la caratteristica corrispondente nel documento PrintCapabilities contiene almeno un'opzione che non è parametrizzata. Anche se il documento PrintCapabilities contiene anche altre istanze di opzioni parametrizzate, il processo di assegnazione dei punteggi deve essere applicato a ogni opzione, perché l'obiettivo è identificare l'opzione di corrispondenza migliore. Il client deve essere in grado di confrontare i candidati di opzioni non parametrizzate con un'opzione di riferimento con parametri.

Poiché l'opzione con parametri viene visualizzata nel PrintTicket, le istanze di ParameterInit devono essere presenti anche come illustrato nel caso precedente. Il processo di assegnazione dei punteggi può semplicemente sostituire qualsiasi istanza di ParameterRef nell'opzione con parametri del PrintTicket con il valore specificato dall'istanza ParameterInit di PrintTicket. In questo modo, un'opzione parametrizzata viene convertita in un valore senza parametri. A questo punto è possibile usare il processo di corrispondenza convenzionale.

## <a name="case-3---nonparameterized-printticket-option-parameterized-printcapabilities-document-option"></a>Caso 3: opzione PrintTicket senza parametri, opzione del documento PrintCapabilities con parametri

In questo caso, l'opzione di riferimento nell'oggetto PrintTicket non è parametrizzata, mentre l'opzione candidata nel documento PrintCapabilities è parametrizzata. Accedere all'istanza di ParameterDef nel documento PrintCapabilities a cui fa riferimento l'istanza ParameterRef dell'opzione candidata nell'oggetto PrintTicket e determinare se il valore definito nell'opzione reference per il ScoredProperty corrispondente rientra nell'intervallo consentito dall'istanza di ParameterDef. In caso affermativo, prendere in considerazione questo ScoredProperty per trovare una corrispondenza. In caso contrario, questo ScoredProperty non è una corrispondenza.

È necessario sottolineare che si determina il modo in cui due istanze delle opzioni corrispondono al numero (e all'importanza) delle istanze di ScoredProperty che corrispondono, indipendentemente dal fatto che le istanze di ScoredProperty contengano istanze di valori esplicite o istanze di ParameterRef. È possibile che un'opzione candidata sia la migliore corrispondenza, anche se contiene diverse istanze di proprietà che non corrispondono a quelle dell'opzione di riferimento o che non hanno proprietà corrispondenti nell'opzione reference.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



