---
description: Un oggetto prestazione è un'entità per la quale sono disponibili i dati sulle prestazioni.
ms.assetid: 97b9c9ec-e758-4928-b3fa-90d220bca5fb
title: Progettazione di oggetti e contatori
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9556882f5dd6c323697d9d41fa80727895550a5d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967514"
---
# <a name="object-and-counter-design"></a>Progettazione di oggetti e contatori

Un oggetto prestazione è un'entità per la quale sono disponibili i dati sulle prestazioni. I contatori delle prestazioni definiscono il tipo di dati disponibili per un oggetto prestazioni. Un'applicazione può fornire informazioni per più oggetti prestazione. Gli oggetti prestazioni possono contenere contatori a istanza singola o più contatori di istanza. Un singolo oggetto istanza restituisce un singolo set di valori del contatore.

Un oggetto a più istanze restituisce un'istanza dell'oggetto per ogni occorrenza dell'oggetto controllato dall'applicazione. Ad esempio, un'applicazione SCSI può definire un oggetto unità con due contatori, ad esempio byte letti e byte scritti. Quando il consumer esegue una query sull'oggetto, la DLL di prestazioni restituisce un'istanza dell'oggetto per ogni unità controllata dall'applicazione.

Dopo aver deciso se l'oggetto supporta una sola istanza o più istanze, è necessario stabilire il tipo di contatori che si desidera venga fornito dall'oggetto. È ad esempio possibile specificare i valori dei contatori visualizzati come valori non elaborati, come frequenze o come percentuali.

Per un elenco dei tipi di contatori predefiniti da scegliere, vedere la sezione relativa ai tipi di contatore del [Kit di distribuzione di Windows Server 2003](/previous-versions/windows/it-pro/windows-server-2003/cc776490(v=ws.10)). A seconda del tipo di contatore, è possibile fornire semplicemente i dati non elaborati oppure è anche necessario fornire informazioni su tempo e frequenza e dati del contatore aggiuntivi utilizzati dal consumer per calcolare un valore visualizzabile.

Il metodo utilizzato per raccogliere i dati può essere semplice come incrementare un contatore ogni volta che viene chiamata una determinata routine nell'applicazione oppure può includere calcoli che richiedono molto tempo. I contatori e i timer devono essere incrementati e non devono mai essere cancellati. È possibile eseguire il wrapping dei contatori, purché non vengano inclusi due volte tra campionati dal consumer. L'applicazione può raccogliere e archiviare i dati durante la normale esecuzione, purché non influisca sulle prestazioni.

Per alcuni tipi di dati, può essere più efficiente o appropriato raccogliere i dati su richiesta. In questa situazione, la DLL di prestazioni deve comunicare con l'applicazione che i dati sono stati richiesti. Per i dati che sono costosi da raccogliere (in termini di tempo del processore o utilizzo della memoria), è consigliabile raccogliere i dati solo quando il consumer richiede i dati **costosi** . Questo consente a un consumer di richiedere periodicamente i dati per tutti i contatori che non sono costosi. I dati possono essere richiesti solo quando necessario. Lo strumento prestazioni non raccoglie i dati **costosi** .

 

 
