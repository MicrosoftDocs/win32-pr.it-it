---
description: I writer di applicazioni possono apportare modifiche secondarie al codice sorgente per aggiungere operazioni di file e Registro di sistema transazione tramite Gestione transazioni kernel.
ms.assetid: 356c66dc-5ddd-472f-835c-2e2cb019bcfd
title: Utilizzo delle transazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eda967e3c8fe165c3a59de6534c26bc125dfb8dd209be68b5914ea099b0023e7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119146514"
---
# <a name="working-with-transactions"></a>Utilizzo delle transazioni

I writer di applicazioni possono apportare modifiche secondarie al codice sorgente per aggiungere operazioni di file e Registro di sistema transazione tramite Gestione transazioni kernel. In genere, ciò comporta la creazione di una transazione e il passaggio dell'handle ad altre funzioni fornite dalle risorse transazionali, ad esempio [NTFS](/windows/desktop/FileIO/transactional-ntfs-portal) transazionale e il Registro di sistema transazionale.

KTM fornisce all'applicazione meccanismi per partecipare alle transazioni e per scrivere il proprio gestore di risorse transazionale. Sono disponibili funzioni che consentono di creare, gestire e usare quattro classi di oggetti kernel: transazioni, gestori transazioni, gestori di risorse ed integrazioni. Se si usano semplicemente transazioni, è sufficiente usare gli oggetti transazione e usare le funzioni seguenti:

-   [**CreateTransaction**](/windows/desktop/api/KtmW32/nf-ktmw32-createtransaction)
-   [**CommitTransaction**](/windows/desktop/api/Ktmw32/nf-ktmw32-committransaction)
-   [**RollbackTransaction**](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbacktransaction)

Non presupporre mai che una transazione sia attiva. È possibile eseguire il rollback delle transazioni per diversi motivi e in qualsiasi momento.

Windows espone un'interfaccia basata su handle alle risorse di sistema. Per usare un oggetto del sistema operativo, l'applicazione richiede innanzitutto un handle all'oggetto e quindi lo usa nelle chiamate di funzione successive per accedere all'oggetto o modificarlo. Un handle può in genere essere aperto in modalità diverse. La modalità specificata influisce sulla semantica delle chiamate di funzione successive. Ad esempio, un handle di file aperto da una chiamata a [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) con il flag *dwDesiredAccess* impostato su **GENERIC \_ READ** non può essere usato nelle chiamate che modificano il file.

È possibile coordinarsi [con Distributed Transaction Coordinator](/previous-versions/windows/desktop/ms684146(v=vs.85)) in modalità utente, ad esempio SQL o MSMQ, e con le risorse in modalità kernel che usano KTM. Creare prima di tutto una transazione DTC o un oggetto [**System.Transactions,**](/dotnet/api/system.transactions?view=dotnet-plat-ext-3.1) quindi chiamare l'oggetto [**IKernelTransaction,**](/previous-versions/windows/desktop/aa344210(v=vs.85)) da cui è possibile ottenere l'handle KTM. **L'oggetto IKernelTransaction** crea una transazione KTM subordinata alla transazione DTC. Con questo handle è possibile creare gli oggetti transazione, ma segnalare il risultato della transazione usando DTC **o System.Transactions.**

 

 
