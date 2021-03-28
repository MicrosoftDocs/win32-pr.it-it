---
description: Questa classe è la classe del tipo di evento che contrassegna l'inizio degli eventi di lettura, scrittura e scaricamento di I/O su disco. La sintassi seguente è semplificata dal codice MOF.
ms.assetid: 96543ef9-cc2b-4d9a-86a8-f2458439e4d8
title: Classe DiskIo_TypeGroup2
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskIo_TypeGroup2
- DiskIo_TypeGroup2.Irp
- DiskIo_TypeGroup2.IssuingThreadId
api_type:
- NA
api_location: ''
ms.openlocfilehash: ea08f32106c935be628bcdcd22e39ab92a0566e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525261"
---
# <a name="diskio_typegroup2-class"></a><span data-ttu-id="e2516-104">\_Classe DiskIo TypeGroup2</span><span class="sxs-lookup"><span data-stu-id="e2516-104">DiskIo\_TypeGroup2 class</span></span>

<span data-ttu-id="e2516-105">Questa classe è la classe del tipo di evento che contrassegna l'inizio degli eventi di lettura, scrittura e scaricamento di I/O su disco.</span><span class="sxs-lookup"><span data-stu-id="e2516-105">This class is the event type class that marks the beginning of the disk I/O read, write, and flush events.</span></span>

<span data-ttu-id="e2516-106">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="e2516-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2516-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e2516-107">Syntax</span></span>

``` syntax
[EventType{12, 13, 15}, EventTypeName{"ReadInit", "WriteInit", "FlushInit"}]
class DiskIo_TypeGroup2 : DiskIo
{
  uint32 Irp;
  uint32 IssuingThreadId;
};
```

## <a name="members"></a><span data-ttu-id="e2516-108">Members</span><span class="sxs-lookup"><span data-stu-id="e2516-108">Members</span></span>

<span data-ttu-id="e2516-109">La **classe \_ TypeGroup2 di DiskIo** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="e2516-109">The **DiskIo\_TypeGroup2** class has these types of members:</span></span>

-   [<span data-ttu-id="e2516-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="e2516-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e2516-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="e2516-111">Properties</span></span>

<span data-ttu-id="e2516-112">La **classe \_ TypeGroup2 di DiskIo** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="e2516-112">The **DiskIo\_TypeGroup2** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e2516-113">**IRP**</span><span class="sxs-lookup"><span data-stu-id="e2516-113">**Irp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2516-114">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e2516-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e2516-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e2516-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2516-116">Qualificatori: [**WmiDataId**](event-tracing-mof-qualifiers.md) (1), [**puntatore**](event-tracing-mof-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="e2516-116">Qualifiers: [**WmiDataId**](event-tracing-mof-qualifiers.md) (1), [**Pointer**](event-tracing-mof-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="e2516-117">Pacchetto della richiesta di I/O.</span><span class="sxs-lookup"><span data-stu-id="e2516-117">I/O request packet.</span></span> <span data-ttu-id="e2516-118">Questa proprietà identifica l'attività IO.</span><span class="sxs-lookup"><span data-stu-id="e2516-118">This property identifies the IO activity.</span></span>

</dd> <dt>

<span data-ttu-id="e2516-119">**IssuingThreadId**</span><span class="sxs-lookup"><span data-stu-id="e2516-119">**IssuingThreadId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2516-120">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e2516-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e2516-121">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e2516-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2516-122">Qualificatori: [**WmiDataId**](event-tracing-mof-qualifiers.md) (2)</span><span class="sxs-lookup"><span data-stu-id="e2516-122">Qualifiers: [**WmiDataId**](event-tracing-mof-qualifiers.md) (2)</span></span>
</dt> </dl>

<span data-ttu-id="e2516-123">Identificatore del thread emittente.</span><span class="sxs-lookup"><span data-stu-id="e2516-123">The identifier of the issuing thread.</span></span>

<span data-ttu-id="e2516-124">**Windows server 2008 R2, Windows server 2008, Windows 7 e Windows Vista:** Questa proprietà non è supportata.</span><span class="sxs-lookup"><span data-stu-id="e2516-124">**Windows Server 2008 R2, Windows Server 2008, Windows 7 and Windows Vista:** This property is not supported.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e2516-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e2516-125">Requirements</span></span>



| <span data-ttu-id="e2516-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="e2516-126">Requirement</span></span> | <span data-ttu-id="e2516-127">Valore</span><span class="sxs-lookup"><span data-stu-id="e2516-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="e2516-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e2516-128">Minimum supported client</span></span><br/> | <span data-ttu-id="e2516-129">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e2516-129">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="e2516-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e2516-130">Minimum supported server</span></span><br/> | <span data-ttu-id="e2516-131">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e2516-131">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e2516-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e2516-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2516-133">**DiskIo**</span><span class="sxs-lookup"><span data-stu-id="e2516-133">**DiskIo**</span></span>](diskio.md)
</dt> </dl>

 

 




