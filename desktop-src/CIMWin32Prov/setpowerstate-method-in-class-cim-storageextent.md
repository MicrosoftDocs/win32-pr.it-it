---
description: Il metodo SetPowerState della classe CIM \_ StorageExtent imposta lo stato di alimentazione desiderato per un dispositivo logico e quando un dispositivo deve essere inserito in tale stato.
ms.assetid: a344575f-c8b5-4fa5-a055-bd9c02332e2b
ms.tgt_platform: multiple
title: Metodo SetPowerState della classe CIM_StorageExtent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_StorageExtent.SetPowerState
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: e5b00ded3e8e08f3f809b21fc56607f8a8d257fa
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104522897"
---
# <a name="setpowerstate-method-of-the-cim_storageextent-class"></a><span data-ttu-id="57f40-103">Metodo SetPowerState della classe CIM \_ StorageExtent</span><span class="sxs-lookup"><span data-stu-id="57f40-103">SetPowerState method of the CIM\_StorageExtent class</span></span>

<span data-ttu-id="57f40-104">Il metodo **SetPowerState** della classe CIM \_ StorageExtent imposta lo stato di alimentazione desiderato per un dispositivo logico e quando un dispositivo deve essere inserito in tale stato.</span><span class="sxs-lookup"><span data-stu-id="57f40-104">The **SetPowerState** method of the CIM\_StorageExtent class sets the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="57f40-105">In una sottoclasse, è necessario specificare il set di possibili codici restituiti utilizzando un qualificatore **ValueMap** nel metodo.</span><span class="sxs-lookup"><span data-stu-id="57f40-105">In a subclass, the set of possible return codes should be specified by using a **ValueMap** qualifier on the method.</span></span> <span data-ttu-id="57f40-106">Le stringhe a cui viene convertito il contenuto **ValueMap** devono essere specificate anche nella sottoclasse come qualificatore della matrice di **valori** .</span><span class="sxs-lookup"><span data-stu-id="57f40-106">The strings to which the **ValueMap** contents are translated should also be specified in the subclass as a **Values** array qualifier.</span></span> <span data-ttu-id="57f40-107">Questo metodo viene ereditato da [**\_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="57f40-107">This method is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="57f40-108">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="57f40-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="57f40-109">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="57f40-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="57f40-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="57f40-110">Syntax</span></span>


```mof
uint32 SetPowerState(
  [in] uint16   PowerState,
  [in] datetime Time
);
```



## <a name="parameters"></a><span data-ttu-id="57f40-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="57f40-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="57f40-112">*PowerState* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="57f40-112">*PowerState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="57f40-113">Valore **ValueMap** che specifica lo stato di alimentazione desiderato per questo dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="57f40-113">A **ValueMap** value that specifies the desired power state for this logical device.</span></span>

<dt>

<span data-ttu-id="57f40-114">1</span><span class="sxs-lookup"><span data-stu-id="57f40-114">1</span></span>
</dt> <dd>

<span data-ttu-id="57f40-115">Potenza piena.</span><span class="sxs-lookup"><span data-stu-id="57f40-115">Full power.</span></span>

</dd> <dt>

<span data-ttu-id="57f40-116">2</span><span class="sxs-lookup"><span data-stu-id="57f40-116">2</span></span>
</dt> <dd>

<span data-ttu-id="57f40-117">Risparmio energia-modalità a basso consumo.</span><span class="sxs-lookup"><span data-stu-id="57f40-117">Power save   low-power mode.</span></span>

</dd> <dt>

<span data-ttu-id="57f40-118">3</span><span class="sxs-lookup"><span data-stu-id="57f40-118">3</span></span>
</dt> <dd>

<span data-ttu-id="57f40-119">Risparmio energia standby.</span><span class="sxs-lookup"><span data-stu-id="57f40-119">Power save   standby.</span></span>

</dd> <dt>

<span data-ttu-id="57f40-120">4</span><span class="sxs-lookup"><span data-stu-id="57f40-120">4</span></span>
</dt> <dd>

<span data-ttu-id="57f40-121">Risparmio di energia.</span><span class="sxs-lookup"><span data-stu-id="57f40-121">Power save   other.</span></span>

</dd> <dt>

<span data-ttu-id="57f40-122">5</span><span class="sxs-lookup"><span data-stu-id="57f40-122">5</span></span>
</dt> <dd>

<span data-ttu-id="57f40-123">Ciclo di alimentazione.</span><span class="sxs-lookup"><span data-stu-id="57f40-123">Power cycle.</span></span>

</dd> <dt>

<span data-ttu-id="57f40-124">6</span><span class="sxs-lookup"><span data-stu-id="57f40-124">6</span></span>
</dt> <dd>

<span data-ttu-id="57f40-125">Spegnimento.</span><span class="sxs-lookup"><span data-stu-id="57f40-125">Power off.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="57f40-126">*Ora* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="57f40-126">*Time* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="57f40-127">Specifica quando deve essere impostato lo stato di alimentazione, come valore di data e ora normale o come valore di intervallo, in cui l'intervallo inizia quando viene ricevuta la chiamata al metodo.</span><span class="sxs-lookup"><span data-stu-id="57f40-127">Specifies when the power state should be set, either as a regular date-time value or as an interval value (where the interval begins when the method invocation is received).</span></span> <span data-ttu-id="57f40-128">Quando il parametro *PowerState* è uguale a 5 ("ciclo di alimentazione"), il parametro *Time* indica quando riaccendere il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="57f40-128">When the *PowerState* parameter is equal to 5 ("Power Cycle"), the *Time* parameter indicates when the device should power on again.</span></span> <span data-ttu-id="57f40-129">Lo spegnimento è immediato.</span><span class="sxs-lookup"><span data-stu-id="57f40-129">Power-off is immediate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="57f40-130">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="57f40-130">Return value</span></span>

<span data-ttu-id="57f40-131">Restituisce 0 (zero) se ha esito positivo, 1 (uno) se la richiesta *PowerState* e *Time* specificata non è supportata e un altro valore se si sono verificati altri errori.</span><span class="sxs-lookup"><span data-stu-id="57f40-131">Returns 0 (zero) if successful, 1 (one) if the specified *PowerState* and *Time* request is not supported, and another value if any other error occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="57f40-132">Commenti</span><span class="sxs-lookup"><span data-stu-id="57f40-132">Remarks</span></span>

<span data-ttu-id="57f40-133">Questo metodo non è attualmente implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="57f40-133">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="57f40-134">Per usare questo metodo, è necessario implementarlo nel proprio provider.</span><span class="sxs-lookup"><span data-stu-id="57f40-134">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="57f40-135">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="57f40-135">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="57f40-136">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="57f40-136">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="57f40-137">Requisiti</span><span class="sxs-lookup"><span data-stu-id="57f40-137">Requirements</span></span>



| <span data-ttu-id="57f40-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="57f40-138">Requirement</span></span> | <span data-ttu-id="57f40-139">Valore</span><span class="sxs-lookup"><span data-stu-id="57f40-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="57f40-140">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="57f40-140">Minimum supported client</span></span><br/> | <span data-ttu-id="57f40-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="57f40-141">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="57f40-142">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="57f40-142">Minimum supported server</span></span><br/> | <span data-ttu-id="57f40-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="57f40-143">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="57f40-144">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="57f40-144">Namespace</span></span><br/>                | <span data-ttu-id="57f40-145">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="57f40-145">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="57f40-146">MOF</span><span class="sxs-lookup"><span data-stu-id="57f40-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="57f40-147"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="57f40-147"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="57f40-148">DLL</span><span class="sxs-lookup"><span data-stu-id="57f40-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="57f40-149"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="57f40-149"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="57f40-150">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="57f40-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57f40-151">\_STORAGEEXTENT CIM</span><span class="sxs-lookup"><span data-stu-id="57f40-151">CIM\_StorageExtent</span></span>](setpowerstate-method-in-class-cim-storageextent.md)
</dt> <dt>

[<span data-ttu-id="57f40-152">**\_STORAGEEXTENT CIM**</span><span class="sxs-lookup"><span data-stu-id="57f40-152">**CIM\_StorageExtent**</span></span>](cim-storageextent.md)
</dt> </dl>

 

 




