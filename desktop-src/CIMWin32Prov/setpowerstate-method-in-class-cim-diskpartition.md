---
description: Il metodo SetPowerState della classe CIM \_ DiskPartition imposta lo stato di alimentazione desiderato per un dispositivo logico e quando un dispositivo deve essere inserito in tale stato.
ms.assetid: cfc68ad3-819c-438f-baca-bed6e2592369
ms.tgt_platform: multiple
title: Metodo SetPowerState della classe CIM_DiskPartition
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DiskPartition.SetPowerState
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: a8316dbf0bc0c6aa438b2881c691cde6976501c0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304664"
---
# <a name="setpowerstate-method-of-the-cim_diskpartition-class"></a><span data-ttu-id="15426-103">Metodo SetPowerState della classe CIM \_ DiskPartition</span><span class="sxs-lookup"><span data-stu-id="15426-103">SetPowerState method of the CIM\_DiskPartition class</span></span>

<span data-ttu-id="15426-104">Il metodo **SetPowerState** della classe CIM \_ DiskPartition imposta lo stato di alimentazione desiderato per un dispositivo logico e quando un dispositivo deve essere inserito in tale stato.</span><span class="sxs-lookup"><span data-stu-id="15426-104">The **SetPowerState** method of the CIM\_DiskPartition class sets the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="15426-105">In una sottoclasse, è necessario specificare il set di possibili codici restituiti utilizzando un qualificatore **ValueMap** nel metodo.</span><span class="sxs-lookup"><span data-stu-id="15426-105">In a subclass, the set of possible return codes should be specified by using a **ValueMap** qualifier on the method.</span></span> <span data-ttu-id="15426-106">Le stringhe a cui viene convertito il contenuto **ValueMap** devono essere specificate anche nella sottoclasse come qualificatore della matrice di **valori** .</span><span class="sxs-lookup"><span data-stu-id="15426-106">The strings to which the **ValueMap** contents are translated should also be specified in the subclass as a **Values** array qualifier.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="15426-107">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="15426-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="15426-108">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="15426-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="15426-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="15426-109">Syntax</span></span>


```mof
uint32 SetPowerState(
  [in] uint16   PowerState,
  [in] datetime Time
);
```



## <a name="parameters"></a><span data-ttu-id="15426-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="15426-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="15426-111">*PowerState* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="15426-111">*PowerState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="15426-112">Valore **ValueMap** che specifica lo stato di alimentazione desiderato per questo dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="15426-112">A **ValueMap** value that specifies the desired power state for this logical device.</span></span>

<dt>

<span data-ttu-id="15426-113">1</span><span class="sxs-lookup"><span data-stu-id="15426-113">1</span></span>
</dt> <dd>

<span data-ttu-id="15426-114">Potenza piena.</span><span class="sxs-lookup"><span data-stu-id="15426-114">Full power.</span></span>

</dd> <dt>

<span data-ttu-id="15426-115">2</span><span class="sxs-lookup"><span data-stu-id="15426-115">2</span></span>
</dt> <dd>

<span data-ttu-id="15426-116">Risparmio energia-modalità a basso consumo.</span><span class="sxs-lookup"><span data-stu-id="15426-116">Power save   low-power mode.</span></span>

</dd> <dt>

<span data-ttu-id="15426-117">3</span><span class="sxs-lookup"><span data-stu-id="15426-117">3</span></span>
</dt> <dd>

<span data-ttu-id="15426-118">Risparmio energia standby.</span><span class="sxs-lookup"><span data-stu-id="15426-118">Power save   standby.</span></span>

</dd> <dt>

<span data-ttu-id="15426-119">4</span><span class="sxs-lookup"><span data-stu-id="15426-119">4</span></span>
</dt> <dd>

<span data-ttu-id="15426-120">Risparmio di energia.</span><span class="sxs-lookup"><span data-stu-id="15426-120">Power save   other.</span></span>

</dd> <dt>

