---
title: Implementazione del set di proprietà informazioni di riepilogo
description: Quando si implementa un set di proprietà di informazioni di riepilogo per l'archiviazione strutturata, sono disponibili linee guida da seguire.
ms.assetid: e1204de5-b712-4bd5-bffb-6a12ec8d7052
keywords:
- Implementazione del set di proprietà informazioni di riepilogo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69e5ae6208aa5cb7a325d1cccf77f17e969c5b75
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707300"
---
# <a name="implementing-the-summary-information-property-set"></a>Implementazione del set di proprietà informazioni di riepilogo

Quando si implementa un set di proprietà di informazioni di riepilogo per l'archiviazione strutturata, sono disponibili linee guida da seguire.

Di seguito sono riportate le linee guida per l'implementazione [del set di proprietà informazioni di riepilogo](the-summary-information-property-set.md):

-   **PID \_ Il modello** fa riferimento a un documento esterno contenente informazioni sul formato e sullo stile. Il processo con cui si trova il modello è definito dall'implementazione.
-   **PID \_ LASTAUTHOR** è il nome archiviato nelle informazioni utente dall'applicazione. Ad esempio, Mary crea un documento nel computer e lo assegna a John, che lo modifica e lo salva. Mary è l'autore, Giorgio è l'ultimo salvataggio per valore.
-   **PID \_ REVNUMBER** è il numero di volte in cui il comando file/Salva è stato chiamato in questo documento.
-   Ognuno dei valori di data/ora deve essere archiviato in formato UTC (Universal Coordinated Time).
-   **PID \_ CREATE \_ DTM** è una proprietà di sola lettura. Questa proprietà deve essere impostata quando viene creato un documento, ma non deve essere modificata successivamente.
-   Per **l' \_ Anteprima PID**, le applicazioni devono archiviare i dati nel formato **CF \_ DIB** o **CF \_ METAFILEPICT** . **CF \_** È consigliabile usare METAFILEPICT.
-   **PID \_ La sicurezza** è il livello di sicurezza suggerito per il documento. Annotando il livello di sicurezza del documento, un'applicazione diversa dal creatore del documento può modificare l'interfaccia utente per le proprietà. Un'applicazione non deve visualizzare informazioni su un documento protetto da password o abilitare le modifiche apportate Read-Only o documenti bloccati per le annotazioni. Se l'utente tenta di modificare le proprietà, l'applicazione deve avvisare l'utente sulla Read-Only stato consigliato.



| Livello di sicurezza         | Valore |
|------------------------|-------|
| nessuno                   | 0     |
| Protetto da password     | 1     |
| Di sola lettura consigliata  | 2     |
| Applicazione di sola lettura     | 4     |
| Bloccato per le annotazioni | 8     |



 

 

 




