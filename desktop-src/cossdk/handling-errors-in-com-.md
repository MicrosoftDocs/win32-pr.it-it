---
description: La parte più problematica della scrittura dei componenti è la gestione dei possibili errori.
ms.assetid: 12f41eef-9953-4125-8490-07ff64967f95
title: Gestione degli errori in COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04b66ecfd2d66d30b601fdc9e3e580d258ab912db5c10e3af422b9e7fde2b7a2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118306550"
---
# <a name="handling-errors-in-com"></a>Gestione degli errori in COM+

La parte più problematica della scrittura dei componenti è la gestione dei possibili errori. Il tentativo di determinare cosa può andare storto e cosa fare al riguardo può risultare complesso nelle condizioni migliori. Gli errori comuni che il componente potrebbe verificare e gestire sono le connessioni di rete non riuscite, gli errori di sicurezza e gli errori associati a oggetti non raggiungibili.

Inoltre, è possibile sviluppare codici di errore personalizzati per segnalare errori specifici dell'interfaccia, ad esempio quando una regola business è stata violata.

In linea con il modello di programmazione COM+, un oggetto può (e spesso) chiamare metodi di interfaccia su altri oggetti per eseguire operazioni. Poiché i programmatori possono scrivere componenti in linguaggi di programmazione diversi, COM+ richiede che tutti i meccanismi di gestione degli errori siano indipendenti dal linguaggio, ad esempio raccolte HRESULT ed [**ErrorInfo.**](errorinfo.md)

Questa sezione include argomenti, descritti nella tabella seguente, che illustrano le tecniche per la gestione degli errori nelle applicazioni COM+, le funzionalità di COM+ che influiscono sul comportamento degli errori e suggerimenti per la diagnosi degli errori COM+.



| Argomento                                                                                           | Descrizione                                                                                                                                                 |
|-------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Strategie per la gestione degli errori in COM+](strategies-for-handling-errors-in-com-.md)<br/> | Elenca e descrive le linee guida di base per la gestione degli errori in COM+, incluso quando usare HRESULT e [**raccolte ErrorInfo.**](errorinfo.md)<br/> |
| [Modalità di modifica dei valori restituiti da COM+](how-com--modifies-return-values.md)<br/>               | Identifica la singola condizione in cui COM+ converte un HRESULT standard in un codice di errore COM+ prima di passarlo nuovamente al chiamante.<br/>             |
| [Isolamento degli errori e criteri failfast](fault-isolation-and-failfast-policy.md)<br/>       | Illustra in che modo l'isolamento degli errori e i criteri failfast influiscono sul comportamento di COM+.<br/>                                                                          |
| [Ricerca dell'origine di un errore](finding-the-source-of-an-error.md)<br/>                 | Viene descritto come diagnosticare l'origine e ottenere una descrizione degli errori dell'applicazione. <br/>                                                       |
| [Interpretazione dei codici di errore](interpreting-error-codes.md)<br/>                             | Identifica il meccanismo di gestione degli errori predominante Microsoft Visual C++, il linguaggio Java e Microsoft Visual Basic. <br/>                    |
| [Risoluzione dei problemi](troubleshooting.md)<br/>                                               | Fornisce ulteriore assistenza per la diagnosi degli errori.<br/>                                                                                             |
| [Contattare il supporto tecnico](contacting-support.md)<br/>                                         | Identifica importanti informazioni sulla risoluzione dei problemi da fornire quando si contatta il supporto tecnico.<br/>                                                     |



 

Per informazioni dettagliate sulla gestione degli errori associati a vari servizi COM+, vedere le sezioni seguenti:

-   [Velocizzare le transazioni inviando una notifica all'oggetto radice](speeding-transactions-by-notifying-the-root-object.md)
-   [Gestione degli errori](handling-errors-in-queued-components.md) (per i componenti in coda)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Debug di applicazioni COM+](debugging-com--applications.md)
</dt> </dl>

 

 




