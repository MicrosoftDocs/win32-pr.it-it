---
description: 'Metodo SetPowerState della classe CIM_AggregatePExtent: il metodo SetPowerState imposta lo stato di alimentazione desiderato per un dispositivo logico e quando il dispositivo deve essere inserito in tale stato.'
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
ms.openlocfilehash: 5ed988e5f58464479aa29d709eb628feb13f0d1c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108089539"
---
# <a name="setpowerstate-method-of-the-cim_aggregatepextent-class"></a><span data-ttu-id="95fb8-103">Metodo SetPowerState della classe CIM \_ AggregatePExtent</span><span class="sxs-lookup"><span data-stu-id="95fb8-103">SetPowerState method of the CIM\_AggregatePExtent class</span></span>

<span data-ttu-id="95fb8-104">Il **metodo SetPowerState** imposta lo stato di alimentazione desiderato per un dispositivo logico e quando il dispositivo deve essere inserito in tale stato.</span><span class="sxs-lookup"><span data-stu-id="95fb8-104">The **SetPowerState** method sets the desired power state for a logical device and when the device should be put into that state.</span></span> <span data-ttu-id="95fb8-105">In una sottoclasse, il set di possibili codici restituiti deve essere specificato usando un **qualificatore ValueMap** nel metodo.</span><span class="sxs-lookup"><span data-stu-id="95fb8-105">In a subclass, the set of possible return codes should be specified using a **ValueMap** qualifier on the method.</span></span> <span data-ttu-id="95fb8-106">Le stringhe in cui viene convertito **il contenuto di ValueMap** devono essere specificate anche nella sottoclasse come **qualificatore di** matrice Values.</span><span class="sxs-lookup"><span data-stu-id="95fb8-106">The strings to which the **ValueMap** contents are translated should also be specified in the subclass as a **Values** array qualifier.</span></span> <span data-ttu-id="95fb8-107">Questo metodo viene ereditato da [**CIM \_ LogicalDevice.**](cim-logicaldevice.md)</span><span class="sxs-lookup"><span data-stu-id="95fb8-107">This method is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="95fb8-108">Per altre informazioni sull'uso di questo metodo con C/C++, vedere [Chiamata di un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="95fb8-108">For more information about using this method with C/C++, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="95fb8-109">Le classi CIM (Distributed Management Task Force) DMTF (Distributed Management Task Force) Common Information Model sono le classi padre su cui vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="95fb8-109">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="95fb8-110">WMI supporta attualmente solo gli [schemi della versione CIM 2.x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="95fb8-110">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="95fb8-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="95fb8-111">Syntax</span></span>


```mof
uint32 SetPowerState(
  [in] uint16   PowerState,
  [in] datetime Time
);
```



## <a name="parameters"></a><span data-ttu-id="95fb8-112">Parametri</span><span class="sxs-lookup"><span data-stu-id="95fb8-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="95fb8-113">*PowerState* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="95fb8-113">*PowerState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95fb8-114">Valore **ValueMap** che specifica lo stato di alimentazione desiderato per questo dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="95fb8-114">The **ValueMap** value that specifies the desired power state for this logical device.</span></span>

<dt>

<span data-ttu-id="95fb8-115">1</span><span class="sxs-lookup"><span data-stu-id="95fb8-115">1</span></span>
</dt> <dd>

<span data-ttu-id="95fb8-116">Alimentazione completa</span><span class="sxs-lookup"><span data-stu-id="95fb8-116">Full power</span></span>

</dd> <dt>

<span data-ttu-id="95fb8-117">2</span><span class="sxs-lookup"><span data-stu-id="95fb8-117">2</span></span>
</dt> <dd>

<span data-ttu-id="95fb8-118">Risparmio energia - Modalità a basso consumo</span><span class="sxs-lookup"><span data-stu-id="95fb8-118">Power-save   low-power mode</span></span>

</dd> <dt>

<span data-ttu-id="95fb8-119">3</span><span class="sxs-lookup"><span data-stu-id="95fb8-119">3</span></span>
</dt> <dd>

<span data-ttu-id="95fb8-120">Risparmio energia standby</span><span class="sxs-lookup"><span data-stu-id="95fb8-120">Power-save   standby</span></span>

</dd> <dt>

<span data-ttu-id="95fb8-121">4</span><span class="sxs-lookup"><span data-stu-id="95fb8-121">4</span></span>
</dt> <dd>

<span data-ttu-id="95fb8-122">Risparmio energia - Altro</span><span class="sxs-lookup"><span data-stu-id="95fb8-122">Power-save   other</span></span>

