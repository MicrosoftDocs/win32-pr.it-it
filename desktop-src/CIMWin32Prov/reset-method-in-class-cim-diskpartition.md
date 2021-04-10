---
description: Il metodo Reset richiede la reimpostazione del dispositivo logico. Questo metodo viene ereditato da \_ LOGICALDEVICE CIM.
ms.assetid: 874f8eb4-784a-41ab-9c58-9e48486a7f71
ms.tgt_platform: multiple
title: Reimposta il metodo della classe CIM_DiskPartition
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DiskPartition.Reset
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 236a8c018b584fbc2d5ef1d13b0429d946b868fe
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225551"
---
# <a name="reset-method-of-the-cim_diskpartition-class"></a><span data-ttu-id="3478b-104">Metodo Reset della classe CIM \_ DiskPartition</span><span class="sxs-lookup"><span data-stu-id="3478b-104">Reset method of the CIM\_DiskPartition class</span></span>

<span data-ttu-id="3478b-105">Il metodo **Reset** richiede la reimpostazione del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="3478b-105">The **Reset** method requests a reset of the logical device.</span></span> <span data-ttu-id="3478b-106">Questo metodo viene ereditato da [**\_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="3478b-106">This method is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3478b-107">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="3478b-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="3478b-108">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="3478b-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="3478b-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3478b-109">Syntax</span></span>


```mof
uint32 Reset();
```



## <a name="parameters"></a><span data-ttu-id="3478b-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="3478b-110">Parameters</span></span>

<span data-ttu-id="3478b-111">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="3478b-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="3478b-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3478b-112">Return value</span></span>

<span data-ttu-id="3478b-113">Restituisce 0 (zero) se la richiesta è stata eseguita correttamente, 1 (uno) se la richiesta non è supportata e un altro valore se si è verificato un errore.</span><span class="sxs-lookup"><span data-stu-id="3478b-113">Returns 0 (zero) if the request was successfully executed, 1 (one) if the request is not supported, and some other value if an error occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="3478b-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="3478b-114">Remarks</span></span>

<span data-ttu-id="3478b-115">Questo metodo non è attualmente implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="3478b-115">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="3478b-116">Per usare questo metodo, è necessario implementarlo nel proprio provider.</span><span class="sxs-lookup"><span data-stu-id="3478b-116">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="3478b-117">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="3478b-117">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="3478b-118">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="3478b-118">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="3478b-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3478b-119">Requirements</span></span>



| <span data-ttu-id="3478b-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="3478b-120">Requirement</span></span> | <span data-ttu-id="3478b-121">Valore</span><span class="sxs-lookup"><span data-stu-id="3478b-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3478b-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3478b-122">Minimum supported client</span></span><br/> | <span data-ttu-id="3478b-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3478b-123">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3478b-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3478b-124">Minimum supported server</span></span><br/> | <span data-ttu-id="3478b-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3478b-125">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3478b-126">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="3478b-126">Namespace</span></span><br/>                | <span data-ttu-id="3478b-127">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="3478b-127">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="3478b-128">MOF</span><span class="sxs-lookup"><span data-stu-id="3478b-128">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3478b-129"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3478b-129"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="3478b-130">DLL</span><span class="sxs-lookup"><span data-stu-id="3478b-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3478b-131"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3478b-131"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3478b-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3478b-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3478b-133">\_DISKPARTITION CIM</span><span class="sxs-lookup"><span data-stu-id="3478b-133">CIM\_DiskPartition</span></span>](reset-method-in-class-cim-diskpartition.md)
</dt> <dt>

[<span data-ttu-id="3478b-134">**\_DISKPARTITION CIM**</span><span class="sxs-lookup"><span data-stu-id="3478b-134">**CIM\_DiskPartition**</span></span>](cim-diskpartition.md)
</dt> </dl>

 

 




