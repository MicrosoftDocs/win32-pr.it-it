---
description: Windows Installer è integrato con i criteri di restrizione software in Microsoft Windows XP.
ms.assetid: b1e58336-8908-45ee-86f0-81b2314fa77a
title: Criteri di restrizione software e Windows Installer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b080a1ed9a1396f4ac212e73d1fda6e2719bf40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314193"
---
# <a name="windows-installer-and-software-restriction-policy"></a>Criteri di restrizione software e Windows Installer

Windows Installer è integrato con i criteri di restrizione software in Microsoft Windows XP. I criteri di restrizione software possono essere configurati tramite criteri di gruppo. I criteri di restrizione software consentono a un amministratore di impedire agli amministratori e agli utenti non amministratori di eseguire file in base ai criteri percorso, zona URL, hash o editore. I criteri di restrizione software hanno due livelli: senza restrizioni e non consentiti. Il Windows Installer installa solo i pacchetti di cui è consentita l'esecuzione al livello Unrestricted.

È inoltre necessario consentire l'esecuzione di patch o trasformazioni a livello illimitato. Se un pacchetto, una patch o una trasformazione è configurata per l'esecuzione a un livello diverso da Unrestricted, il Windows Installer Visualizza un messaggio di errore e registra una voce nel registro eventi dell'applicazione. I criteri di restrizione software vengono valutati la prima volta che un'applicazione viene installata, quando viene applicata una nuova patch e quando il pacchetto di installazione viene nuovamente memorizzato nella cache.

Se un pacchetto, una patch o una trasformazione è limitata, nel Windows Installer viene visualizzato un messaggio di errore e viene scritta una voce di [registrazione eventi](event-logging.md) nel registro eventi dell'applicazione. I criteri di restrizione software vengono valutati la prima volta che un'applicazione viene installata, quando viene applicata una nuova patch e quando il pacchetto di installazione viene nuovamente memorizzato nella cache.

Per ulteriori informazioni sui criteri di restrizione software, consultare la documentazione del prodotto e [cercare il sito TechNet](https://www.microsoft.com/technet/sitemap.mspx).

 

 



