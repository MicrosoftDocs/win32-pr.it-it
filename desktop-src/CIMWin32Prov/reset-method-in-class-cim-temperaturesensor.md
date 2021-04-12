---
description: Il metodo Reset della classe CIM \_ sensore richiede la reimpostazione del dispositivo logico.
ms.assetid: c764da9a-561b-4a0b-9cdf-6b4af50f1df0
ms.tgt_platform: multiple
title: Reimposta il metodo della classe CIM_TemperatureSensor
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_TemperatureSensor.Reset
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 050836529b95d610c25902eee9b36d4720dc639e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104401378"
---
# <a name="reset-method-of-the-cim_temperaturesensor-class"></a><span data-ttu-id="ce244-103">Metodo Reset della classe CIM \_ sensore</span><span class="sxs-lookup"><span data-stu-id="ce244-103">Reset method of the CIM\_TemperatureSensor class</span></span>

<span data-ttu-id="ce244-104">Il metodo **Reset** della classe CIM \_ sensore richiede la reimpostazione del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="ce244-104">The **Reset** method of the CIM\_TemperatureSensor class requests a reset of the logical device.</span></span> <span data-ttu-id="ce244-105">Questo metodo viene ereditato da [**\_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="ce244-105">This method is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ce244-106">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="ce244-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="ce244-107">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="ce244-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="ce244-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ce244-108">Syntax</span></span>


```mof
uint32 Reset();
```



## <a name="parameters"></a><span data-ttu-id="ce244-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="ce244-109">Parameters</span></span>

<span data-ttu-id="ce244-110">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="ce244-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ce244-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ce244-111">Return value</span></span>

<span data-ttu-id="ce244-112">Restituisce 0 (zero) se la richiesta è stata eseguita correttamente, 1 (uno) se la richiesta non è supportata e un altro valore se si è verificato un errore.</span><span class="sxs-lookup"><span data-stu-id="ce244-112">Returns 0 (zero) if the request was successfully executed, 1 (one) if the request is not supported, and some other value if an error occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="ce244-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="ce244-113">Remarks</span></span>

<span data-ttu-id="ce244-114">Questo metodo non è attualmente implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="ce244-114">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="ce244-115">Per usare questo metodo, è necessario implementarlo nel proprio provider.</span><span class="sxs-lookup"><span data-stu-id="ce244-115">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="ce244-116">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="ce244-116">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="ce244-117">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="ce244-117">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="ce244-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ce244-118">Requirements</span></span>



| <span data-ttu-id="ce244-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="ce244-119">Requirement</span></span> | <span data-ttu-id="ce244-120">Valore</span><span class="sxs-lookup"><span data-stu-id="ce244-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ce244-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ce244-121">Minimum supported client</span></span><br/> | <span data-ttu-id="ce244-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ce244-122">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ce244-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ce244-123">Minimum supported server</span></span><br/> | <span data-ttu-id="ce244-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ce244-124">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ce244-125">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="ce244-125">Namespace</span></span><br/>                | <span data-ttu-id="ce244-126">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="ce244-126">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="ce244-127">MOF</span><span class="sxs-lookup"><span data-stu-id="ce244-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ce244-128"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ce244-128"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="ce244-129">DLL</span><span class="sxs-lookup"><span data-stu-id="ce244-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ce244-130"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ce244-130"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ce244-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ce244-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce244-132">\_Sensore CIM</span><span class="sxs-lookup"><span data-stu-id="ce244-132">CIM\_TemperatureSensor</span></span>](reset-method-in-class-cim-temperaturesensor.md)
</dt> <dt>

[<span data-ttu-id="ce244-133">**\_Sensore CIM**</span><span class="sxs-lookup"><span data-stu-id="ce244-133">**CIM\_TemperatureSensor**</span></span>](cim-temperaturesensor.md)
</dt> </dl>

 

 