</dd> <dt>

<span data-ttu-id="95fb8-123">5</span><span class="sxs-lookup"><span data-stu-id="95fb8-123">5</span></span>
</dt> <dd>

<span data-ttu-id="95fb8-124">Ciclo di alimentazione</span><span class="sxs-lookup"><span data-stu-id="95fb8-124">Power cycle</span></span>

</dd> <dt>

<span data-ttu-id="95fb8-125">6</span><span class="sxs-lookup"><span data-stu-id="95fb8-125">6</span></span>
</dt> <dd>

<span data-ttu-id="95fb8-126">Spegnimento</span><span class="sxs-lookup"><span data-stu-id="95fb8-126">Power off</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="95fb8-127">*Ora* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="95fb8-127">*Time* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95fb8-128">Quando lo stato di alimentazione deve essere impostato, come valore di data e ora normale o come valore di intervallo (dove l'intervallo inizia quando viene ricevuta la chiamata al metodo).</span><span class="sxs-lookup"><span data-stu-id="95fb8-128">When the power state should be set, either as a regular date-time value or as an interval value (where the interval begins when the method invocation is received).</span></span> <span data-ttu-id="95fb8-129">Quando il *parametro PowerState* è uguale a 5 (ciclo di alimentazione), il parametro *Time* indica quando il dispositivo deve essere ri accensione.</span><span class="sxs-lookup"><span data-stu-id="95fb8-129">When the *PowerState* parameter is equal to 5 (power cycle), the *Time* parameter indicates when the device should power-on again.</span></span> <span data-ttu-id="95fb8-130">L'accensione è immediata.</span><span class="sxs-lookup"><span data-stu-id="95fb8-130">Power-off is immediate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="95fb8-131">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="95fb8-131">Return value</span></span>

<span data-ttu-id="95fb8-132">Restituisce 0 (zero) se ha esito positivo, 1 (uno) se le richieste *PowerState* e *Time* specificate non sono supportate e un altro valore se si è verificato un altro errore.</span><span class="sxs-lookup"><span data-stu-id="95fb8-132">Returns 0 (zero) if successful, 1 (one) if the specified *PowerState* and *Time* request is not supported, and another value if any other error occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="95fb8-133">Commenti</span><span class="sxs-lookup"><span data-stu-id="95fb8-133">Remarks</span></span>

<span data-ttu-id="95fb8-134">Questo metodo non è attualmente implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="95fb8-134">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="95fb8-135">Per usare questo metodo, è necessario implementarlo nel proprio provider.</span><span class="sxs-lookup"><span data-stu-id="95fb8-135">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="95fb8-136">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="95fb8-136">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="95fb8-137">Microsoft potrebbe aver apportato modifiche per correggere errori minori, essere conforme agli standard della documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="95fb8-137">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="95fb8-138">Requisiti</span><span class="sxs-lookup"><span data-stu-id="95fb8-138">Requirements</span></span>



| <span data-ttu-id="95fb8-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="95fb8-139">Requirement</span></span> | <span data-ttu-id="95fb8-140">Valore</span><span class="sxs-lookup"><span data-stu-id="95fb8-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="95fb8-141">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="95fb8-141">Minimum supported client</span></span><br/> | <span data-ttu-id="95fb8-142">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="95fb8-142">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="95fb8-143">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="95fb8-143">Minimum supported server</span></span><br/> | <span data-ttu-id="95fb8-144">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="95fb8-144">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="95fb8-145">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="95fb8-145">Namespace</span></span><br/>                | <span data-ttu-id="95fb8-146">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="95fb8-146">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="95fb8-147">MOF</span><span class="sxs-lookup"><span data-stu-id="95fb8-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="95fb8-148"><dt>CIMWin32.mof</dt></span><span class="sxs-lookup"><span data-stu-id="95fb8-148"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="95fb8-149">DLL</span><span class="sxs-lookup"><span data-stu-id="95fb8-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="95fb8-150"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="95fb8-150"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="95fb8-151">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="95fb8-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95fb8-152">**CIM \_ AggregatePExtent**</span><span class="sxs-lookup"><span data-stu-id="95fb8-152">**CIM\_AggregatePExtent**</span></span>](setpowerstate-method-in-class-cim-aggregatepextent.md)
</dt> <dt>

[<span data-ttu-id="95fb8-153">**CIM \_ AggregatePExtent**</span><span class="sxs-lookup"><span data-stu-id="95fb8-153">**CIM\_AggregatePExtent**</span></span>](cim-aggregatepextent.md)
</dt> </dl>

 

