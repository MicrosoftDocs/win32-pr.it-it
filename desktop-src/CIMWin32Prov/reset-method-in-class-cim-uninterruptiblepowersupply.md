---
description: Il metodo Reset della classe CIM \_ UninterruptiblePowerSupply richiede la reimpostazione del dispositivo logico.
ms.assetid: be04a10d-267c-4001-93ac-408a133ca923
ms.tgt_platform: multiple
title: Reimposta il metodo della classe CIM_UninterruptiblePowerSupply
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_UninterruptiblePowerSupply.Reset
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 54068e460ef2a1c6e6eee7500c018c485b81bd6b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878265"
---
# <a name="reset-method-of-the-cim_uninterruptiblepowersupply-class"></a><span data-ttu-id="8d6e9-103">Metodo Reset della classe CIM \_ UninterruptiblePowerSupply</span><span class="sxs-lookup"><span data-stu-id="8d6e9-103">Reset method of the CIM\_UninterruptiblePowerSupply class</span></span>

<span data-ttu-id="8d6e9-104">Il metodo **Reset** della classe CIM \_ UninterruptiblePowerSupply richiede la reimpostazione del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="8d6e9-104">The **Reset** method of the CIM\_UninterruptiblePowerSupply class requests a reset of the logical device.</span></span> <span data-ttu-id="8d6e9-105">Questo metodo viene ereditato da [**\_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="8d6e9-105">This method is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8d6e9-106">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="8d6e9-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="8d6e9-107">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="8d6e9-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="8d6e9-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8d6e9-108">Syntax</span></span>


```mof
uint32 Reset();
```



## <a name="parameters"></a><span data-ttu-id="8d6e9-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="8d6e9-109">Parameters</span></span>

<span data-ttu-id="8d6e9-110">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="8d6e9-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="8d6e9-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8d6e9-111">Return value</span></span>

<span data-ttu-id="8d6e9-112">Restituisce 0 (zero) se la richiesta è stata eseguita correttamente, 1 (uno) se la richiesta non è supportata e un altro valore se si è verificato un errore.</span><span class="sxs-lookup"><span data-stu-id="8d6e9-112">Returns 0 (zero) if the request was successfully executed, 1 (one) if the request is not supported, and some other value if an error occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="8d6e9-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="8d6e9-113">Remarks</span></span>

<span data-ttu-id="8d6e9-114">Questo metodo non è attualmente implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="8d6e9-114">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="8d6e9-115">Per usare questo metodo, è necessario implementarlo nel proprio provider.</span><span class="sxs-lookup"><span data-stu-id="8d6e9-115">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="8d6e9-116">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="8d6e9-116">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="8d6e9-117">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="8d6e9-117">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="8d6e9-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8d6e9-118">Requirements</span></span>



| <span data-ttu-id="8d6e9-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="8d6e9-119">Requirement</span></span> | <span data-ttu-id="8d6e9-120">Valore</span><span class="sxs-lookup"><span data-stu-id="8d6e9-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8d6e9-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8d6e9-121">Minimum supported client</span></span><br/> | <span data-ttu-id="8d6e9-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8d6e9-122">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8d6e9-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8d6e9-123">Minimum supported server</span></span><br/> | <span data-ttu-id="8d6e9-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8d6e9-124">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8d6e9-125">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="8d6e9-125">Namespace</span></span><br/>                | <span data-ttu-id="8d6e9-126">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="8d6e9-126">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="8d6e9-127">MOF</span><span class="sxs-lookup"><span data-stu-id="8d6e9-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8d6e9-128"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8d6e9-128"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="8d6e9-129">DLL</span><span class="sxs-lookup"><span data-stu-id="8d6e9-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8d6e9-130"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8d6e9-130"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8d6e9-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8d6e9-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d6e9-132">\_UNINTERRUPTIBLEPOWERSUPPLY CIM</span><span class="sxs-lookup"><span data-stu-id="8d6e9-132">CIM\_UninterruptiblePowerSupply</span></span>](reset-method-in-class-cim-uninterruptiblepowersupply.md)
</dt> <dt>

[<span data-ttu-id="8d6e9-133">**\_UNINTERRUPTIBLEPOWERSUPPLY CIM**</span><span class="sxs-lookup"><span data-stu-id="8d6e9-133">**CIM\_UninterruptiblePowerSupply**</span></span>](cim-uninterruptiblepowersupply.md)
</dt> </dl>

 

 




