---
description: "SystemConfig_V0_Power classe: questa classe è la classe del tipo di evento per gli eventi di configurazione dell'alimentazione. La sintassi seguente è semplificata dal codice MOF."
ms.assetid: b3391435-dac0-4c48-b788-eb4d4a7aa635
title: SystemConfig_V0_Power classe
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
ms.openlocfilehash: ab268e719374906e149dc9c1b733487f986e8308
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105939"
---
# <a name="systemconfig_v0_power-class"></a><span data-ttu-id="26b0f-104">Classe SystemConfig \_ V0 \_ Power</span><span class="sxs-lookup"><span data-stu-id="26b0f-104">SystemConfig\_V0\_Power class</span></span>

<span data-ttu-id="26b0f-105">Questa classe è la classe del tipo di evento per gli eventi di configurazione dell'alimentazione.</span><span class="sxs-lookup"><span data-stu-id="26b0f-105">This class is the event type class for power configuration events.</span></span>

<span data-ttu-id="26b0f-106">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="26b0f-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="26b0f-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="26b0f-107">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="26b0f-108">Members</span><span class="sxs-lookup"><span data-stu-id="26b0f-108">Members</span></span>

<span data-ttu-id="26b0f-109">La **classe SystemConfig \_ V0 \_ Power** ha questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="26b0f-109">The **SystemConfig\_V0\_Power** class has these types of members:</span></span>

