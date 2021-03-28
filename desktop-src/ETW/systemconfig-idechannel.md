---
description: Questa classe è la classe del tipo di evento per gli eventi del canale IDE. La sintassi seguente è semplificata dal codice MOF.
ms.assetid: 2265a4a6-4377-4aa9-926a-def6e8eda998
title: Classe SystemConfig_IDEChannel
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_IDEChannel
- SystemConfig_IDEChannel.TargetId
- SystemConfig_IDEChannel.DeviceType
- SystemConfig_IDEChannel.DeviceTimingMode
- SystemConfig_IDEChannel.LocationInformationLen
- SystemConfig_IDEChannel.LocationInformation
api_type:
- NA
api_location: ''
ms.openlocfilehash: 60cdfcec8f62e6fb96dcedc895d874f01a209430
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526382"
---
# <a name="systemconfig_idechannel-class"></a><span data-ttu-id="80bc9-104">\_Classe SystemConfig IDEChannel</span><span class="sxs-lookup"><span data-stu-id="80bc9-104">SystemConfig\_IDEChannel class</span></span>

<span data-ttu-id="80bc9-105">Questa classe è la classe del tipo di evento per gli eventi del canale IDE.</span><span class="sxs-lookup"><span data-stu-id="80bc9-105">This class is the event type class for IDE channel events.</span></span>

<span data-ttu-id="80bc9-106">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="80bc9-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="80bc9-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="80bc9-107">Syntax</span></span>

``` syntax
[EventType(23), EventTypeName("IDEChannel")]
class SystemConfig_IDEChannel : SystemConfig
{
  uint32 TargetId;
  uint32 DeviceType;
  uint32 DeviceTimingMode;
  uint32 LocationInformationLen;
  string LocationInformation;
};
```

## <a name="members"></a><span data-ttu-id="80bc9-108">Members</span><span class="sxs-lookup"><span data-stu-id="80bc9-108">Members</span></span>

<span data-ttu-id="80bc9-109">La **classe \_ IDEChannel di SystemConfig** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="80bc9-109">The **SystemConfig\_IDEChannel** class has these types of members:</span></span>

