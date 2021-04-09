---
description: Se questo criterio di sistema è impostato su 1, il programma di installazione non archivia i file di rollback durante l'installazione e Disabilita il rollback dell'installazione.
ms.assetid: 01747de6-7478-4403-ba36-8ff1abc2b70f
title: DisableRollback
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7f0ce15e618880f021e04adf7d2146a97f6ed65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966833"
---
# <a name="disablerollback"></a><span data-ttu-id="203cc-103">DisableRollback</span><span class="sxs-lookup"><span data-stu-id="203cc-103">DisableRollback</span></span>

<span data-ttu-id="203cc-104">Se questo [criterio di sistema](system-policy.md) è impostato su 1, il programma di installazione non archivia i file di rollback durante l'installazione e Disabilita il rollback dell'installazione.</span><span class="sxs-lookup"><span data-stu-id="203cc-104">If this [system policy](system-policy.md) is set to 1, the installer does not store rollback files during installation and disables installation rollback.</span></span> <span data-ttu-id="203cc-105">Per impostazione predefinita, il rollback è abilitato.</span><span class="sxs-lookup"><span data-stu-id="203cc-105">By default, rollback is enabled.</span></span> <span data-ttu-id="203cc-106">Si consiglia agli amministratori di non utilizzare questo criterio a meno che non sia assolutamente essenziale.</span><span class="sxs-lookup"><span data-stu-id="203cc-106">Administrators are advised to not use this policy unless it is absolutely essential.</span></span> <span data-ttu-id="203cc-107">Per ulteriori informazioni, vedere [rollback Installation](rollback-installation.md).</span><span class="sxs-lookup"><span data-stu-id="203cc-107">For more information, see [Rollback Installation](rollback-installation.md).</span></span>

## <a name="registry-key"></a><span data-ttu-id="203cc-108">Chiave del Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="203cc-108">Registry Key</span></span>

<span data-ttu-id="203cc-109">Per disabilitare il rollback per le installazioni per utente, impostare **DisableRollback** su 1 nella chiave del registro di sistema seguente:</span><span class="sxs-lookup"><span data-stu-id="203cc-109">To disable rollback for per-user installations, set **DisableRollback** to 1 under the following registry key:</span></span>

<span data-ttu-id="203cc-110">**HKEY \_ Criteri \_ software utente correnti** \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer**</span><span class="sxs-lookup"><span data-stu-id="203cc-110">**HKEY\_CURRENT\_USER**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

<span data-ttu-id="203cc-111">Per disabilitare il rollback per le installazioni per computer, impostare **DisableRollback** su 1 nella seguente chiave del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="203cc-111">To disable rollback for per-computer installations, set **DisableRollback** to 1 under the following registry key.</span></span>

<span data-ttu-id="203cc-112">**HKEY \_ Criteri software del \_ computer locale** \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer**</span><span class="sxs-lookup"><span data-stu-id="203cc-112">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="203cc-113">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="203cc-113">Data Type</span></span>

<span data-ttu-id="203cc-114">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="203cc-114">**REG\_DWORD**</span></span>

 

 



