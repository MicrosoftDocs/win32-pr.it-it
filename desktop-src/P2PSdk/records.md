---
description: I record sono un modo per comunicare tra i nodi di un grafico o i membri di un gruppo.
ms.assetid: f4c0869f-f147-4c2b-9418-3b407e22cb16
title: Record
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9c2d3c5ae3bd80bc0b3c0ca100155fc8efd7c71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968014"
---
# <a name="records"></a>Record

I record sono un modo per comunicare tra i nodi di un grafico o i membri di un gruppo. Un record è costituito dalle due parti seguenti:

-   Intestazione record
-   Contenuto dati opaco specifico

L'intestazione contiene informazioni sul record, tra cui la versione, l'autore e il tipo di dati da pubblicare. L'intestazione contiene anche un campo degli attributi XML che consente alle applicazioni di aggiungere attributi nome-valore che descrivono i dati e di cercare in modo efficiente nel database di record record specifici che sono stati pubblicati in precedenza. Il contenuto è i dati definiti dall'applicazione ed è opaco per l'infrastruttura peer.

Quando viene pubblicato un record, esso (intestazione e dati) viene sovraccaricato nel grafico o nel gruppo. I peer sincronizzati ricevono questi dati e li archiviano in un database locale. I peer non sincronizzati e offline ricevono i dati la volta successiva che si connettono e si sincronizzano con il grafo o il gruppo peer.

Per informazioni sull'utilizzo dei record, vedere gli argomenti seguenti:

-   [Registrare le dipendenze](record-dependencies.md)
-   [Gestione dei record](record-management.md)
-   [Schema attributo record](record-attribute-schema.md)
-   [Formato della query di ricerca record](record-search-query-format.md)

 

 



