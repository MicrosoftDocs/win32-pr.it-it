---
description: 'Metodo SetPowerState della classe CIM_CDROMDrive: il metodo SetPowerState imposta lo stato di alimentazione desiderato per un dispositivo logico e quando un dispositivo deve essere inserito in tale stato.'
ms.assetid: 2f252d65-55ad-43b2-bee4-d5db24ca9d29
ms.tgt_platform: multiple
title: Metodo SetPowerState della classe CIM_CDROMDrive
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_CDROMDrive.SetPowerState
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: a8a69b3f3d810fe48b7a0e1d31a57a96e279d14a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108089499"
---
# <a name="setpowerstate-method-of-the-cim_cdromdrive-class"></a><span data-ttu-id="1f1e5-103">Metodo SetPowerState della classe \_ CIM CDROMDrive</span><span class="sxs-lookup"><span data-stu-id="1f1e5-103">SetPowerState method of the CIM\_CDROMDrive class</span></span>

<span data-ttu-id="1f1e5-104">Il **metodo SetPowerState** imposta lo stato di alimentazione desiderato per un dispositivo logico e quando un dispositivo deve essere inserito in tale stato.</span><span class="sxs-lookup"><span data-stu-id="1f1e5-104">The **SetPowerState** method sets the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="1f1e5-105">In una sottoclasse, il set di possibili codici restituiti deve essere specificato usando un **qualificatore ValueMap** nel metodo.</span><span class="sxs-lookup"><span data-stu-id="1f1e5-105">In a subclass, the set of possible return codes should be specified using a **ValueMap** qualifier on the method.</span></span> <span data-ttu-id="1f1e5-106">Le stringhe in cui vengono **convertiti i contenuti di ValueMap** devono essere specificate anche nella sottoclasse come qualificatore di matrice **Values.**</span><span class="sxs-lookup"><span data-stu-id="1f1e5-106">The strings to which the **ValueMap** contents are translated should also be specified in the subclass as a **Values** array qualifier.</span></span> <span data-ttu-id="1f1e5-107">Questo metodo viene ereditato da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="1f1e5-107">This method is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1f1e5-108">Le classi CIM (Distributed Management Task Force) DMTF (Common Information Model) sono le classi padre su cui vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="1f1e5-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="1f1e5-109">WMI attualmente supporta solo gli [schemi della versione CIM 2.x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="1f1e5-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="1f1e5-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1f1e5-110">Syntax</span></span>


```mof
uint32 SetPowerState(
  [in] uint16   PowerState,
  [in] datetime Time
);
```



## <a name="parameters"></a><span data-ttu-id="1f1e5-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="1f1e5-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1f1e5-112">*PowerState* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="1f1e5-112">*PowerState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1f1e5-113">Valore **ValueMap** che specifica lo stato di alimentazione desiderato per questo dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="1f1e5-113">A **ValueMap** value that specifies the desired power state for this logical device.</span></span>

<dt>

<span data-ttu-id="1f1e5-114">1</span><span class="sxs-lookup"><span data-stu-id="1f1e5-114">1</span></span>
</dt> <dd>

<span data-ttu-id="1f1e5-115">Alimentazione completa.</span><span class="sxs-lookup"><span data-stu-id="1f1e5-115">Full power.</span></span>

</dd> <dt>

<span data-ttu-id="1f1e5-116">2</span><span class="sxs-lookup"><span data-stu-id="1f1e5-116">2</span></span>
</dt> <dd>

<span data-ttu-id="1f1e5-117">Risparmio energia in modalità a basso consumo.</span><span class="sxs-lookup"><span data-stu-id="1f1e5-117">Power save   low-power mode.</span></span>

</dd> <dt>

<span data-ttu-id="1f1e5-118">3</span><span class="sxs-lookup"><span data-stu-id="1f1e5-118">3</span></span>
</dt> <dd>

<span data-ttu-id="1f1e5-119">Risparmio energia standby.</span><span class="sxs-lookup"><span data-stu-id="1f1e5-119">Power save   standby.</span></span>

</dd> <dt>

<span data-ttu-id="1f1e5-120">4</span><span class="sxs-lookup"><span data-stu-id="1f1e5-120">4</span></span>
</dt> <dd>

<span data-ttu-id="1f1e5-121">Risparmio energia altro.</span><span class="sxs-lookup"><span data-stu-id="1f1e5-121">Power save   other.</span></span>

</dd> <dt>

<span data-ttu-id="1f1e5-122">5</span><span class="sxs-lookup"><span data-stu-id="1f1e5-122">5</span></span>
</dt> <dd>

<span data-ttu-id="1f1e5-123">Ciclo di alimentazione.</span><span class="sxs-lookup"><span data-stu-id="1f1e5-123">Power cycle.</span></span>

</dd> <dt>

<span data-ttu-id="1f1e5-124">6</span><span class="sxs-lookup"><span data-stu-id="1f1e5-124">6</span></span>
</dt> <dd>

<span data-ttu-id="1f1e5-125">Spegnere.</span><span class="sxs-lookup"><span data-stu-id="1f1e5-125">Power off.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="1f1e5-126">*Ora* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="1f1e5-126">*Time* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1f1e5-127">Specifica quando deve essere impostato lo stato di alimentazione, come valore di data e ora regolare o come valore di intervallo (in cui l'intervallo inizia quando viene ricevuta la chiamata al metodo).</span><span class="sxs-lookup"><span data-stu-id="1f1e5-127">Specifies when the power state should be set, either as a regular date-time value or as an interval value (where the interval begins when the method invocation is received).</span></span> <span data-ttu-id="1f1e5-128">Quando il *parametro PowerState* è uguale a 5 ("Ciclo di alimentazione"), il *parametro Time* indica quando il dispositivo deve essere ri accensione.</span><span class="sxs-lookup"><span data-stu-id="1f1e5-128">When the *PowerState* parameter is equal to 5 ("Power Cycle"), the *Time* parameter indicates when the device should power on again.</span></span> <span data-ttu-id="1f1e5-129">L'accensione è immediata.</span><span class="sxs-lookup"><span data-stu-id="1f1e5-129">Power-off is immediate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1f1e5-130">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1f1e5-130">Return value</span></span>

<span data-ttu-id="1f1e5-131">Restituisce 0 (zero) se ha esito positivo, 1 (uno) se le richieste *PowerState* e *Time* specificate non sono supportate e un altro valore se si è verificato un altro errore.</span><span class="sxs-lookup"><span data-stu-id="1f1e5-131">Returns 0 (zero) if successful, 1 (one) if the specified *PowerState* and *Time* request is not supported, and another value if any other error occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="1f1e5-132">Commenti</span><span class="sxs-lookup"><span data-stu-id="1f1e5-132">Remarks</span></span>

<span data-ttu-id="1f1e5-133">Questo metodo non è attualmente implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="1f1e5-133">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="1f1e5-134">Per usare questo metodo, è necessario implementarlo nel proprio provider.</span><span class="sxs-lookup"><span data-stu-id="1f1e5-134">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="1f1e5-135">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="1f1e5-135">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="1f1e5-136">Microsoft potrebbe aver apportato modifiche per correggere errori minori, essere conforme agli standard della documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="1f1e5-136">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="1f1e5-137">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1f1e5-137">Requirements</span></span>



| <span data-ttu-id="1f1e5-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="1f1e5-138">Requirement</span></span> | <span data-ttu-id="1f1e5-139">Valore</span><span class="sxs-lookup"><span data-stu-id="1f1e5-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1f1e5-140">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1f1e5-140">Minimum supported client</span></span><br/> | <span data-ttu-id="1f1e5-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1f1e5-141">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1f1e5-142">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1f1e5-142">Minimum supported server</span></span><br/> | <span data-ttu-id="1f1e5-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1f1e5-143">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1f1e5-144">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="1f1e5-144">Namespace</span></span><br/>                | <span data-ttu-id="1f1e5-145">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="1f1e5-145">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="1f1e5-146">MOF</span><span class="sxs-lookup"><span data-stu-id="1f1e5-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1f1e5-147"><dt>CIMWin32.mof</dt></span><span class="sxs-lookup"><span data-stu-id="1f1e5-147"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="1f1e5-148">DLL</span><span class="sxs-lookup"><span data-stu-id="1f1e5-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1f1e5-149"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1f1e5-149"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1f1e5-150">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1f1e5-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f1e5-151">CIM \_ CDROMDrive</span><span class="sxs-lookup"><span data-stu-id="1f1e5-151">CIM\_CDROMDrive</span></span>](setpowerstate-method-in-class-cim-cdromdrive.md)
</dt> <dt>

[<span data-ttu-id="1f1e5-152">**CIM \_ CDROMDrive**</span><span class="sxs-lookup"><span data-stu-id="1f1e5-152">**CIM\_CDROMDrive**</span></span>](cim-cdromdrive.md)
</dt> </dl>

 

 




