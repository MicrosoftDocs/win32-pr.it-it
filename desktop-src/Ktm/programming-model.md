---
description: Gli sviluppatori di applicazioni possono apportare modifiche minime al codice sorgente per aggiungere operazioni di file e registro di sistema transazionali mediante gestione transazioni kernel.
ms.assetid: 356c66dc-5ddd-472f-835c-2e2cb019bcfd
title: Utilizzo delle transazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 255e40fb38ca4bfb24acdce717f133dbcf0c76f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882417"
---
# <a name="working-with-transactions"></a>Utilizzo delle transazioni

Gli sviluppatori di applicazioni possono apportare modifiche minime al codice sorgente per aggiungere operazioni di file e registro di sistema transazionali mediante gestione transazioni kernel. In genere, ciò comporta la creazione di una transazione e il passaggio dell'handle ad altre funzioni fornite dalle risorse transazionali, ad esempio [transazionale NTFS](/windows/desktop/FileIO/transactional-ntfs-portal) e il registro di sistema transazionale.

KTM fornisce meccanismi che consentono all'applicazione di partecipare alle transazioni e di scrivere il proprio gestore di risorse transazionale. Sono disponibili funzioni che consentono di creare, gestire e utilizzare quattro classi di oggetti kernel: transazioni, gestori transazioni, gestori di risorse e integrazioni. Se si utilizzano semplicemente le transazioni, è necessario utilizzare solo gli oggetti transazione e utilizzare le funzioni seguenti:

-   [**CreateTransaction**](/windows/desktop/api/KtmW32/nf-ktmw32-createtransaction)
-   [**CommitTransaction**](/windows/desktop/api/Ktmw32/nf-ktmw32-committransaction)
-   [**RollbackTransaction**](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbacktransaction)

Non presupporre che una transazione sia attiva. È possibile eseguire il rollback delle transazioni per diversi motivi e in qualsiasi momento.

Windows espone un'interfaccia basata su handle per le risorse di sistema. Per usare un oggetto sistema operativo, l'applicazione richiede prima di tutto un handle all'oggetto, quindi usa questo handle nelle chiamate di funzione successive per accedere o modificare l'oggetto. Un handle può in genere essere aperto in modalità diverse. la modalità specificata influiscono sulla semantica delle chiamate di funzione successive. Un handle di file aperto da una chiamata a [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) con il flag *DwDesiredAccess* impostato su **Generic \_ Read** , ad esempio, non può essere utilizzato nelle chiamate che modificano il file.

È possibile coordinare con [Distributed Transaction Coordinator](/previous-versions/windows/desktop/ms684146(v=vs.85)) risorse in modalità utente, ad esempio SQL o MSMQ, e con risorse in modalità kernel che usano la KTM. Per prima cosa, creare una transazione DTC o un oggetto [**System. Transactions**](/dotnet/api/system.transactions?view=dotnet-plat-ext-3.1) , quindi chiamare l'oggetto [**IKernelTransaction**](/previous-versions/windows/desktop/aa344210(v=vs.85)) da cui è possibile ottenere l'handle KTM. L'oggetto **IKernelTransaction** crea una transazione KTM subordinata alla transazione DTC. Con questo handle è possibile creare gli oggetti transazionali, ma segnalare il risultato della transazione utilizzando DTC o **System. Transactions**.

 

 
