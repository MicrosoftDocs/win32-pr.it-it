---
description: Windows Il programma di installazione è integrato con Criteri di restrizione software in Microsoft Windows XP.
ms.assetid: b1e58336-8908-45ee-86f0-81b2314fa77a
title: Windows Programma di installazione e criteri di restrizione software
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e96d1c422b38fd82110cac34953f24be39909eeb64fa2236d3a993925a55c6e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119786561"
---
# <a name="windows-installer-and-software-restriction-policy"></a>Windows Programma di installazione e criteri di restrizione software

Windows Il programma di installazione è integrato con Criteri di restrizione software in Microsoft Windows XP. Criteri di restrizione software è configurabile tramite Criteri di gruppo. Criteri di restrizione software consente a un amministratore di limitare l'esecuzione di file sia agli amministratori che agli utenti non amministratori in base al percorso, all'area URL, all'hash o ai criteri dell'editore. I criteri di restrizione software hanno due livelli: senza restrizioni e non consentito. Il Windows installa solo i pacchetti che possono essere eseguiti a livello senza restrizioni.

È inoltre necessario che le patch o le trasformazioni siano consentite per l'esecuzione a livello senza restrizioni. Se un pacchetto, una patch o una trasformazione è configurato per l'esecuzione a un livello diverso da senza restrizioni, il programma di installazione di Windows visualizza un messaggio di errore e registra una voce nel registro eventi dell'applicazione. I criteri di restrizione software vengono valutati la prima volta che un'applicazione viene installata, quando viene applicata una nuova patch e quando il pacchetto di installazione viene ri-memorizzato nella cache.

Se un pacchetto, una patch o una trasformazione è limitato, il programma di installazione Windows visualizza un messaggio di errore e scrive una [voce di](event-logging.md) registrazione eventi nel registro eventi dell'applicazione. I criteri di restrizione software vengono valutati la prima volta che un'applicazione viene installata, quando viene applicata una nuova patch e quando il pacchetto di installazione viene ri-memorizzato nella cache.

Per altre informazioni sui criteri di restrizione software, consultare la documentazione del prodotto ed [eseguire una ricerca nel sito TechNet.](https://www.microsoft.com/technet/sitemap.mspx)

 

 



