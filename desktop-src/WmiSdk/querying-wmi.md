---
description: Uno degli strumenti principali di Strumentazione gestione Windows (WMI) è la possibilità di eseguire query sul repository WMI per informazioni sulle classi e sulle istanze.
ms.assetid: 0cceda42-fba0-4a08-90dd-43f022d0be41
ms.tgt_platform: multiple
title: Esecuzione di query su WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fdae44d4c40e1127bfc4d3436d6230eafd52146a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309921"
---
# <a name="querying-wmi"></a>Esecuzione di query su WMI

Uno degli strumenti principali di Strumentazione gestione Windows (WMI) è la possibilità di eseguire query sul repository WMI per informazioni sulle classi e sulle istanze. È ad esempio possibile richiedere che WMI restituisca tutti gli oggetti che rappresentano gli eventi di chiusura dal sistema desktop. È inoltre possibile recuperare i dati della classe, dell'istanza o dello schema. Nella tabella seguente sono elencati i diversi tipi di query che è possibile eseguire.



| Argomento                                                                | Descrizione                                                                                                                                                                                      |
|----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Richiamo di una query sincrona](invoking-a-synchronous-query.md)     | Viene descritto come gestire un collegamento con WMI durante il processo di query. Le query sincrone sono valide per query o query di piccole dimensioni in un sistema locale.<br/>                                  |
| [Richiamo di una query asincrona](invoking-an-asynchronous-query.md) | Viene descritto come configurare un processo separato per la ricezione di query. Le query asincrone sono più complesse e forniscono un livello di sicurezza inferiore, ma in genere migliorano le prestazioni del sistema.<br/> |



 

Oltre a eseguire query sul repository WMI, è inoltre possibile utilizzare il [*WMI Query Language (WQL)*](gloss-w.md) per indirizzare gli eventi di notifica all'applicazione. Per ulteriori informazioni, vedere [ricezione di un evento WMI](receiving-a-wmi-event.md).

> [!Note]
>
> Per eseguire correttamente una query su WMI, è necessario avere una conoscenza corretta di WQL. Una query non corretta, troppo complessa o inappropriata può causare la restituzione di un errore o di risultati imprevisti da parte di query processor. Per una guida completa a WQL, vedere [esecuzione di query con WQL](querying-with-wql.md).
>
> Esistono limiti al numero di parole chiave **and** e **or** che possono essere utilizzate nelle query WQL. Un numero elevato di parole chiave WQL utilizzate in una query complessa può causare la restituzione del codice di errore di **\_ \_ \_ violazione della quota E di WBEM** come valore **HRESULT** . Il limite di parole chiave WQL dipende dalla complessità della query.
>
> Quando si esegue una query per i valori delle proprietà con un tipo di dati **UInt64** o **sint64** in un linguaggio di scripting come VBScript, WMI restituisce i valori stringa. Quando si confrontano questi valori, possono verificarsi risultati imprevisti, perché il confronto di stringhe restituisce risultati diversi rispetto al confronto dei numeri. Ad esempio, "10 miliardi" è minore di "9" durante il confronto di stringhe e 9 è minore di 10 miliardi durante il confronto dei numeri. Per evitare confusione, è consigliabile usare il metodo [CDbl](/previous-versions//ftekwwt0(v=vs.85)) in VBScript quando le proprietà di tipo **UInt64** o **SINT64** vengono recuperate da WMI.

 

> [!Note]  

 

Per ulteriori informazioni, vedere [modifica delle informazioni sulle classi e sulle istanze](manipulating-class-and-instance-information.md).

 

