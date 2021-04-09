---
description: Il metodo seurge imposta il livello di urgenza desiderato per un allarme.
ms.assetid: ac2e7fda-1317-440a-adbd-1ef0844d124c
ms.tgt_platform: multiple
title: Metodo seurgement della classe CIM_AlarmDevice
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AlarmDevice.SetUrgency
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 35918677e210ac2fe7ac4798a04db9dc628f5fa1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966136"
---
# <a name="seturgency-method-of-the-cim_alarmdevice-class"></a><span data-ttu-id="f8255-103">Metodo seurgement della \_ classe CIM AlarmDevice</span><span class="sxs-lookup"><span data-stu-id="f8255-103">SetUrgency method of the CIM\_AlarmDevice class</span></span>

<span data-ttu-id="f8255-104">Il metodo **seurge** imposta il livello di urgenza desiderato per un allarme.</span><span class="sxs-lookup"><span data-stu-id="f8255-104">The **SetUrgency** method sets the desired urgency level for an alarm.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f8255-105">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="f8255-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="f8255-106">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="f8255-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="f8255-107">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="f8255-107">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="f8255-108">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="f8255-108">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="f8255-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f8255-109">Syntax</span></span>


```mof
uint32 SetUrgency(
  [in] uint16 RequestedUrgency
);
```



## <a name="parameters"></a><span data-ttu-id="f8255-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="f8255-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f8255-111">*RequestedUrgency* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f8255-111">*RequestedUrgency* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f8255-112">Frequenza relativa con cui l'allarme lampeggia, vibra o emette toni acustici.</span><span class="sxs-lookup"><span data-stu-id="f8255-112">Relative frequency at which the alarm flashes, vibrates, or emits audible tones.</span></span> <span data-ttu-id="f8255-113">I valori seguenti sono dalla proprietà **urgenza** in [**CIM \_ AlarmDevice**](cim-alarmdevice.md).</span><span class="sxs-lookup"><span data-stu-id="f8255-113">The following values are from the **Urgency** property in [**CIM\_AlarmDevice**](cim-alarmdevice.md).</span></span>

<dt>

<span data-ttu-id="f8255-114">0</span><span class="sxs-lookup"><span data-stu-id="f8255-114">0</span></span>
</dt> <dd>

<span data-ttu-id="f8255-115">Sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="f8255-115">Unknown.</span></span>

</dd> <dt>

<span data-ttu-id="f8255-116">1</span><span class="sxs-lookup"><span data-stu-id="f8255-116">1</span></span>
</dt> <dd>

<span data-ttu-id="f8255-117">Altro.</span><span class="sxs-lookup"><span data-stu-id="f8255-117">Other.</span></span>

</dd> <dt>

<span data-ttu-id="f8255-118">2</span><span class="sxs-lookup"><span data-stu-id="f8255-118">2</span></span>
</dt> <dd>

<span data-ttu-id="f8255-119">Non supportata.</span><span class="sxs-lookup"><span data-stu-id="f8255-119">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="f8255-120">3</span><span class="sxs-lookup"><span data-stu-id="f8255-120">3</span></span>
</dt> <dd>

<span data-ttu-id="f8255-121">Si tratta di un messaggio informativo.</span><span class="sxs-lookup"><span data-stu-id="f8255-121">Informational.</span></span>

</dd> <dt>

<span data-ttu-id="f8255-122">4</span><span class="sxs-lookup"><span data-stu-id="f8255-122">4</span></span>
</dt> <dd>

<span data-ttu-id="f8255-123">Non critico.</span><span class="sxs-lookup"><span data-stu-id="f8255-123">Non-critical.</span></span>

</dd> <dt>

<span data-ttu-id="f8255-124">5</span><span class="sxs-lookup"><span data-stu-id="f8255-124">5</span></span>
</dt> <dd>

<span data-ttu-id="f8255-125">Critica.</span><span class="sxs-lookup"><span data-stu-id="f8255-125">Critical.</span></span>

</dd> <dt>

<span data-ttu-id="f8255-126">6</span><span class="sxs-lookup"><span data-stu-id="f8255-126">6</span></span>
</dt> <dd>

<span data-ttu-id="f8255-127">Irreversibile.</span><span class="sxs-lookup"><span data-stu-id="f8255-127">Unrecoverable.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f8255-128">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f8255-128">Return value</span></span>

<span data-ttu-id="f8255-129">Restituisce un valore pari a 0 (zero) in caso di esito positivo, 1 (uno) se il livello di urgenza richiesto non è supportato e qualsiasi altro numero per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="f8255-129">Returns a value of 0 (zero) on success, 1 (one) if the requested urgency level is not supported, and any other number to indicate an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="f8255-130">Commenti</span><span class="sxs-lookup"><span data-stu-id="f8255-130">Remarks</span></span>

<span data-ttu-id="f8255-131">Questo metodo non è attualmente implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="f8255-131">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="f8255-132">Per usare questo metodo, è necessario implementarlo nel proprio provider.</span><span class="sxs-lookup"><span data-stu-id="f8255-132">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="f8255-133">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="f8255-133">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="f8255-134">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="f8255-134">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="f8255-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f8255-135">Requirements</span></span>



| <span data-ttu-id="f8255-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="f8255-136">Requirement</span></span> | <span data-ttu-id="f8255-137">Valore</span><span class="sxs-lookup"><span data-stu-id="f8255-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f8255-138">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f8255-138">Minimum supported client</span></span><br/> | <span data-ttu-id="f8255-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f8255-139">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f8255-140">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f8255-140">Minimum supported server</span></span><br/> | <span data-ttu-id="f8255-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f8255-141">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f8255-142">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="f8255-142">Namespace</span></span><br/>                | <span data-ttu-id="f8255-143">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="f8255-143">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="f8255-144">MOF</span><span class="sxs-lookup"><span data-stu-id="f8255-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f8255-145"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f8255-145"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="f8255-146">DLL</span><span class="sxs-lookup"><span data-stu-id="f8255-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f8255-147"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f8255-147"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f8255-148">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f8255-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8255-149">\_ALARMDEVICE CIM</span><span class="sxs-lookup"><span data-stu-id="f8255-149">CIM\_AlarmDevice</span></span>](seturgency-method-in-class-cim-alarmdevice.md)
</dt> <dt>

[<span data-ttu-id="f8255-150">**\_ALARMDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="f8255-150">**CIM\_AlarmDevice**</span></span>](cim-alarmdevice.md)
</dt> </dl>

 