-   [<span data-ttu-id="26b0f-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="26b0f-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="26b0f-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="26b0f-111">Properties</span></span>

<span data-ttu-id="26b0f-112">La **classe SystemConfig \_ V0 \_ Power** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="26b0f-112">The **SystemConfig\_V0\_Power** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="26b0f-113">Pad1</span><span class="sxs-lookup"><span data-stu-id="26b0f-113">Pad1</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26b0f-114">Tipo di dati: **uint8**</span><span class="sxs-lookup"><span data-stu-id="26b0f-114">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="26b0f-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="26b0f-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26b0f-116">Qualificatori: WmiDataId(6)</span><span class="sxs-lookup"><span data-stu-id="26b0f-116">Qualifiers: WmiDataId(6)</span></span>
</dt> </dl>

<span data-ttu-id="26b0f-117">Riservato.</span><span class="sxs-lookup"><span data-stu-id="26b0f-117">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="26b0f-118">Pad2</span><span class="sxs-lookup"><span data-stu-id="26b0f-118">Pad2</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26b0f-119">Tipo di dati: **uint8**</span><span class="sxs-lookup"><span data-stu-id="26b0f-119">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="26b0f-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="26b0f-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26b0f-121">Qualificatori: WmiDataId(7)</span><span class="sxs-lookup"><span data-stu-id="26b0f-121">Qualifiers: WmiDataId(7)</span></span>
</dt> </dl>

<span data-ttu-id="26b0f-122">Riservato.</span><span class="sxs-lookup"><span data-stu-id="26b0f-122">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="26b0f-123">Pad3</span><span class="sxs-lookup"><span data-stu-id="26b0f-123">Pad3</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26b0f-124">Tipo di dati: **uint8**</span><span class="sxs-lookup"><span data-stu-id="26b0f-124">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="26b0f-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="26b0f-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26b0f-126">Qualificatori: WmiDataId(8)</span><span class="sxs-lookup"><span data-stu-id="26b0f-126">Qualifiers: WmiDataId(8)</span></span>
</dt> </dl>

<span data-ttu-id="26b0f-127">Riservato.</span><span class="sxs-lookup"><span data-stu-id="26b0f-127">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="26b0f-128">s1</span><span class="sxs-lookup"><span data-stu-id="26b0f-128">s1</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26b0f-129">Tipo di dati: **booleano**</span><span class="sxs-lookup"><span data-stu-id="26b0f-129">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="26b0f-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="26b0f-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26b0f-131">Qualificatori: WmiDataId(1)</span><span class="sxs-lookup"><span data-stu-id="26b0f-131">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="26b0f-132">True indica che il sistema supporta lo stato di sospensione S1.</span><span class="sxs-lookup"><span data-stu-id="26b0f-132">True indicates the system supports sleep state S1.</span></span>

</dd> <dt>

<span data-ttu-id="26b0f-133">s2</span><span class="sxs-lookup"><span data-stu-id="26b0f-133">s2</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26b0f-134">Tipo di dati: **booleano**</span><span class="sxs-lookup"><span data-stu-id="26b0f-134">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="26b0f-135">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="26b0f-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26b0f-136">Qualificatori: WmiDataId(2)</span><span class="sxs-lookup"><span data-stu-id="26b0f-136">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="26b0f-137">True indica che il sistema supporta lo stato di sospensione S2.</span><span class="sxs-lookup"><span data-stu-id="26b0f-137">True indicates the system supports sleep state S2.</span></span>

</dd> <dt>

<span data-ttu-id="26b0f-138">s3</span><span class="sxs-lookup"><span data-stu-id="26b0f-138">s3</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26b0f-139">Tipo di dati: **booleano**</span><span class="sxs-lookup"><span data-stu-id="26b0f-139">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="26b0f-140">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="26b0f-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26b0f-141">Qualificatori: WmiDataId(3)</span><span class="sxs-lookup"><span data-stu-id="26b0f-141">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="26b0f-142">True indica che il sistema supporta lo stato di sospensione S3.</span><span class="sxs-lookup"><span data-stu-id="26b0f-142">True indicates the system supports sleep state S3.</span></span>

</dd> <dt>

<span data-ttu-id="26b0f-143">s4</span><span class="sxs-lookup"><span data-stu-id="26b0f-143">s4</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26b0f-144">Tipo di dati: **booleano**</span><span class="sxs-lookup"><span data-stu-id="26b0f-144">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="26b0f-145">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="26b0f-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26b0f-146">Qualificatori: WmiDataId(4)</span><span class="sxs-lookup"><span data-stu-id="26b0f-146">Qualifiers: WmiDataId(4)</span></span>
</dt> </dl>

<span data-ttu-id="26b0f-147">True indica che il sistema supporta lo stato di sospensione S4.</span><span class="sxs-lookup"><span data-stu-id="26b0f-147">True indicates the system supports sleep state S4.</span></span>

</dd> <dt>

<span data-ttu-id="26b0f-148">s5</span><span class="sxs-lookup"><span data-stu-id="26b0f-148">s5</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26b0f-149">Tipo di dati: **booleano**</span><span class="sxs-lookup"><span data-stu-id="26b0f-149">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="26b0f-150">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="26b0f-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26b0f-151">Qualificatori: WmiDataId(5)</span><span class="sxs-lookup"><span data-stu-id="26b0f-151">Qualifiers: WmiDataId(5)</span></span>
</dt> </dl>

<span data-ttu-id="26b0f-152">True indica che il sistema supporta lo stato di sospensione S5.</span><span class="sxs-lookup"><span data-stu-id="26b0f-152">True indicates the system supports sleep state S5.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="26b0f-153">Requisiti</span><span class="sxs-lookup"><span data-stu-id="26b0f-153">Requirements</span></span>



| <span data-ttu-id="26b0f-154">Requisito</span><span class="sxs-lookup"><span data-stu-id="26b0f-154">Requirement</span></span> | <span data-ttu-id="26b0f-155">Valore</span><span class="sxs-lookup"><span data-stu-id="26b0f-155">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="26b0f-156">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="26b0f-156">Minimum supported client</span></span><br/> | <span data-ttu-id="26b0f-157">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="26b0f-157">None supported</span></span><br/>                            |
| <span data-ttu-id="26b0f-158">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="26b0f-158">Minimum supported server</span></span><br/> | <span data-ttu-id="26b0f-159">Solo app desktop di Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="26b0f-159">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="26b0f-160">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="26b0f-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26b0f-161">**SystemConfig \_ V0**</span><span class="sxs-lookup"><span data-stu-id="26b0f-161">**SystemConfig\_V0**</span></span>](systemconfig-v0.md)
</dt> </dl>

 

 




