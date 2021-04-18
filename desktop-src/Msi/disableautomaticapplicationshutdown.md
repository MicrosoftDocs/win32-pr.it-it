---
description: Se il criterio di sistema per computer è impostato su 1 (uno), Windows Installer non interagisce con Gestione riavvio, ma userà la finestra di dialogo FilesInUse. se il criterio di sistema per computer è impostato su 2 (due), Windows Installer usa la finestra di dialogo filesinus.
ms.assetid: a59de5bb-e0a1-459d-83e6-afaf81298123
title: DisableAutomaticApplicationShutdown
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 060c4027a1fb4026f4e1d578bd1d0c2ed8cd979c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310527"
---
# <a name="disableautomaticapplicationshutdown"></a><span data-ttu-id="3b8c1-103">DisableAutomaticApplicationShutdown</span><span class="sxs-lookup"><span data-stu-id="3b8c1-103">DisableAutomaticApplicationShutdown</span></span>

<span data-ttu-id="3b8c1-104">Se i criteri di sistema per computer sono impostati su 1 (uno), Windows Installer non interagisce con [Gestione riavvio](/windows/desktop/RstMgr/restart-manager-portal), ma userà la finestra di [dialogo filesinus](filesinuse-dialog.md).</span><span class="sxs-lookup"><span data-stu-id="3b8c1-104">If this per-machine system policy is set to 1 (one), Windows Installer does not interact with [Restart Manager](/windows/desktop/RstMgr/restart-manager-portal), but it will use the [FilesInUse Dialog](filesinuse-dialog.md).</span></span>

<span data-ttu-id="3b8c1-105">Se il criterio di sistema per computer è impostato su 2 (due), Windows Installer usa la [finestra di dialogo Filesinusale](filesinuse-dialog.md).</span><span class="sxs-lookup"><span data-stu-id="3b8c1-105">If this per-machine system policy is set to 2 (two), Windows Installer uses the [FilesInUse Dialog](filesinuse-dialog.md).</span></span> <span data-ttu-id="3b8c1-106">Questa impostazione Disabilita i tentativi da parte di [Gestione riavvio](/windows/desktop/RstMgr/restart-manager-portal) per ridurre i riavvii durante l'installazione di un pacchetto di Windows Installer che non è stato creato per usare Gestione riavvio.</span><span class="sxs-lookup"><span data-stu-id="3b8c1-106">This setting disables attempts by the [Restart Manager](/windows/desktop/RstMgr/restart-manager-portal) to mitigate restarts when installing a Windows Installer package that has not been authored to use the Restart Manager.</span></span> <span data-ttu-id="3b8c1-107">Il programma di installazione utilizza ancora Gestione riavvio per rilevare i file utilizzati dalle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="3b8c1-107">The installer still uses the Restart Manager to detect files in use by applications.</span></span>

<span data-ttu-id="3b8c1-108">Il criterio DisableAutomaticApplicationShutdown è disponibile a partire dalla versione Windows Installer 4,0 in Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="3b8c1-108">The DisableAutomaticApplicationShutdown policy is available beginning with Windows Installer version 4.0 on Windows Vista.</span></span>

## <a name="registry-key"></a><span data-ttu-id="3b8c1-109">Chiave del Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="3b8c1-109">Registry Key</span></span>

<span data-ttu-id="3b8c1-110">**HKEY \_ Criteri software del \_ computer locale** \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer**</span><span class="sxs-lookup"><span data-stu-id="3b8c1-110">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="3b8c1-111">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="3b8c1-111">Data Type</span></span>

<span data-ttu-id="3b8c1-112">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="3b8c1-112">**REG\_DWORD**</span></span>

## <a name="related-topics"></a><span data-ttu-id="3b8c1-113">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3b8c1-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3b8c1-114">**MSIRESTARTMANAGERCONTROL**</span><span class="sxs-lookup"><span data-stu-id="3b8c1-114">**MSIRESTARTMANAGERCONTROL**</span></span>](msirestartmanagercontrol.md)
</dt> <dt>

[<span data-ttu-id="3b8c1-115">Non supportato in Windows Installer 3,1 e versioni precedenti</span><span class="sxs-lookup"><span data-stu-id="3b8c1-115">Not Supported in Windows Installer 3.1 and earlier versions</span></span>](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 
