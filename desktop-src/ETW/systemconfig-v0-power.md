---
description: Questa classe è la classe del tipo di evento per gli eventi di configurazione dell'alimentazione. La sintassi seguente è semplificata dal codice MOF.
ms.assetid: b3391435-dac0-4c48-b788-eb4d4a7aa635
title: Classe SystemConfig_V0_Power
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_V0_Power
- SystemConfig_V0_Power.s1
- SystemConfig_V0_Power.s2
- SystemConfig_V0_Power.s3
- SystemConfig_V0_Power.s4
- SystemConfig_V0_Power.s5
- SystemConfig_V0_Power.Pad1
- SystemConfig_V0_Power.Pad2
- SystemConfig_V0_Power.Pad3
api_type:
- NA
api_location: ''
ms.openlocfilehash: 2e42af68ad12857d65d776b7a73794d2d13b2b48
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977466"
---
# <a name="systemconfig_v0_power-class"></a><span data-ttu-id="9f49a-104">\_Classe di \_ alimentazione SystemConfig V0</span><span class="sxs-lookup"><span data-stu-id="9f49a-104">SystemConfig\_V0\_Power class</span></span>

<span data-ttu-id="9f49a-105">Questa classe è la classe del tipo di evento per gli eventi di configurazione dell'alimentazione.</span><span class="sxs-lookup"><span data-stu-id="9f49a-105">This class is the event type class for power configuration events.</span></span>

<span data-ttu-id="9f49a-106">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="9f49a-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f49a-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9f49a-107">Syntax</span></span>

``` syntax
[EventType(16), EventTypeName("Power")]
class SystemConfig_V0_Power : SystemConfig_V0
{
  boolean s1;
  boolean s2;
  boolean s3;
  boolean s4;
  boolean s5;
  uint8   Pad1;
  uint8   Pad2;
  uint8   Pad3;
};
```

## <a name="members"></a><span data-ttu-id="9f49a-108">Members</span><span class="sxs-lookup"><span data-stu-id="9f49a-108">Members</span></span>

<span data-ttu-id="9f49a-109">La classe di **\_ \_ alimentazione SystemConfig V0** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="9f49a-109">The **SystemConfig\_V0\_Power** class has these types of members:</span></span>

