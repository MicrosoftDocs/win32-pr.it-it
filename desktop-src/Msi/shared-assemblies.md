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
# <a name="shared-assemblies"></a><span data-ttu-id="19d8e-104">Assembly condivisi</span><span class="sxs-lookup"><span data-stu-id="19d8e-104">Shared Assemblies</span></span>

<span data-ttu-id="19d8e-105">Un assembly Win32 può essere installato come assembly condiviso ed essere disponibile per l'utilizzo da parte di più applicazioni nel computer.</span><span class="sxs-lookup"><span data-stu-id="19d8e-105">A Win32 assembly can be installed as a shared assembly and be available for use by multiple applications on the computer.</span></span> <span data-ttu-id="19d8e-106">Gli assembly condivisi devono essere installati da un pacchetto di Windows Installer usato per installare o aggiornare un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="19d8e-106">Shared assemblies should be installed by a Windows Installer package used to install or update an application.</span></span>

<span data-ttu-id="19d8e-107">Gli assembly condivisi vengono installati come [assembly side-by-side](side-by-side-assemblies.md).</span><span class="sxs-lookup"><span data-stu-id="19d8e-107">Shared assemblies are installed as [side-by-side assemblies](side-by-side-assemblies.md).</span></span> <span data-ttu-id="19d8e-108">Il Windows Installer installa gli assembly affiancati condivisi nella cartella WinSxS.</span><span class="sxs-lookup"><span data-stu-id="19d8e-108">The Windows Installer installs shared side-by-side assemblies into the Winsxs folder.</span></span> <span data-ttu-id="19d8e-109">Gli assembly non sono registrati a livello globale nel sistema, ma sono disponibili a livello globale per tutte le applicazioni che specificano una dipendenza dall'assembly in un file manifesto.</span><span class="sxs-lookup"><span data-stu-id="19d8e-109">The assemblies are not registered globally on the system, but they are globally available to any application that specifies a dependency on the assembly in a manifest file.</span></span> <span data-ttu-id="19d8e-110">Per altre informazioni, vedere [applicazioni isolate e assembly affiancati](../sbscs/isolated-applications-and-side-by-side-assemblies-portal.md).</span><span class="sxs-lookup"><span data-stu-id="19d8e-110">For more information, see [Isolated Applications and Side-by-side Assemblies](../sbscs/isolated-applications-and-side-by-side-assemblies-portal.md).</span></span>

<span data-ttu-id="19d8e-111">Nei sistemi operativi precedenti a Windows XP gli assembly condivisi vengono in genere installati nella cartella di sistema di Windows e registrati a livello globale.</span><span class="sxs-lookup"><span data-stu-id="19d8e-111">On operating systems earlier than Windows XP, shared assemblies are usually installed in the Windows system folder and registered globally.</span></span> <span data-ttu-id="19d8e-112">La versione installata più recente è disponibile per tutte le applicazioni associate.</span><span class="sxs-lookup"><span data-stu-id="19d8e-112">The latest installed version is available to any application that binds to it.</span></span>

<span data-ttu-id="19d8e-113">Per informazioni su come creare un pacchetto di Windows Installer per installare un assembly condiviso, vedere gli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="19d8e-113">For information on how to author a Windows Installer package to install a shared assembly, see the following:</span></span>

-   [<span data-ttu-id="19d8e-114">Installazione degli assembly Win32 per la condivisione side-by-side in Windows XP</span><span class="sxs-lookup"><span data-stu-id="19d8e-114">Installing Win32 Assemblies for Side-by-Side Sharing on Windows XP</span></span>](installing-win32-assemblies-for-side-by-side-sharing-on-windows-xp.md)
-   [<span data-ttu-id="19d8e-115">Installazione di assembly Win32 per l'utilizzo privato di un'applicazione in Windows XP</span><span class="sxs-lookup"><span data-stu-id="19d8e-115">Installing Win32 Assemblies for the Private Use of an Application on Windows XP</span></span>](installing-win32-assemblies-for-the-private-use-of-an-application-on-windows-xp.md)

 

 
