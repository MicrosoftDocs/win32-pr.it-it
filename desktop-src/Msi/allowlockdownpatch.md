---
description: Se questo criterio di sistema per computer non è impostato, solo gli amministratori possono applicare patch ai prodotti esistenti installati con privilegi elevati.
ms.assetid: cd07dcb0-b9b5-4186-a916-604c40f88b5f
title: AllowLockdownPatch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c85507d4f24209220ffb64411b452bbe46f3c76a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967292"
---
# <a name="allowlockdownpatch"></a><span data-ttu-id="79ed9-103">AllowLockdownPatch</span><span class="sxs-lookup"><span data-stu-id="79ed9-103">AllowLockdownPatch</span></span>

<span data-ttu-id="79ed9-104">Se questo [criterio di sistema](system-policy.md) per computer non è impostato, solo gli amministratori possono applicare patch ai prodotti esistenti installati con privilegi elevati.</span><span class="sxs-lookup"><span data-stu-id="79ed9-104">If this per-machine [system policy](system-policy.md) is not set, only administrators can patch existing products that were installed using elevated privileges.</span></span> <span data-ttu-id="79ed9-105">Se AllowLockdownPatch è impostato su "1", gli utenti non amministratori possono, in alcuni casi, applicare patch ai prodotti durante l'esecuzione di un'installazione con privilegi elevati.</span><span class="sxs-lookup"><span data-stu-id="79ed9-105">If AllowLockdownPatch is set to "1", nonadministrative users can, in some cases, apply patches to products while running an installation using elevated privileges.</span></span> <span data-ttu-id="79ed9-106">Con il set di criteri, la patch può installare [aggiornamenti secondari](minor-upgrades.md) durante l'esecuzione di un'installazione con privilegi elevati, la patch non può installare gli [aggiornamenti principali](major-upgrades.md).</span><span class="sxs-lookup"><span data-stu-id="79ed9-106">With the policy set, the patch can install [minor upgrades](minor-upgrades.md) while running an installation using elevated privileges, the patch cannot install [major upgrades](major-upgrades.md).</span></span> <span data-ttu-id="79ed9-107">L'impostazione di questo criterio consente inoltre agli utenti non amministratori di eseguire programmi con privilegi LocalSystem durante un'installazione con privilegi elevati.</span><span class="sxs-lookup"><span data-stu-id="79ed9-107">Setting this policy also enables nonadministrative users to run programs at LocalSystem privileges during an elevated installation.</span></span>

<span data-ttu-id="79ed9-108">L'impostazione predefinita è consigliata per garantire un ambiente protetto.</span><span class="sxs-lookup"><span data-stu-id="79ed9-108">The default setting is recommended to ensure a secure environment.</span></span>

## <a name="registry-key"></a><span data-ttu-id="79ed9-109">Chiave del Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="79ed9-109">Registry Key</span></span>

<span data-ttu-id="79ed9-110">**HKEY \_ Criteri software del \_ computer locale** \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer**</span><span class="sxs-lookup"><span data-stu-id="79ed9-110">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="79ed9-111">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="79ed9-111">Data Type</span></span>

<span data-ttu-id="79ed9-112">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="79ed9-112">**REG\_DWORD**</span></span>

## <a name="remarks"></a><span data-ttu-id="79ed9-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="79ed9-113">Remarks</span></span>

<span data-ttu-id="79ed9-114">Qualsiasi utente può applicare una patch durante un'installazione non con privilegi elevati.</span><span class="sxs-lookup"><span data-stu-id="79ed9-114">Any user can apply a patch during a nonelevated installation.</span></span> <span data-ttu-id="79ed9-115">L'impostazione di questo [criterio di sistema](system-policy.md) per computer su "1" offre agli utenti non amministrativi la flessibilità aggiuntiva per l'applicazione di patch a qualsiasi prodotto durante un'installazione con privilegi elevati.</span><span class="sxs-lookup"><span data-stu-id="79ed9-115">Setting this per-machine [system policy](system-policy.md) to "1" gives nonadministrative users the additional flexibility of applying patches to any product during an elevated installation.</span></span> <span data-ttu-id="79ed9-116">Se questo criterio non è impostato, gli utenti non amministratori non possono applicare una patch alle applicazioni assegnate o pubblicate.</span><span class="sxs-lookup"><span data-stu-id="79ed9-116">If this policy is not set, nonadministrative users cannot apply a patch to assigned or published applications.</span></span>

<span data-ttu-id="79ed9-117">L'impostazione di questo criterio consente inoltre agli utenti non amministratori di eseguire programmi arbitrari con privilegi LocalSystem se hanno un pacchetto Windows Installer patch che installa o avvia tali programmi.</span><span class="sxs-lookup"><span data-stu-id="79ed9-117">Setting this policy also enables nonadministrative users to run arbitrary programs at LocalSystem privileges if they have a Windows Installer patch package that installs or launches those programs.</span></span>

 

 