-   [<span data-ttu-id="80bc9-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="80bc9-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="80bc9-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="80bc9-111">Properties</span></span>

<span data-ttu-id="80bc9-112">La **classe \_ IDEChannel di SystemConfig** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="80bc9-112">The **SystemConfig\_IDEChannel** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="80bc9-113">**DeviceTimingMode**</span><span class="sxs-lookup"><span data-stu-id="80bc9-113">**DeviceTimingMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80bc9-114">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="80bc9-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="80bc9-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="80bc9-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="80bc9-116">Qualificatori: WmiDataId (3), Format ("x")</span><span class="sxs-lookup"><span data-stu-id="80bc9-116">Qualifiers: WmiDataId(3), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="80bc9-117">Modalità di funzionamento dell'IDE.</span><span class="sxs-lookup"><span data-stu-id="80bc9-117">The mode in which the IDE could function.</span></span> <span data-ttu-id="80bc9-118">Di seguito sono indicati i valori possibili:</span><span class="sxs-lookup"><span data-stu-id="80bc9-118">The following are the possible values:</span></span>

-   <span data-ttu-id="80bc9-119">PIO \_ MODE0 (0x1)</span><span class="sxs-lookup"><span data-stu-id="80bc9-119">PIO\_MODE0 (0x1)</span></span>
-   <span data-ttu-id="80bc9-120">PIO \_ Mode1 (0x2)</span><span class="sxs-lookup"><span data-stu-id="80bc9-120">PIO\_MODE1 (0x2)</span></span>
-   <span data-ttu-id="80bc9-121">PIO \_ Mode2 (0x4)</span><span class="sxs-lookup"><span data-stu-id="80bc9-121">PIO\_MODE2 (0x4)</span></span>
-   <span data-ttu-id="80bc9-122">PIO \_ Mode3 (0x8)</span><span class="sxs-lookup"><span data-stu-id="80bc9-122">PIO\_MODE3 (0x8)</span></span>
-   <span data-ttu-id="80bc9-123">PIO \_ MODE4 (0x10)</span><span class="sxs-lookup"><span data-stu-id="80bc9-123">PIO\_MODE4 (0x10)</span></span>
-   <span data-ttu-id="80bc9-124">SWDMA \_ MODE0 (0x20)</span><span class="sxs-lookup"><span data-stu-id="80bc9-124">SWDMA\_MODE0 (0x20)</span></span>
-   <span data-ttu-id="80bc9-125">SWDMA \_ Mode1 (0x40)</span><span class="sxs-lookup"><span data-stu-id="80bc9-125">SWDMA\_MODE1 (0x40)</span></span>
-   <span data-ttu-id="80bc9-126">SWDMA \_ Mode2 (0x80)</span><span class="sxs-lookup"><span data-stu-id="80bc9-126">SWDMA\_MODE2 (0x80)</span></span>
-   <span data-ttu-id="80bc9-127">MWDMA \_ MODE0 (0x100)</span><span class="sxs-lookup"><span data-stu-id="80bc9-127">MWDMA\_MODE0 (0x100)</span></span>
-   <span data-ttu-id="80bc9-128">MWDMA \_ Mode2 (0x200)</span><span class="sxs-lookup"><span data-stu-id="80bc9-128">MWDMA\_MODE2 (0x200)</span></span>
-   <span data-ttu-id="80bc9-129">MWDMA \_ Mode3 (0x400)</span><span class="sxs-lookup"><span data-stu-id="80bc9-129">MWDMA\_MODE3 (0x400)</span></span>
-   <span data-ttu-id="80bc9-130">\_MODE0 UDMA (0x800)</span><span class="sxs-lookup"><span data-stu-id="80bc9-130">UDMA\_MODE0 (0x800)</span></span>
-   <span data-ttu-id="80bc9-131">\_Mode1 UDMA (0x1000)</span><span class="sxs-lookup"><span data-stu-id="80bc9-131">UDMA\_MODE1 (0x1000)</span></span>
-   <span data-ttu-id="80bc9-132">\_Mode2 UDMA (0x2000)</span><span class="sxs-lookup"><span data-stu-id="80bc9-132">UDMA\_MODE2 (0x2000)</span></span>
-   <span data-ttu-id="80bc9-133">\_Mode3 UDMA (0x4000)</span><span class="sxs-lookup"><span data-stu-id="80bc9-133">UDMA\_MODE3 (0x4000)</span></span>
-   <span data-ttu-id="80bc9-134">\_MODE4 UDMA (0x8000)</span><span class="sxs-lookup"><span data-stu-id="80bc9-134">UDMA\_MODE4 (0x8000)</span></span>
-   <span data-ttu-id="80bc9-135">\_Mode5 UDMA (0x10000)</span><span class="sxs-lookup"><span data-stu-id="80bc9-135">UDMA\_MODE5 (0x10000)</span></span>

</dd> <dt>

<span data-ttu-id="80bc9-136">**DeviceType**</span><span class="sxs-lookup"><span data-stu-id="80bc9-136">**DeviceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80bc9-137">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="80bc9-137">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="80bc9-138">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="80bc9-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="80bc9-139">Qualificatori: WmiDataId (2), Format ("x")</span><span class="sxs-lookup"><span data-stu-id="80bc9-139">Qualifiers: WmiDataId(2), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="80bc9-140">Tipo di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="80bc9-140">The device type.</span></span> <span data-ttu-id="80bc9-141">Di seguito sono indicati i valori possibili:</span><span class="sxs-lookup"><span data-stu-id="80bc9-141">The following are the possible values:</span></span>

-   <span data-ttu-id="80bc9-142">ATA (1)</span><span class="sxs-lookup"><span data-stu-id="80bc9-142">ATA (1)</span></span>
-   <span data-ttu-id="80bc9-143">ATAPI (2)</span><span class="sxs-lookup"><span data-stu-id="80bc9-143">ATAPI (2)</span></span>

</dd> <dt>

<span data-ttu-id="80bc9-144">**LocationInformation**</span><span class="sxs-lookup"><span data-stu-id="80bc9-144">**LocationInformation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80bc9-145">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="80bc9-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="80bc9-146">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="80bc9-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="80bc9-147">Qualificatori: WmiDataId (5), StringTermination ("NullTerminated"), Format ("w")</span><span class="sxs-lookup"><span data-stu-id="80bc9-147">Qualifiers: WmiDataId(5), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="80bc9-148">Il canale IDE, ad esempio canale primario, canale secondario e così via.</span><span class="sxs-lookup"><span data-stu-id="80bc9-148">The IDE channel (for example, Primary Channel, Secondary Channel, and so on).</span></span>

</dd> <dt>

<span data-ttu-id="80bc9-149">**LocationInformationLen**</span><span class="sxs-lookup"><span data-stu-id="80bc9-149">**LocationInformationLen**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80bc9-150">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="80bc9-150">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="80bc9-151">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="80bc9-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="80bc9-152">Qualificatori: WmiDataId (4)</span><span class="sxs-lookup"><span data-stu-id="80bc9-152">Qualifiers: WmiDataId(4)</span></span>
</dt> </dl>

<span data-ttu-id="80bc9-153">Lunghezza della stringa **LocationInformation** .</span><span class="sxs-lookup"><span data-stu-id="80bc9-153">Length of the **LocationInformation** string.</span></span>

</dd> <dt>

<span data-ttu-id="80bc9-154">**TargetId**</span><span class="sxs-lookup"><span data-stu-id="80bc9-154">**TargetId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80bc9-155">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="80bc9-155">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="80bc9-156">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="80bc9-156">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="80bc9-157">Qualificatori: WmiDataId (1)</span><span class="sxs-lookup"><span data-stu-id="80bc9-157">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="80bc9-158">Identificatore del disco.</span><span class="sxs-lookup"><span data-stu-id="80bc9-158">The identifier of the disk.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="80bc9-159">Requisiti</span><span class="sxs-lookup"><span data-stu-id="80bc9-159">Requirements</span></span>



| <span data-ttu-id="80bc9-160">Requisito</span><span class="sxs-lookup"><span data-stu-id="80bc9-160">Requirement</span></span> | <span data-ttu-id="80bc9-161">Valore</span><span class="sxs-lookup"><span data-stu-id="80bc9-161">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="80bc9-162">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="80bc9-162">Minimum supported client</span></span><br/> | <span data-ttu-id="80bc9-163">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="80bc9-163">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="80bc9-164">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="80bc9-164">Minimum supported server</span></span><br/> | <span data-ttu-id="80bc9-165">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="80bc9-165">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="80bc9-166">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="80bc9-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80bc9-167">**SystemConfig**</span><span class="sxs-lookup"><span data-stu-id="80bc9-167">**SystemConfig**</span></span>](systemconfig.md)
</dt> </dl>

 

 




