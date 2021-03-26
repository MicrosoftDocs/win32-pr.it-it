---
description: Questa classe è la classe del tipo di evento per gli eventi PnP. La sintassi seguente è semplificata dal codice MOF.
ms.assetid: 01e9a8bb-3f54-4e20-b4db-1b4bba745d4f
title: Classe SystemConfig_PnP
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_PnP
- SystemConfig_PnP.IDLength
- SystemConfig_PnP.DescriptionLength
- SystemConfig_PnP.FriendlyNameLength
- SystemConfig_PnP.DeviceID
- SystemConfig_PnP.DeviceDescription
- SystemConfig_PnP.FriendlyName
api_type:
- NA
api_location: ''
ms.openlocfilehash: 2bd4cdbbec5c61f453a0ef6fae3fef0bd494edac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484668"
---
# <a name="systemconfig_pnp-class"></a><span data-ttu-id="30643-104">\_Classe PNP SystemConfig</span><span class="sxs-lookup"><span data-stu-id="30643-104">SystemConfig\_PnP class</span></span>

<span data-ttu-id="30643-105">Questa classe è la classe del tipo di evento per gli eventi PnP.</span><span class="sxs-lookup"><span data-stu-id="30643-105">This class is the event type class for PnP events.</span></span>

<span data-ttu-id="30643-106">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="30643-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="30643-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="30643-107">Syntax</span></span>

``` syntax
[EventType(22), EventTypeName("PnP")]
class SystemConfig_PnP : SystemConfig
{
  uint32 IDLength;
  uint32 DescriptionLength;
  uint32 FriendlyNameLength;
  string DeviceID;
  string DeviceDescription;
  string FriendlyName;
};
```

## <a name="members"></a><span data-ttu-id="30643-108">Members</span><span class="sxs-lookup"><span data-stu-id="30643-108">Members</span></span>

<span data-ttu-id="30643-109">La **classe \_ PNP SystemConfig** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="30643-109">The **SystemConfig\_PnP** class has these types of members:</span></span>

-   [<span data-ttu-id="30643-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="30643-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="30643-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="30643-111">Properties</span></span>

<span data-ttu-id="30643-112">La **classe \_ PNP SystemConfig** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="30643-112">The **SystemConfig\_PnP** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="30643-113">**DescriptionLength**</span><span class="sxs-lookup"><span data-stu-id="30643-113">**DescriptionLength**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="30643-114">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="30643-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="30643-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="30643-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="30643-116">Qualificatori: WmiDataId (2)</span><span class="sxs-lookup"><span data-stu-id="30643-116">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="30643-117">Lunghezza, in caratteri, della stringa DeviceDescription.</span><span class="sxs-lookup"><span data-stu-id="30643-117">Length, in characters, of the DeviceDescription string.</span></span>

</dd> <dt>

<span data-ttu-id="30643-118">**DeviceDescription**</span><span class="sxs-lookup"><span data-stu-id="30643-118">**DeviceDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="30643-119">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="30643-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="30643-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="30643-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="30643-121">Qualificatori: WmiDataId (5), StringTermination ("NullTerminated"), Format ("w")</span><span class="sxs-lookup"><span data-stu-id="30643-121">Qualifiers: WmiDataId(5), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="30643-122">Descrizione del dispositivo PnP.</span><span class="sxs-lookup"><span data-stu-id="30643-122">Description of the PnP device.</span></span>

</dd> <dt>

<span data-ttu-id="30643-123">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="30643-123">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="30643-124">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="30643-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="30643-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="30643-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="30643-126">Qualificatori: WmiDataId (4), StringTermination ("NullTerminated"), Format ("w")</span><span class="sxs-lookup"><span data-stu-id="30643-126">Qualifiers: WmiDataId(4), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="30643-127">Identifica il dispositivo PnP.</span><span class="sxs-lookup"><span data-stu-id="30643-127">Identifies the PnP device.</span></span>

</dd> <dt>

<span data-ttu-id="30643-128">**FriendlyName**</span><span class="sxs-lookup"><span data-stu-id="30643-128">**FriendlyName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="30643-129">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="30643-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="30643-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="30643-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="30643-131">Qualificatori: WmiDataId (6), StringTermination ("NullTerminated"), Format ("w")</span><span class="sxs-lookup"><span data-stu-id="30643-131">Qualifiers: WmiDataId(6), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="30643-132">Nome del dispositivo PnP da usare in un'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="30643-132">Name of the PnP device to use in a user interface.</span></span>

</dd> <dt>

<span data-ttu-id="30643-133">**FriendlyNameLength**</span><span class="sxs-lookup"><span data-stu-id="30643-133">**FriendlyNameLength**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="30643-134">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="30643-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="30643-135">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="30643-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="30643-136">Qualificatori: WmiDataId (3)</span><span class="sxs-lookup"><span data-stu-id="30643-136">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="30643-137">Lunghezza, in caratteri, della stringa FriendlyName.</span><span class="sxs-lookup"><span data-stu-id="30643-137">Length, in characters, of the FriendlyName string.</span></span>

</dd> <dt>

<span data-ttu-id="30643-138">**IDLength**</span><span class="sxs-lookup"><span data-stu-id="30643-138">**IDLength**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="30643-139">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="30643-139">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="30643-140">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="30643-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="30643-141">Qualificatori: WmiDataId (1)</span><span class="sxs-lookup"><span data-stu-id="30643-141">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="30643-142">Lunghezza, in caratteri, della stringa DeviceID.</span><span class="sxs-lookup"><span data-stu-id="30643-142">Length, in characters, of the DeviceID string.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="30643-143">Requisiti</span><span class="sxs-lookup"><span data-stu-id="30643-143">Requirements</span></span>



| <span data-ttu-id="30643-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="30643-144">Requirement</span></span> | <span data-ttu-id="30643-145">Valore</span><span class="sxs-lookup"><span data-stu-id="30643-145">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="30643-146">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="30643-146">Minimum supported client</span></span><br/> | <span data-ttu-id="30643-147">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="30643-147">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="30643-148">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="30643-148">Minimum supported server</span></span><br/> | <span data-ttu-id="30643-149">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="30643-149">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="30643-150">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="30643-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30643-151">**SystemConfig**</span><span class="sxs-lookup"><span data-stu-id="30643-151">**SystemConfig**</span></span>](systemconfig.md)
</dt> </dl>

 

 




