---
description: Questa classe è la classe del tipo di evento per gli eventi di configurazione dell'alimentazione. La sintassi seguente è semplificata dal codice MOF.
ms.assetid: 7065b0b0-9a1d-4fce-a494-5762d5efb239
title: Classe SystemConfig_Power
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_Power
- SystemConfig_Power.s1
- SystemConfig_Power.s2
- SystemConfig_Power.s3
- SystemConfig_Power.s4
- SystemConfig_Power.s5
- SystemConfig_Power.Pad1
- SystemConfig_Power.Pad2
- SystemConfig_Power.Pad3
api_type:
- NA
api_location: ''
ms.openlocfilehash: d27586451f944ac9c94e9ec2d204035c21f37679
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977474"
---
# <a name="systemconfig_power-class"></a><span data-ttu-id="39dbf-104">\_Classe Power SystemConfig</span><span class="sxs-lookup"><span data-stu-id="39dbf-104">SystemConfig\_Power class</span></span>

<span data-ttu-id="39dbf-105">Questa classe è la classe del tipo di evento per gli eventi di configurazione dell'alimentazione.</span><span class="sxs-lookup"><span data-stu-id="39dbf-105">This class is the event type class for power configuration events.</span></span>

<span data-ttu-id="39dbf-106">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="39dbf-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="39dbf-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="39dbf-107">Syntax</span></span>

``` syntax
[EventType(16), EventTypeName("Power")]
class SystemConfig_Power : SystemConfig
{
  uint8 s1;
  uint8 s2;
  uint8 s3;
  uint8 s4;
  uint8 s5;
  uint8 Pad1;
  uint8 Pad2;
  uint8 Pad3;
};
```

## <a name="members"></a><span data-ttu-id="39dbf-108">Members</span><span class="sxs-lookup"><span data-stu-id="39dbf-108">Members</span></span>

<span data-ttu-id="39dbf-109">La **classe \_ Power di SystemConfig** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="39dbf-109">The **SystemConfig\_Power** class has these types of members:</span></span>

