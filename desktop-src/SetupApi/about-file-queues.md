---
description: Una coda di file è un elenco di operazioni di file elaborate in una sola volta. Le operazioni sui file nella coda possono essere operazioni di copia, ridenominazione o eliminazione. La coda file organizza le operazioni sui file in base al tipo, creando la copia, la ridenominazione e l'eliminazione delle code secondarie.
ms.assetid: 9ad42c37-1d6b-4f1b-8173-629e2d3678f2
title: Informazioni sulle code di file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af441a1195bad5116306ca93cfbe658be5b3efc6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306521"
---
# <a name="about-file-queues"></a>Informazioni sulle code di file

Una coda di file è un elenco di operazioni di file elaborate in una sola volta. Le operazioni sui file nella coda possono essere operazioni di copia, ridenominazione o eliminazione. La coda file organizza le operazioni sui file in base al tipo, creando la copia, la ridenominazione e l'eliminazione delle code secondarie.

Queste operazioni possono essere inviate alla coda in qualsiasi ordine e il processo di Accodamento non deve essere contiguo. Quando viene eseguito il commit della coda, la funzione [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) esegue le operazioni sui file in ordine del tipo di operazione.

In genere, tutte le operazioni sui file necessarie per un'intera installazione vengono accodate alla coda di file e quindi elaborate in un singolo batch quando viene eseguito il commit della coda.

Un vantaggio di accodamento delle operazioni sui file rispetto all'installazione dei file sezione per sezione da un file INF è che è possibile semplificare il processo di installazione. Anziché dover ottenere informazioni dall'utente per ogni sezione da installare, è possibile ottenere informazioni sull'installazione dall'utente per tutti i file da installare durante la compilazione della coda. In questo modo l'utente può proseguire con altre attività mentre le operazioni di copia che richiedono molto tempo vengono elaborate dalla funzione [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) .

Un altro vantaggio delle code di file è che è possibile tenere traccia dello stato di avanzamento dell'installazione nel suo complesso. Quando si installa la sezione per sezione da un file INF, gli indicatori di stato, ad esempio le barre di stato, possono tenere traccia solo della sezione INF corrente. Quando viene installata la sezione successiva, l'indicatore di stato viene riavviato. Con una coda, il numero totale di file da elaborare durante l'intera installazione è noto prima del commit della coda, quindi è possibile generare un indicatore di stato per tenere traccia dell'intera installazione.

Per altre informazioni, vedere i seguenti argomenti:

-   [Ordine di impegno della coda](order-of-queue-commitment.md)
-   [Notifiche della coda](queue-notifications.md)

 

 



