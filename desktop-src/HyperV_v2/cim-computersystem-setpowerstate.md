---
description: Imposta lo stato di alimentazione del computer. L'uso di questo metodo è stato deprecato. Usare invece il metodo SetPowerState nella classe PowerManagementService associata.
ms.assetid: c2196f35-f687-4d82-a068-f8499f77473a
title: Metodo SetPowerState della classe CIM_ComputerSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ComputerSystem.SetPowerState
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 9c9e264e8ec62c1e49e92226d1abc8ac902c0b2b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050162"
---
# <a name="setpowerstate-method-of-the-cim_computersystem-class"></a><span data-ttu-id="b6e89-105">Metodo SetPowerState della classe CIM \_ ComputerSystem</span><span class="sxs-lookup"><span data-stu-id="b6e89-105">SetPowerState method of the CIM\_ComputerSystem class</span></span>

<span data-ttu-id="b6e89-106">Imposta lo stato di alimentazione del computer.</span><span class="sxs-lookup"><span data-stu-id="b6e89-106">Sets the power state of the computer.</span></span> <span data-ttu-id="b6e89-107">L'uso di questo metodo è stato deprecato.</span><span class="sxs-lookup"><span data-stu-id="b6e89-107">The use of this method has been deprecated.</span></span> <span data-ttu-id="b6e89-108">Usare invece il metodo **SetPowerState** nella classe **PowerManagementService** associata.</span><span class="sxs-lookup"><span data-stu-id="b6e89-108">Instead, use the **SetPowerState** method in the associated **PowerManagementService** class.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6e89-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b6e89-109">Syntax</span></span>


```mof
uint32 SetPowerState(
  [in] uint32   PowerState,
  [in] datetime Time
);
```



## <a name="parameters"></a><span data-ttu-id="b6e89-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="b6e89-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b6e89-111">*PowerState* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b6e89-111">*PowerState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6e89-112">Stato desiderato per il sistema del computer.</span><span class="sxs-lookup"><span data-stu-id="b6e89-112">The desired state for the computer system.</span></span>

<dt>

<span id="Full_Power"></span><span id="full_power"></span><span id="FULL_POWER"></span>

<span data-ttu-id="b6e89-113">**Potenza completa** (1)</span><span class="sxs-lookup"><span data-stu-id="b6e89-113">**Full Power** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="b6e89-114">**Risparmio energia-modalità a basso consumo** (2)</span><span class="sxs-lookup"><span data-stu-id="b6e89-114">**Power Save - Low Power Mode** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="b6e89-115">**Risparmio energia-standby** (3)</span><span class="sxs-lookup"><span data-stu-id="b6e89-115">**Power Save - Standby** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Other"></span><span id="power_save_-_other"></span><span id="POWER_SAVE_-_OTHER"></span>

<span data-ttu-id="b6e89-116">**Risparmio energia-altro** (4)</span><span class="sxs-lookup"><span data-stu-id="b6e89-116">**Power Save - Other** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="b6e89-117">**Ciclo di alimentazione** (5)</span><span class="sxs-lookup"><span data-stu-id="b6e89-117">**Power Cycle** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="b6e89-118">**Spegnimento (6** )</span><span class="sxs-lookup"><span data-stu-id="b6e89-118">**Power Off** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Hibernate"></span><span id="hibernate"></span><span id="HIBERNATE"></span>

<span data-ttu-id="b6e89-119">**Ibernazione** (7)</span><span class="sxs-lookup"><span data-stu-id="b6e89-119">**Hibernate** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Soft_Off"></span><span id="soft_off"></span><span id="SOFT_OFF"></span>

<span data-ttu-id="b6e89-120">**Soft off** (8)</span><span class="sxs-lookup"><span data-stu-id="b6e89-120">**Soft Off** (8)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="b6e89-121">*Ora* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="b6e89-121">*Time* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6e89-122">Time indica quando deve essere impostato lo stato di alimentazione, come valore di data e ora normale o come valore di intervallo, in cui l'intervallo inizia quando viene ricevuta la chiamata al metodo.</span><span class="sxs-lookup"><span data-stu-id="b6e89-122">Time indicates when the power state should be set, either as a regular date-time value or as an interval value (where the interval begins when the method invocation is received).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b6e89-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b6e89-123">Requirements</span></span>



| <span data-ttu-id="b6e89-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="b6e89-124">Requirement</span></span> | <span data-ttu-id="b6e89-125">Valore</span><span class="sxs-lookup"><span data-stu-id="b6e89-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6e89-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b6e89-126">Minimum supported client</span></span><br/> | <span data-ttu-id="b6e89-127">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="b6e89-127">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="b6e89-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b6e89-128">Minimum supported server</span></span><br/> | <span data-ttu-id="b6e89-129">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="b6e89-129">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="b6e89-130">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="b6e89-130">Namespace</span></span><br/>                | <span data-ttu-id="b6e89-131">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="b6e89-131">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="b6e89-132">MOF</span><span class="sxs-lookup"><span data-stu-id="b6e89-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b6e89-133"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b6e89-133"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b6e89-134">DLL</span><span class="sxs-lookup"><span data-stu-id="b6e89-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b6e89-135"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b6e89-135"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="b6e89-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b6e89-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6e89-137">**\_ComputerSystem CIM**</span><span class="sxs-lookup"><span data-stu-id="b6e89-137">**CIM\_ComputerSystem**</span></span>](cim-computersystem.md)
</dt> </dl>

 

 




