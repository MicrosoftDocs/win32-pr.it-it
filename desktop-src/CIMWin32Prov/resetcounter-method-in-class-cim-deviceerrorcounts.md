---
description: Il metodo ResetCounter Reimposta i contatori di errore e di avviso.
ms.assetid: 5bc6c939-cd97-40ca-a16c-5227e7f27c76
ms.tgt_platform: multiple
title: Metodo ResetCounter della classe CIM_DeviceErrorCounts
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceErrorCounts.ResetCounter
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 386547362f5a7aa52bddfbf9df3af01949aecbdd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877350"
---
# <a name="resetcounter-method-of-the-cim_deviceerrorcounts-class"></a><span data-ttu-id="b0c72-103">Metodo ResetCounter della classe CIM \_ DeviceErrorCounts</span><span class="sxs-lookup"><span data-stu-id="b0c72-103">ResetCounter method of the CIM\_DeviceErrorCounts class</span></span>

<span data-ttu-id="b0c72-104">Il metodo **ResetCounter** Reimposta i contatori di errore e di avviso.</span><span class="sxs-lookup"><span data-stu-id="b0c72-104">The **ResetCounter** method resets the error and warning counters.</span></span> <span data-ttu-id="b0c72-105">Viene usato un metodo in modo che la strumentazione del dispositivo logico, che cataloga gli errori e gli avvisi, possa anche reimpostare i contatori e l'elaborazione interna.</span><span class="sxs-lookup"><span data-stu-id="b0c72-105">A method is used so that the logical device's instrumentation, which tabulates the errors and warnings, can also reset its internal processing and counters.</span></span> <span data-ttu-id="b0c72-106">In una sottoclasse, il set di possibili codici restituiti può essere specificato utilizzando un qualificatore **ValueMap** nel metodo.</span><span class="sxs-lookup"><span data-stu-id="b0c72-106">In a subclass, the set of possible return codes can be specified using a **ValueMap** qualifier on the method.</span></span> <span data-ttu-id="b0c72-107">Le stringhe a cui viene convertito il contenuto **ValueMap** possono anche essere specificate nella sottoclasse come qualificatore della matrice di **valori** .</span><span class="sxs-lookup"><span data-stu-id="b0c72-107">The strings to which the **ValueMap** contents are translated can also be specified in the subclass as a **Values** array qualifier.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b0c72-108">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="b0c72-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="b0c72-109">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="b0c72-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="b0c72-110">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="b0c72-110">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="b0c72-111">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="b0c72-111">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="b0c72-112">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b0c72-112">Syntax</span></span>


```mof
uint32 ResetCounter(
  [in] uint16 SelectedCounter
);
```



## <a name="parameters"></a><span data-ttu-id="b0c72-113">Parametri</span><span class="sxs-lookup"><span data-stu-id="b0c72-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b0c72-114">*SelectedCounter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b0c72-114">*SelectedCounter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b0c72-115">Contatore degli errori da ripristinare.</span><span class="sxs-lookup"><span data-stu-id="b0c72-115">Error counter to reset.</span></span>

<dt>

<span id="All"></span><span id="all"></span><span id="ALL"></span>

<span data-ttu-id="b0c72-116">**Tutto** (0)</span><span class="sxs-lookup"><span data-stu-id="b0c72-116">**All** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Indeterminate_Error_Counter"></span><span id="indeterminate_error_counter"></span><span id="INDETERMINATE_ERROR_COUNTER"></span>

<span data-ttu-id="b0c72-117">**Contatore errori indeterminato** (1)</span><span class="sxs-lookup"><span data-stu-id="b0c72-117">**Indeterminate Error Counter** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Critical_Error_Counter"></span><span id="critical_error_counter"></span><span id="CRITICAL_ERROR_COUNTER"></span>

<span data-ttu-id="b0c72-118">**Contatore errore critico** (2)</span><span class="sxs-lookup"><span data-stu-id="b0c72-118">**Critical Error Counter** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Major_Error_Counter"></span><span id="major_error_counter"></span><span id="MAJOR_ERROR_COUNTER"></span>

<span data-ttu-id="b0c72-119">**Contatore errore principale** (3)</span><span class="sxs-lookup"><span data-stu-id="b0c72-119">**Major Error Counter** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Minor_Error_Counter"></span><span id="minor_error_counter"></span><span id="MINOR_ERROR_COUNTER"></span>

<span data-ttu-id="b0c72-120">**Contatore errori secondari** (4)</span><span class="sxs-lookup"><span data-stu-id="b0c72-120">**Minor Error Counter** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning_Counter"></span><span id="warning_counter"></span><span id="WARNING_COUNTER"></span>

<span data-ttu-id="b0c72-121">**Contatore avvisi** (5)</span><span class="sxs-lookup"><span data-stu-id="b0c72-121">**Warning Counter** (5)</span></span>


<span data-ttu-id="b0c72-122"></dt> <dd></dd> </dl> </dd> </dl></span><span class="sxs-lookup"><span data-stu-id="b0c72-122"></dt> <dd></dd> </dl> </dd> </dl></span></span>

## <a name="return-value"></a><span data-ttu-id="b0c72-123">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b0c72-123">Return value</span></span>

<span data-ttu-id="b0c72-124">Restituisce 0 (zero) se ha esito positivo, 1 (uno) se non è supportato e qualsiasi altro valore se si è verificato un errore.</span><span class="sxs-lookup"><span data-stu-id="b0c72-124">Returns 0 (zero) if successful, 1 (one) if not supported, and any other value if an error occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="b0c72-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="b0c72-125">Remarks</span></span>

<span data-ttu-id="b0c72-126">Questo metodo non è attualmente implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="b0c72-126">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="b0c72-127">Per usare questo metodo, è necessario implementarlo nel proprio provider.</span><span class="sxs-lookup"><span data-stu-id="b0c72-127">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="b0c72-128">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="b0c72-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="b0c72-129">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="b0c72-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="b0c72-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b0c72-130">Requirements</span></span>



| <span data-ttu-id="b0c72-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="b0c72-131">Requirement</span></span> | <span data-ttu-id="b0c72-132">Valore</span><span class="sxs-lookup"><span data-stu-id="b0c72-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b0c72-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b0c72-133">Minimum supported client</span></span><br/> | <span data-ttu-id="b0c72-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b0c72-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b0c72-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b0c72-135">Minimum supported server</span></span><br/> | <span data-ttu-id="b0c72-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b0c72-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b0c72-137">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="b0c72-137">Namespace</span></span><br/>                | <span data-ttu-id="b0c72-138">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="b0c72-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b0c72-139">MOF</span><span class="sxs-lookup"><span data-stu-id="b0c72-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b0c72-140"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b0c72-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b0c72-141">DLL</span><span class="sxs-lookup"><span data-stu-id="b0c72-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b0c72-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b0c72-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b0c72-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b0c72-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0c72-144">\_DEVICEERRORCOUNTS CIM</span><span class="sxs-lookup"><span data-stu-id="b0c72-144">CIM\_DeviceErrorCounts</span></span>](resetcounter-method-in-class-cim-deviceerrorcounts.md)
</dt> <dt>

[<span data-ttu-id="b0c72-145">**\_DEVICEERRORCOUNTS CIM**</span><span class="sxs-lookup"><span data-stu-id="b0c72-145">**CIM\_DeviceErrorCounts**</span></span>](cim-deviceerrorcounts.md)
</dt> </dl>

 

