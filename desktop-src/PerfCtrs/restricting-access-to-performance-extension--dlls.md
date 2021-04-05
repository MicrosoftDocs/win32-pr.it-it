---
description: A partire da Windows Server 2003, il gruppo Performance Monitor Users e il gruppo Performance Log Users sono stati resi disponibili per gli sviluppatori e gli utenti delle DLL di prestazioni e le funzioni API PDH (Performance Data Helper).
ms.assetid: 423359be-9d41-4a5f-91cd-f6d7a6a91d9d
title: Limitazione dell'accesso alle DLL dell'estensione per le prestazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd433cad68ec3e50f6b17994da98164e2ae9f237
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881737"
---
# <a name="restricting-access-to-performance-extension-dlls"></a>Limitazione dell'accesso alle DLL dell'estensione per le prestazioni

A partire da Windows Server 2003, il gruppo Performance Monitor Users e il gruppo Performance Log Users sono stati resi disponibili per gli sviluppatori e gli utenti delle DLL di prestazioni e le funzioni API PDH (Performance Data Helper). Questi gruppi di sicurezza delle prestazioni devono essere utilizzati dagli amministratori di sistema per limitare l'accesso alle informazioni esposte dalle DLL delle prestazioni a un elenco specifico di utenti.

Il gruppo Performance Monitor Users consente di includere utenti che visualizzano i dati dei contatori e non registrano i dati del contatore utilizzando il servizio Avvisi e registri di prestazioni. Il gruppo Performance Log Users deve includere utenti che dispongono dell'autorizzazione per utilizzare i registri di prestazioni e il servizio avvisi per registrare i contatori nel server locale o remoto. I privilegi di questo gruppo includono anche la creazione di file di log in sistemi locali o remoti, l'utilizzo del servizio avvisi e l'esecuzione di programmi come parte del servizio.

Si noti che questi gruppi di sicurezza delle prestazioni non sono da soli un meccanismo di restrizione dell'accesso. Per eseguire questa operazione, è necessario usare questi gruppi con il modello di controllo di accesso agli oggetti di Windows.

La maggior parte delle applicazioni comunica con la DLL di prestazioni tramite un meccanismo IPC, in genere memoria condivisa. Pertanto, è possibile aggiungere i membri di un gruppo di sicurezza delle prestazioni al descrittore di sicurezza dell'oggetto Shared Memory per limitare l'accesso alla DLL a tali membri del gruppo di sicurezza. Quando si esegue questa operazione, è necessario aggiungere anche i membri del gruppo al descrittore di sicurezza degli oggetti di sistema a cui accede la DLL per le prestazioni per fornire dati del contatore, ad esempio file di log e cartelle. Per informazioni più dettagliate sull'aggiunta di ACL ai descrittori di sicurezza degli oggetti, vedere [modifica dell'ACL di un oggetto](/windows/desktop/SecAuthZ/modifying-the-acls-of-an-object-in-c--).

Un altro metodo che è possibile utilizzare per modificare le informazioni ACL del descrittore di sicurezza di un oggetto di sistema IPC consiste nel specificare i membri dell'elenco dei gruppi di sicurezza delle prestazioni con il linguaggio SDDL (Security Descriptor Definition Language) e chiamare [**ConvertStringSecurityDescriptorToSecurityDescriptor ha**](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) per creare il descrittore di sicurezza. Questo descrittore di sicurezza viene quindi collegato all'oggetto di sistema IPC. Di seguito viene illustrata una stringa SDDL che include il gruppo Performance Monitor Users, MU e il gruppo Performance Log Users, LU.

``` syntax
D:(A;OICI;GA;;;SY)(A;OICI;GA;;;BA)(A;OICI;FRFWFXSDRC;;;NS)(A;OICI;FRFWFXSDRC;;;LU)(A;OICI;FRFX;;;MU) 
```

 

 
