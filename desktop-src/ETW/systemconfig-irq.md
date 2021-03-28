---
description: Questa classe è la classe del tipo di evento per gli eventi di richiesta di interrupt (IRQ). La sintassi seguente è semplificata dal codice MOF.
ms.assetid: 9d4692e8-f19f-478c-a003-396722e426c3
title: Classe SystemConfig_IRQ
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_IRQ
- SystemConfig_IRQ.IRQAffinity
- SystemConfig_IRQ.IRQNum
- SystemConfig_IRQ.DeviceDescriptionLen
- SystemConfig_IRQ.DeviceDescription
api_type:
- NA
api_location: ''
ms.openlocfilehash: e1dd674c34c06259bc343615c17d165be3f57d32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977591"
---
# <a name="systemconfig_irq-class"></a><span data-ttu-id="44494-104">\_Classe IRQ SystemConfig</span><span class="sxs-lookup"><span data-stu-id="44494-104">SystemConfig\_IRQ class</span></span>

<span data-ttu-id="44494-105">Questa classe è la classe del tipo di evento per gli eventi di richiesta di interrupt (IRQ).</span><span class="sxs-lookup"><span data-stu-id="44494-105">This class is the event type class for interrupt request (IRQ) events.</span></span>

<span data-ttu-id="44494-106">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="44494-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="44494-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="44494-107">Syntax</span></span>

``` syntax
[EventType(21), EventTypeName("IRQ")]
class SystemConfig_IRQ : SystemConfig
{
  uint64 IRQAffinity;
  uint32 IRQNum;
  uint32 DeviceDescriptionLen;
  string DeviceDescription;
};
```

## <a name="members"></a><span data-ttu-id="44494-108">Members</span><span class="sxs-lookup"><span data-stu-id="44494-108">Members</span></span>

<span data-ttu-id="44494-109">La **classe \_ IRQ SystemConfig** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="44494-109">The **SystemConfig\_IRQ** class has these types of members:</span></span>

-   [<span data-ttu-id="44494-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="44494-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="44494-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="44494-111">Properties</span></span>

<span data-ttu-id="44494-112">La **classe \_ IRQ SystemConfig** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="44494-112">The **SystemConfig\_IRQ** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="44494-113">**DeviceDescription**</span><span class="sxs-lookup"><span data-stu-id="44494-113">**DeviceDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44494-114">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="44494-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="44494-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="44494-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="44494-116">Qualificatori: WmiDataId (4), StringTermination ("NullTerminated"), Format ("w")</span><span class="sxs-lookup"><span data-stu-id="44494-116">Qualifiers: WmiDataId(4), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="44494-117">Descrizione del dispositivo o del software che effettua la richiesta.</span><span class="sxs-lookup"><span data-stu-id="44494-117">Description of the device or software making the request.</span></span>

</dd> <dt>

<span data-ttu-id="44494-118">**DeviceDescriptionLen**</span><span class="sxs-lookup"><span data-stu-id="44494-118">**DeviceDescriptionLen**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44494-119">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="44494-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="44494-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="44494-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="44494-121">Qualificatori: WmiDataId (3)</span><span class="sxs-lookup"><span data-stu-id="44494-121">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="44494-122">Lunghezza, in caratteri, della stringa in **DeviceDescription**.</span><span class="sxs-lookup"><span data-stu-id="44494-122">Length, in characters, of the string in **DeviceDescription**.</span></span>

</dd> <dt>

<span data-ttu-id="44494-123">**IRQAffinity**</span><span class="sxs-lookup"><span data-stu-id="44494-123">**IRQAffinity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44494-124">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="44494-124">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="44494-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="44494-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="44494-126">Qualificatori: WmiDataId (1), Format ("x")</span><span class="sxs-lookup"><span data-stu-id="44494-126">Qualifiers: WmiDataId(1), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="44494-127">Maschera di affinità IRQ.</span><span class="sxs-lookup"><span data-stu-id="44494-127">IRQ affinity mask.</span></span> <span data-ttu-id="44494-128">Affinity mask identifica i processori o i gruppi di processori specifici che possono ricevere l'IRQ.</span><span class="sxs-lookup"><span data-stu-id="44494-128">The affinity mask identifies the specific processors (or groups of processors) that can receive the IRQ.</span></span>

</dd> <dt>

<span data-ttu-id="44494-129">**IRQNum**</span><span class="sxs-lookup"><span data-stu-id="44494-129">**IRQNum**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44494-130">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="44494-130">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="44494-131">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="44494-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="44494-132">Qualificatori: WmiDataId (2)</span><span class="sxs-lookup"><span data-stu-id="44494-132">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="44494-133">Numero di riga della richiesta di interrupt.</span><span class="sxs-lookup"><span data-stu-id="44494-133">Interrupt request line number.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="44494-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="44494-134">Requirements</span></span>



| <span data-ttu-id="44494-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="44494-135">Requirement</span></span> | <span data-ttu-id="44494-136">Valore</span><span class="sxs-lookup"><span data-stu-id="44494-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="44494-137">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="44494-137">Minimum supported client</span></span><br/> | <span data-ttu-id="44494-138">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="44494-138">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="44494-139">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="44494-139">Minimum supported server</span></span><br/> | <span data-ttu-id="44494-140">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="44494-140">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="44494-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="44494-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44494-142">**SystemConfig**</span><span class="sxs-lookup"><span data-stu-id="44494-142">**SystemConfig**</span></span>](systemconfig.md)
</dt> </dl>

 

 




