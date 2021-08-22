---
description: Un assembly condiviso è un assembly disponibile per l'utilizzo da parte di più applicazioni nel computer.
ms.assetid: E42688E0-83D8-4C64-98A8-1BE82E4348FA
title: Informazioni sugli assembly condivisi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a5db7f10ea5ffa6e04fd5cd905262eb026b4ca4c24309ffd4c53cb10f9df00b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119142624"
---
# <a name="about-shared-assemblies"></a>Informazioni sugli assembly condivisi

Un assembly condiviso è un assembly disponibile per l'utilizzo da parte di più applicazioni nel computer. In Windows Vista Windows XP, gli assembly [side-by-side](about-side-by-side-assemblies-.md) possono essere installati come assembly condivisi. Gli assembly side-by-side condivisi non vengono registrati a livello globale nel sistema, ma sono disponibili a livello globale per le applicazioni che specificano una dipendenza dall'assembly nei [manifesti](manifests.md). Più versioni di assembly side-by-side possono essere condivise da applicazioni diverse in esecuzione contemporaneamente. Per altre informazioni, vedere [Informazioni sulle applicazioni isolate e sugli assembly side-by-side.](about-isolated-applications-and-side-by-side-assemblies.md) Ad esempio, gli [assembly side-by-side Microsoft](supported-microsoft-side-by-side-assemblies.md) supportati forniti con Windows XP vengono in genere usati come assembly condivisi da più applicazioni.

Gli assembly side-by-side condivisi vengono installati nella cartella WinSxS. Gli autori di assembly, le applicazioni e gli amministratori possono modificare la versione delle dipendenze degli assembly side-by-side dopo la distribuzione tramite la [configurazione](configuration.md). Gli assembly side-by-side condivisi possono essere installati da un aggiornamento del sistema operativo o da un pacchetto di Windows Installer che installa o aggiorna un'applicazione. Per altre informazioni, vedere [Installazione di assembly Win32.](../msi/installation-of-win32-assemblies.md)

Prima di Windows XP, gli assembly condivisi venivano registrati a livello globale e installati nella Windows System. In questo caso, la versione installata più recente dell'assembly è disponibile per qualsiasi applicazione associata. Un assembly side-by-side può anche essere installato come assembly privato per l'uso esclusivo di un'applicazione. Per ulteriori informazioni, vedere [assembly privati](/windows/desktop/Msi/private-assemblies).

 

 
