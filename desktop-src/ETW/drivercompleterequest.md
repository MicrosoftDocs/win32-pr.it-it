---
description: Questa classe è la classe del tipo di evento per gli eventi di richiesta completi del driver. La sintassi seguente è semplificata dal codice MOF.
ms.assetid: c9c9be05-c1c6-4d77-a47a-44a61ebfcdc7
title: Classe DriverCompleteRequest
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DriverCompleteRequest
- DriverCompleteRequest.RoutineAddr
- DriverCompleteRequest.Irp
- DriverCompleteRequest.UniqMatchId
api_type:
- NA
api_location: ''
ms.openlocfilehash: 57cf49d0e37dc870c0eb46c31ef39e0d81689811
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977151"
---
# <a name="drivercompleterequest-class"></a><span data-ttu-id="e9093-104">Classe DriverCompleteRequest</span><span class="sxs-lookup"><span data-stu-id="e9093-104">DriverCompleteRequest class</span></span>

<span data-ttu-id="e9093-105">Questa classe è la classe del tipo di evento per gli eventi di richiesta completi del driver.</span><span class="sxs-lookup"><span data-stu-id="e9093-105">This class is the event type class for driver complete request events.</span></span>

<span data-ttu-id="e9093-106">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="e9093-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9093-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e9093-107">Syntax</span></span>

``` syntax
[EventType{52}, EventTypeName{"DrvComplReq"}]
class DriverCompleteRequest : DiskIo
{
  uint32 RoutineAddr;
  uint32 Irp;
  uint32 UniqMatchId;
};
```

## <a name="members"></a><span data-ttu-id="e9093-108">Members</span><span class="sxs-lookup"><span data-stu-id="e9093-108">Members</span></span>

<span data-ttu-id="e9093-109">La classe **DriverCompleteRequest** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="e9093-109">The **DriverCompleteRequest** class has these types of members:</span></span>

-   [<span data-ttu-id="e9093-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="e9093-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e9093-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="e9093-111">Properties</span></span>

<span data-ttu-id="e9093-112">La classe **DriverCompleteRequest** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="e9093-112">The **DriverCompleteRequest** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e9093-113">**IRP**</span><span class="sxs-lookup"><span data-stu-id="e9093-113">**Irp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9093-114">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e9093-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e9093-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e9093-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e9093-116">Qualificatori: WmiDataId (2), puntatore</span><span class="sxs-lookup"><span data-stu-id="e9093-116">Qualifiers: WmiDataId(2), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="e9093-117">Pacchetto di richiesta IO.</span><span class="sxs-lookup"><span data-stu-id="e9093-117">IO request packet.</span></span>

</dd> <dt>

<span data-ttu-id="e9093-118">**RoutineAddr**</span><span class="sxs-lookup"><span data-stu-id="e9093-118">**RoutineAddr**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9093-119">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e9093-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e9093-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e9093-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e9093-121">Qualificatori: WmiDataId (1), puntatore</span><span class="sxs-lookup"><span data-stu-id="e9093-121">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="e9093-122">Indirizzo della funzione di driver chiamata.</span><span class="sxs-lookup"><span data-stu-id="e9093-122">Address of the driver function being called.</span></span>

</dd> <dt>

<span data-ttu-id="e9093-123">**UniqMatchId**</span><span class="sxs-lookup"><span data-stu-id="e9093-123">**UniqMatchId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9093-124">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e9093-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e9093-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e9093-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e9093-126">Qualificatori: WmiDataId (3)</span><span class="sxs-lookup"><span data-stu-id="e9093-126">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="e9093-127">Identificatore che identifica in modo univoco la richiesta.</span><span class="sxs-lookup"><span data-stu-id="e9093-127">Identifier that uniquely identifies request.</span></span> <span data-ttu-id="e9093-128">Usare questo identificatore per la correlazione con gli altri eventi del driver, ad esempio l'evento [**DriverCompleteRequestReturn**](drivercompleterequestreturn.md) .</span><span class="sxs-lookup"><span data-stu-id="e9093-128">Use this identifier to correlate with the other driver events, for example, the [**DriverCompleteRequestReturn**](drivercompleterequestreturn.md) event.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e9093-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e9093-129">Requirements</span></span>



| <span data-ttu-id="e9093-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="e9093-130">Requirement</span></span> | <span data-ttu-id="e9093-131">Valore</span><span class="sxs-lookup"><span data-stu-id="e9093-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="e9093-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e9093-132">Minimum supported client</span></span><br/> | <span data-ttu-id="e9093-133">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e9093-133">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="e9093-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e9093-134">Minimum supported server</span></span><br/> | <span data-ttu-id="e9093-135">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e9093-135">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e9093-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e9093-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9093-137">**DiskIo**</span><span class="sxs-lookup"><span data-stu-id="e9093-137">**DiskIo**</span></span>](diskio.md)
</dt> </dl>

 

 




