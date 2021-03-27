---
description: Questa classe è la classe del tipo di evento per gli eventi del profilo campionati. La sintassi seguente è semplificata dal codice MOF.
ms.assetid: 75ea1e5e-2554-40bb-aa9d-c6d4942c5801
title: Classe SampledProfile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SampledProfile
- SampledProfile.InstructionPointer
- SampledProfile.ThreadId
- SampledProfile.Count
api_type:
- NA
api_location: ''
ms.openlocfilehash: 3d7a69eef1a2a7988569ffcd930b73a559e18d90
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980554"
---
# <a name="sampledprofile-class"></a><span data-ttu-id="cf36b-104">Classe SampledProfile</span><span class="sxs-lookup"><span data-stu-id="cf36b-104">SampledProfile class</span></span>

<span data-ttu-id="cf36b-105">Questa classe è la classe del tipo di evento per gli eventi del profilo campionati.</span><span class="sxs-lookup"><span data-stu-id="cf36b-105">This class is the event type class for sampled profile events.</span></span>

<span data-ttu-id="cf36b-106">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="cf36b-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf36b-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cf36b-107">Syntax</span></span>

``` syntax
[EventType{46}, EventTypeName{"SampleProfile"}]
class SampledProfile : PerfInfo
{
  uint32 InstructionPointer;
  uint32 ThreadId;
  uint32 Count;
};
```

## <a name="members"></a><span data-ttu-id="cf36b-108">Members</span><span class="sxs-lookup"><span data-stu-id="cf36b-108">Members</span></span>

<span data-ttu-id="cf36b-109">La classe **SampledProfile** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="cf36b-109">The **SampledProfile** class has these types of members:</span></span>

-   [<span data-ttu-id="cf36b-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="cf36b-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="cf36b-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="cf36b-111">Properties</span></span>

<span data-ttu-id="cf36b-112">La classe **SampledProfile** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="cf36b-112">The **SampledProfile** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="cf36b-113">**Count**</span><span class="sxs-lookup"><span data-stu-id="cf36b-113">**Count**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf36b-114">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cf36b-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cf36b-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cf36b-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cf36b-116">Qualificatori: WmiDataId (3)</span><span class="sxs-lookup"><span data-stu-id="cf36b-116">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="cf36b-117">Non usato.</span><span class="sxs-lookup"><span data-stu-id="cf36b-117">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="cf36b-118">**InstructionPointer**</span><span class="sxs-lookup"><span data-stu-id="cf36b-118">**InstructionPointer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf36b-119">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cf36b-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cf36b-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cf36b-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cf36b-121">Qualificatori: WmiDataId (1), puntatore</span><span class="sxs-lookup"><span data-stu-id="cf36b-121">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="cf36b-122">Indirizzo dell'immagine in esecuzione al momento del campionamento del processore.</span><span class="sxs-lookup"><span data-stu-id="cf36b-122">Address of the image that was running at the time the processor was sampled.</span></span>

</dd> <dt>

<span data-ttu-id="cf36b-123">**ThreadId**</span><span class="sxs-lookup"><span data-stu-id="cf36b-123">**ThreadId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf36b-124">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cf36b-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cf36b-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cf36b-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cf36b-126">Qualificatori: WmiDataId (2)</span><span class="sxs-lookup"><span data-stu-id="cf36b-126">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="cf36b-127">Identificatore del thread che era in esecuzione al momento del campionamento del processore.</span><span class="sxs-lookup"><span data-stu-id="cf36b-127">Thread identifier of the thread that was running at the time the processor was sampled.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cf36b-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="cf36b-128">Remarks</span></span>

<span data-ttu-id="cf36b-129">Questi eventi forniscono un profilo di esecuzione campionato.</span><span class="sxs-lookup"><span data-stu-id="cf36b-129">These events provide a sampled execution profile.</span></span> <span data-ttu-id="cf36b-130">L'evento registra gli elementi eseguiti sul processore.</span><span class="sxs-lookup"><span data-stu-id="cf36b-130">The event records what was being executed on the processor.</span></span> <span data-ttu-id="cf36b-131">È possibile usare gli eventi di immagine per identificare il modulo binario contenente tale istruzione.</span><span class="sxs-lookup"><span data-stu-id="cf36b-131">You can use the Image events to identify the binary module containing that instruction.</span></span> <span data-ttu-id="cf36b-132">È quindi possibile usare queste informazioni per produrre un profilo di esecuzione per la durata della traccia.</span><span class="sxs-lookup"><span data-stu-id="cf36b-132">You can then use this information to produce an execution profile for the duration of the trace.</span></span>

## <a name="requirements"></a><span data-ttu-id="cf36b-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cf36b-133">Requirements</span></span>



| <span data-ttu-id="cf36b-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="cf36b-134">Requirement</span></span> | <span data-ttu-id="cf36b-135">Valore</span><span class="sxs-lookup"><span data-stu-id="cf36b-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="cf36b-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cf36b-136">Minimum supported client</span></span><br/> | <span data-ttu-id="cf36b-137">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="cf36b-137">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="cf36b-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cf36b-138">Minimum supported server</span></span><br/> | <span data-ttu-id="cf36b-139">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="cf36b-139">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




