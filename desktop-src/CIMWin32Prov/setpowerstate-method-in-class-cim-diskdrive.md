---
description: 'Metodo SetPowerState della classe CIM_DiskDrive: il metodo SetPowerState imposta lo stato di alimentazione desiderato per un dispositivo logico e quando un dispositivo deve essere inserito in tale stato.'
ms.assetid: 6a77d4ce-f895-4eed-a963-b2718d0e26cc
ms.tgt_platform: multiple
title: Metodo SetPowerState della classe CIM_DiskDrive
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DiskDrive.SetPowerState
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: a63e9346dc0229de296e106a47927ba73e20f60d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108089389"
---
# <a name="setpowerstate-method-of-the-cim_diskdrive-class"></a><span data-ttu-id="c1bb6-103">Metodo SetPowerState della classe \_ CiM DiskDrive</span><span class="sxs-lookup"><span data-stu-id="c1bb6-103">SetPowerState method of the CIM\_DiskDrive class</span></span>

<span data-ttu-id="c1bb6-104">Il **metodo SetPowerState** imposta lo stato di alimentazione desiderato per un dispositivo logico e quando un dispositivo deve essere inserito in tale stato.</span><span class="sxs-lookup"><span data-stu-id="c1bb6-104">The **SetPowerState** method sets the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="c1bb6-105">In una sottoclasse, il set di possibili codici restituiti deve essere specificato usando un **qualificatore ValueMap** nel metodo.</span><span class="sxs-lookup"><span data-stu-id="c1bb6-105">In a subclass, the set of possible return codes should be specified using a **ValueMap** qualifier on the method.</span></span> <span data-ttu-id="c1bb6-106">Le stringhe in cui vengono **convertiti i contenuti di ValueMap** devono essere specificate anche nella sottoclasse come qualificatore di matrice **Values.**</span><span class="sxs-lookup"><span data-stu-id="c1bb6-106">The strings to which the **ValueMap** contents are translated should also be specified in the subclass as a **Values** array qualifier.</span></span> <span data-ttu-id="c1bb6-107">Questo metodo viene ereditato da [**CIM \_ LogicalDevice.**](cim-logicaldevice.md)</span><span class="sxs-lookup"><span data-stu-id="c1bb6-107">This method is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c1bb6-108">Le classi CIM (Distributed Management Task Force) DMTF (Common Information Model Distributed Management Task Force) sono le classi padre su cui vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="c1bb6-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="c1bb6-109">WMI attualmente supporta solo gli schemi [della versione CIM 2.x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="c1bb6-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="c1bb6-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c1bb6-110">Syntax</span></span>


```mof
uint32 SetPowerState(
  [in] uint16   PowerState,
  [in] datetime Time
);
```



## <a name="parameters"></a><span data-ttu-id="c1bb6-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="c1bb6-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c1bb6-112">*PowerState* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="c1bb6-112">*PowerState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1bb6-113">Valore **ValueMap** che specifica lo stato di alimentazione desiderato per questo dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="c1bb6-113">A **ValueMap** value that specifies the desired power state for this logical device.</span></span>

<dt>

<span data-ttu-id="c1bb6-114">1</span><span class="sxs-lookup"><span data-stu-id="c1bb6-114">1</span></span>
</dt> <dd>

<span data-ttu-id="c1bb6-115">Alimentazione completa.</span><span class="sxs-lookup"><span data-stu-id="c1bb6-115">Full power.</span></span>

</dd> <dt>

<span data-ttu-id="c1bb6-116">2</span><span class="sxs-lookup"><span data-stu-id="c1bb6-116">2</span></span>
</dt> <dd>

<span data-ttu-id="c1bb6-117">Risparmio energia in modalità a basso consumo.</span><span class="sxs-lookup"><span data-stu-id="c1bb6-117">Power save   low-power mode.</span></span>

</dd> <dt>

<span data-ttu-id="c1bb6-118">3</span><span class="sxs-lookup"><span data-stu-id="c1bb6-118">3</span></span>
</dt> <dd>

<span data-ttu-id="c1bb6-119">Risparmio energia standby.</span><span class="sxs-lookup"><span data-stu-id="c1bb6-119">Power save   standby.</span></span>

</dd> <dt>

<span data-ttu-id="c1bb6-120">4</span><span class="sxs-lookup"><span data-stu-id="c1bb6-120">4</span></span>
</dt> <dd>

<span data-ttu-id="c1bb6-121">Risparmio energia altro.</span><span class="sxs-lookup"><span data-stu-id="c1bb6-121">Power save   other.</span></span>

</dd> <dt>

<span data-ttu-id="c1bb6-122">5</span><span class="sxs-lookup"><span data-stu-id="c1bb6-122">5</span></span>
</dt> <dd>

<span data-ttu-id="c1bb6-123">Ciclo di alimentazione.</span><span class="sxs-lookup"><span data-stu-id="c1bb6-123">Power cycle.</span></span>

</dd> <dt>

<span data-ttu-id="c1bb6-124">6</span><span class="sxs-lookup"><span data-stu-id="c1bb6-124">6</span></span>
</dt> <dd>

<span data-ttu-id="c1bb6-125">Spegnere.</span><span class="sxs-lookup"><span data-stu-id="c1bb6-125">Power off.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="c1bb6-126">*Ora* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="c1bb6-126">*Time* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1bb6-127">Specifica quando deve essere impostato lo stato di alimentazione, come valore di data e ora regolare o come valore di intervallo (in cui l'intervallo inizia quando viene ricevuta la chiamata al metodo).</span><span class="sxs-lookup"><span data-stu-id="c1bb6-127">Specifies when the power state should be set, either as a regular date-time value or as an interval value (where the interval begins when the method invocation is received).</span></span> <span data-ttu-id="c1bb6-128">Quando il *parametro PowerState* è uguale a 5 ("Ciclo di alimentazione"), il *parametro Time* indica quando il dispositivo deve essere ri accensione.</span><span class="sxs-lookup"><span data-stu-id="c1bb6-128">When the *PowerState* parameter is equal to 5 ("Power Cycle"), the *Time* parameter indicates when the device should power on again.</span></span> <span data-ttu-id="c1bb6-129">L'accensione è immediata.</span><span class="sxs-lookup"><span data-stu-id="c1bb6-129">Power-off is immediate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c1bb6-130">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c1bb6-130">Return value</span></span>

<span data-ttu-id="c1bb6-131">Restituisce 0 (zero) in caso di esito positivo, 1 (uno) se la richiesta *PowerState* e *Time* specificata non è supportata e un altro valore se si è verificato un altro errore.</span><span class="sxs-lookup"><span data-stu-id="c1bb6-131">Returns 0 (zero) if successful, 1 (one) if the specified *PowerState* and *Time* request is not supported, and another value if any other error occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="c1bb6-132">Commenti</span><span class="sxs-lookup"><span data-stu-id="c1bb6-132">Remarks</span></span>

<span data-ttu-id="c1bb6-133">Questo metodo non è attualmente implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="c1bb6-133">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="c1bb6-134">Per usare questo metodo, è necessario implementarlo nel proprio provider.</span><span class="sxs-lookup"><span data-stu-id="c1bb6-134">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="c1bb6-135">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="c1bb6-135">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="c1bb6-136">Microsoft potrebbe aver apportato modifiche per correggere errori secondari, essere conforme agli standard della documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="c1bb6-136">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="c1bb6-137">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c1bb6-137">Requirements</span></span>



| <span data-ttu-id="c1bb6-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="c1bb6-138">Requirement</span></span> | <span data-ttu-id="c1bb6-139">Valore</span><span class="sxs-lookup"><span data-stu-id="c1bb6-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c1bb6-140">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c1bb6-140">Minimum supported client</span></span><br/> | <span data-ttu-id="c1bb6-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c1bb6-141">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c1bb6-142">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c1bb6-142">Minimum supported server</span></span><br/> | <span data-ttu-id="c1bb6-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c1bb6-143">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c1bb6-144">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="c1bb6-144">Namespace</span></span><br/>                | <span data-ttu-id="c1bb6-145">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="c1bb6-145">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="c1bb6-146">MOF</span><span class="sxs-lookup"><span data-stu-id="c1bb6-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c1bb6-147"><dt>CIMWin32.mof</dt></span><span class="sxs-lookup"><span data-stu-id="c1bb6-147"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="c1bb6-148">DLL</span><span class="sxs-lookup"><span data-stu-id="c1bb6-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c1bb6-149"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c1bb6-149"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c1bb6-150">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c1bb6-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1bb6-151">CIM \_ DiskDrive</span><span class="sxs-lookup"><span data-stu-id="c1bb6-151">CIM\_DiskDrive</span></span>](setpowerstate-method-in-class-cim-diskdrive.md)
</dt> <dt>

[<span data-ttu-id="c1bb6-152">**CIM \_ DiskDrive**</span><span class="sxs-lookup"><span data-stu-id="c1bb6-152">**CIM\_DiskDrive**</span></span>](cim-diskdrive.md)
</dt> </dl>

 

 