<span data-ttu-id="15426-121">5</span><span class="sxs-lookup"><span data-stu-id="15426-121">5</span></span>
</dt> <dd>

<span data-ttu-id="15426-122">Ciclo di alimentazione.</span><span class="sxs-lookup"><span data-stu-id="15426-122">Power cycle.</span></span>

</dd> <dt>

<span data-ttu-id="15426-123">6</span><span class="sxs-lookup"><span data-stu-id="15426-123">6</span></span>
</dt> <dd>

<span data-ttu-id="15426-124">Spegnimento.</span><span class="sxs-lookup"><span data-stu-id="15426-124">Power off.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="15426-125">*Ora* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="15426-125">*Time* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="15426-126">Specifica quando deve essere impostato lo stato di alimentazione, come valore di data e ora normale o come valore di intervallo, in cui l'intervallo inizia quando viene ricevuta la chiamata al metodo.</span><span class="sxs-lookup"><span data-stu-id="15426-126">Specifies when the power state should be set, either as a regular date-time value or as an interval value (where the interval begins when the method invocation is received).</span></span> <span data-ttu-id="15426-127">Quando il parametro *PowerState* è uguale a 5 ("ciclo di alimentazione"), il parametro *Time* indica quando riaccendere il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="15426-127">When the *PowerState* parameter is equal to 5 ("Power Cycle"), the *Time* parameter indicates when the device should power on again.</span></span> <span data-ttu-id="15426-128">Lo spegnimento è immediato.</span><span class="sxs-lookup"><span data-stu-id="15426-128">Power-off is immediate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="15426-129">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="15426-129">Return value</span></span>

<span data-ttu-id="15426-130">Restituisce 0 (zero) se ha esito positivo, 1 (uno) se la richiesta *PowerState* e *Time* specificata non è supportata e un altro valore se si sono verificati altri errori.</span><span class="sxs-lookup"><span data-stu-id="15426-130">Returns 0 (zero) if successful, 1 (one) if the specified *PowerState* and *Time* request is not supported, and another value if any other error occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="15426-131">Commenti</span><span class="sxs-lookup"><span data-stu-id="15426-131">Remarks</span></span>

<span data-ttu-id="15426-132">Questo metodo non è attualmente implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="15426-132">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="15426-133">Per usare questo metodo, è necessario implementarlo nel proprio provider.</span><span class="sxs-lookup"><span data-stu-id="15426-133">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="15426-134">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="15426-134">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="15426-135">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="15426-135">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="15426-136">Requisiti</span><span class="sxs-lookup"><span data-stu-id="15426-136">Requirements</span></span>



| <span data-ttu-id="15426-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="15426-137">Requirement</span></span> | <span data-ttu-id="15426-138">Valore</span><span class="sxs-lookup"><span data-stu-id="15426-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="15426-139">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="15426-139">Minimum supported client</span></span><br/> | <span data-ttu-id="15426-140">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="15426-140">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="15426-141">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="15426-141">Minimum supported server</span></span><br/> | <span data-ttu-id="15426-142">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="15426-142">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="15426-143">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="15426-143">Namespace</span></span><br/>                | <span data-ttu-id="15426-144">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="15426-144">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="15426-145">MOF</span><span class="sxs-lookup"><span data-stu-id="15426-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="15426-146"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="15426-146"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="15426-147">DLL</span><span class="sxs-lookup"><span data-stu-id="15426-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="15426-148"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="15426-148"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="15426-149">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="15426-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15426-150">\_DISKPARTITION CIM</span><span class="sxs-lookup"><span data-stu-id="15426-150">CIM\_DiskPartition</span></span>](setpowerstate-method-in-class-cim-diskpartition.md)
</dt> <dt>

[<span data-ttu-id="15426-151">**\_DISKPARTITION CIM**</span><span class="sxs-lookup"><span data-stu-id="15426-151">**CIM\_DiskPartition**</span></span>](cim-diskpartition.md)
</dt> </dl>

 

 




