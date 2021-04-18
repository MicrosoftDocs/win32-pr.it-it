---
description: Configura le schede di rete all'interno del sistema operativo guest.
ms.assetid: 698e0c17-f8bd-433f-b982-5481f9701ba6
title: Metodo SetGuestNetworkAdapterConfiguration della classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.SetGuestNetworkAdapterConfiguration
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 02c79df7aa08faa842e2b702b4cf18944e96bdfe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104529041"
---
# <a name="setguestnetworkadapterconfiguration-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="2c7a7-103">Metodo SetGuestNetworkAdapterConfiguration della classe MSVM \_ VirtualSystemManagementService</span><span class="sxs-lookup"><span data-stu-id="2c7a7-103">SetGuestNetworkAdapterConfiguration method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="2c7a7-104">Configura le schede di rete all'interno del sistema operativo guest.</span><span class="sxs-lookup"><span data-stu-id="2c7a7-104">Configures the network adapters within the guest operating system.</span></span> <span data-ttu-id="2c7a7-105">Questi parametri di configurazione vengono applicati immediatamente dopo aver stabilito la comunicazione con il componente di integrazione di KVP Exchange in esecuzione nel sistema operativo guest.</span><span class="sxs-lookup"><span data-stu-id="2c7a7-105">These configuration parameters are applied immediately upon establishing communication with the KVP Exchange integration component running within the guest operating system.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c7a7-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2c7a7-106">Syntax</span></span>


```mof
uint32 SetGuestNetworkAdapterConfiguration(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  string                 NetworkConfiguration[],
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="2c7a7-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="2c7a7-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2c7a7-108">*ComputerSystem* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2c7a7-108">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2c7a7-109">Riferimento all'istanza [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) di cui devono essere configurate le schede di rete.</span><span class="sxs-lookup"><span data-stu-id="2c7a7-109">A reference to the [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) instance whose network adapters are to be configured.</span></span>

</dd> <dt>

<span data-ttu-id="2c7a7-110">*NetworkConfiguration* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2c7a7-110">*NetworkConfiguration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2c7a7-111">Matrice di istanze incorporate della classe [**MSVM \_ GuestNetworkAdapterConfiguration**](msvm-guestnetworkadapterconfiguration.md) .</span><span class="sxs-lookup"><span data-stu-id="2c7a7-111">An array of embedded instances of the [**Msvm\_GuestNetworkAdapterConfiguration**](msvm-guestnetworkadapterconfiguration.md) class.</span></span> <span data-ttu-id="2c7a7-112">Ogni istanza descrive i parametri di configurazione per una delle schede di rete all'interno della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="2c7a7-112">Each instance describes the configuration parameters for one of the network adapters within the virtual machine.</span></span> <span data-ttu-id="2c7a7-113">È necessario specificare la proprietà **DHCPEnabled** per ogni istanza.</span><span class="sxs-lookup"><span data-stu-id="2c7a7-113">The **DHCPEnabled** property must be specified for each instance.</span></span>

</dd> <dt>

<span data-ttu-id="2c7a7-114">*Processo* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="2c7a7-114">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2c7a7-115">Se l'operazione viene eseguita in modo asincrono, questo metodo restituirà 4096 e questo parametro conterrà un riferimento a un oggetto derivato da [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="2c7a7-115">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2c7a7-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2c7a7-116">Return value</span></span>

<span data-ttu-id="2c7a7-117">Questo metodo restituisce uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="2c7a7-117">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="2c7a7-118">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="2c7a7-118">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="2c7a7-119">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="2c7a7-119">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="2c7a7-120">**Non riuscito** (32768)</span><span class="sxs-lookup"><span data-stu-id="2c7a7-120">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="2c7a7-121">**Accesso negato** (32769)</span><span class="sxs-lookup"><span data-stu-id="2c7a7-121">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="2c7a7-122">**Non supportato** (32770)</span><span class="sxs-lookup"><span data-stu-id="2c7a7-122">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="2c7a7-123">**Stato sconosciuto** (32771)</span><span class="sxs-lookup"><span data-stu-id="2c7a7-123">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="2c7a7-124">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="2c7a7-124">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="2c7a7-125">**Parametro non valido** (32773)</span><span class="sxs-lookup"><span data-stu-id="2c7a7-125">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="2c7a7-126">Il **sistema è in uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="2c7a7-126">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="2c7a7-127">**Stato non valido per l'operazione** (32775)</span><span class="sxs-lookup"><span data-stu-id="2c7a7-127">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="2c7a7-128">**Tipo di dati non corretto** (32776)</span><span class="sxs-lookup"><span data-stu-id="2c7a7-128">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="2c7a7-129">**Sistema non disponibile** (32777)</span><span class="sxs-lookup"><span data-stu-id="2c7a7-129">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="2c7a7-130">**Memoria insufficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="2c7a7-130">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="2c7a7-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2c7a7-131">Requirements</span></span>



| <span data-ttu-id="2c7a7-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="2c7a7-132">Requirement</span></span> | <span data-ttu-id="2c7a7-133">Valore</span><span class="sxs-lookup"><span data-stu-id="2c7a7-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c7a7-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2c7a7-134">Minimum supported client</span></span><br/> | <span data-ttu-id="2c7a7-135">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="2c7a7-135">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="2c7a7-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2c7a7-136">Minimum supported server</span></span><br/> | <span data-ttu-id="2c7a7-137">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="2c7a7-137">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2c7a7-138">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="2c7a7-138">Namespace</span></span><br/>                | <span data-ttu-id="2c7a7-139">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="2c7a7-139">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="2c7a7-140">MOF</span><span class="sxs-lookup"><span data-stu-id="2c7a7-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2c7a7-141"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2c7a7-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="2c7a7-142">DLL</span><span class="sxs-lookup"><span data-stu-id="2c7a7-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2c7a7-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="2c7a7-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="2c7a7-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2c7a7-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c7a7-145">**\_VirtualSystemManagementService MSVM**</span><span class="sxs-lookup"><span data-stu-id="2c7a7-145">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

