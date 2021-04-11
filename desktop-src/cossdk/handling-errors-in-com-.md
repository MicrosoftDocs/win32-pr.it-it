---
description: La parte più problematica della scrittura di componenti è la gestione di possibili errori.
ms.assetid: 12f41eef-9953-4125-8490-07ff64967f95
title: Gestione degli errori in COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc1979fc49ff8f14bb83b194be7e1787feaf7d86
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127794"
---
# <a name="handling-errors-in-com"></a>Gestione degli errori in COM+

La parte più problematica della scrittura di componenti è la gestione di possibili errori. Il tentativo di determinare cosa può andare male e le operazioni da eseguire su di esso può essere difficile in caso di condizioni ottimali. Errori comuni che il componente potrebbe controllare e gestire sono le connessioni di rete non riuscite, errori di sicurezza ed errori associati a oggetti non raggiungibili.

Inoltre, è possibile sviluppare codici di errore personalizzati per segnalare errori specifici dell'interfaccia, ad esempio quando una regola business è stata violata.

In conformità con il modello di programmazione COM+, un oggetto può (e spesso) chiamare metodi di interfaccia su altri oggetti per eseguire il lavoro. Poiché i programmatori possono scrivere componenti in linguaggi di programmazione diversi, COM+ richiede che tutti i meccanismi di gestione degli errori siano indipendenti dalla lingua, ad esempio: HRESULTs e raccolte [**errorInfo**](errorinfo.md) .

In questa sezione sono inclusi argomenti, descritti nella tabella seguente, in cui vengono illustrate le tecniche per la gestione degli errori nelle applicazioni COM+, le funzionalità di COM+ che influiscono sul comportamento degli errori e suggerimenti per la diagnosi degli errori COM+.



| Argomento                                                                                           | Descrizione                                                                                                                                                 |
|-------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Strategie per la gestione degli errori in COM+](strategies-for-handling-errors-in-com-.md)<br/> | Elenca e descrive le linee guida di base per la gestione degli errori in COM+, incluso il momento in cui usare HRESULTs e le raccolte [**errorInfo**](errorinfo.md) .<br/> |
| [Modalità di modifica dei valori restituiti da COM+](how-com--modifies-return-values.md)<br/>               | Identifica la singola condizione in cui COM+ converte un valore HRESULT standard in un codice di errore COM+ prima di passarlo di nuovo al chiamante.<br/>             |
| [Criteri di isolamento degli errori e FailFast](fault-isolation-and-failfast-policy.md)<br/>       | Mostra in che modo l'isolamento degli errori e i criteri di FailFast influiscono sul comportamento COM+.<br/>                                                                          |
| [Individuazione dell'origine di un errore](finding-the-source-of-an-error.md)<br/>                 | Viene descritto come è possibile diagnosticare l'origine e ottenere una descrizione degli errori dell'applicazione. <br/>                                                       |
| [Interpretazione dei codici di errore](interpreting-error-codes.md)<br/>                             | Identifica il meccanismo di gestione degli errori predominante per Microsoft Visual C++, il linguaggio Java e Microsoft Visual Basic. <br/>                    |
| [Risoluzione dei problemi](troubleshooting.md)<br/>                                               | Fornisce assistenza aggiuntiva per la diagnosi degli errori.<br/>                                                                                             |
| [Contattare il supporto tecnico](contacting-support.md)<br/>                                         | Identifica importanti informazioni di risoluzione dei problemi da fornire quando si contatta il supporto tecnico.<br/>                                                     |



 

Per informazioni dettagliate sulla gestione degli errori associati a vari servizi COM+, vedere le sezioni seguenti:

-   [Velocizzare le transazioni inviando una notifica all'oggetto radice](speeding-transactions-by-notifying-the-root-object.md)
-   [Gestione degli errori](handling-errors-in-queued-components.md) (per i componenti in coda)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Debug di applicazioni COM+](debugging-com--applications.md)
</dt> </dl>

 

 




