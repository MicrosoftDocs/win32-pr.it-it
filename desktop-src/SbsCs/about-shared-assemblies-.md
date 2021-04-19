---
description: Un assembly condiviso è un assembly disponibile per l'utilizzo da parte di più applicazioni nel computer.
ms.assetid: E42688E0-83D8-4C64-98A8-1BE82E4348FA
title: Informazioni sugli assembly condivisi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed044f2c0f6b8e8e04927035991da651b4c26674
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311620"
---
# <a name="about-shared-assemblies"></a>Informazioni sugli assembly condivisi

Un assembly condiviso è un assembly disponibile per l'utilizzo da parte di più applicazioni nel computer. In Windows Vista e Windows XP è possibile installare [assembly side-by-side](about-side-by-side-assemblies-.md) come assembly condivisi. Gli assembly affiancati condivisi non sono registrati a livello globale nel sistema, ma sono disponibili a livello globale per le applicazioni che specificano una dipendenza dall'assembly nei [manifesti](manifests.md). Più versioni di assembly side-by-side possono essere condivise da diverse applicazioni in esecuzione nello stesso momento. Per ulteriori informazioni, vedere [informazioni sulle applicazioni isolate e gli assembly affiancati](about-isolated-applications-and-side-by-side-assemblies.md). Ad esempio, gli [assembly affiancati Microsoft supportati](supported-microsoft-side-by-side-assemblies.md) forniti con Windows XP vengono in genere utilizzati come assembly condivisi da più applicazioni.

Gli assembly affiancati condivisi vengono installati nella cartella WinSxS. Gli autori di assembly, le applicazioni e gli amministratori possono modificare la versione delle dipendenze dell'assembly affiancato dopo la distribuzione tramite la [configurazione](configuration.md). Gli assembly affiancati condivisi possono essere installati da un aggiornamento del sistema operativo o da un pacchetto di Windows Installer per l'installazione o l'aggiornamento di un'applicazione. Per ulteriori informazioni, vedere [installazione di assembly Win32](../msi/installation-of-win32-assemblies.md).

Prima di Windows XP, gli assembly condivisi venivano registrati a livello globale e installati nella cartella di sistema di Windows. In questo caso, l'ultima versione installata dell'assembly è disponibile per tutte le applicazioni associate. Un assembly affiancato può essere installato anche come assembly privato per l'uso esclusivo di un'applicazione. Per ulteriori informazioni, vedere [assembly privati](/windows/desktop/Msi/private-assemblies).

 

 
