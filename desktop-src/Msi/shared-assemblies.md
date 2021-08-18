---
description: Un assembly Win32 può essere installato come assembly condiviso ed essere disponibile per l'uso da parte di più applicazioni nel computer. Gli assembly condivisi devono essere installati da un pacchetto Windows installer usato per installare o aggiornare un'applicazione.
ms.assetid: d408b0a9-8dc5-4cd0-93b3-429de7d12b17
title: Assembly condivisi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1097a0f2bbbc4d91a6206734cb2dead53bb38748b82c0204daff476d3eb663e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119628511"
---
# <a name="shared-assemblies"></a>Assembly condivisi

Un assembly Win32 può essere installato come assembly condiviso ed essere disponibile per l'uso da parte di più applicazioni nel computer. Gli assembly condivisi devono essere installati da un pacchetto Windows installer usato per installare o aggiornare un'applicazione.

Gli assembly condivisi vengono installati [come assembly side-by-side.](side-by-side-assemblies.md) Il Windows installer installa assembly side-by-side condivisi nella cartella Winsxs. Gli assembly non vengono registrati a livello globale nel sistema, ma sono disponibili a livello globale per qualsiasi applicazione che specifica una dipendenza dall'assembly in un file manifesto. Per altre informazioni, vedere Applicazioni isolate e assembly [side-by-side](../sbscs/isolated-applications-and-side-by-side-assemblies-portal.md).

Nei sistemi operativi precedenti a Windows XP, gli assembly condivisi vengono in genere installati nella Windows di sistema e registrati a livello globale. La versione più recente installata è disponibile per qualsiasi applicazione associata.

Per informazioni su come creare un pacchetto Windows installer per installare un assembly condiviso, vedere quanto segue:

-   [Installazione di assembly Win32 per la condivisione side-by-side in Windows XP](installing-win32-assemblies-for-side-by-side-sharing-on-windows-xp.md)
-   [Installazione di assembly Win32 per l'uso privato di un'applicazione in Windows XP](installing-win32-assemblies-for-the-private-use-of-an-application-on-windows-xp.md)

 

 
