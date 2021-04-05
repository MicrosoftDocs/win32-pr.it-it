---
description: Un assembly Win32 può essere installato come assembly condiviso ed essere disponibile per l'utilizzo da parte di più applicazioni nel computer. Gli assembly condivisi devono essere installati da un pacchetto di Windows Installer usato per installare o aggiornare un'applicazione.
ms.assetid: d408b0a9-8dc5-4cd0-93b3-429de7d12b17
title: Assembly condivisi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e99d805614c05838abe9f5c869fc9c072b1fa8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757811"
---
# <a name="shared-assemblies"></a>Assembly condivisi

Un assembly Win32 può essere installato come assembly condiviso ed essere disponibile per l'utilizzo da parte di più applicazioni nel computer. Gli assembly condivisi devono essere installati da un pacchetto di Windows Installer usato per installare o aggiornare un'applicazione.

Gli assembly condivisi vengono installati come [assembly side-by-side](side-by-side-assemblies.md). Il Windows Installer installa gli assembly affiancati condivisi nella cartella WinSxS. Gli assembly non sono registrati a livello globale nel sistema, ma sono disponibili a livello globale per tutte le applicazioni che specificano una dipendenza dall'assembly in un file manifesto. Per altre informazioni, vedere [applicazioni isolate e assembly affiancati](../sbscs/isolated-applications-and-side-by-side-assemblies-portal.md).

Nei sistemi operativi precedenti a Windows XP gli assembly condivisi vengono in genere installati nella cartella di sistema di Windows e registrati a livello globale. La versione installata più recente è disponibile per tutte le applicazioni associate.

Per informazioni su come creare un pacchetto di Windows Installer per installare un assembly condiviso, vedere gli argomenti seguenti:

-   [Installazione degli assembly Win32 per la condivisione side-by-side in Windows XP](installing-win32-assemblies-for-side-by-side-sharing-on-windows-xp.md)
-   [Installazione di assembly Win32 per l'utilizzo privato di un'applicazione in Windows XP](installing-win32-assemblies-for-the-private-use-of-an-application-on-windows-xp.md)

 

 
