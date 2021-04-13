---
description: A partire da Windows Server 2008 e Windows Vista, questo criterio non ha più alcun effetto.
ms.assetid: 27a4192e-0574-414d-993e-6c715577f0ba
title: EnableAdminTSRemote
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 383339ab5c2a592f3d6ab2cd81b4d6a446780411
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226622"
---
# <a name="enableadmintsremote"></a><span data-ttu-id="10424-103">EnableAdminTSRemote</span><span class="sxs-lookup"><span data-stu-id="10424-103">EnableAdminTSRemote</span></span>

<span data-ttu-id="10424-104">A partire da Windows Server 2008 e Windows Vista, questo criterio non ha più alcun effetto.</span><span class="sxs-lookup"><span data-stu-id="10424-104">Beginning with Windows Server 2008 and Windows Vista, this policy no longer has any effect.</span></span> <span data-ttu-id="10424-105">Un amministratore può eseguire un'installazione dalla sessione della console di un server terminal.</span><span class="sxs-lookup"><span data-stu-id="10424-105">An administrator can perform an installation from the console session of a terminal server.</span></span> <span data-ttu-id="10424-106">Un amministratore può inoltre eseguire un'installazione da una sessione client di Terminal Server.</span><span class="sxs-lookup"><span data-stu-id="10424-106">An administrator can also perform an installation from a client session of the terminal server.</span></span>

<span data-ttu-id="10424-107">Per ulteriori informazioni, vedere [Servizi terminal](/windows/desktop/TermServ/terminal-services-portal) in Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="10424-107">For more information, see [Terminal Services](/windows/desktop/TermServ/terminal-services-portal) in the Microsoft Windows Software Development Kit (SDK).</span></span>

<span data-ttu-id="10424-108">\* \* Sistemi operativi precedenti a Windows Server 2008 e Windows Vista: \* \*</span><span class="sxs-lookup"><span data-stu-id="10424-108">\*\*Operating systems earlier than Windows Server 2008 and Windows Vista:  \*\*</span></span>

<span data-ttu-id="10424-109">L'impostazione di questo [criterio di sistema](system-policy.md) per computer consente agli amministratori di eseguire installazioni da una sessione client di Terminal Server.</span><span class="sxs-lookup"><span data-stu-id="10424-109">Setting this per-machine [system policy](system-policy.md) enables administrators to perform installations from a client session of the terminal server.</span></span> <span data-ttu-id="10424-110">Se questo criterio non è impostato, gli amministratori possono eseguire le installazioni solo dalla sessione della console.</span><span class="sxs-lookup"><span data-stu-id="10424-110">If this policy is not set, administrators can only perform installations from the console session.</span></span> <span data-ttu-id="10424-111">Gli utenti non amministratori non possono mai eseguire installazioni da una sessione client.</span><span class="sxs-lookup"><span data-stu-id="10424-111">Nonadministrative users can never perform installations from a client session.</span></span> <span data-ttu-id="10424-112">Il valore predefinito per questo criterio consente solo agli amministratori di eseguire installazioni dalla sessione della console.</span><span class="sxs-lookup"><span data-stu-id="10424-112">The default value for this policy allows only administrators to perform installations from the console session.</span></span> <span data-ttu-id="10424-113">Gli amministratori possono sempre eseguire [installazioni amministrative](administrative-installation.md) da una sessione client di Terminal Server o dalla sessione della console, indipendentemente dal fatto che questi criteri siano impostati.</span><span class="sxs-lookup"><span data-stu-id="10424-113">Administrators can always do [Administrative installations](administrative-installation.md) from a client session of the terminal server, or from the console session, regardless of whether this policy is set.</span></span>

## <a name="registry-key"></a><span data-ttu-id="10424-114">Chiave del Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="10424-114">Registry Key</span></span>

<span data-ttu-id="10424-115">**HKEY \_ Criteri software del \_ computer locale** \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer**</span><span class="sxs-lookup"><span data-stu-id="10424-115">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="10424-116">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="10424-116">Data Type</span></span>

<span data-ttu-id="10424-117">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="10424-117">**REG\_DWORD**</span></span>

## <a name="remarks"></a><span data-ttu-id="10424-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="10424-118">Remarks</span></span>

<span data-ttu-id="10424-119">Per ulteriori informazioni, vedere anche [utilizzo di Windows Installer con una Terminal Server](using-windows-installer-with-a-terminal-server.md).</span><span class="sxs-lookup"><span data-stu-id="10424-119">For more information see also, [Using Windows Installer with a Terminal Server](using-windows-installer-with-a-terminal-server.md).</span></span>

 

 
