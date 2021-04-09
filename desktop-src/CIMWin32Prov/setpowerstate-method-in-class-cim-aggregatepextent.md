---
description: Il metodo SetPowerState imposta lo stato di alimentazione desiderato per un dispositivo logico e quando il dispositivo deve essere inserito in tale stato.
ms.assetid: 1a1a8d5e-d685-4b7e-99fb-61fa2e7bdafa
ms.tgt_platform: multiple
title: Metodo SetPowerState della classe CIM_AggregatePExtent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AggregatePExtent.SetPowerState
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 47c97f30da1c8b6f2fe9a6032ef9be9ae87a7d6c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966182"
---
# <a name="setpowerstate-method-of-the-cim_aggregatepextent-class"></a><span data-ttu-id="6b6c7-103">Metodo SetPowerState della classe CIM \_ AggregatePExtent</span><span class="sxs-lookup"><span data-stu-id="6b6c7-103">SetPowerState method of the CIM\_AggregatePExtent class</span></span>

<span data-ttu-id="6b6c7-104">Il metodo **SetPowerState** imposta lo stato di alimentazione desiderato per un dispositivo logico e quando il dispositivo deve essere inserito in tale stato.</span><span class="sxs-lookup"><span data-stu-id="6b6c7-104">The **SetPowerState** method sets the desired power state for a logical device and when the device should be put into that state.</span></span> <span data-ttu-id="6b6c7-105">In una sottoclasse, il set di possibili codici restituiti deve essere specificato utilizzando un qualificatore **ValueMap** nel metodo.</span><span class="sxs-lookup"><span data-stu-id="6b6c7-105">In a subclass, the set of possible return codes should be specified using a **ValueMap** qualifier on the method.</span></span> <span data-ttu-id="6b6c7-106">Le stringhe a cui viene convertito il contenuto **ValueMap** devono essere specificate anche nella sottoclasse come qualificatore della matrice di **valori** .</span><span class="sxs-lookup"><span data-stu-id="6b6c7-106">The strings to which the **ValueMap** contents are translated should also be specified in the subclass as a **Values** array qualifier.</span></span> <span data-ttu-id="6b6c7-107">Questo metodo viene ereditato da [**\_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="6b6c7-107">This method is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="6b6c7-108">Per ulteriori informazioni sull'utilizzo di questo metodo con C/C++, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="6b6c7-108">For more information about using this method with C/C++, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6b6c7-109">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="6b6c7-109">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="6b6c7-110">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="6b6c7-110">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="6b6c7-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6b6c7-111">Syntax</span></span>


```mof
uint32 SetPowerState(
  [in] uint16   PowerState,
  [in] datetime Time
);
```



## <a name="parameters"></a><span data-ttu-id="6b6c7-112">Parametri</span><span class="sxs-lookup"><span data-stu-id="6b6c7-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6b6c7-113">*PowerState* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6b6c7-113">*PowerState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6b6c7-114">Valore **ValueMap** che specifica lo stato di alimentazione desiderato per questo dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="6b6c7-114">The **ValueMap** value that specifies the desired power state for this logical device.</span></span>

<dt>

<span data-ttu-id="6b6c7-115">1</span><span class="sxs-lookup"><span data-stu-id="6b6c7-115">1</span></span>
</dt> <dd>

<span data-ttu-id="6b6c7-116">Potenza completa</span><span class="sxs-lookup"><span data-stu-id="6b6c7-116">Full power</span></span>

</dd> <dt>

<span data-ttu-id="6b6c7-117">2</span><span class="sxs-lookup"><span data-stu-id="6b6c7-117">2</span></span>
</dt> <dd>

<span data-ttu-id="6b6c7-118">Risparmio energia-modalità a basso consumo</span><span class="sxs-lookup"><span data-stu-id="6b6c7-118">Power-save   low-power mode</span></span>

</dd> <dt>

<span data-ttu-id="6b6c7-119">3</span><span class="sxs-lookup"><span data-stu-id="6b6c7-119">3</span></span>
</dt> <dd>

<span data-ttu-id="6b6c7-120">Risparmio energia-standby</span><span class="sxs-lookup"><span data-stu-id="6b6c7-120">Power-save   standby</span></span>

</dd> <dt>

<span data-ttu-id="6b6c7-121">4</span><span class="sxs-lookup"><span data-stu-id="6b6c7-121">4</span></span>
</dt> <dd>

<span data-ttu-id="6b6c7-122">Risparmio energia-altro</span><span class="sxs-lookup"><span data-stu-id="6b6c7-122">Power-save   other</span></span>

</dd> <dt>

<span data-ttu-id="6b6c7-123">5</span><span class="sxs-lookup"><span data-stu-id="6b6c7-123">5</span></span>
</dt> <dd>

<span data-ttu-id="6b6c7-124">Ciclo di alimentazione</span><span class="sxs-lookup"><span data-stu-id="6b6c7-124">Power cycle</span></span>

</dd> <dt>

<span data-ttu-id="6b6c7-125">6</span><span class="sxs-lookup"><span data-stu-id="6b6c7-125">6</span></span>
</dt> <dd>

<span data-ttu-id="6b6c7-126">Spegnimento</span><span class="sxs-lookup"><span data-stu-id="6b6c7-126">Power off</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="6b6c7-127">*Ora* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="6b6c7-127">*Time* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6b6c7-128">Quando è necessario impostare lo stato di alimentazione, come valore di data e ora normale o come valore di intervallo (dove l'intervallo inizia quando viene ricevuta la chiamata al metodo).</span><span class="sxs-lookup"><span data-stu-id="6b6c7-128">When the power state should be set, either as a regular date-time value or as an interval value (where the interval begins when the method invocation is received).</span></span> <span data-ttu-id="6b6c7-129">Quando il parametro *PowerState* è uguale a 5 (ciclo di alimentazione), il parametro *Time* indica quando il dispositivo deve accendere di nuovo il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6b6c7-129">When the *PowerState* parameter is equal to 5 (power cycle), the *Time* parameter indicates when the device should power-on again.</span></span> <span data-ttu-id="6b6c7-130">Lo spegnimento è immediato.</span><span class="sxs-lookup"><span data-stu-id="6b6c7-130">Power-off is immediate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6b6c7-131">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6b6c7-131">Return value</span></span>

<span data-ttu-id="6b6c7-132">Restituisce 0 (zero) se ha esito positivo, 1 (uno) se la richiesta *PowerState* e *Time* specificata non è supportata e un altro valore se si sono verificati altri errori.</span><span class="sxs-lookup"><span data-stu-id="6b6c7-132">Returns 0 (zero) if successful, 1 (one) if the specified *PowerState* and *Time* request is not supported, and another value if any other error occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="6b6c7-133">Commenti</span><span class="sxs-lookup"><span data-stu-id="6b6c7-133">Remarks</span></span>

<span data-ttu-id="6b6c7-134">Questo metodo non è attualmente implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="6b6c7-134">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="6b6c7-135">Per usare questo metodo, è necessario implementarlo nel proprio provider.</span><span class="sxs-lookup"><span data-stu-id="6b6c7-135">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="6b6c7-136">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="6b6c7-136">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="6b6c7-137">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="6b6c7-137">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="6b6c7-138">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6b6c7-138">Requirements</span></span>



| <span data-ttu-id="6b6c7-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="6b6c7-139">Requirement</span></span> | <span data-ttu-id="6b6c7-140">Valore</span><span class="sxs-lookup"><span data-stu-id="6b6c7-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6b6c7-141">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6b6c7-141">Minimum supported client</span></span><br/> | <span data-ttu-id="6b6c7-142">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6b6c7-142">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6b6c7-143">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6b6c7-143">Minimum supported server</span></span><br/> | <span data-ttu-id="6b6c7-144">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6b6c7-144">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6b6c7-145">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="6b6c7-145">Namespace</span></span><br/>                | <span data-ttu-id="6b6c7-146">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="6b6c7-146">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="6b6c7-147">MOF</span><span class="sxs-lookup"><span data-stu-id="6b6c7-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6b6c7-148"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6b6c7-148"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="6b6c7-149">DLL</span><span class="sxs-lookup"><span data-stu-id="6b6c7-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6b6c7-150"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6b6c7-150"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6b6c7-151">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6b6c7-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b6c7-152">**\_AGGREGATEPEXTENT CIM**</span><span class="sxs-lookup"><span data-stu-id="6b6c7-152">**CIM\_AggregatePExtent**</span></span>](setpowerstate-method-in-class-cim-aggregatepextent.md)
</dt> <dt>

[<span data-ttu-id="6b6c7-153">**\_AGGREGATEPEXTENT CIM**</span><span class="sxs-lookup"><span data-stu-id="6b6c7-153">**CIM\_AggregatePExtent**</span></span>](cim-aggregatepextent.md)
</dt> </dl>

 