-   [<span data-ttu-id="39dbf-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="39dbf-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="39dbf-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="39dbf-111">Properties</span></span>

<span data-ttu-id="39dbf-112">La **classe \_ Power di SystemConfig** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="39dbf-112">The **SystemConfig\_Power** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="39dbf-113">Pad1</span><span class="sxs-lookup"><span data-stu-id="39dbf-113">Pad1</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39dbf-114">Tipo di dati: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="39dbf-114">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="39dbf-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="39dbf-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="39dbf-116">Qualificatori: WmiDataId (6)</span><span class="sxs-lookup"><span data-stu-id="39dbf-116">Qualifiers: WmiDataId(6)</span></span>
</dt> </dl>

<span data-ttu-id="39dbf-117">Non usato.</span><span class="sxs-lookup"><span data-stu-id="39dbf-117">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="39dbf-118">Pad2</span><span class="sxs-lookup"><span data-stu-id="39dbf-118">Pad2</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39dbf-119">Tipo di dati: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="39dbf-119">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="39dbf-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="39dbf-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="39dbf-121">Qualificatori: WmiDataId (7)</span><span class="sxs-lookup"><span data-stu-id="39dbf-121">Qualifiers: WmiDataId(7)</span></span>
</dt> </dl>

<span data-ttu-id="39dbf-122">Non usato.</span><span class="sxs-lookup"><span data-stu-id="39dbf-122">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="39dbf-123">Pad3</span><span class="sxs-lookup"><span data-stu-id="39dbf-123">Pad3</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39dbf-124">Tipo di dati: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="39dbf-124">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="39dbf-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="39dbf-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="39dbf-126">Qualificatori: WmiDataId (8)</span><span class="sxs-lookup"><span data-stu-id="39dbf-126">Qualifiers: WmiDataId(8)</span></span>
</dt> </dl>

<span data-ttu-id="39dbf-127">Non usato.</span><span class="sxs-lookup"><span data-stu-id="39dbf-127">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="39dbf-128">s1</span><span class="sxs-lookup"><span data-stu-id="39dbf-128">s1</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39dbf-129">Tipo di dati: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="39dbf-129">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="39dbf-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="39dbf-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="39dbf-131">Qualificatori: WmiDataId (1)</span><span class="sxs-lookup"><span data-stu-id="39dbf-131">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="39dbf-132">True indica che il sistema supporta lo stato di sospensione S1.</span><span class="sxs-lookup"><span data-stu-id="39dbf-132">True indicates the system supports sleep state S1.</span></span>

</dd> <dt>

<span data-ttu-id="39dbf-133">s2</span><span class="sxs-lookup"><span data-stu-id="39dbf-133">s2</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39dbf-134">Tipo di dati: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="39dbf-134">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="39dbf-135">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="39dbf-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="39dbf-136">Qualificatori: WmiDataId (2)</span><span class="sxs-lookup"><span data-stu-id="39dbf-136">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="39dbf-137">True indica che il sistema supporta lo stato di sospensione S2.</span><span class="sxs-lookup"><span data-stu-id="39dbf-137">True indicates the system supports sleep state S2.</span></span>

</dd> <dt>

<span data-ttu-id="39dbf-138">s3</span><span class="sxs-lookup"><span data-stu-id="39dbf-138">s3</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39dbf-139">Tipo di dati: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="39dbf-139">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="39dbf-140">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="39dbf-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="39dbf-141">Qualificatori: WmiDataId (3)</span><span class="sxs-lookup"><span data-stu-id="39dbf-141">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="39dbf-142">True indica che il sistema supporta lo stato di sospensione S3.</span><span class="sxs-lookup"><span data-stu-id="39dbf-142">True indicates the system supports sleep state S3.</span></span>

</dd> <dt>

<span data-ttu-id="39dbf-143">S4</span><span class="sxs-lookup"><span data-stu-id="39dbf-143">s4</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39dbf-144">Tipo di dati: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="39dbf-144">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="39dbf-145">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="39dbf-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="39dbf-146">Qualificatori: WmiDataId (4)</span><span class="sxs-lookup"><span data-stu-id="39dbf-146">Qualifiers: WmiDataId(4)</span></span>
</dt> </dl>

<span data-ttu-id="39dbf-147">True indica che il sistema supporta lo stato di sospensione S4.</span><span class="sxs-lookup"><span data-stu-id="39dbf-147">True indicates the system supports sleep state S4.</span></span>

</dd> <dt>

<span data-ttu-id="39dbf-148">S5</span><span class="sxs-lookup"><span data-stu-id="39dbf-148">s5</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39dbf-149">Tipo di dati: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="39dbf-149">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="39dbf-150">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="39dbf-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="39dbf-151">Qualificatori: WmiDataId (5)</span><span class="sxs-lookup"><span data-stu-id="39dbf-151">Qualifiers: WmiDataId(5)</span></span>
</dt> </dl>

<span data-ttu-id="39dbf-152">True indica che il sistema supporta lo stato di sospensione S5.</span><span class="sxs-lookup"><span data-stu-id="39dbf-152">True indicates the system supports sleep state S5.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="39dbf-153">Requisiti</span><span class="sxs-lookup"><span data-stu-id="39dbf-153">Requirements</span></span>



| <span data-ttu-id="39dbf-154">Requisito</span><span class="sxs-lookup"><span data-stu-id="39dbf-154">Requirement</span></span> | <span data-ttu-id="39dbf-155">Valore</span><span class="sxs-lookup"><span data-stu-id="39dbf-155">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="39dbf-156">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="39dbf-156">Minimum supported client</span></span><br/> | <span data-ttu-id="39dbf-157">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="39dbf-157">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="39dbf-158">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="39dbf-158">Minimum supported server</span></span><br/> | <span data-ttu-id="39dbf-159">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="39dbf-159">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="39dbf-160">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="39dbf-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39dbf-161">**SystemConfig**</span><span class="sxs-lookup"><span data-stu-id="39dbf-161">**SystemConfig**</span></span>](systemconfig.md)
</dt> </dl>

 

 




