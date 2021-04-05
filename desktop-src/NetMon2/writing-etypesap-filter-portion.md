---
description: La parte ETYPE/SAP del filtro di acquisizione notifica al driver Network Monitor di accettare i frame con una combinazione specifica di ETYPE del e punti di accesso al servizio (SAP).
ms.assetid: 57dcf1cd-f27f-4bd3-a5a8-9e978a2d213e
title: Scrittura della parte di filtro ETYPE/SAP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b072d123ca18d3aa2b3f2c91db4a8461473a854
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968093"
---
# <a name="writing-etypesap-filter-portion"></a><span data-ttu-id="73e78-103">Scrittura della parte di filtro ETYPE/SAP</span><span class="sxs-lookup"><span data-stu-id="73e78-103">Writing Etype/SAP Filter Portion</span></span>

<span data-ttu-id="73e78-104">La parte ETYPE/SAP del filtro di acquisizione notifica al driver Network Monitor di accettare i frame con una combinazione specifica di ETYPE del e [*punti di accesso al servizio*](s.md) (SAP).</span><span class="sxs-lookup"><span data-stu-id="73e78-104">The Etype/SAP portion of the capture filter notifies the Network Monitor driver to accept frames that have a specific combination of Etypes and [*service access points*](s.md) (SAPs).</span></span> <span data-ttu-id="73e78-105">ETYPE del e SAP sono entrambi modi che i protocolli di basso livello, ad esempio Ethernet, LLC e snap, indicano il protocollo che li segue.</span><span class="sxs-lookup"><span data-stu-id="73e78-105">Etypes and SAPs are both ways that low-level protocols such as Ethernet, LLC, and Snap indicate which protocol follows them.</span></span> <span data-ttu-id="73e78-106">In particolare:</span><span class="sxs-lookup"><span data-stu-id="73e78-106">Specifically:</span></span>

-   <span data-ttu-id="73e78-107">Ethernet specifica un etype</span><span class="sxs-lookup"><span data-stu-id="73e78-107">Ethernet specifies an Etype</span></span>
-   <span data-ttu-id="73e78-108">LLC specifica un SAP</span><span class="sxs-lookup"><span data-stu-id="73e78-108">LLC specifies a SAP</span></span>
-   <span data-ttu-id="73e78-109">Snap specifica un etype</span><span class="sxs-lookup"><span data-stu-id="73e78-109">Snap specifies an Etype</span></span>

## <a name="etypesap-capture-filter-flags"></a><span data-ttu-id="73e78-110">Flag di filtro di acquisizione ETYPE/SAP</span><span class="sxs-lookup"><span data-stu-id="73e78-110">Etype/SAP Capture Filter Flags</span></span>

<span data-ttu-id="73e78-111">Usare le informazioni seguenti per impostare i flag nel membro **FilterFlags** della struttura [**capturefilter**](capturefilter.md) .</span><span class="sxs-lookup"><span data-stu-id="73e78-111">Use the following information to set the flags in the **FilterFlags** member of the [**CAPTUREFILTER**](capturefilter.md) structure.</span></span>



| <span data-ttu-id="73e78-112">Contrassegno</span><span class="sxs-lookup"><span data-stu-id="73e78-112">Flag</span></span>                                         | <span data-ttu-id="73e78-113">Significato</span><span class="sxs-lookup"><span data-stu-id="73e78-113">Meaning</span></span>                                                                                                                                                                                                                                                     |
|----------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="73e78-114">\_i flag capturefilter \_ includono \_ tutti i \_ succhi</span><span class="sxs-lookup"><span data-stu-id="73e78-114">CAPTUREFILTER\_ FLAGS\_INCLUDE\_ ALL\_SAPS</span></span>   | <span data-ttu-id="73e78-115">Passa tutti i valori SAP e notifica al driver che tutti i valori SAP sono validi.</span><span class="sxs-lookup"><span data-stu-id="73e78-115">Passes all SAP values and notifies the driver that all SAP values are valid.</span></span> <span data-ttu-id="73e78-116">Se combinato con qualsiasi valore nel membro **lpSapTable** , questo flag notifica al driver che tutti i valori SAP ad eccezione di quelli presenti in **lpSapTable** sono validi.</span><span class="sxs-lookup"><span data-stu-id="73e78-116">If combined with any values in the **lpSapTable** member, this flag notifies the driver that all SAP values except those in the **lpSapTable** are valid.</span></span><br/>           |
| <span data-ttu-id="73e78-117">\_i flag capturefilter \_ includono \_ tutti \_ etype del</span><span class="sxs-lookup"><span data-stu-id="73e78-117">CAPTUREFILTER\_ FLAGS\_INCLUDE\_ ALL\_ETYPES</span></span> | <span data-ttu-id="73e78-118">Passa tutti i valori di etype e notifica al driver che tutti i valori di ETYPE sono validi.</span><span class="sxs-lookup"><span data-stu-id="73e78-118">Passes all Etype values and notifies the driver that all Etype values are valid.</span></span> <span data-ttu-id="73e78-119">Se combinato con qualsiasi valore nel membro **lpEtypeTable** , questo flag notifica al driver che tutti i valori ETYPE ad eccezione di quelli nel **lpEtypeTable** sono validi.</span><span class="sxs-lookup"><span data-stu-id="73e78-119">If combined with any values in the **lpEtypeTable** member, this flag notifies the driver that all Etype values except those in the **lpEtypeTable** are valid.</span></span><br/> |
| <span data-ttu-id="73e78-120">\_flag capturefilter \_ \_ solo locale</span><span class="sxs-lookup"><span data-stu-id="73e78-120">CAPTUREFILTER\_ FLAGS\_LOCAL\_ONLY</span></span>           | <span data-ttu-id="73e78-121">Se si imposta questo flag, una scheda di interfaccia di rete non verrà impostata su P-mode.</span><span class="sxs-lookup"><span data-stu-id="73e78-121">Setting this flag will not set a NIC to P-Mode.</span></span> <span data-ttu-id="73e78-122">Viene visualizzato solo il traffico locale (tutti i frame nel computer locale).</span><span class="sxs-lookup"><span data-stu-id="73e78-122">You will only see local traffic (any frames to the local machine).</span></span>                                                                                                                                          |
| <span data-ttu-id="73e78-123">\_flag capturefilter \_ Keep \_ RAW</span><span class="sxs-lookup"><span data-stu-id="73e78-123">CAPTUREFILTER\_ FLAGS\_KEEP\_RAW</span></span>             | <span data-ttu-id="73e78-124">Mantiene i frame MAC SMT e token ring.</span><span class="sxs-lookup"><span data-stu-id="73e78-124">Keeps SMT and Token Ring MAC frames.</span></span>                                                                                                                                                                                                                        |



 

