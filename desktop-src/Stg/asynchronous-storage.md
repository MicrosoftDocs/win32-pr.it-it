---
title: Archiviazione asincrona
description: L'archiviazione asincrona migliora la specifica di archiviazione strutturata COM per supportare il download asincrono di oggetti di archiviazione su reti a latenza elevata e a collegamento lento, ad esempio Internet.
ms.assetid: 12b97059-2c8c-4712-8a76-03c3ce7094a0
keywords:
- Archiviazione strutturata Strctd STG, archiviazione asincrona
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39dd1d739223fb07c72de6c63ee173c316a132e0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473795"
---
# <a name="asynchronous-storage"></a>Archiviazione asincrona

L'archiviazione asincrona migliora la specifica di archiviazione strutturata COM per supportare il download asincrono di oggetti di archiviazione su reti a latenza elevata e a collegamento lento, ad esempio Internet. L'archiviazione asincrona consente alle applicazioni nuove e legacy che usano file composti di eseguire in modo efficiente il rendering del contenuto in caso di accesso tramite protocolli Internet esistenti. Una singola richiesta a un server di World Wide Web attiva il download degli oggetti annidati contenuti in una pagina Web, eliminando la necessità di richiedere separatamente ogni oggetto. Un meccanismo di download e accesso asincrono consente a un'applicazione di eseguire il rendering della prima pagina di dati prima della ricezione di tutti i dati. L'ordine esatto in cui gli elementi di una pagina diventano disponibili può essere specificato dal server di pubblicazione Web e non dipende da fattori casuali della topologia di rete e della disponibilità del server.

L'archiviazione asincrona funziona insieme ai moniker asincroni per fornire un comportamento di associazione asincrono completo. Per ulteriori informazioni sui moniker asincroni, vedere Microsoft ActiveX Software Development Kit. Un moniker asincrono specifico del protocollo attiva l'operazione di associazione e imposta i componenti richiesti. In Internet, questo moniker può essere analizzato da un URL per l'associazione a un oggetto o a una risorsa di archiviazione. Se la destinazione dell'operazione di associazione è un oggetto persistente, la chiamata a [**IMoniker:: BindToStorage**](/windows/win32/api/objidl/nf-objidl-imoniker-bindtostorage) restituisce un oggetto di archiviazione asincrono.

> [!Note]  
> La versione corrente dei moniker URL Microsoft non supporta l'archiviazione asincrona.

 

Un client moniker asincrono richiede il binding asincrono implementando un oggetto callback di stato bind e la registrazione con il contesto di associazione. L'oggetto di callback bind-status espone l'interfaccia [**IBindStatusCallback**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775060(v=vs.85)) , che consente al client di specificare le preferenze di binding e di ricevere notifiche di stato e di disponibilità dei dati globali durante un'operazione di associazione. L'implementazione asincrona dei file composti fornisce un punto di connessione per [**IProgressNotify**](/windows/win32/api/objidl/nn-objidl-iprogressnotify), che i client possono usare per ricevere notifiche di disponibilità specifiche sui singoli flussi.

 

 