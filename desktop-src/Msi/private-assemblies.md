---
description: Un assembly Win32 può essere installato come assembly privato ed essere disponibile esclusivamente per l'uso da parte di un'applicazione. Gli assembly privati devono essere installati da un pacchetto Windows Installer usato per installare o aggiornare un'applicazione.
ms.assetid: 4c6dac5f-fdd3-4125-b54a-74941ee6b3b4
title: Assembly privati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45cc9bd9c9f4c5230dcb24ed7059f6817d4c5f3c7cfdeb4b7cfd25d95ca2a3eb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119327846"
---
# <a name="private-assemblies"></a>Assembly privati

Un assembly Win32 può essere installato come assembly privato ed essere disponibile esclusivamente per l'uso da parte di un'applicazione. Gli assembly privati devono essere installati da un pacchetto Windows Installer usato per installare o aggiornare un'applicazione.

In Windows XP gli assembly privati vengono installati come [assembly side-by-side.](side-by-side-assemblies.md) Il Windows installa assembly side-by-side privati in una cartella privata dell'applicazione. In genere la cartella che contiene il file eseguibile delle applicazioni. La dipendenza dell'applicazione dall'assembly privato viene specificata in un file manifesto dell'applicazione. Per altre informazioni, vedere Applicazioni isolate e [assembly side-by-side.](../sbscs/isolated-applications-and-side-by-side-assemblies-portal.md)

Nei sistemi operativi precedenti a Windows XP, una copia dell'assembly privato e un file con estensione local vengono installati in una cartella privata per l'uso esclusivo dell'applicazione. Anche una versione dell'assembly viene registrata a livello globale nel sistema e disponibile per qualsiasi applicazione associata ad esso. La versione globale dell'assembly può essere la versione installata con l'applicazione o una versione precedente. La versione globale è determinata dalle stesse regole usate da [Isolated Components.](isolated-components.md)

Si noti che Windows Installer non può installare un assembly privato in un percorso contenente più di 234 caratteri, incluso il carattere null di terminazione.

 

 
