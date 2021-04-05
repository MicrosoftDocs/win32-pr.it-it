---
description: Questo metodo viene utilizzato per trovare la riserva effettiva con il parametro di input corrispondente al numero di processori di macchine virtuali per cui viene calcolata la riserva.
ms.assetid: C0497900-00F3-4975-9D12-C82C13C03D8E
title: Metodo CalculatePossibleReserve della classe Msvm_ProcessorPool
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ProcessorPool.CalculatePossibleReserve
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: c7f88bcf3295b1792fca6be88ae0c9282b72646e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756623"
---
# <a name="calculatepossiblereserve-method-of-the-msvm_processorpool-class"></a><span data-ttu-id="eee5a-103">Metodo CalculatePossibleReserve della classe MSVM \_ ProcessorPool</span><span class="sxs-lookup"><span data-stu-id="eee5a-103">CalculatePossibleReserve method of the Msvm\_ProcessorPool class</span></span>

<span data-ttu-id="eee5a-104">Questo metodo viene utilizzato per trovare la riserva effettiva con il parametro di input corrispondente al numero di processori di macchine virtuali per cui viene calcolata la riserva.</span><span class="sxs-lookup"><span data-stu-id="eee5a-104">This method is used to find the actual reserve with the input parameter being the number of virtual machine processors for which the reserve is calculated.</span></span> <span data-ttu-id="eee5a-105">Questo metodo è necessario perché la prenotazione delle risorse del processore dipende molto dal numero di processori che devono essere pianificati in parallelo.</span><span class="sxs-lookup"><span data-stu-id="eee5a-105">This method is necessary because the reservation of processor resources is highly dependent on the number of processors which must be scheduled in parallel.</span></span>

## <a name="syntax"></a><span data-ttu-id="eee5a-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="eee5a-106">Syntax</span></span>


```mof
uint32 CalculatePossibleReserve(
  [in] uint16 ProcessorCount
);
```



## <a name="parameters"></a><span data-ttu-id="eee5a-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="eee5a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eee5a-108">*ProcessorCount* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="eee5a-108">*ProcessorCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eee5a-109">Tipo: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="eee5a-109">Type: **uint16**</span></span>

<span data-ttu-id="eee5a-110">Il numero di processori di macchine virtuali per cui viene calcolata la riserva.</span><span class="sxs-lookup"><span data-stu-id="eee5a-110">The number of virtual machine processors for which the reserve is calculated.</span></span> <span data-ttu-id="eee5a-111">Il valore massimo per questa proprietà è il numero di processori logici per il computer host.</span><span class="sxs-lookup"><span data-stu-id="eee5a-111">The maximum value for this property is the logical processor count for the host computer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eee5a-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="eee5a-112">Return value</span></span>

<span data-ttu-id="eee5a-113">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="eee5a-113">Type: **uint32**</span></span>

<span data-ttu-id="eee5a-114">Quantità di risorse della CPU che possono essere riservate per una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="eee5a-114">The amount of CPU resources that may be reserved for a virtual machine.</span></span>

## <a name="remarks"></a><span data-ttu-id="eee5a-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="eee5a-115">Remarks</span></span>

<span data-ttu-id="eee5a-116">L'accesso alla [**classe \_ ProcessorPool di MSVM**](msvm-processorpool.md) potrebbe essere limitato dal filtraggio del controllo dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="eee5a-116">Access to the [**Msvm\_ProcessorPool**](msvm-processorpool.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="eee5a-117">Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="eee5a-117">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="eee5a-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="eee5a-118">Requirements</span></span>



| <span data-ttu-id="eee5a-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="eee5a-119">Requirement</span></span> | <span data-ttu-id="eee5a-120">Valore</span><span class="sxs-lookup"><span data-stu-id="eee5a-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eee5a-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="eee5a-121">Minimum supported client</span></span><br/> | <span data-ttu-id="eee5a-122">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="eee5a-122">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="eee5a-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="eee5a-123">Minimum supported server</span></span><br/> | <span data-ttu-id="eee5a-124">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="eee5a-124">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="eee5a-125">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="eee5a-125">Namespace</span></span><br/>                | <span data-ttu-id="eee5a-126">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="eee5a-126">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="eee5a-127">MOF</span><span class="sxs-lookup"><span data-stu-id="eee5a-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="eee5a-128"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="eee5a-128"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="eee5a-129">DLL</span><span class="sxs-lookup"><span data-stu-id="eee5a-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eee5a-130"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="eee5a-130"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="eee5a-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="eee5a-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eee5a-132">**\_ProcessorPool MSVM**</span><span class="sxs-lookup"><span data-stu-id="eee5a-132">**Msvm\_ProcessorPool**</span></span>](msvm-processorpool.md)
</dt> </dl>

 

