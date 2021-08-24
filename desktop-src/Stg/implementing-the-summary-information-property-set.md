---
title: Implementazione del set di proprietà Summary Information
description: Esistono linee guida da seguire quando si implementa un set di proprietà di informazioni di riepilogo per l'Archiviazione.
ms.assetid: e1204de5-b712-4bd5-bffb-6a12ec8d7052
keywords:
- Implementazione del set di proprietà Summary Information
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbe847d9a7353074727c94250d0f1ec1fec2194b5b7d250099464a86667861f6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119796911"
---
# <a name="implementing-the-summary-information-property-set"></a>Implementazione del set di proprietà Summary Information

Esistono linee guida da seguire quando si implementa un set di proprietà di informazioni di riepilogo per l'Archiviazione.

Di seguito sono riportate le linee guida per l'implementazione [del set di proprietà Riepilogo informazioni](the-summary-information-property-set.md):

-   **PID \_ TEMPLATE** fa riferimento a un documento esterno contenente informazioni sul formato e sullo stile. Il processo in base al quale si trova il modello è definito dall'implementazione.
-   **PID \_ LASTAUTHOR è** il nome archiviato in Informazioni utente dall'applicazione. Ad esempio, Maria crea un documento nel computer e lo assegna a Giorgio, che lo modifica e lo salva. Maria è l'autore, John è l'ultimo salvato per valore.
-   **PID \_ REVNUMBER è** il numero di volte in cui è stato chiamato il comando File/Salva in questo documento.
-   Ognuno dei valori di data/ora deve essere archiviato in formato UTC (Universal Coordinated Time).
-   **PID \_ CREATE \_ DTM** è una proprietà di sola lettura. Questa proprietà deve essere impostata quando viene creato un documento, ma non deve essere modificata successivamente.
-   Per **PID \_ THUMBNAIL,** le applicazioni devono archiviare i dati in **formato CF \_ DIB** o **CF \_ METAFILEPICT.** **CF \_ È consigliabile utilizzare METAFILEPICT.**
-   **PID \_ SECURITY** è il livello di sicurezza suggerito per il documento. Notando il livello di sicurezza nel documento, un'applicazione diversa dall'autore del documento può modificare l'interfaccia utente in base alle proprietà. Un'applicazione non deve visualizzare informazioni su un documento protetto da password o abilitare le modifiche ai documenti Read-Only o Locked-for-Annotations. Se l'utente tenta di modificare le proprietà, l'applicazione deve avvisare l'utente Read-Only stato Consigliato.



| Livello di sicurezza         | Valore |
|------------------------|-------|
| nessuno                   | 0     |
| Protetto da password     | 1     |
| Consigliato in sola lettura  | 2     |
| Applicazione in sola lettura     | 4     |
| Bloccato per le annotazioni | 8     |



 

 

 




