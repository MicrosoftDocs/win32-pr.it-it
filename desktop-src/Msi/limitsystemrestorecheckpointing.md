---
description: Questo criterio di sistema per computer disattiva la creazione di checkpoint per Windows Installer.
ms.assetid: 706d6c85-3876-4205-b7da-b0fd709e65dd
title: LimitSystemRestoreCheckpointing
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7606d266b4e9e42f6287669df9b3ab33a3ad9f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307249"
---
# <a name="limitsystemrestorecheckpointing"></a><span data-ttu-id="ab2dc-103">LimitSystemRestoreCheckpointing</span><span class="sxs-lookup"><span data-stu-id="ab2dc-103">LimitSystemRestoreCheckpointing</span></span>

<span data-ttu-id="ab2dc-104">Questo [criterio di sistema](system-policy.md) per computer disattiva la creazione di checkpoint per Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="ab2dc-104">This per-machine [system policy](system-policy.md) turns off the creation of checkpoints by Windows Installer.</span></span>

<span data-ttu-id="ab2dc-105">Impostato su 0 o assente, il programma di installazione esegue normali checkpoint per l'installazione o la disinstallazione.</span><span class="sxs-lookup"><span data-stu-id="ab2dc-105">Set to 0 or absent, the installer does normal checkpointing for install or uninstall.</span></span> <span data-ttu-id="ab2dc-106">Impostando su 1, il programma di installazione non crea alcun checkpoint.</span><span class="sxs-lookup"><span data-stu-id="ab2dc-106">Set to 1, the installer creates no checkpoints.</span></span>

<span data-ttu-id="ab2dc-107">Questo criterio ha effetto solo sui checkpoint impostati dal Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="ab2dc-107">This policy affects only checkpoints set by Windows Installer.</span></span> <span data-ttu-id="ab2dc-108">Nei computer Windows XP, gli amministratori possono decidere di disabilitare il checkpoint dall'interno Windows Installer per migliorare le prestazioni.</span><span class="sxs-lookup"><span data-stu-id="ab2dc-108">On Windows XP computers, administrators may decide to disable checkpointing from within Windows Installer to improve performance.</span></span> <span data-ttu-id="ab2dc-109">[**Ripristino configurazione di sistema**](../sr/system-restore-portal.md) crea anche ulteriori checkpoint.</span><span class="sxs-lookup"><span data-stu-id="ab2dc-109">[**System Restore**](../sr/system-restore-portal.md) also creates additional checkpoints.</span></span> <span data-ttu-id="ab2dc-110">Per ulteriori informazioni, vedere [punti di ripristino del sistema e il Windows Installer](system-restore-points-and-the-windows-installer.md) e [impostazione di un punto di ripristino da un'azione personalizzata](setting-a-restore-point-from-a-custom-action.md).</span><span class="sxs-lookup"><span data-stu-id="ab2dc-110">For more information, see [System Restore Points and the Windows Installer](system-restore-points-and-the-windows-installer.md) and [Setting a Restore Point from a Custom Action](setting-a-restore-point-from-a-custom-action.md).</span></span>

## <a name="registry-key"></a><span data-ttu-id="ab2dc-111">Chiave del Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="ab2dc-111">Registry Key</span></span>

<span data-ttu-id="ab2dc-112">Impostare il valore denominato LimitSystemRestoreCheckpointing nella seguente chiave del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="ab2dc-112">Set the value named LimitSystemRestoreCheckpointing under the following registry key.</span></span>

<span data-ttu-id="ab2dc-113">**HKEY \_ \_ criteri software del computer locale \\ \\ \\ Microsoft \\ Windows \\ Installer**</span><span class="sxs-lookup"><span data-stu-id="ab2dc-113">**HKEY\_LOCAL\_MACHINE\\Software\\Policies\\Microsoft\\Windows\\Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="ab2dc-114">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="ab2dc-114">Data Type</span></span>

<span data-ttu-id="ab2dc-115">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="ab2dc-115">**REG\_DWORD**</span></span>

 

 
