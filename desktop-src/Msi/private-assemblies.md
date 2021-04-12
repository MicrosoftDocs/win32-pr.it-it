---
description: Un assembly Win32 può essere installato come assembly privato ed essere disponibile esclusivamente per l'uso da parte di un'applicazione. Gli assembly privati devono essere installati da un pacchetto di Windows Installer usato per installare o aggiornare un'applicazione.
ms.assetid: 4c6dac5f-fdd3-4125-b54a-74941ee6b3b4
title: Assembly privati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1073426e080cc4b8b30358ce26feb99515abb185
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104231860"
---
# <a name="private-assemblies"></a>Assembly privati

Un assembly Win32 può essere installato come assembly privato ed essere disponibile esclusivamente per l'uso da parte di un'applicazione. Gli assembly privati devono essere installati da un pacchetto di Windows Installer usato per installare o aggiornare un'applicazione.

In Windows XP gli assembly privati vengono installati come [assembly side-by-side](side-by-side-assemblies.md). Il Windows Installer installa gli assembly side-by-side privati in una cartella privata per l'applicazione. Generalmente la cartella che contiene il file eseguibile delle applicazioni. La dipendenza dell'applicazione nell'assembly privato viene specificata in un file manifesto dell'applicazione. Per altre informazioni, vedere [applicazioni isolate e assembly affiancati](../sbscs/isolated-applications-and-side-by-side-assemblies-portal.md).

Nei sistemi operativi precedenti a Windows XP, una copia dell'assembly privato e di un file con estensione local viene installata in una cartella privata per l'utilizzo esclusivo dell'applicazione. Una versione dell'assembly viene anche registrata a livello globale nel sistema e disponibile per qualsiasi applicazione associata. La versione globale dell'assembly può essere la versione installata con l'applicazione o una versione precedente. La versione globale è determinata dalle stesse regole utilizzate dai [componenti isolati](isolated-components.md).

Si noti che il Windows Installer non è in grado di installare un assembly privato in una posizione con un percorso contenente più di 234 caratteri, incluso il carattere null di terminazione.

 

 