-   [<span data-ttu-id="9f49a-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="9f49a-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9f49a-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="9f49a-111">Properties</span></span>

<span data-ttu-id="9f49a-112">La **classe \_ \_ Power V0 SystemConfig** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="9f49a-112">The **SystemConfig\_V0\_Power** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9f49a-113">Pad1</span><span class="sxs-lookup"><span data-stu-id="9f49a-113">Pad1</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f49a-114">Tipo di dati: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="9f49a-114">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="9f49a-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9f49a-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9f49a-116">Qualificatori: WmiDataId (6)</span><span class="sxs-lookup"><span data-stu-id="9f49a-116">Qualifiers: WmiDataId(6)</span></span>
</dt> </dl>

<span data-ttu-id="9f49a-117">Riservato.</span><span class="sxs-lookup"><span data-stu-id="9f49a-117">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="9f49a-118">Pad2</span><span class="sxs-lookup"><span data-stu-id="9f49a-118">Pad2</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f49a-119">Tipo di dati: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="9f49a-119">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="9f49a-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9f49a-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9f49a-121">Qualificatori: WmiDataId (7)</span><span class="sxs-lookup"><span data-stu-id="9f49a-121">Qualifiers: WmiDataId(7)</span></span>
</dt> </dl>

<span data-ttu-id="9f49a-122">Riservato.</span><span class="sxs-lookup"><span data-stu-id="9f49a-122">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="9f49a-123">Pad3</span><span class="sxs-lookup"><span data-stu-id="9f49a-123">Pad3</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f49a-124">Tipo di dati: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="9f49a-124">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="9f49a-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9f49a-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9f49a-126">Qualificatori: WmiDataId (8)</span><span class="sxs-lookup"><span data-stu-id="9f49a-126">Qualifiers: WmiDataId(8)</span></span>
</dt> </dl>

<span data-ttu-id="9f49a-127">Riservato.</span><span class="sxs-lookup"><span data-stu-id="9f49a-127">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="9f49a-128">s1</span><span class="sxs-lookup"><span data-stu-id="9f49a-128">s1</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f49a-129">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="9f49a-129">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9f49a-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9f49a-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9f49a-131">Qualificatori: WmiDataId (1)</span><span class="sxs-lookup"><span data-stu-id="9f49a-131">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="9f49a-132">True indica che il sistema supporta lo stato di sospensione S1.</span><span class="sxs-lookup"><span data-stu-id="9f49a-132">True indicates the system supports sleep state S1.</span></span>

</dd> <dt>

<span data-ttu-id="9f49a-133">s2</span><span class="sxs-lookup"><span data-stu-id="9f49a-133">s2</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f49a-134">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="9f49a-134">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9f49a-135">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9f49a-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9f49a-136">Qualificatori: WmiDataId (2)</span><span class="sxs-lookup"><span data-stu-id="9f49a-136">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="9f49a-137">True indica che il sistema supporta lo stato di sospensione S2.</span><span class="sxs-lookup"><span data-stu-id="9f49a-137">True indicates the system supports sleep state S2.</span></span>

</dd> <dt>

<span data-ttu-id="9f49a-138">s3</span><span class="sxs-lookup"><span data-stu-id="9f49a-138">s3</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f49a-139">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="9f49a-139">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9f49a-140">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9f49a-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9f49a-141">Qualificatori: WmiDataId (3)</span><span class="sxs-lookup"><span data-stu-id="9f49a-141">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="9f49a-142">True indica che il sistema supporta lo stato di sospensione S3.</span><span class="sxs-lookup"><span data-stu-id="9f49a-142">True indicates the system supports sleep state S3.</span></span>

</dd> <dt>

<span data-ttu-id="9f49a-143">S4</span><span class="sxs-lookup"><span data-stu-id="9f49a-143">s4</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f49a-144">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="9f49a-144">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9f49a-145">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9f49a-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9f49a-146">Qualificatori: WmiDataId (4)</span><span class="sxs-lookup"><span data-stu-id="9f49a-146">Qualifiers: WmiDataId(4)</span></span>
</dt> </dl>

<span data-ttu-id="9f49a-147">True indica che il sistema supporta lo stato di sospensione S4.</span><span class="sxs-lookup"><span data-stu-id="9f49a-147">True indicates the system supports sleep state S4.</span></span>

</dd> <dt>

<span data-ttu-id="9f49a-148">S5</span><span class="sxs-lookup"><span data-stu-id="9f49a-148">s5</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f49a-149">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="9f49a-149">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9f49a-150">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9f49a-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9f49a-151">Qualificatori: WmiDataId (5)</span><span class="sxs-lookup"><span data-stu-id="9f49a-151">Qualifiers: WmiDataId(5)</span></span>
</dt> </dl>

<span data-ttu-id="9f49a-152">True indica che il sistema supporta lo stato di sospensione S5.</span><span class="sxs-lookup"><span data-stu-id="9f49a-152">True indicates the system supports sleep state S5.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9f49a-153">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9f49a-153">Requirements</span></span>



| <span data-ttu-id="9f49a-154">Requisito</span><span class="sxs-lookup"><span data-stu-id="9f49a-154">Requirement</span></span> | <span data-ttu-id="9f49a-155">Valore</span><span class="sxs-lookup"><span data-stu-id="9f49a-155">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="9f49a-156">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9f49a-156">Minimum supported client</span></span><br/> | <span data-ttu-id="9f49a-157">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="9f49a-157">None supported</span></span><br/>                            |
| <span data-ttu-id="9f49a-158">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9f49a-158">Minimum supported server</span></span><br/> | <span data-ttu-id="9f49a-159">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="9f49a-159">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9f49a-160">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9f49a-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f49a-161">**SystemConfig \_ V0**</span><span class="sxs-lookup"><span data-stu-id="9f49a-161">**SystemConfig\_V0**</span></span>](systemconfig-v0.md)
</dt> </dl>

 

 




