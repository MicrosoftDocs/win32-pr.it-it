---
description: Questa classe è la classe del tipo di evento per gli eventi di fine dell'operazione su file. La sintassi seguente è semplificata dal codice MOF.
ms.assetid: 3925d5bf-f412-4248-a61f-e667efa9debd
title: Classe FileIo_OpEnd
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FileIo_OpEnd
- FileIo_OpEnd.IrpPtr
- FileIo_OpEnd.ExtraInfo
- FileIo_OpEnd.NtStatus
api_type:
- NA
api_location: ''
ms.openlocfilehash: d3f1c495cf44b84f8d7661b40cadec6ea255c6a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758429"
---
# <a name="fileio_opend-class"></a><span data-ttu-id="6af86-104">\_Classe aprita FileIO</span><span class="sxs-lookup"><span data-stu-id="6af86-104">FileIo\_OpEnd class</span></span>

<span data-ttu-id="6af86-105">Questa classe è la classe del tipo di evento per gli eventi di fine dell'operazione su file.</span><span class="sxs-lookup"><span data-stu-id="6af86-105">This class is the event type class for file operation end events.</span></span>

<span data-ttu-id="6af86-106">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="6af86-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="6af86-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6af86-107">Syntax</span></span>

``` syntax
[EventType{76}, EventTypeName{"OperationEnd"}]
class FileIo_OpEnd : FileIo
{
  uint32 IrpPtr;
  uint32 ExtraInfo;
  uint32 NtStatus;
};
```

## <a name="members"></a><span data-ttu-id="6af86-108">Members</span><span class="sxs-lookup"><span data-stu-id="6af86-108">Members</span></span>

<span data-ttu-id="6af86-109">I tipi di membri della classe **\_ Open FileIO** sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="6af86-109">The **FileIo\_OpEnd** class has these types of members:</span></span>

-   [<span data-ttu-id="6af86-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="6af86-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6af86-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="6af86-111">Properties</span></span>

<span data-ttu-id="6af86-112">Le proprietà della classe **\_ Aprita del FileIO** sono tali.</span><span class="sxs-lookup"><span data-stu-id="6af86-112">The **FileIo\_OpEnd** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6af86-113">**ExtraInfo**</span><span class="sxs-lookup"><span data-stu-id="6af86-113">**ExtraInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6af86-114">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6af86-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6af86-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6af86-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6af86-116">Qualificatori: WmiDataId (2), puntatore</span><span class="sxs-lookup"><span data-stu-id="6af86-116">Qualifiers: WmiDataId(2), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="6af86-117">Informazioni aggiuntive restituite dal file system per l'operazione.</span><span class="sxs-lookup"><span data-stu-id="6af86-117">Extra information returned by the file system for the operation.</span></span> <span data-ttu-id="6af86-118">Ad esempio, per una richiesta di lettura, il numero effettivo di byte letti.</span><span class="sxs-lookup"><span data-stu-id="6af86-118">For example for a read request, the actual number of bytes that were read.</span></span>

</dd> <dt>

<span data-ttu-id="6af86-119">**IrpPtr**</span><span class="sxs-lookup"><span data-stu-id="6af86-119">**IrpPtr**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6af86-120">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6af86-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6af86-121">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6af86-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6af86-122">Qualificatori: WmiDataId (1), puntatore</span><span class="sxs-lookup"><span data-stu-id="6af86-122">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="6af86-123">Pacchetto di richiesta IO.</span><span class="sxs-lookup"><span data-stu-id="6af86-123">IO request packet.</span></span> <span data-ttu-id="6af86-124">Questa proprietà identifica l'attività IO che sta terminando.</span><span class="sxs-lookup"><span data-stu-id="6af86-124">This property identifies the IO activity that is ending.</span></span>

</dd> <dt>

<span data-ttu-id="6af86-125">**NtStatus**</span><span class="sxs-lookup"><span data-stu-id="6af86-125">**NtStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6af86-126">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6af86-126">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6af86-127">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6af86-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6af86-128">Qualificatori: WmiDataId (3)</span><span class="sxs-lookup"><span data-stu-id="6af86-128">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="6af86-129">Valore restituito dall'operazione.</span><span class="sxs-lookup"><span data-stu-id="6af86-129">Return value from the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6af86-130">Commenti</span><span class="sxs-lookup"><span data-stu-id="6af86-130">Remarks</span></span>

<span data-ttu-id="6af86-131">Gli eventi [**FileIO**](fileio.md) vengono registrati all'inizio dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="6af86-131">[**FileIo**](fileio.md) events are logged at the beginning of the operation.</span></span> <span data-ttu-id="6af86-132">Gli eventi aperti possono essere abilitati separatamente per indicare la fine di tali operazioni.</span><span class="sxs-lookup"><span data-stu-id="6af86-132">OpEnd events can be enabled separately to indicate the end of those operations.</span></span> <span data-ttu-id="6af86-133">È possibile utilizzare l'IRP per correlare gli eventi di inizio e di fine.</span><span class="sxs-lookup"><span data-stu-id="6af86-133">Irp can be used to correlate the begin and end events.</span></span>

## <a name="requirements"></a><span data-ttu-id="6af86-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6af86-134">Requirements</span></span>



| <span data-ttu-id="6af86-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="6af86-135">Requirement</span></span> | <span data-ttu-id="6af86-136">Valore</span><span class="sxs-lookup"><span data-stu-id="6af86-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="6af86-137">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6af86-137">Minimum supported client</span></span><br/> | <span data-ttu-id="6af86-138">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6af86-138">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="6af86-139">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6af86-139">Minimum supported server</span></span><br/> | <span data-ttu-id="6af86-140">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="6af86-140">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6af86-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6af86-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6af86-142">**FileIo**</span><span class="sxs-lookup"><span data-stu-id="6af86-142">**FileIo**</span></span>](fileio.md)
</dt> </dl>

 

 




