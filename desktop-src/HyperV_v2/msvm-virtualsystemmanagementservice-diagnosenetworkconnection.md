---
description: Diagnostica la connettività di rete di una macchina virtuale in un ambiente di virtualizzazione rete Windows.
ms.assetid: c18f48bf-1f57-4a23-a495-462afad42750
title: Metodo DiagnoseNetworkConnection della classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.DiagnoseNetworkConnection
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 70760f771e3908265a4ac70ebc1cbdf957d652c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306009"
---
# <a name="diagnosenetworkconnection-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="540f0-103">Metodo DiagnoseNetworkConnection della classe MSVM \_ VirtualSystemManagementService</span><span class="sxs-lookup"><span data-stu-id="540f0-103">DiagnoseNetworkConnection method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="540f0-104">Diagnostica la connettività di rete di una macchina virtuale in un ambiente di virtualizzazione rete Windows.</span><span class="sxs-lookup"><span data-stu-id="540f0-104">Diagnoses the network connectivity of a VM in a Windows Network Virtualization Environment.</span></span>

## <a name="syntax"></a><span data-ttu-id="540f0-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="540f0-105">Syntax</span></span>


```mof
uint32 DiagnoseNetworkConnection(
  [in]  Msvm_EthernetPortAllocationSettingData REF TargetNetworkAdapter,
  [in]  string                                     DiagnosticSettings,
  [out] string                                     DiagnosticInformation,
  [out] CIM_ConcreteJob                        REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="540f0-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="540f0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="540f0-107">*TargetNetworkAdapter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="540f0-107">*TargetNetworkAdapter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="540f0-108">Riferimento a un [**\_ EthernetPortAllocationSettingData MSVM**](msvm-ethernetportallocationsettingdata.md) che descrive la scheda di rete di destinazione.</span><span class="sxs-lookup"><span data-stu-id="540f0-108">Reference to an [**Msvm\_EthernetPortAllocationSettingData**](msvm-ethernetportallocationsettingdata.md) that describes the target network adapter.</span></span>

</dd> <dt>

<span data-ttu-id="540f0-109">*DiagnosticSettings* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="540f0-109">*DiagnosticSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="540f0-110">Impostazioni di diagnostica da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="540f0-110">The diagnostic settings to use.</span></span>

</dd> <dt>

<span data-ttu-id="540f0-111">*DiagnosticInformation* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="540f0-111">*DiagnosticInformation* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="540f0-112">Se l'operazione riesce, restituisce le informazioni di diagnostica.</span><span class="sxs-lookup"><span data-stu-id="540f0-112">On success, returns the diagnostic information.</span></span>

</dd> <dt>

<span data-ttu-id="540f0-113">*Processo* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="540f0-113">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="540f0-114">Se l'operazione viene eseguita in modo asincrono, questo metodo restituirà 4096 e questo parametro conterrà un riferimento a un oggetto derivato da [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="540f0-114">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="540f0-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="540f0-115">Return value</span></span>

<span data-ttu-id="540f0-116">Restituisce 0 o 4096 in caso di esito positivo. in caso contrario, restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="540f0-116">Returns a 0 or 4096 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="540f0-117">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="540f0-117">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="540f0-118">**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="540f0-118">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="540f0-119">**Non riuscito** (2)</span><span class="sxs-lookup"><span data-stu-id="540f0-119">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="540f0-120">**Timeout** (3)</span><span class="sxs-lookup"><span data-stu-id="540f0-120">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="540f0-121">**Parametro non valido** (4)</span><span class="sxs-lookup"><span data-stu-id="540f0-121">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="540f0-122">**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="540f0-122">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="540f0-123">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="540f0-123">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="540f0-124">**Metodo riservato** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="540f0-124">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="540f0-125">**Specifico del fornitore** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="540f0-125">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="540f0-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="540f0-126">Requirements</span></span>



| <span data-ttu-id="540f0-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="540f0-127">Requirement</span></span> | <span data-ttu-id="540f0-128">Valore</span><span class="sxs-lookup"><span data-stu-id="540f0-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="540f0-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="540f0-129">Minimum supported client</span></span><br/> | <span data-ttu-id="540f0-130">Solo app desktop Windows 10 versione 1703 \[\]</span><span class="sxs-lookup"><span data-stu-id="540f0-130">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="540f0-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="540f0-131">Minimum supported server</span></span><br/> | <span data-ttu-id="540f0-132">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="540f0-132">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="540f0-133">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="540f0-133">Namespace</span></span><br/>                | <span data-ttu-id="540f0-134">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="540f0-134">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="540f0-135">MOF</span><span class="sxs-lookup"><span data-stu-id="540f0-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="540f0-136"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="540f0-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="540f0-137">DLL</span><span class="sxs-lookup"><span data-stu-id="540f0-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="540f0-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="540f0-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="540f0-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="540f0-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="540f0-140">**\_VirtualSystemManagementService MSVM**</span><span class="sxs-lookup"><span data-stu-id="540f0-140">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

