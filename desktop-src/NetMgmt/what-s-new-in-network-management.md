---
title: Novità della gestione della rete
description: Novità della gestione della rete
ms.assetid: f805b662-1807-4703-b27e-4721895fe450
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e688d340b8282015b99ccb3d7fa6404dfa332748
ms.sourcegitcommit: 89f99926f946dc6c5ea600fb7c41f6b19ceac516
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/21/2020
ms.locfileid: "104399909"
---
# <a name="whats-new-in-network-management"></a><span data-ttu-id="9f270-103">Novità della gestione della rete</span><span class="sxs-lookup"><span data-stu-id="9f270-103">What's New in Network Management</span></span>

## <a name="windows-8-and-windows-server-2012"></a><span data-ttu-id="9f270-104">Windows 8 e Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9f270-104">Windows 8 and Windows Server 2012</span></span>

<span data-ttu-id="9f270-105">In Microsoft Windows 8 sono state introdotte nuove funzionalità di programmazione per la gestione della rete.</span><span class="sxs-lookup"><span data-stu-id="9f270-105">Microsoft Windows 8 introduces new Network Management programming features.</span></span> <span data-ttu-id="9f270-106">Questi nuovi elementi estendono le funzionalità di gestione della rete per creare pacchetti di provisioning per operazioni di aggiunta a un dominio offline quando si effettua il provisioning dei computer con Windows 8.</span><span class="sxs-lookup"><span data-stu-id="9f270-106">These new elements extend the capability of Network Management to create provisioning packages for offline domain join operations when provisioning computers with Windows 8.</span></span>

<span data-ttu-id="9f270-107">Di seguito sono riportate le nuove funzioni di gestione della rete:</span><span class="sxs-lookup"><span data-stu-id="9f270-107">The following are new Network Management functions:</span></span>

-   [<span data-ttu-id="9f270-108">**NetCreateProvisioningPackage**</span><span class="sxs-lookup"><span data-stu-id="9f270-108">**NetCreateProvisioningPackage**</span></span>](/windows/desktop/api/Lmjoin/nf-lmjoin-netprovisioncomputeraccount)
-   [<span data-ttu-id="9f270-109">**NetRequestProvisioningPackageInstall**</span><span class="sxs-lookup"><span data-stu-id="9f270-109">**NetRequestProvisioningPackageInstall**</span></span>](/windows/desktop/api/Lmjoin/nf-lmjoin-netrequestprovisioningpackageinstall)

<span data-ttu-id="9f270-110">Di seguito sono riportate le nuove strutture di gestione della rete:</span><span class="sxs-lookup"><span data-stu-id="9f270-110">The following are new Network Management structures:</span></span>

-   [<span data-ttu-id="9f270-111">**\_parametri di PROvisioning di Netsetup \_**</span><span class="sxs-lookup"><span data-stu-id="9f270-111">**NETSETUP\_PROVISIONING\_PARAMS**</span></span>](/windows/desktop/api/Lmjoin/ns-lmjoin-netsetup_provisioning_params)
-   [<span data-ttu-id="9f270-112">**\_Informazioni utente \_ 24**</span><span class="sxs-lookup"><span data-stu-id="9f270-112">**USER\_INFO\_24**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_24)

<span data-ttu-id="9f270-113">La funzione [**NetUserGetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetinfo) è stata migliorata in Windows 8 per supportare un nuovo livello di informazioni e restituire una struttura [**\_ Info utente \_ 24**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_24) con le informazioni sull'account utente per un account connesso a un'identità Internet.</span><span class="sxs-lookup"><span data-stu-id="9f270-113">The [**NetUserGetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetinfo) function has been enhanced on Windows 8 to support a new information level and return a [**USER\_INFO\_24**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_24) structure with user account information for an account connected to an Internet identity.</span></span>

## <a name="windows-7-and-windows-server-2008-r2"></a><span data-ttu-id="9f270-114">Windows 7 e Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="9f270-114">Windows 7 and Windows Server 2008 R2</span></span>

<span data-ttu-id="9f270-115">In Microsoft Windows 7 sono state introdotte nuove funzionalità di programmazione per la gestione della rete.</span><span class="sxs-lookup"><span data-stu-id="9f270-115">Microsoft Windows 7 introduces new Network Management programming features.</span></span> <span data-ttu-id="9f270-116">Questi elementi estendono le funzionalità di gestione della rete per consentire operazioni di aggiunta a un dominio offline durante il provisioning dei computer con Windows 7.</span><span class="sxs-lookup"><span data-stu-id="9f270-116">These elements extend the capability of Network Management to allow offline domain join operations when provisioning computers with Windows 7.</span></span>

