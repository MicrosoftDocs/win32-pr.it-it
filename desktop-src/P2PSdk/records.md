---
description: I record sono un modo per comunicare tra i nodi di un grafo o i membri di un gruppo.
ms.assetid: f4c0869f-f147-4c2b-9418-3b407e22cb16
title: Record
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe3066bb6d309ce70a790947f002e1a74eb329c862ffcb0ef2c1766ca315323f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119675001"
---
# <a name="records"></a>Record

I record sono un modo per comunicare tra i nodi di un grafo o i membri di un gruppo. Un record è costituito dalle due parti seguenti:

-   Intestazione del record
-   Contenuto specifico dei dati opachi

L'intestazione contiene informazioni sul record, tra cui la versione, l'autore e il tipo di dati da pubblicare. L'intestazione contiene anche un campo attributi XML che consente alle applicazioni di aggiungere attributi nome-valore che descrivono i dati e di cercare in modo efficiente nel database dei record record specifici pubblicati in precedenza. Il contenuto è dato dai dati definiti dall'applicazione ed è opaco per l'infrastruttura peer.

Quando viene pubblicato, un record (sia intestazione che dati) viene inondato in tutto il grafico o nel gruppo. I peer sincronizzati ricevono questi dati e lo archiviano in un database locale. I peer non sincronizzati e offline ricevono i dati alla successiva connessione e sincronizzazione con il grafo o il gruppo peer.

Per informazioni sull'uso dei record, vedere gli argomenti seguenti:

-   [Registrare le dipendenze](record-dependencies.md)
-   [Gestione dei record](record-management.md)
-   [Schema dell'attributo record](record-attribute-schema.md)
-   [Formato query di ricerca record](record-search-query-format.md)

 

 



