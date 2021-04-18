---
title: Requisiti di firma delle funzionalità di avvio protetto per i driver in modalità kernel
description: Requisiti di firma delle funzionalità di avvio protetto per i driver in modalità kernel
ms.assetid: 7FF64BA2-89E3-4E6F-B542-7BC7BF7F4FB2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a63a8b1fca1677aa125bac96dfec290dcd736b5
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/01/2020
ms.locfileid: "106300567"
---
# <a name="secure-boot-feature-signing-requirements-for-kernel-mode-drivers"></a><span data-ttu-id="127d9-103">Requisiti di firma delle funzionalità di avvio protetto per i driver in modalità kernel</span><span class="sxs-lookup"><span data-stu-id="127d9-103">Secure boot feature signing requirements for kernel-mode drivers</span></span>

## <a name="platforms"></a><span data-ttu-id="127d9-104">Piattaforme</span><span class="sxs-lookup"><span data-stu-id="127d9-104">Platforms</span></span>

<span data-ttu-id="127d9-105">**Client** -Windows 8</span><span class="sxs-lookup"><span data-stu-id="127d9-105">**Clients** – Windows 8</span></span>  
<span data-ttu-id="127d9-106">**Server** : Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="127d9-106">**Servers** – Windows Server 2012</span></span>  


## <a name="description"></a><span data-ttu-id="127d9-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="127d9-107">Description</span></span>

<span data-ttu-id="127d9-108">In Windows 8 e Windows Server 2012, incluso WinPE, il kernel è stato bloccato per impedire che malware introdotto da boot o kit radice eludesse i requisiti di sicurezza del sistema operativo Windows per i driver firmati.</span><span class="sxs-lookup"><span data-stu-id="127d9-108">In Windows 8 and Windows Server 2012, including WinPE, the kernel has been locked down to prevent malware introduced by boot or root kits from circumventing Windows operating system security requirements for signed drivers.</span></span>

<span data-ttu-id="127d9-109">Questa modifica ha effetto su tutti i driver in modalità kernel per i dispositivi che supportano l'avvio protetto UEFI (Unified Extensible Firmware Interface). L'avvio protetto UEFI è necessario per la certificazione di Windows 8 per i computer client e facoltativa per i server.</span><span class="sxs-lookup"><span data-stu-id="127d9-109">This change affects all kernel-mode drivers for devices that support unified extensible firmware interface (UEFI) Secure Boot; UEFI Secure Boot is required for Windows 8 certification for client machines, and optional for servers.</span></span> <span data-ttu-id="127d9-110">Non influisce sui driver in modalità utente.</span><span class="sxs-lookup"><span data-stu-id="127d9-110">It does not affect user-mode drivers.</span></span>

<span data-ttu-id="127d9-111">Lo sviluppo standard per i driver in modalità kernel comporta l'utilizzo del debug in modalità kernel o dell'impostazione dati di configurazione di avvio (BCD) <testsigning> .</span><span class="sxs-lookup"><span data-stu-id="127d9-111">Standard development for kernel-mode drivers involves either the use of kernel mode debugging or the boot configuration data (BCD) <testsigning> setting.</span></span> <span data-ttu-id="127d9-112">Entrambi sono disabilitati quando è abilitato l'avvio protetto.</span><span class="sxs-lookup"><span data-stu-id="127d9-112">Both of these are disabled when Secured Boot is on.</span></span>

## <a name="manifestation"></a><span data-ttu-id="127d9-113">Manifestazione</span><span class="sxs-lookup"><span data-stu-id="127d9-113">Manifestation</span></span>

<span data-ttu-id="127d9-114">I driver in modalità kernel non verranno eseguiti se non sono firmati correttamente da un'autorità di certificazione (CA) attendibile.</span><span class="sxs-lookup"><span data-stu-id="127d9-114">Kernel-mode drivers will not run if they are not properly signed by a trusted certification authority (CA).</span></span> <span data-ttu-id="127d9-115">Il sistema operativo non consentirà l'esecuzione di driver non attendibili e i meccanismi standard come il debug del kernel e testsigning non saranno consentiti.</span><span class="sxs-lookup"><span data-stu-id="127d9-115">The operating system will not allow untrusted drivers to run and standard mechanisms like kernel debugging and testsigning will not be permitted.</span></span>

## <a name="mitigation"></a><span data-ttu-id="127d9-116">Strategia di riduzione del rischio</span><span class="sxs-lookup"><span data-stu-id="127d9-116">Mitigation</span></span>

<span data-ttu-id="127d9-117">Per testare i driver, è necessario disabilitare l'avvio protetto nel BIOS e soddisfare gli altri requisiti di firma dei test (vedere di seguito).</span><span class="sxs-lookup"><span data-stu-id="127d9-117">To test drivers, you must disable Secure Boot in BIOS as well as meet the other test-signing requirements (see below).</span></span>

<span data-ttu-id="127d9-118">Quando si distribuiscono i driver più ampiamente, devono essere firmati correttamente da un'autorità di certificazione attendibile.</span><span class="sxs-lookup"><span data-stu-id="127d9-118">When distributing drivers more widely they must be properly signed by a trusted CA.</span></span>

## <a name="resources"></a><span data-ttu-id="127d9-119">Risorse</span><span class="sxs-lookup"><span data-stu-id="127d9-119">Resources</span></span>

-   <span data-ttu-id="127d9-120">[Firma dei driver](/previous-versions/windows/hardware/design/dn653563(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="127d9-120">[Signing Drivers](/previous-versions/windows/hardware/design/dn653563(v=vs.85))</span></span>

 

 