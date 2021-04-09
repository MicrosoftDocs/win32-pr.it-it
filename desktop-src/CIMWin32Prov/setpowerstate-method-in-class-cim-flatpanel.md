---
description: Il metodo SetPowerState della classe CIM \_ piatto imposta lo stato di alimentazione desiderato per un dispositivo logico e quando un dispositivo deve essere inserito in tale stato.
ms.assetid: 75f5f588-f3d3-471c-bff4-a511abcee576
ms.tgt_platform: multiple
title: Metodo SetPowerState della classe CIM_FlatPanel
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_FlatPanel.SetPowerState
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 592507944e3e83eefa60d457059b7eb16028caff
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877953"
---
# <a name="setpowerstate-method-of-the-cim_flatpanel-class"></a><span data-ttu-id="ffa7e-103">Metodo SetPowerState della classe CIM \_ piatto</span><span class="sxs-lookup"><span data-stu-id="ffa7e-103">SetPowerState method of the CIM\_FlatPanel class</span></span>

<span data-ttu-id="ffa7e-104">Il metodo **SetPowerState** della classe CIM \_ piatto imposta lo stato di alimentazione desiderato per un dispositivo logico e quando un dispositivo deve essere inserito in tale stato.</span><span class="sxs-lookup"><span data-stu-id="ffa7e-104">The **SetPowerState** method of the CIM\_FlatPanel class sets the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="ffa7e-105">In una sottoclasse, è necessario specificare il set di possibili codici restituiti utilizzando un qualificatore **ValueMap** nel metodo.</span><span class="sxs-lookup"><span data-stu-id="ffa7e-105">In a subclass, the set of possible return codes should be specified by using a **ValueMap** qualifier on the method.</span></span> <span data-ttu-id="ffa7e-106">Le stringhe a cui viene convertito il contenuto **ValueMap** devono essere specificate anche nella sottoclasse come qualificatore della matrice di **valori** .</span><span class="sxs-lookup"><span data-stu-id="ffa7e-106">The strings to which the **ValueMap** contents are translated should also be specified in the subclass as a **Values** array qualifier.</span></span> <span data-ttu-id="ffa7e-107">Questo metodo viene ereditato da [**\_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="ffa7e-107">This method is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ffa7e-108">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="ffa7e-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="ffa7e-109">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="ffa7e-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="ffa7e-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ffa7e-110">Syntax</span></span>


```mof
uint32 SetPowerState(
  [in] uint16   PowerState,
  [in] datetime Time
);
```



## <a name="parameters"></a><span data-ttu-id="ffa7e-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="ffa7e-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ffa7e-112">*PowerState* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ffa7e-112">*PowerState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ffa7e-113">Valore **ValueMap** che specifica lo stato di alimentazione desiderato per il dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="ffa7e-113">A **ValueMap** value that specifies the desired power state for the logical device.</span></span>

<dt>

<span data-ttu-id="ffa7e-114">1</span><span class="sxs-lookup"><span data-stu-id="ffa7e-114">1</span></span>
</dt> <dd>

<span data-ttu-id="ffa7e-115">Potenza piena.</span><span class="sxs-lookup"><span data-stu-id="ffa7e-115">Full power.</span></span>

</dd> <dt>

<span data-ttu-id="ffa7e-116">2</span><span class="sxs-lookup"><span data-stu-id="ffa7e-116">2</span></span>
</dt> <dd>

<span data-ttu-id="ffa7e-117">Risparmio energia-modalità a basso consumo.</span><span class="sxs-lookup"><span data-stu-id="ffa7e-117">Power save   low-power mode.</span></span>

</dd> <dt>

<span data-ttu-id="ffa7e-118">3</span><span class="sxs-lookup"><span data-stu-id="ffa7e-118">3</span></span>
</dt> <dd>

<span data-ttu-id="ffa7e-119">Risparmio energia standby.</span><span class="sxs-lookup"><span data-stu-id="ffa7e-119">Power save   standby.</span></span>

</dd> <dt>

<span data-ttu-id="ffa7e-120">4</span><span class="sxs-lookup"><span data-stu-id="ffa7e-120">4</span></span>
</dt> <dd>

<span data-ttu-id="ffa7e-121">Risparmio di energia.</span><span class="sxs-lookup"><span data-stu-id="ffa7e-121">Power save   other.</span></span>

</dd> <dt>

<span data-ttu-id="ffa7e-122">5</span><span class="sxs-lookup"><span data-stu-id="ffa7e-122">5</span></span>
</dt> <dd>

<span data-ttu-id="ffa7e-123">Ciclo di alimentazione.</span><span class="sxs-lookup"><span data-stu-id="ffa7e-123">Power cycle.</span></span>

</dd> <dt>

<span data-ttu-id="ffa7e-124">6</span><span class="sxs-lookup"><span data-stu-id="ffa7e-124">6</span></span>
</dt> <dd>

<span data-ttu-id="ffa7e-125">Spegnimento.</span><span class="sxs-lookup"><span data-stu-id="ffa7e-125">Power off.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="ffa7e-126">*Ora* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="ffa7e-126">*Time* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ffa7e-127">Specifica quando deve essere impostato lo stato di alimentazione, come valore di data e ora normale o come valore di intervallo, in cui l'intervallo inizia quando viene ricevuta la chiamata al metodo.</span><span class="sxs-lookup"><span data-stu-id="ffa7e-127">Specifies when the power state should be set, either as a regular date-time value or as an interval value (where the interval begins when the method invocation is received).</span></span> <span data-ttu-id="ffa7e-128">Quando il parametro *PowerState* è uguale a 5 ("ciclo di alimentazione"), il parametro *Time* indica quando riaccendere il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ffa7e-128">When the *PowerState* parameter is equal to 5 ("Power Cycle"), the *Time* parameter indicates when the device should power on again.</span></span> <span data-ttu-id="ffa7e-129">Lo spegnimento è immediato.</span><span class="sxs-lookup"><span data-stu-id="ffa7e-129">Power-off is immediate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ffa7e-130">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ffa7e-130">Return value</span></span>

<span data-ttu-id="ffa7e-131">Restituisce 0 (zero) se ha esito positivo, 1 (uno) se la richiesta *PowerState* e *Time* specificata non è supportata e un altro valore se si sono verificati altri errori.</span><span class="sxs-lookup"><span data-stu-id="ffa7e-131">Returns 0 (zero) if successful, 1 (one) if the specified *PowerState* and *Time* request is not supported, and another value if any other error occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="ffa7e-132">Commenti</span><span class="sxs-lookup"><span data-stu-id="ffa7e-132">Remarks</span></span>

<span data-ttu-id="ffa7e-133">Questo metodo non è attualmente implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="ffa7e-133">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="ffa7e-134">Per usare questo metodo, è necessario implementarlo nel proprio provider.</span><span class="sxs-lookup"><span data-stu-id="ffa7e-134">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="ffa7e-135">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="ffa7e-135">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="ffa7e-136">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="ffa7e-136">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="ffa7e-137">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ffa7e-137">Requirements</span></span>



| <span data-ttu-id="ffa7e-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="ffa7e-138">Requirement</span></span> | <span data-ttu-id="ffa7e-139">Valore</span><span class="sxs-lookup"><span data-stu-id="ffa7e-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ffa7e-140">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ffa7e-140">Minimum supported client</span></span><br/> | <span data-ttu-id="ffa7e-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ffa7e-141">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ffa7e-142">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ffa7e-142">Minimum supported server</span></span><br/> | <span data-ttu-id="ffa7e-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ffa7e-143">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ffa7e-144">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="ffa7e-144">Namespace</span></span><br/>                | <span data-ttu-id="ffa7e-145">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="ffa7e-145">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="ffa7e-146">MOF</span><span class="sxs-lookup"><span data-stu-id="ffa7e-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ffa7e-147"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ffa7e-147"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="ffa7e-148">DLL</span><span class="sxs-lookup"><span data-stu-id="ffa7e-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ffa7e-149"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ffa7e-149"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ffa7e-150">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ffa7e-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ffa7e-151">\_Piatto CIM</span><span class="sxs-lookup"><span data-stu-id="ffa7e-151">CIM\_FlatPanel</span></span>](setpowerstate-method-in-class-cim-flatpanel.md)
</dt> <dt>

[<span data-ttu-id="ffa7e-152">**\_Piatto CIM**</span><span class="sxs-lookup"><span data-stu-id="ffa7e-152">**CIM\_FlatPanel**</span></span>](cim-flatpanel.md)
</dt> </dl>

 

 




