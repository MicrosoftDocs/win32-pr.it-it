---
description: Rappresenta le funzionalità e la gestione di un'unità nastro.
ms.assetid: 8140fd9a-8a12-43b4-bc61-ec143e5d754c
title: Classe CIM_TapeDrive (gestione Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_TapeDrive
- CIM_TapeDrive.EOTWarningZoneSize
- CIM_TapeDrive.MaxPartitionCount
- CIM_TapeDrive.Padding
- CIM_TapeDrive.MaxRewindTime
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: b92360388b71abcb0b67d30fddea9b4f5ed7920f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310572"
---
# <a name="cim_tapedrive-class-hyper-v-management"></a><span data-ttu-id="72946-103">Classe CIM_TapeDrive (gestione Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="72946-103">CIM_TapeDrive class (Hyper-V management)</span></span>

<span data-ttu-id="72946-104">Rappresenta le funzionalità e la gestione di un'unità nastro.</span><span class="sxs-lookup"><span data-stu-id="72946-104">Represents the capabilities and management of a tape drive.</span></span>

## <a name="syntax"></a><span data-ttu-id="72946-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="72946-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.6.0"), UMLPackagePath("CIM::Device::StorageDevices")]
class CIM_TapeDrive : CIM_MediaAccessDevice
{
  uint32 EOTWarningZoneSize;
  uint32 MaxPartitionCount;
  uint32 Padding;
  uint64 MaxRewindTime;
};
```

## <a name="members"></a><span data-ttu-id="72946-106">Members</span><span class="sxs-lookup"><span data-stu-id="72946-106">Members</span></span>

<span data-ttu-id="72946-107">La classe **CIM \_ TapeDrive** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="72946-107">The **CIM\_TapeDrive** class has these types of members:</span></span>

-   [<span data-ttu-id="72946-108">Proprietà</span><span class="sxs-lookup"><span data-stu-id="72946-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="72946-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="72946-109">Properties</span></span>

<span data-ttu-id="72946-110">La classe **CIM \_ TapeDrive** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="72946-110">The **CIM\_TapeDrive** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="72946-111">**EOTWarningZoneSize**</span><span class="sxs-lookup"><span data-stu-id="72946-111">**EOTWarningZoneSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72946-112">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="72946-112">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="72946-113">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="72946-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="72946-114">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("byte"), **punito** ("byte")</span><span class="sxs-lookup"><span data-stu-id="72946-114">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bytes"), **PUnit** ("byte")</span></span>
</dt> </dl>

<span data-ttu-id="72946-115">Dimensione, in byte, dell'area designata come "fine del nastro".</span><span class="sxs-lookup"><span data-stu-id="72946-115">The size, in bytes, of the area designated as "end of tape".</span></span> <span data-ttu-id="72946-116">L'accesso in quest'area genera un avviso "fine nastro".</span><span class="sxs-lookup"><span data-stu-id="72946-116">Access in this area generates an "end of tape" warning.</span></span>

</dd> <dt>

<span data-ttu-id="72946-117">**MaxPartitionCount**</span><span class="sxs-lookup"><span data-stu-id="72946-117">**MaxPartitionCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72946-118">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="72946-118">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="72946-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="72946-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="72946-120">Numero massimo di partizioni per l'unità nastro.</span><span class="sxs-lookup"><span data-stu-id="72946-120">The maximum partition count for the tape drive.</span></span>

</dd> <dt>

<span data-ttu-id="72946-121">**MaxRewindTime**</span><span class="sxs-lookup"><span data-stu-id="72946-121">**MaxRewindTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72946-122">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="72946-122">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="72946-123">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="72946-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="72946-124">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("millisecondi"), **punito** ("secondo \* 10 ^-3")</span><span class="sxs-lookup"><span data-stu-id="72946-124">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("MilliSeconds"), **PUnit** ("second \* 10^-3")</span></span>
</dt> </dl>

<span data-ttu-id="72946-125">Tempo, in millisecondi, per lo spostamento dal punto più distante fisicamente sul nastro all'inizio.</span><span class="sxs-lookup"><span data-stu-id="72946-125">The time, in milliseconds, to move from the most physically distant point on the tape to the beginning.</span></span>

</dd> <dt>

<span data-ttu-id="72946-126">**Riempimento**</span><span class="sxs-lookup"><span data-stu-id="72946-126">**Padding**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72946-127">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="72946-127">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="72946-128">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="72946-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="72946-129">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("byte"), **punito** ("byte")</span><span class="sxs-lookup"><span data-stu-id="72946-129">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bytes"), **PUnit** ("byte")</span></span>
</dt> </dl>

<span data-ttu-id="72946-130">Numero di byte inseriti tra i blocchi sui supporti su nastro.</span><span class="sxs-lookup"><span data-stu-id="72946-130">The number of bytes inserted between blocks on tape media.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="72946-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="72946-131">Requirements</span></span>



| <span data-ttu-id="72946-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="72946-132">Requirement</span></span> | <span data-ttu-id="72946-133">Valore</span><span class="sxs-lookup"><span data-stu-id="72946-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="72946-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="72946-134">Minimum supported client</span></span><br/> | <span data-ttu-id="72946-135">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="72946-135">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="72946-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="72946-136">Minimum supported server</span></span><br/> | <span data-ttu-id="72946-137">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="72946-137">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="72946-138">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="72946-138">Namespace</span></span><br/>                | <span data-ttu-id="72946-139">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="72946-139">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="72946-140">MOF</span><span class="sxs-lookup"><span data-stu-id="72946-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="72946-141"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="72946-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="72946-142">DLL</span><span class="sxs-lookup"><span data-stu-id="72946-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="72946-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="72946-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="72946-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="72946-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72946-145">**\_MEDIAACCESSDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="72946-145">**CIM\_MediaAccessDevice**</span></span>](cim-mediaaccessdevice.md)
</dt> </dl>

 

