---
description: Uno degli strumenti principali di Strumentazione gestione Windows (WMI) è la possibilità di eseguire query nel repository WMI per ottenere informazioni su classi e istanze.
ms.assetid: 0cceda42-fba0-4a08-90dd-43f022d0be41
ms.tgt_platform: multiple
title: Esecuzione di query su WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfc9cd51946bad1df482bb286c538e38bba8e2b3337776e3cd62e0a0da652574
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118817539"
---
# <a name="querying-wmi"></a>Esecuzione di query su WMI

Uno degli strumenti principali di Strumentazione gestione Windows (WMI) è la possibilità di eseguire query nel repository WMI per ottenere informazioni su classi e istanze. Ad esempio, è possibile richiedere a WMI di restituire tutti gli oggetti che rappresentano gli eventi di arresto dal sistema desktop. È anche possibile recuperare i dati della classe, dell'istanza o dello schema. Nella tabella seguente sono elencati i diversi tipi di query che è possibile eseguire.



| Argomento                                                                | Descrizione                                                                                                                                                                                      |
|----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Chiamata di una query sincrona](invoking-a-synchronous-query.md)     | Viene descritto come mantenere un collegamento con WMI in tutto il processo di query. Le query sincrone sono buone per query di piccole dimensioni o query in un sistema locale.<br/>                                  |
| [Chiamata di una query asincrona](invoking-an-asynchronous-query.md) | Viene descritto come configurare un processo separato per ricevere query. Le query asincrone sono più complesse e offrono un livello di sicurezza inferiore, ma in genere migliorano le prestazioni del sistema.<br/> |



 

Oltre a eseguire query sul repository WMI, è anche possibile usare WMI Query Language [*(WQL)*](gloss-w.md) per instradare gli eventi di notifica all'applicazione. Per altre informazioni, vedere [Ricezione di un evento WMI.](receiving-a-wmi-event.md)

> [!Note]
>
> Per eseguire correttamente query su WMI, è necessario avere una buona conoscenza di WQL. Una query non corretta, troppo complessa o inappropriata può causare la restituzione di un errore o di risultati imprevisti da parte di Query Processor. Per una guida completa a WQL, vedere [Esecuzione di query con WQL.](querying-with-wql.md)
>
> Esistono limiti al numero di parole **chiave AND** **e OR** che possono essere usate nelle query WQL. Un numero elevato di parole chiave WQL usate in una query complessa può causare la restituzione del codice di errore **WBEM \_ E \_ QUOTA \_ VIOLATION** da parte di WMI come **valore HRESULT.** Il limite delle parole chiave WQL dipende dalla complessità della query.
>
> Quando si esegue una query per i valori delle proprietà con un tipo di dati **uint64** o **sint64** in un linguaggio di scripting come VBScript, WMI restituisce valori stringa. Quando si confrontano questi valori, possono verificarsi risultati imprevisti, perché il confronto di stringhe restituisce risultati diversi rispetto al confronto dei numeri. Ad esempio, "10000000000" è minore di "9" quando si confrontano le stringhe e 9 è minore di 1000000000 quando si confrontano i numeri. Per evitare confusione, è consigliabile usare il metodo [CDbl](/previous-versions//ftekwwt0(v=vs.85)) in VBScript quando le proprietà di tipo **uint64** o **sint64** vengono recuperate da WMI.

 

> [!Note]  

 

Per altre informazioni, vedere [Modifica delle informazioni su classi e istanze](manipulating-class-and-instance-information.md).

 

