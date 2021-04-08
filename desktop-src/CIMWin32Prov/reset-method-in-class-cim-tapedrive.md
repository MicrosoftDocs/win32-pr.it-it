---
description: Il metodo Reset della classe CIM \_ TapeDrive richiede la reimpostazione del dispositivo logico.
ms.assetid: 48097e0d-7986-46b9-884d-7534f3848dd7
ms.tgt_platform: multiple
title: Reimposta il metodo della classe CIM_TapeDrive
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_TapeDrive.Reset
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: e5fd76d038e743ba5148f4c82555d50f0a5dde5d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878266"
---
# <a name="reset-method-of-the-cim_tapedrive-class"></a><span data-ttu-id="730f4-103">Metodo Reset della classe CIM \_ TapeDrive</span><span class="sxs-lookup"><span data-stu-id="730f4-103">Reset method of the CIM\_TapeDrive class</span></span>

<span data-ttu-id="730f4-104">Il metodo **Reset** della classe CIM \_ TapeDrive richiede la reimpostazione del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="730f4-104">The **Reset** method of the CIM\_TapeDrive class requests a reset of the logical device.</span></span> <span data-ttu-id="730f4-105">Questo metodo viene ereditato da [**\_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="730f4-105">This method is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="730f4-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="730f4-106">Syntax</span></span>


```mof
uint32 Reset();
```



## <a name="parameters"></a><span data-ttu-id="730f4-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="730f4-107">Parameters</span></span>

<span data-ttu-id="730f4-108">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="730f4-108">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="730f4-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="730f4-109">Return value</span></span>

<span data-ttu-id="730f4-110">Restituisce 0 (zero) se la richiesta è stata eseguita correttamente, 1 (uno) se la richiesta non è supportata e un altro valore se si è verificato un errore.</span><span class="sxs-lookup"><span data-stu-id="730f4-110">Returns 0 (zero) if the request was successfully executed, 1 (one) if the request is not supported, and some other value if an error occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="730f4-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="730f4-111">Remarks</span></span>

<span data-ttu-id="730f4-112">Questo metodo non è attualmente implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="730f4-112">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="730f4-113">Per usare questo metodo, è necessario implementarlo nel proprio provider.</span><span class="sxs-lookup"><span data-stu-id="730f4-113">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="730f4-114">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="730f4-114">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="730f4-115">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="730f4-115">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="730f4-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="730f4-116">Requirements</span></span>



| <span data-ttu-id="730f4-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="730f4-117">Requirement</span></span> | <span data-ttu-id="730f4-118">Valore</span><span class="sxs-lookup"><span data-stu-id="730f4-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="730f4-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="730f4-119">Minimum supported client</span></span><br/> | <span data-ttu-id="730f4-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="730f4-120">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="730f4-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="730f4-121">Minimum supported server</span></span><br/> | <span data-ttu-id="730f4-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="730f4-122">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="730f4-123">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="730f4-123">Namespace</span></span><br/>                | <span data-ttu-id="730f4-124">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="730f4-124">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="730f4-125">MOF</span><span class="sxs-lookup"><span data-stu-id="730f4-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="730f4-126"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="730f4-126"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="730f4-127">DLL</span><span class="sxs-lookup"><span data-stu-id="730f4-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="730f4-128"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="730f4-128"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="730f4-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="730f4-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="730f4-130">\_TAPEDRIVE CIM</span><span class="sxs-lookup"><span data-stu-id="730f4-130">CIM\_TapeDrive</span></span>](reset-method-in-class-cim-tapedrive.md)
</dt> <dt>

[<span data-ttu-id="730f4-131">**\_TAPEDRIVE CIM**</span><span class="sxs-lookup"><span data-stu-id="730f4-131">**CIM\_TapeDrive**</span></span>](cim-tapedrive.md)
</dt> </dl>

 

 




