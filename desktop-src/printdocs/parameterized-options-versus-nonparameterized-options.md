---
description: Informazioni su come PrintTicket e PrintCapabilities gestiscono le opzioni con parametri e senza parametri.
ms.assetid: 92438df1-afde-4038-853e-9b98f7e589ea
title: Opzioni con parametri e opzioni non parametrizzate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4c788eaf2fa08f4f29a541a775d2bcbf523aa51
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407224"
---
# <a name="parameterized-options-versus-nonparameterized-options"></a>Opzioni con parametri e opzioni non parametrizzate

Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Specifica [dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

I provider PrintCapabilities e PrintTicket devono gestire correttamente le istanze Option con parametri durante il processo di convalida PrintTicket. Come illustrato [in](option-definitions.md)Definizioni delle opzioni, un passaggio eseguito nella convalida PrintTicket consiste nel trovare l'opzione nel documento PrintCapabilities del dispositivo corrente (opzione candidata) che corrisponde meglio all'opzione specificata in PrintTicket (opzione di riferimento). Quando una o entrambe le istanze option sono parametrizzate, esistono tre casi possibili che devono essere gestiti dal processo di assegnazione dei punteggi definito dal driver di dispositivo: il caso in cui entrambe le istanze Option sono parametrizzate e i due casi in cui un'opzione è con parametri e l'altra no. Nei casi seguenti si presuppone che vi sia una corrispondenza tra le istanze scoredProperty con parametri nell'opzione PrintTicket e una particolare ScoredProperty nell'opzione PrintCapabilities. Se non è presente alcuna corrispondenza, il processo di assegnazione dei punteggi può trattare queste istanze ScoredProperty nello stesso modo in cui considera qualsiasi altra istanza ScoredProperty che non risponde.

## <a name="case-1---parameterized-printticket-and-printcapabilities-document-options"></a>Caso 1 - Opzioni dei documenti PrintTicket e PrintCapabilities con parametri

In questo caso, sia l'opzione di riferimento (in PrintTicket) che l'opzione candidata (nel documento PrintCapabilities) sono parametrizzate. Accedere all'istanza ParameterDef a cui fa riferimento l'opzione candidata (entrambe nel documento PrintCapabilities) e determinare se il valore ParameterInit specificato in PrintTicket rientra nell'intervallo consentito dall'istanza ParameterDef. In tal caso, considerare scoredProperty come una corrispondenza. In caso contrario, scoredProperty non è una corrispondenza.

## <a name="case-2---parameterized-printticket-option-nonparameterized-printcapabilities-document-option"></a>Caso 2- Opzione PrintTicket con parametri, opzione documento PrintCapabilities non parametrizzato

In questo caso, PrintTicket contiene una funzionalità con un'opzione con parametri, mentre la funzionalità corrispondente nel documento PrintCapabilities contiene almeno un'opzione che non è con parametri. Anche se il documento PrintCapabilities contiene anche altre istanze Option con parametri, il processo di assegnazione dei punteggi deve essere applicato a ogni opzione, perché l'obiettivo è identificare l'opzione di corrispondenza migliore. Il client deve essere in grado di confrontare i candidati option non parametrizzati con un'opzione di riferimento con parametri.

Poiché l'opzione con parametri viene visualizzata in PrintTicket, anche le istanze ParameterInit devono essere presenti come illustrato nel caso precedente. Il processo di assegnazione dei punteggi può semplicemente sostituire qualsiasi istanza ParameterRef nell'opzione con parametri di PrintTicket con il valore specificato dall'istanza ParameterInit di PrintTicket. In questo modo un'opzione con parametri viene convertita in un'opzione che non è con parametri. A questo punto è possibile usare il processo di corrispondenza convenzionale.

## <a name="case-3---nonparameterized-printticket-option-parameterized-printcapabilities-document-option"></a>Caso 3 - Opzione PrintTicket non parametrizzata, opzione del documento PrintCapabilities con parametri

In questo caso, l'opzione di riferimento in PrintTicket non è con parametri, mentre l'opzione candidata nel documento PrintCapabilities è con parametri. Accedere all'istanza ParameterDef nel documento PrintCapabilities a cui fa riferimento l'istanza ParameterRef dell'opzione candidata in PrintTicket e determinare se il valore definito nell'opzione di riferimento per l'oggetto ScoredProperty corrispondente rientra nell'intervallo consentito dall'istanza ParameterDef. In tal caso, considerare scoredProperty come una corrispondenza. In caso contrario, scoredProperty non è una corrispondenza.

È importante sottolineare che si determina la corrispondenza tra due istanze option in base al numero (e al significato) delle istanze ScoredProperty corrispondenti, indipendentemente dal fatto che le istanze ScoredProperty contengano istanze Value esplicite o ParameterRef. È possibile che un'opzione candidata sia la corrispondenza migliore, anche se contiene diverse istanze property che non corrispondono a quelle dell'opzione di riferimento o che non hanno alcuna proprietà corrispondente nell'opzione di riferimento.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



