---
description: Gestione degli errori in COM+ CRM
ms.assetid: 9de31fb5-31e9-494a-b61f-87bcff0d5085
title: Gestione degli errori in COM+ CRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4aba2b5c4541485433a85fe01fee7870c2e43f62
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483452"
---
# <a name="error-handling-in-the-com-crm"></a>Gestione degli errori in COM+ CRM

Le applicazioni server COM+ implementano un criterio FailFast. Se viene rilevato un errore interno grave, il processo dell'applicazione server viene chiuso e viene scritto un messaggio di errore nel registro eventi di Windows. Ciò consente di rilevare rapidamente i problemi ed è possibile a causa della protezione dei dati dell'applicazione da parte dell'elaborazione delle transazioni. Controllare sempre nel registro eventi di Windows eventuali errori del CRM, durante lo sviluppo o durante la distribuzione finale.

Errori di base nell'uso delle interfacce CRM, ad esempio argomenti non validi o errori di sequenza (ad esempio, il tentativo di scrivere un record di log prima di registrare il compensatore CRM), restituire i codici di errore e non attivare FailFast. Per lo sviluppo di CRM, è possibile scegliere di impostare la chiave del registro di sistema VTRACE1 (vedere [le impostazioni del registro di sistema com+ CRM](com--crm-registry-settings.md)), che consente di visualizzare un messaggio nella finestra di output del debugger per ogni errore.

Possono verificarsi anche errori temporanei. Questi errori sono in genere causati da condizioni di temporizzazione e comportano la restituzione di un codice di errore. Lo sviluppatore di CRM deve assicurarsi che queste condizioni di errore vengano gestite. Ad esempio, durante la scrittura di un record di log, è possibile che la transazione venga interrotta a causa di un timeout. Il metodo restituisce quindi un errore, che il chiamante deve verificare e gestire in modo appropriato.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Concetti Gestione risorse di compensazione COM+](com--compensating-resource-manager-concepts.md)
</dt> </dl>

 

 



