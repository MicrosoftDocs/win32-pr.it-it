---
title: Interfaccia ITsSbTargetEx
description: Espone le proprietà che archiviano le informazioni di configurazione e di stato relative a una destinazione.
ms.assetid: 3f0f26fb-e8bc-47eb-8038-e51792ad4376
ms.tgt_platform: multiple
keywords:
- Interfaccia ITsSbTargetEx Servizi Desktop remoto
- Interfaccia ITsSbTargetEx Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- ITsSbTargetEx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d53d126d9419f87d91b027b0d69847f67de84be6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964881"
---
# <a name="itssbtargetex-interface"></a><span data-ttu-id="a70f6-105">Interfaccia ITsSbTargetEx</span><span class="sxs-lookup"><span data-stu-id="a70f6-105">ITsSbTargetEx interface</span></span>

<span data-ttu-id="a70f6-106">Espone le proprietà che archiviano le informazioni di configurazione e di stato relative a una destinazione.</span><span class="sxs-lookup"><span data-stu-id="a70f6-106">Exposes properties that store configuration and state information about a target.</span></span>

<span data-ttu-id="a70f6-107">Questa interfaccia è disponibile solo in Windows Server 2012 R2 con [KB3091411](https://support.microsoft.com/kb/3091411) installato.</span><span class="sxs-lookup"><span data-stu-id="a70f6-107">This interface is only available on Windows Server 2012 R2 with [KB3091411](https://support.microsoft.com/kb/3091411) installed.</span></span> <span data-ttu-id="a70f6-108">La proprietà [**TargetLoad**](itssbtarget-targetload.md) dell'interfaccia [**ITsSbTarget**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget) è disponibile a partire da Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="a70f6-108">The [**TargetLoad**](itssbtarget-targetload.md) property of the [**ITsSbTarget**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget) interface is available starting with Windows Server 2016.</span></span>

## <a name="members"></a><span data-ttu-id="a70f6-109">Membri</span><span class="sxs-lookup"><span data-stu-id="a70f6-109">Members</span></span>

<span data-ttu-id="a70f6-110">L'interfaccia **ITsSbTargetEx** eredita da [**ITsSbTarget**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget).</span><span class="sxs-lookup"><span data-stu-id="a70f6-110">The **ITsSbTargetEx** interface inherits from [**ITsSbTarget**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget).</span></span> <span data-ttu-id="a70f6-111">**ITsSbTargetEx** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="a70f6-111">**ITsSbTargetEx** also has these types of members:</span></span>

-   [<span data-ttu-id="a70f6-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="a70f6-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a70f6-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="a70f6-113">Properties</span></span>

<span data-ttu-id="a70f6-114">L'interfaccia **ITsSbTargetEx** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="a70f6-114">The **ITsSbTargetEx** interface has these properties.</span></span>



| <span data-ttu-id="a70f6-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="a70f6-115">Property</span></span>                                                                      | <span data-ttu-id="a70f6-116">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="a70f6-116">Access type</span></span>           | <span data-ttu-id="a70f6-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a70f6-117">Description</span></span>                                                                               |
|:------------------------------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a70f6-118">**EnvironmentName**</span><span class="sxs-lookup"><span data-stu-id="a70f6-118">**EnvironmentName**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtarget-get_environmentname)<br/>             | <span data-ttu-id="a70f6-119">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="a70f6-119">Read/write</span></span><br/> | <span data-ttu-id="a70f6-120">Recupera o specifica il nome dell'ambiente associato alla destinazione.</span><span class="sxs-lookup"><span data-stu-id="a70f6-120">Retrieves or specifies the name of the environment associated with the target.</span></span><br/> |
| [<span data-ttu-id="a70f6-121">**Farmname**</span><span class="sxs-lookup"><span data-stu-id="a70f6-121">**FarmName**</span></span>](itssbtarget-farmname.md)<br/>                           | <span data-ttu-id="a70f6-122">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="a70f6-122">Read/write</span></span><br/> | <span data-ttu-id="a70f6-123">Specifica o Recupera il nome della farm a cui viene unita la destinazione.</span><span class="sxs-lookup"><span data-stu-id="a70f6-123">Specifies or retrieves the name of the farm to which this target is joined.</span></span><br/>    |
| [<span data-ttu-id="a70f6-124">**IpAddresses**</span><span class="sxs-lookup"><span data-stu-id="a70f6-124">**IpAddresses**</span></span>](itssbtarget-ipaddresses.md)<br/>                     | <span data-ttu-id="a70f6-125">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="a70f6-125">Read/write</span></span><br/> | <span data-ttu-id="a70f6-126">Recupera o specifica gli indirizzi IP esterni della destinazione.</span><span class="sxs-lookup"><span data-stu-id="a70f6-126">Retrieves or specifies the external IP addresses of the target.</span></span><br/>                |
| [<span data-ttu-id="a70f6-127">**NumPendingConnections**</span><span class="sxs-lookup"><span data-stu-id="a70f6-127">**NumPendingConnections**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtarget-get_numpendingconnections)<br/> | <span data-ttu-id="a70f6-128">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="a70f6-128">Read-only</span></span><br/>  | <span data-ttu-id="a70f6-129">Recupera il numero di connessioni utente in sospeso per la destinazione.</span><span class="sxs-lookup"><span data-stu-id="a70f6-129">Retrieves the number of pending user connections for the target.</span></span><br/>               |
| [<span data-ttu-id="a70f6-130">**NumSessions**</span><span class="sxs-lookup"><span data-stu-id="a70f6-130">**NumSessions**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtarget-get_numsessions)<br/>                     | <span data-ttu-id="a70f6-131">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="a70f6-131">Read-only</span></span><br/>  | <span data-ttu-id="a70f6-132">Recupera il numero di sessioni gestite da Service Broker per la destinazione.</span><span class="sxs-lookup"><span data-stu-id="a70f6-132">Retrieves the number of sessions maintained by broker for the target.</span></span><br/>          |
| [<span data-ttu-id="a70f6-133">**TargetFQDN**</span><span class="sxs-lookup"><span data-stu-id="a70f6-133">**TargetFQDN**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtarget-get_targetfqdn)<br/>                       | <span data-ttu-id="a70f6-134">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="a70f6-134">Read/write</span></span><br/> | <span data-ttu-id="a70f6-135">Specifica o Recupera il nome di dominio completo della destinazione.</span><span class="sxs-lookup"><span data-stu-id="a70f6-135">Specifies or retrieves the fully qualified domain name of the target.</span></span><br/>          |
| <span data-ttu-id="a70f6-136">[**TargetLoad**](/previous-versions/windows/desktop/legacy/mt703468(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a70f6-136">[**TargetLoad**](/previous-versions/windows/desktop/legacy/mt703468(v=vs.85))</span></span><br/>                     | <span data-ttu-id="a70f6-137">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="a70f6-137">Read-only</span></span><br/>  | <span data-ttu-id="a70f6-138">Recupera il carico relativo in una destinazione.</span><span class="sxs-lookup"><span data-stu-id="a70f6-138">Retrieves the relative load on a target.</span></span><br/>                                       |
| [<span data-ttu-id="a70f6-139">**TargetName**</span><span class="sxs-lookup"><span data-stu-id="a70f6-139">**TargetName**</span></span>](itssbtarget-targetname.md)<br/>                       | <span data-ttu-id="a70f6-140">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="a70f6-140">Read/write</span></span><br/> | <span data-ttu-id="a70f6-141">Specifica o Recupera il nome della destinazione.</span><span class="sxs-lookup"><span data-stu-id="a70f6-141">Specifies or retrieves the name of the target.</span></span><br/>                                 |
| [<span data-ttu-id="a70f6-142">**TargetNetbios**</span><span class="sxs-lookup"><span data-stu-id="a70f6-142">**TargetNetbios**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtarget-get_targetnetbios)<br/>                 | <span data-ttu-id="a70f6-143">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="a70f6-143">Read/write</span></span><br/> | <span data-ttu-id="a70f6-144">Specifica o Recupera il nome NetBIOS della destinazione.</span><span class="sxs-lookup"><span data-stu-id="a70f6-144">Specifies or retrieves the NetBIOS name of the target.</span></span><br/>                         |
| [<span data-ttu-id="a70f6-145">**TargetPropertySet**</span><span class="sxs-lookup"><span data-stu-id="a70f6-145">**TargetPropertySet**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtarget-get_targetpropertyset)<br/>         | <span data-ttu-id="a70f6-146">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="a70f6-146">Read/write</span></span><br/> | <span data-ttu-id="a70f6-147">Specifica o Recupera il set di proprietà per la destinazione.</span><span class="sxs-lookup"><span data-stu-id="a70f6-147">Specifies or retrieves the property set for the target.</span></span><br/>                        |
| [<span data-ttu-id="a70f6-148">**TargetState**</span><span class="sxs-lookup"><span data-stu-id="a70f6-148">**TargetState**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtarget-get_targetstate)<br/>                     | <span data-ttu-id="a70f6-149">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="a70f6-149">Read/write</span></span><br/> | <span data-ttu-id="a70f6-150">Specifica o recupera lo stato di destinazione.</span><span class="sxs-lookup"><span data-stu-id="a70f6-150">Specifies or retrieves the target state.</span></span><br/>                                       |



 

## <a name="requirements"></a><span data-ttu-id="a70f6-151">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a70f6-151">Requirements</span></span>



| <span data-ttu-id="a70f6-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="a70f6-152">Requirement</span></span> | <span data-ttu-id="a70f6-153">Valore</span><span class="sxs-lookup"><span data-stu-id="a70f6-153">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="a70f6-154">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a70f6-154">Minimum supported client</span></span><br/> | <span data-ttu-id="a70f6-155">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="a70f6-155">None supported</span></span><br/>                                                        |
| <span data-ttu-id="a70f6-156">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a70f6-156">Minimum supported server</span></span><br/> | <span data-ttu-id="a70f6-157">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="a70f6-157">Windows Server 2012 R2</span></span><br/>                                                |
| <span data-ttu-id="a70f6-158">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="a70f6-158">End of server support</span></span><br/>    | <span data-ttu-id="a70f6-159">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="a70f6-159">Windows Server 2012 R2</span></span><br/>                                                |
| <span data-ttu-id="a70f6-160">IID</span><span class="sxs-lookup"><span data-stu-id="a70f6-160">IID</span></span><br/>                      | <span data-ttu-id="a70f6-161">IID \_ ITsSbTargetEx è definito come 74f99987-625d-11e5-bea1-a0481c7e9064</span><span class="sxs-lookup"><span data-stu-id="a70f6-161">IID\_ITsSbTargetEx is defined as 74f99987-625d-11e5-bea1-a0481c7e9064</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a70f6-162">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a70f6-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a70f6-163">**ITsSbTarget**</span><span class="sxs-lookup"><span data-stu-id="a70f6-163">**ITsSbTarget**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget)
</dt> <dt>

[<span data-ttu-id="a70f6-164">Interfacce di virtualizzazione Desktop remoto</span><span class="sxs-lookup"><span data-stu-id="a70f6-164">Remote Desktop Virtualization Interfaces</span></span>](remote-desktop-virtualization-interfaces.md)
</dt> </dl>

 

