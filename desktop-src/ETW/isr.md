---
description: Questa classe è la classe del tipo di evento per gli eventi di routine del servizio di interrupt (ISR). La sintassi seguente è semplificata dal codice MOF.
ms.assetid: 2c7ccace-3384-43f4-905e-e7eeeee6f87b
title: ISR (classe)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISR
- ISR.InitialTime
- ISR.Routine
- ISR.ReturnValue
- ISR.Vector
- ISR.Reserved
api_type:
- NA
api_location: ''
ms.openlocfilehash: 5e27d5aa2712f8493b80ea11884aae1d0ef7abee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104979874"
---
# <a name="isr-class"></a><span data-ttu-id="fc113-104">ISR (classe)</span><span class="sxs-lookup"><span data-stu-id="fc113-104">ISR class</span></span>

<span data-ttu-id="fc113-105">Questa classe è la classe del tipo di evento per gli eventi di routine del servizio di interrupt (ISR).</span><span class="sxs-lookup"><span data-stu-id="fc113-105">This class is the event type class for interrupt service routine (ISR) events.</span></span>

<span data-ttu-id="fc113-106">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="fc113-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc113-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fc113-107">Syntax</span></span>

``` syntax
[EventType{67}, EventTypeName{"ISR"}]
class ISR : PerfInfo
{
  object InitialTime;
  uint32 Routine;
  uint8  ReturnValue;
  uint8  Vector;
  uint16 Reserved;
};
```

## <a name="members"></a><span data-ttu-id="fc113-108">Members</span><span class="sxs-lookup"><span data-stu-id="fc113-108">Members</span></span>

<span data-ttu-id="fc113-109">La classe **ISR** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="fc113-109">The **ISR** class has these types of members:</span></span>

-   [<span data-ttu-id="fc113-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="fc113-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fc113-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="fc113-111">Properties</span></span>

<span data-ttu-id="fc113-112">La classe **ISR** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="fc113-112">The **ISR** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="fc113-113">**InitialTime**</span><span class="sxs-lookup"><span data-stu-id="fc113-113">**InitialTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc113-114">Tipo di dati: **Object**</span><span class="sxs-lookup"><span data-stu-id="fc113-114">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="fc113-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fc113-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fc113-116">Qualificatori: WmiDataId (1), Extension ("WmiTime")</span><span class="sxs-lookup"><span data-stu-id="fc113-116">Qualifiers: WmiDataId(1), Extension("WmiTime")</span></span>
</dt> </dl>

<span data-ttu-id="fc113-117">Ora di ingresso ISR.</span><span class="sxs-lookup"><span data-stu-id="fc113-117">ISR entry time.</span></span>

</dd> <dt>

<span data-ttu-id="fc113-118">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="fc113-118">**Reserved**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc113-119">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fc113-119">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fc113-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fc113-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fc113-121">Qualificatori: WmiDataId (5), puntatore</span><span class="sxs-lookup"><span data-stu-id="fc113-121">Qualifiers: WmiDataId(5), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="fc113-122">Riservato.</span><span class="sxs-lookup"><span data-stu-id="fc113-122">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="fc113-123">**ReturnValue**</span><span class="sxs-lookup"><span data-stu-id="fc113-123">**ReturnValue**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc113-124">Tipo di dati: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="fc113-124">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="fc113-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fc113-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fc113-126">Qualificatori: WmiDataId (3)</span><span class="sxs-lookup"><span data-stu-id="fc113-126">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="fc113-127">Valore booleano che indica se l'interrupt è stato richiesto (è true se l'interrupt è stato richiesto).</span><span class="sxs-lookup"><span data-stu-id="fc113-127">Boolean indicating if the interrupt was claimed (is True if the interrupt was claimed).</span></span>

</dd> <dt>

<span data-ttu-id="fc113-128">**Routine**</span><span class="sxs-lookup"><span data-stu-id="fc113-128">**Routine**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc113-129">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fc113-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fc113-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fc113-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fc113-131">Qualificatori: WmiDataId (2), puntatore</span><span class="sxs-lookup"><span data-stu-id="fc113-131">Qualifiers: WmiDataId(2), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="fc113-132">Indirizzo della routine ISR.</span><span class="sxs-lookup"><span data-stu-id="fc113-132">Address of ISR routine.</span></span> <span data-ttu-id="fc113-133">Usare l'indirizzo con gli eventi di immagine per individuare l'immagine avviata.</span><span class="sxs-lookup"><span data-stu-id="fc113-133">Use the address with the Image events to find which image started.</span></span>

</dd> <dt>

<span data-ttu-id="fc113-134">**Vettore**</span><span class="sxs-lookup"><span data-stu-id="fc113-134">**Vector**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc113-135">Tipo di dati: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="fc113-135">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="fc113-136">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fc113-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fc113-137">Qualificatori: WmiDataId (4)</span><span class="sxs-lookup"><span data-stu-id="fc113-137">Qualifiers: WmiDataId(4)</span></span>
</dt> </dl>

<span data-ttu-id="fc113-138">Vettore dalla tabella del descrittore di interrupt a cui è assegnata la routine ISR.</span><span class="sxs-lookup"><span data-stu-id="fc113-138">Vector from interrupt descriptor table to which ISR routine is assigned.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fc113-139">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fc113-139">Requirements</span></span>



| <span data-ttu-id="fc113-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="fc113-140">Requirement</span></span> | <span data-ttu-id="fc113-141">Valore</span><span class="sxs-lookup"><span data-stu-id="fc113-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="fc113-142">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fc113-142">Minimum supported client</span></span><br/> | <span data-ttu-id="fc113-143">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fc113-143">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="fc113-144">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fc113-144">Minimum supported server</span></span><br/> | <span data-ttu-id="fc113-145">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="fc113-145">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




