---
description: Configura le impostazioni IP delle schede di rete da applicare a una macchina virtuale dopo un failover.
ms.assetid: a49d089e-f5dc-4bfb-9f66-2593304b9795
title: Metodo SetFailoverNetworkAdapterSettings della classe Msvm_ReplicationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.SetFailoverNetworkAdapterSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: da5bb8c820e1dbca5103c430a7b2ce2a525a8fca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311770"
---
# <a name="setfailovernetworkadaptersettings-method-of-the-msvm_replicationservice-class"></a><span data-ttu-id="1204d-103">Metodo SetFailoverNetworkAdapterSettings della classe MSVM \_ ReplicationService</span><span class="sxs-lookup"><span data-stu-id="1204d-103">SetFailoverNetworkAdapterSettings method of the Msvm\_ReplicationService class</span></span>

<span data-ttu-id="1204d-104">Configura le impostazioni IP della scheda di rete da applicare a una macchina virtuale dopo un failover.</span><span class="sxs-lookup"><span data-stu-id="1204d-104">Configures the network adapter's IP settings to be applied to a virtual machine after a failover.</span></span> <span data-ttu-id="1204d-105">Questi parametri di configurazione vengono applicati dopo un'operazione di failover, immediatamente dopo aver stabilito la comunicazione con il componente di integrazione di Exchange per KVP in esecuzione nel sistema operativo guest.</span><span class="sxs-lookup"><span data-stu-id="1204d-105">These configuration parameters are applied after a failover operation, immediately upon establishing communication with the KVP Exchange integration component running within the guest operating system.</span></span>

## <a name="syntax"></a><span data-ttu-id="1204d-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1204d-106">Syntax</span></span>


```mof
uint32 SetFailoverNetworkAdapterSettings(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  string                 NetworkSettings[],
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="1204d-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="1204d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1204d-108">*ComputerSystem* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1204d-108">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1204d-109">Riferimento a un'istanza di [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) che rappresenta la macchina virtuale di cui devono essere configurate le schede di rete.</span><span class="sxs-lookup"><span data-stu-id="1204d-109">A reference to a [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) instance that represents the virtual machine whose network adapters are to be configured.</span></span>

</dd> <dt>

<span data-ttu-id="1204d-110">*NetworkSettings* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1204d-110">*NetworkSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1204d-111">Matrice di istanze incorporate di [**oggetti \_ FailoverNetworkAdapterSettingData di MSVM**](msvm-failovernetworkadaptersettingdata.md) .</span><span class="sxs-lookup"><span data-stu-id="1204d-111">An array of embedded instances of [**Msvm\_FailoverNetworkAdapterSettingData**](msvm-failovernetworkadaptersettingdata.md) objects.</span></span> <span data-ttu-id="1204d-112">Ogni istanza descrive i parametri di configurazione per una delle schede di rete all'interno della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="1204d-112">Each instance describes the configuration parameters for one of the network adapters within the virtual machine.</span></span> <span data-ttu-id="1204d-113">È necessario specificare le proprietà **IPAddresses** e **DHCPEnabled** in ogni istanza.</span><span class="sxs-lookup"><span data-stu-id="1204d-113">The **IPAddresses** and **DHCPEnabled** properties must be specified on each instance.</span></span>

</dd> <dt>

<span data-ttu-id="1204d-114">*Processo* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="1204d-114">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1204d-115">Se l'operazione viene eseguita in modo asincrono, questo metodo restituirà 4096 e questo parametro conterrà un riferimento a un oggetto derivato da [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="1204d-115">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1204d-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1204d-116">Return value</span></span>

<span data-ttu-id="1204d-117">Questo metodo restituisce uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="1204d-117">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="1204d-118">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="1204d-118">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="1204d-119">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="1204d-119">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="1204d-120">**Non riuscito** (32768)</span><span class="sxs-lookup"><span data-stu-id="1204d-120">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="1204d-121">**Accesso negato** (32769)</span><span class="sxs-lookup"><span data-stu-id="1204d-121">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="1204d-122">**Non supportato** (32770)</span><span class="sxs-lookup"><span data-stu-id="1204d-122">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="1204d-123">**Stato sconosciuto** (32771)</span><span class="sxs-lookup"><span data-stu-id="1204d-123">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="1204d-124">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="1204d-124">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="1204d-125">**Parametro non valido** (32773)</span><span class="sxs-lookup"><span data-stu-id="1204d-125">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="1204d-126">Il **sistema è in uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="1204d-126">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="1204d-127">**Stato non valido per l'operazione** (32775)</span><span class="sxs-lookup"><span data-stu-id="1204d-127">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="1204d-128">**Tipo di dati non corretto** (32776)</span><span class="sxs-lookup"><span data-stu-id="1204d-128">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="1204d-129">**Sistema non disponibile** (32777)</span><span class="sxs-lookup"><span data-stu-id="1204d-129">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="1204d-130">**Memoria insufficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="1204d-130">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="1204d-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1204d-131">Requirements</span></span>



| <span data-ttu-id="1204d-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="1204d-132">Requirement</span></span> | <span data-ttu-id="1204d-133">Valore</span><span class="sxs-lookup"><span data-stu-id="1204d-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1204d-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1204d-134">Minimum supported client</span></span><br/> | <span data-ttu-id="1204d-135">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="1204d-135">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="1204d-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1204d-136">Minimum supported server</span></span><br/> | <span data-ttu-id="1204d-137">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="1204d-137">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1204d-138">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="1204d-138">Namespace</span></span><br/>                | <span data-ttu-id="1204d-139">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="1204d-139">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="1204d-140">MOF</span><span class="sxs-lookup"><span data-stu-id="1204d-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1204d-141"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1204d-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="1204d-142">DLL</span><span class="sxs-lookup"><span data-stu-id="1204d-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1204d-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="1204d-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="1204d-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1204d-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1204d-145">**InitiateFailover**</span><span class="sxs-lookup"><span data-stu-id="1204d-145">**InitiateFailover**</span></span>](initiatefailover-msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="1204d-146">**\_ReplicationService MSVM**</span><span class="sxs-lookup"><span data-stu-id="1204d-146">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> <dt>

[<span data-ttu-id="1204d-147">**RevertFailover**</span><span class="sxs-lookup"><span data-stu-id="1204d-147">**RevertFailover**</span></span>](revertfailover-msvm-replicationservice.md)
</dt> </dl>

 

