---
description: Gestire la condivisione degli assembly e il controllo delle versioni delle DLL nell'archivio di assembly affiancato dei sistemi dai programmi. Scrivere manifesti di assembly e descrivere in autonomia le applicazioni per la condivisione degli assembly e il reindirizzamento delle dll.
ms.assetid: 2f841eb6-9a6c-4c9b-b057-a3da6cd6b0b0
title: Applicazioni isolate e assembly affiancati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59abfbd5392040856c66ef9eb786b66d2a84500f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128822"
---
# <a name="isolated-applications-and-side-by-side-assemblies"></a>Applicazioni isolate e assembly affiancati

## <a name="purpose"></a>Scopo

Le applicazioni isolate e gli assembly affiancati sono una soluzione Microsoft Windows che consente di ridurre i conflitti di controllo delle versioni nelle applicazioni client Windows. Con Windows, gli sviluppatori di applicazioni possono compilare applicazioni isolate completamente autodescrittive e non interessate dalle modifiche apportate al registro di sistema, ad altre applicazioni o ad altre versioni di assembly in esecuzione nel sistema. Gli autori e gli amministratori di applicazioni possono utilizzare i manifesti per gestire la condivisione di assembly affiancati dopo la distribuzione in base a un'applicazione o globale. I clienti traggono vantaggio da applicazioni isolate più stabili e aggiornate in modo più affidabile.

## <a name="where-applicable"></a>Se applicabile

Per lo sviluppo di applicazioni che condividono in modo sicuro gli assembly del sistema operativo, è possibile usare applicazioni isolate e condivisione di assembly affiancati. Gli sviluppatori possono utilizzare questa tecnologia per correggere i conflitti di controllo delle versioni DLL causati da una versione incompatibile di un assembly condiviso.

Se l'applicazione deve ottenere costantemente la versione di un componente testato, è possibile isolare l'applicazione in modo che venga sempre eseguita con la versione testata del componente nel computer dell'utente.

Le applicazioni isolate e gli assembly affiancati sono progettati per lo sviluppo di applicazioni di tipo desktop.

## <a name="developer-audience"></a>Sviluppatori

Questa documentazione è destinata principalmente a sviluppatori di software, sviluppatori di applicazioni e amministratori di rete:

-   Sviluppatori di software che desiderano creare applicazioni isolate che utilizzeranno gli assembly affiancati resi disponibili da Microsoft e altri autori di assembly affiancati.
-   Sviluppatori di applicazioni interessati alla creazione di assembly affiancati per isolare le applicazioni.
-   Amministratori di rete che desiderano ulteriori informazioni sulle applicazioni isolate.

Come riferimento principale per la condivisione di assembly affiancati e le applicazioni isolate, in questa documentazione vengono fornite informazioni generali sulla creazione di manifesti e assembly affiancati, sull'installazione di applicazioni isolate e assembly affiancati e sull'utilizzo dell'API del contesto di attivazione.

## <a name="run-time-requirements"></a>Requisiti di runtime

Windows Server 2003 e versioni successive o Windows XP e versioni successive sono necessari per usare gli assembly affiancati e i manifesti per isolare le applicazioni e usare l'API del contesto di attivazione.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                         | Descrizione                                                                    |
|---------------------------------------------------------------|--------------------------------------------------------------------------------|
| [Riferimento](side-by-side-assemblies-reference.md)<br/> | Documentazione delle applicazioni isolate e degli assembly affiancati.<br/> |



 

 

 




