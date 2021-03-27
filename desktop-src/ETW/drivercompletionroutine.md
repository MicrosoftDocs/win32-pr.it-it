---
description: Questa classe è la classe del tipo di evento per gli eventi di routine di driver completi. La sintassi seguente è semplificata dal codice MOF.
ms.assetid: deb4f0b2-d73f-4ccf-b39b-6e92b32489fb
title: Classe DriverCompletionRoutine
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DriverCompletionRoutine
- DriverCompletionRoutine.Routine
- DriverCompletionRoutine.Irp
- DriverCompletionRoutine.UniqMatchId
api_type:
- NA
api_location: ''
ms.openlocfilehash: 2b43862169cbe8f192f8fb9db561c2e101f377b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878730"
---
# <a name="drivercompletionroutine-class"></a><span data-ttu-id="fc5bb-104">Classe DriverCompletionRoutine</span><span class="sxs-lookup"><span data-stu-id="fc5bb-104">DriverCompletionRoutine class</span></span>

<span data-ttu-id="fc5bb-105">Questa classe è la classe del tipo di evento per gli eventi di routine di driver completi.</span><span class="sxs-lookup"><span data-stu-id="fc5bb-105">This class is the event type class for driver complete routine events.</span></span>

<span data-ttu-id="fc5bb-106">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="fc5bb-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc5bb-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fc5bb-107">Syntax</span></span>

``` syntax
[EventType{37}, EventTypeName{"DrvComplRout"}]
class DriverCompletionRoutine : DiskIo
{
  uint32 Routine;
  uint32 Irp;
  uint32 UniqMatchId;
};
```

## <a name="members"></a><span data-ttu-id="fc5bb-108">Members</span><span class="sxs-lookup"><span data-stu-id="fc5bb-108">Members</span></span>

<span data-ttu-id="fc5bb-109">La classe **DriverCompletionRoutine** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="fc5bb-109">The **DriverCompletionRoutine** class has these types of members:</span></span>

-   [<span data-ttu-id="fc5bb-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="fc5bb-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fc5bb-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="fc5bb-111">Properties</span></span>

<span data-ttu-id="fc5bb-112">La classe **DriverCompletionRoutine** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="fc5bb-112">The **DriverCompletionRoutine** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="fc5bb-113">**IRP**</span><span class="sxs-lookup"><span data-stu-id="fc5bb-113">**Irp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc5bb-114">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fc5bb-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fc5bb-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fc5bb-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fc5bb-116">Qualificatori: WmiDataId (2), puntatore</span><span class="sxs-lookup"><span data-stu-id="fc5bb-116">Qualifiers: WmiDataId(2), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="fc5bb-117">Pacchetto di richiesta IO.</span><span class="sxs-lookup"><span data-stu-id="fc5bb-117">IO request packet.</span></span>

</dd> <dt>

<span data-ttu-id="fc5bb-118">**Routine**</span><span class="sxs-lookup"><span data-stu-id="fc5bb-118">**Routine**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc5bb-119">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fc5bb-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fc5bb-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fc5bb-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fc5bb-121">Qualificatori: WmiDataId (1), puntatore</span><span class="sxs-lookup"><span data-stu-id="fc5bb-121">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="fc5bb-122">Indirizzo della funzione di driver chiamata.</span><span class="sxs-lookup"><span data-stu-id="fc5bb-122">Address of the driver function being called.</span></span>

</dd> <dt>

<span data-ttu-id="fc5bb-123">**UniqMatchId**</span><span class="sxs-lookup"><span data-stu-id="fc5bb-123">**UniqMatchId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc5bb-124">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fc5bb-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fc5bb-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fc5bb-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fc5bb-126">Qualificatori: WmiDataId (3)</span><span class="sxs-lookup"><span data-stu-id="fc5bb-126">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="fc5bb-127">Identificatore che identifica in modo univoco la richiesta.</span><span class="sxs-lookup"><span data-stu-id="fc5bb-127">Identifier that uniquely identifies request.</span></span> <span data-ttu-id="fc5bb-128">Usare questo identificatore per la correlazione con gli altri eventi del driver, ad esempio l'evento [**DriverCompleteRequest**](drivercompleterequest.md) .</span><span class="sxs-lookup"><span data-stu-id="fc5bb-128">Use this identifier to correlate with the other driver events, for example, the [**DriverCompleteRequest**](drivercompleterequest.md) event.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fc5bb-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fc5bb-129">Requirements</span></span>



| <span data-ttu-id="fc5bb-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="fc5bb-130">Requirement</span></span> | <span data-ttu-id="fc5bb-131">Valore</span><span class="sxs-lookup"><span data-stu-id="fc5bb-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="fc5bb-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fc5bb-132">Minimum supported client</span></span><br/> | <span data-ttu-id="fc5bb-133">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fc5bb-133">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="fc5bb-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fc5bb-134">Minimum supported server</span></span><br/> | <span data-ttu-id="fc5bb-135">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="fc5bb-135">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="fc5bb-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fc5bb-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc5bb-137">**DiskIo**</span><span class="sxs-lookup"><span data-stu-id="fc5bb-137">**DiskIo**</span></span>](diskio.md)
</dt> </dl>

 

 