## <a name="etypesap-capture-filter-settings"></a><span data-ttu-id="73e78-125">Impostazioni del filtro di acquisizione di ETYPE/SAP</span><span class="sxs-lookup"><span data-stu-id="73e78-125">Etype/SAP Capture Filter Settings</span></span>

<span data-ttu-id="73e78-126">Usare le informazioni seguenti per impostare i membri **lpSapTable** e **LpEtypeTable** della struttura [**capturefilter**](capturefilter.md) .</span><span class="sxs-lookup"><span data-stu-id="73e78-126">Use the following information to set the **lpSapTable** and **lpEtypeTable** members of the [**CAPTUREFILTER**](capturefilter.md) structure.</span></span>



| <span data-ttu-id="73e78-127">Impostazione</span><span class="sxs-lookup"><span data-stu-id="73e78-127">Setting</span></span>          | <span data-ttu-id="73e78-128">Significato</span><span class="sxs-lookup"><span data-stu-id="73e78-128">Meaning</span></span>                                                                                                                                                                                                                                                              |
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="73e78-129">**lpSapTable**</span><span class="sxs-lookup"><span data-stu-id="73e78-129">**lpSapTable**</span></span>   | <span data-ttu-id="73e78-130">Elenca i valori SAP che si desidera vengano passati dal driver.</span><span class="sxs-lookup"><span data-stu-id="73e78-130">Lists the SAP values that you want the driver to pass.</span></span> <span data-ttu-id="73e78-131">Questo elenco indica al driver Network Monitor di convalidare tutti i frame che contengono una corrispondenza.</span><span class="sxs-lookup"><span data-stu-id="73e78-131">This list tells the Network Monitor driver to validate any frame that contains a match.</span></span> <span data-ttu-id="73e78-132">Se \_ i flag capturefilter \_ includono \_ tutti i \_ succhi sono impostati, questo diventa un elenco di eccezioni (se trovato, non passare).</span><span class="sxs-lookup"><span data-stu-id="73e78-132">If CAPTUREFILTER\_FLAGS\_INCLUDE\_ALL\_SAPS is set, this becomes an exception list (if found, do not pass).</span></span>           |
| <span data-ttu-id="73e78-133">**lpEtypeTable**</span><span class="sxs-lookup"><span data-stu-id="73e78-133">**lpEtypeTable**</span></span> | <span data-ttu-id="73e78-134">Elenca i valori ETYPE che si desidera vengano passati dal driver Network Monitor.</span><span class="sxs-lookup"><span data-stu-id="73e78-134">Lists the Etype values that you want the Network Monitor driver to pass.</span></span> <span data-ttu-id="73e78-135">Questo elenco indica solo al driver di convalidare i frame che contengono una corrispondenza.</span><span class="sxs-lookup"><span data-stu-id="73e78-135">This list alone tells the driver to validate any frame that contains a match.</span></span> <span data-ttu-id="73e78-136">Se \_ i flag capturefilter \_ includono \_ tutti i \_ etype del impostati, questo diventa un elenco di eccezioni (se trovato, non passare).</span><span class="sxs-lookup"><span data-stu-id="73e78-136">If CAPTUREFILTER\_FLAGS\_INCLUDE\_ALL\_ETYPES is set, this becomes an exception list (if found, do not pass).</span></span> |



 

 

 




