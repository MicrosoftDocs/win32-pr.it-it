---
description: Imposta lo stato di alimentazione del dispositivo. L'uso di questo metodo è stato deprecato. Usare invece il metodo SetPowerState nella classe PowerManagementService associata.
ms.assetid: 2f53a8bd-18a8-45aa-92ad-68a33b6a42ab
title: Metodo SetPowerState della classe CIM_LogicalDevice (gestione di Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalDevice.SetPowerState
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: a29f71806747e6d63f53618acd09d472ac8bdea5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968027"
---
# <a name="setpowerstate-method-of-the-cim_logicaldevice-class-hyper-v-management"></a><span data-ttu-id="ef04b-105">Metodo SetPowerState della classe CIM_LogicalDevice (gestione di Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="ef04b-105">SetPowerState method of the CIM_LogicalDevice class (Hyper-V management)</span></span>

<span data-ttu-id="ef04b-106">Imposta lo stato di alimentazione del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ef04b-106">Sets the power state of the Device.</span></span> <span data-ttu-id="ef04b-107">L'uso di questo metodo è stato deprecato.</span><span class="sxs-lookup"><span data-stu-id="ef04b-107">The use of this method has been deprecated.</span></span> <span data-ttu-id="ef04b-108">Usare invece il metodo **SetPowerState** nella classe **PowerManagementService** associata.</span><span class="sxs-lookup"><span data-stu-id="ef04b-108">Instead, use the **SetPowerState** method in the associated **PowerManagementService** class.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef04b-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ef04b-109">Syntax</span></span>


```mof
uint32 SetPowerState(
  [in] uint16   PowerState,
  [in] datetime Time
);
```



## <a name="parameters"></a><span data-ttu-id="ef04b-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="ef04b-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ef04b-111">*PowerState* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ef04b-111">*PowerState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef04b-112">Stato di alimentazione da impostare.</span><span class="sxs-lookup"><span data-stu-id="ef04b-112">The power state to set.</span></span>

<dt>

<span id="Full_Power"></span><span id="full_power"></span><span id="FULL_POWER"></span>

<span data-ttu-id="ef04b-113">**Potenza completa** (1)</span><span class="sxs-lookup"><span data-stu-id="ef04b-113">**Full Power** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="ef04b-114">**Risparmio energia-modalità a basso consumo** (2)</span><span class="sxs-lookup"><span data-stu-id="ef04b-114">**Power Save - Low Power Mode** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="ef04b-115">**Risparmio energia-standby** (3)</span><span class="sxs-lookup"><span data-stu-id="ef04b-115">**Power Save - Standby** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Other"></span><span id="power_save_-_other"></span><span id="POWER_SAVE_-_OTHER"></span>

<span data-ttu-id="ef04b-116">**Risparmio energia-altro** (4)</span><span class="sxs-lookup"><span data-stu-id="ef04b-116">**Power Save - Other** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="ef04b-117">**Ciclo di alimentazione** (5)</span><span class="sxs-lookup"><span data-stu-id="ef04b-117">**Power Cycle** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="ef04b-118">**Spegnimento (6** )</span><span class="sxs-lookup"><span data-stu-id="ef04b-118">**Power Off** (6)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="ef04b-119">*Ora* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="ef04b-119">*Time* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef04b-120">Time indica quando deve essere impostato lo stato di alimentazione, come valore di data e ora normale o come valore di intervallo, in cui l'intervallo inizia quando viene ricevuta la chiamata al metodo.</span><span class="sxs-lookup"><span data-stu-id="ef04b-120">Time indicates when the power state should be set, either as a regular date-time value or as an interval value (where the interval begins when the method invocation is received).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ef04b-121">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ef04b-121">Return value</span></span>

<span data-ttu-id="ef04b-122">Restituisce 0 in caso di esito positivo; in caso contrario, restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="ef04b-122">Returns a 0 on success; otherwise, returns an error.</span></span>

## <a name="requirements"></a><span data-ttu-id="ef04b-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ef04b-123">Requirements</span></span>



| <span data-ttu-id="ef04b-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="ef04b-124">Requirement</span></span> | <span data-ttu-id="ef04b-125">Valore</span><span class="sxs-lookup"><span data-stu-id="ef04b-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ef04b-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ef04b-126">Minimum supported client</span></span><br/> | <span data-ttu-id="ef04b-127">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="ef04b-127">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="ef04b-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ef04b-128">Minimum supported server</span></span><br/> | <span data-ttu-id="ef04b-129">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="ef04b-129">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="ef04b-130">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="ef04b-130">Namespace</span></span><br/>                | <span data-ttu-id="ef04b-131">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="ef04b-131">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="ef04b-132">MOF</span><span class="sxs-lookup"><span data-stu-id="ef04b-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ef04b-133"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ef04b-133"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ef04b-134">DLL</span><span class="sxs-lookup"><span data-stu-id="ef04b-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ef04b-135"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ef04b-135"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="ef04b-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ef04b-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef04b-137">**\_LOGICALDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="ef04b-137">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

 