<span data-ttu-id="9f270-117">Di seguito sono riportate le nuove funzioni di gestione della rete:</span><span class="sxs-lookup"><span data-stu-id="9f270-117">The following are new Network Management functions:</span></span>

-   [<span data-ttu-id="9f270-118">**NetProvisionComputerAccount**</span><span class="sxs-lookup"><span data-stu-id="9f270-118">**NetProvisionComputerAccount**</span></span>](/windows/desktop/api/Lmjoin/nf-lmjoin-netprovisioncomputeraccount)
-   [<span data-ttu-id="9f270-119">**NetRequestOfflineDomainJoin**</span><span class="sxs-lookup"><span data-stu-id="9f270-119">**NetRequestOfflineDomainJoin**</span></span>](/windows/desktop/api/Lmjoin/nf-lmjoin-netrequestofflinedomainjoin)

<span data-ttu-id="9f270-120">Le funzioni di gestione di rete esistenti seguenti sono state migliorate per supportare opzioni aggiuntive:</span><span class="sxs-lookup"><span data-stu-id="9f270-120">The following existing Network Management functions were enhanced to support additional options:</span></span>

-   [<span data-ttu-id="9f270-121">**NetJoinDomain**</span><span class="sxs-lookup"><span data-stu-id="9f270-121">**NetJoinDomain**</span></span>](/windows/desktop/api/Lmjoin/nf-lmjoin-netjoindomain)

## <a name="windows-server-2003"></a><span data-ttu-id="9f270-122">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="9f270-122">Windows Server 2003</span></span>

<span data-ttu-id="9f270-123">Microsoft Windows Server 2003 introduce nuove funzionalità di programmazione per la gestione della rete.</span><span class="sxs-lookup"><span data-stu-id="9f270-123">Microsoft Windows Server 2003 introduces new Network Management programming features.</span></span> <span data-ttu-id="9f270-124">Questi elementi estendono le funzionalità delle operazioni di gestione della rete in Windows Server 2003 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="9f270-124">These elements extend the capability of Network Management operations on Windows Server 2003 and later.</span></span>

## <a name="windows-xp"></a><span data-ttu-id="9f270-125">Windows XP</span><span class="sxs-lookup"><span data-stu-id="9f270-125">Windows XP</span></span>

<span data-ttu-id="9f270-126">In Microsoft Windows XP sono state introdotte nuove funzionalità di programmazione per la gestione della rete.</span><span class="sxs-lookup"><span data-stu-id="9f270-126">Microsoft Windows XP introduces new Network Management programming features.</span></span> <span data-ttu-id="9f270-127">Questi elementi estendono le funzionalità di gestione della rete in Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="9f270-127">These elements extend the capability of Network Management operations on Windows XP and later.</span></span>

<span data-ttu-id="9f270-128">Di seguito sono riportate le nuove funzioni di gestione della rete:</span><span class="sxs-lookup"><span data-stu-id="9f270-128">The following are new Network Management functions:</span></span>

-   [<span data-ttu-id="9f270-129">**NetAddAlternateComputerName**</span><span class="sxs-lookup"><span data-stu-id="9f270-129">**NetAddAlternateComputerName**</span></span>](/windows/desktop/api/Lmjoin/nf-lmjoin-netaddalternatecomputername)
-   [<span data-ttu-id="9f270-130">**NetEnumerateComputerNames**</span><span class="sxs-lookup"><span data-stu-id="9f270-130">**NetEnumerateComputerNames**</span></span>](/windows/desktop/api/Lmjoin/nf-lmjoin-netenumeratecomputernames)
-   [<span data-ttu-id="9f270-131">**NetRemoveAlternateComputerName**</span><span class="sxs-lookup"><span data-stu-id="9f270-131">**NetRemoveAlternateComputerName**</span></span>](/windows/desktop/api/Lmjoin/nf-lmjoin-netremovealternatecomputername)
-   [<span data-ttu-id="9f270-132">**NetSetPrimaryComputerName**</span><span class="sxs-lookup"><span data-stu-id="9f270-132">**NetSetPrimaryComputerName**</span></span>](/windows/desktop/api/Lmjoin/nf-lmjoin-netsetprimarycomputername)
-   [<span data-ttu-id="9f270-133">**SetNetScheduleAccountInformation**</span><span class="sxs-lookup"><span data-stu-id="9f270-133">**SetNetScheduleAccountInformation**</span></span>](/windows/desktop/api/AtAcct/nf-atacct-setnetscheduleaccountinformation)

 

 




