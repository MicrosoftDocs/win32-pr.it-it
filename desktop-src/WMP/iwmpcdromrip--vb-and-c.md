---
title: Interfaccia IWMPCdromRip (VB e C) (WMP. h)
description: Fornisce le proprietà e i metodi per gestire la copia, o il ripping, di tracce da un CD audio. il ritaglio di un CD usando l'interfaccia IWMPCdromRip ha lo stesso effetto del ripping della musica usando l'interfaccia utente di Windows Media Player.
ms.assetid: d7fbfc68-61b5-45bf-8df5-e3125a51a4d8
keywords:
- Interfaccia IWMPCdromRip (VB e C) Windows Media Player
- Interfaccia IWMPCdromRip (VB e C) Windows Media Player, descritta
topic_type:
- apiref
api_name:
- IWMPCdromRip (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d069fd8bd727d6a2a380c2ef29ce7c086db88d0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328219"
---
# <a name="iwmpcdromrip-vb-and-c-interface"></a><span data-ttu-id="45f40-105">Interfaccia IWMPCdromRip (VB e C#)</span><span class="sxs-lookup"><span data-stu-id="45f40-105">IWMPCdromRip (VB and C#) interface</span></span>

<span data-ttu-id="45f40-106">Fornisce le proprietà e i metodi per gestire la copia, o l' *estrazione*, di tracce da un CD audio.</span><span class="sxs-lookup"><span data-stu-id="45f40-106">Provides properties and methods to manage copying, or *ripping*, tracks from an audio CD.</span></span>

<span data-ttu-id="45f40-107">La copia di un CD usando l'interfaccia **IWMPCdromRip** ha lo stesso effetto del ritaglio di musica usando l'interfaccia utente di Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="45f40-107">Ripping a CD by using the **IWMPCdromRip** interface has the same effect as ripping music by using the Windows Media Player user interface.</span></span> <span data-ttu-id="45f40-108">Il contenuto Ripped viene aggiunto automaticamente alla libreria in base alle preferenze dell'utente.</span><span class="sxs-lookup"><span data-stu-id="45f40-108">Ripped content is automatically added to the library according to the user's preferences.</span></span> <span data-ttu-id="45f40-109">Per ulteriori informazioni sulle preferenze utente per il ritaglio di CD, vedere la sezione relativa alla copia di musica da CDs nella Guida di Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="45f40-109">For more information about user preferences for CD ripping, see "Ripping music from CDs" in Windows Media Player Help.</span></span>

<span data-ttu-id="45f40-110">L'interfaccia **IWMPCdromRip** espone le proprietà seguenti.</span><span class="sxs-lookup"><span data-stu-id="45f40-110">The **IWMPCdromRip** interface exposes the following properties.</span></span>

## <a name="members"></a><span data-ttu-id="45f40-111">Membri</span><span class="sxs-lookup"><span data-stu-id="45f40-111">Members</span></span>

<span data-ttu-id="45f40-112">L'interfaccia **IWMPCdromRip (VB e C#)** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="45f40-112">The **IWMPCdromRip (VB and C#)** interface has these types of members:</span></span>

-   [<span data-ttu-id="45f40-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="45f40-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="45f40-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="45f40-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="45f40-115">Metodi</span><span class="sxs-lookup"><span data-stu-id="45f40-115">Methods</span></span>

<span data-ttu-id="45f40-116">L'interfaccia **IWMPCdromRip (VB e C#)** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="45f40-116">The **IWMPCdromRip (VB and C#)** interface has these methods.</span></span>



| <span data-ttu-id="45f40-117">Metodo</span><span class="sxs-lookup"><span data-stu-id="45f40-117">Method</span></span>                                                                 | <span data-ttu-id="45f40-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="45f40-118">Description</span></span>                              |
|:-----------------------------------------------------------------------|:-----------------------------------------|
| [<span data-ttu-id="45f40-119">**startRip**</span><span class="sxs-lookup"><span data-stu-id="45f40-119">**startRip**</span></span>](wmplibiwmpcdromrip-iwmpcdromrip-startrip--vb-and-c.md) | <span data-ttu-id="45f40-120">Estrae il CD.</span><span class="sxs-lookup"><span data-stu-id="45f40-120">Rips the CD.</span></span><br/>                  |
| [<span data-ttu-id="45f40-121">**stopRip**</span><span class="sxs-lookup"><span data-stu-id="45f40-121">**stopRip**</span></span>](wmplibiwmpcdromrip-iwmpcdromrip-stoprip--vb-and-c.md)   | <span data-ttu-id="45f40-122">Arresta il processo di ripping del CD.</span><span class="sxs-lookup"><span data-stu-id="45f40-122">Stops the CD ripping process.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="45f40-123">Proprietà</span><span class="sxs-lookup"><span data-stu-id="45f40-123">Properties</span></span>

<span data-ttu-id="45f40-124">L'interfaccia **IWMPCdromRip (VB e C#)** presenta queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="45f40-124">The **IWMPCdromRip (VB and C#)** interface has these properties.</span></span>



| <span data-ttu-id="45f40-125">Proprietà</span><span class="sxs-lookup"><span data-stu-id="45f40-125">Property</span></span>                                                                                | <span data-ttu-id="45f40-126">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="45f40-126">Access type</span></span>          | <span data-ttu-id="45f40-127">Descrizione</span><span class="sxs-lookup"><span data-stu-id="45f40-127">Description</span></span>                                                                                   |
|:----------------------------------------------------------------------------------------|:---------------------|:----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="45f40-128">**ripProgress**</span><span class="sxs-lookup"><span data-stu-id="45f40-128">**ripProgress**</span></span>](wmplibiwmpcdromrip-iwmpcdromrip-ripprogress--vb-and-c.md)<br/> | <span data-ttu-id="45f40-129">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="45f40-129">Read-only</span></span><br/> | <span data-ttu-id="45f40-130">Ottiene lo stato di ripping del CD come percentuale di completamento.</span><span class="sxs-lookup"><span data-stu-id="45f40-130">Gets the CD ripping progress as percent complete.</span></span><br/>                                  |
| [<span data-ttu-id="45f40-131">**ripState**</span><span class="sxs-lookup"><span data-stu-id="45f40-131">**ripState**</span></span>](wmplibiwmpcdromrip-iwmpcdromrip-ripstate--vb-and-c.md)<br/>       | <span data-ttu-id="45f40-132">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="45f40-132">Read-only</span></span><br/> | <span data-ttu-id="45f40-133">Ottiene un valore di enumerazione che indica lo stato corrente del processo di estrazione.</span><span class="sxs-lookup"><span data-stu-id="45f40-133">Gets an enumeration value that indicates the current state of the ripping process.</span></span><br/> |



 

<span data-ttu-id="45f40-134">Ottenere un'interfaccia **IWMPCdromRip** eseguendo il cast dell'interfaccia **IWMPCdrom** del CD che si vuole copiare.</span><span class="sxs-lookup"><span data-stu-id="45f40-134">Get an **IWMPCdromRip** interface by casting the **IWMPCdrom** interface of the CD that you wish to rip.</span></span>

## <a name="requirements"></a><span data-ttu-id="45f40-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="45f40-135">Requirements</span></span>



| <span data-ttu-id="45f40-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="45f40-136">Requirement</span></span> | <span data-ttu-id="45f40-137">Valore</span><span class="sxs-lookup"><span data-stu-id="45f40-137">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="45f40-138">Intestazione</span><span class="sxs-lookup"><span data-stu-id="45f40-138">Header</span></span><br/> | <dl> <span data-ttu-id="45f40-139"><dt>WMP. h</dt></span><span class="sxs-lookup"><span data-stu-id="45f40-139"><dt>Wmp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="45f40-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="45f40-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45f40-141">**Interfacce per Visual Basic .NET e C #**</span><span class="sxs-lookup"><span data-stu-id="45f40-141">**Interfaces for Visual Basic .NET and C#**</span></span>](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[<span data-ttu-id="45f40-142">**Copia di un CD**</span><span class="sxs-lookup"><span data-stu-id="45f40-142">**Ripping a CD**</span></span>](ripping-a-cd.md)
</dt> </dl>

 

 





