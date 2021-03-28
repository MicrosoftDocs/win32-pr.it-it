---
description: Questa classe è la classe del tipo di evento per gli eventi semplici dell'operazione sui file. La sintassi seguente è semplificata dal codice MOF.
ms.assetid: 5b6374e0-b39a-4d5a-acbd-25b410f1ba52
title: Classe FileIo_SimpleOp
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FileIo_SimpleOp
- FileIo_SimpleOp.IrpPtr
- FileIo_SimpleOp.TTID
- FileIo_SimpleOp.FileObject
- FileIo_SimpleOp.FileKey
api_type:
- NA
api_location: ''
ms.openlocfilehash: f7ff09830653278c9b37cfefa81b182b0f1dc054
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980362"
---
# <a name="fileio_simpleop-class"></a><span data-ttu-id="2e7dd-104">Classe SimpleOp di FileIO \_</span><span class="sxs-lookup"><span data-stu-id="2e7dd-104">FileIo\_SimpleOp class</span></span>

<span data-ttu-id="2e7dd-105">Questa classe è la classe del tipo di evento per gli eventi semplici dell'operazione sui file.</span><span class="sxs-lookup"><span data-stu-id="2e7dd-105">This class is the event type class for simple file operation events.</span></span>

<span data-ttu-id="2e7dd-106">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="2e7dd-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e7dd-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2e7dd-107">Syntax</span></span>

``` syntax
[EventType{65, 66, 73}, EventTypeName{"Cleanup", "Close", "Flush"}]
class FileIo_SimpleOp : FileIo
{
  uint32 IrpPtr;
  uint32 TTID;
  uint32 FileObject;
  uint32 FileKey;
};
```

## <a name="members"></a><span data-ttu-id="2e7dd-108">Members</span><span class="sxs-lookup"><span data-stu-id="2e7dd-108">Members</span></span>

<span data-ttu-id="2e7dd-109">La **classe \_ SimpleOp di FileIO** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="2e7dd-109">The **FileIo\_SimpleOp** class has these types of members:</span></span>

-   [<span data-ttu-id="2e7dd-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="2e7dd-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2e7dd-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="2e7dd-111">Properties</span></span>

<span data-ttu-id="2e7dd-112">La **classe \_ SimpleOp di FileIO** presenta queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="2e7dd-112">The **FileIo\_SimpleOp** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2e7dd-113">**FileKey**</span><span class="sxs-lookup"><span data-stu-id="2e7dd-113">**FileKey**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e7dd-114">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2e7dd-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2e7dd-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2e7dd-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2e7dd-116">Qualificatori: WmiDataId (4), puntatore</span><span class="sxs-lookup"><span data-stu-id="2e7dd-116">Qualifiers: WmiDataId(4), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="2e7dd-117">Per determinare il nome del file, trovare la corrispondenza con il valore di questa proprietà con la proprietà **FileObject** di un evento del [**\_ nome**](fileio-name.md) del FileIO.</span><span class="sxs-lookup"><span data-stu-id="2e7dd-117">To determine the file name, match the value of this property to the **FileObject** property of a [**FileIo\_Name**](fileio-name.md) event.</span></span>

</dd> <dt>

<span data-ttu-id="2e7dd-118">**FileObject**</span><span class="sxs-lookup"><span data-stu-id="2e7dd-118">**FileObject**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e7dd-119">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2e7dd-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2e7dd-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2e7dd-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2e7dd-121">Qualificatori: WmiDataId (3), puntatore</span><span class="sxs-lookup"><span data-stu-id="2e7dd-121">Qualifiers: WmiDataId(3), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="2e7dd-122">Identificatore che può essere usato per correlare le operazioni alla stessa istanza dell'oggetto file aperto tra gli eventi di creazione e chiusura di file.</span><span class="sxs-lookup"><span data-stu-id="2e7dd-122">Identifier that can be used for correlating operations to the same opened file object instance between file create and close events.</span></span>

</dd> <dt>

<span data-ttu-id="2e7dd-123">**IrpPtr**</span><span class="sxs-lookup"><span data-stu-id="2e7dd-123">**IrpPtr**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e7dd-124">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2e7dd-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2e7dd-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2e7dd-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2e7dd-126">Qualificatori: WmiDataId (1), puntatore</span><span class="sxs-lookup"><span data-stu-id="2e7dd-126">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="2e7dd-127">Pacchetto di richiesta IO.</span><span class="sxs-lookup"><span data-stu-id="2e7dd-127">IO request packet.</span></span> <span data-ttu-id="2e7dd-128">Questa proprietà identifica l'attività IO.</span><span class="sxs-lookup"><span data-stu-id="2e7dd-128">This property identifies the IO activity.</span></span>

</dd> <dt>

<span data-ttu-id="2e7dd-129">**TTID**</span><span class="sxs-lookup"><span data-stu-id="2e7dd-129">**TTID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e7dd-130">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2e7dd-130">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2e7dd-131">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2e7dd-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2e7dd-132">Qualificatori: WmiDataId (2), puntatore</span><span class="sxs-lookup"><span data-stu-id="2e7dd-132">Qualifiers: WmiDataId(2), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="2e7dd-133">Identificatore del thread che sta eseguendo l'operazione.</span><span class="sxs-lookup"><span data-stu-id="2e7dd-133">Thread identifier of the thread that is performing the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2e7dd-134">Commenti</span><span class="sxs-lookup"><span data-stu-id="2e7dd-134">Remarks</span></span>

<span data-ttu-id="2e7dd-135">L'evento Cleanup viene registrato quando viene chiuso l'ultimo handle del file.</span><span class="sxs-lookup"><span data-stu-id="2e7dd-135">The Cleanup event is logged when the last handle to the file is closed.</span></span> <span data-ttu-id="2e7dd-136">L'evento Close specifica che un oggetto file viene liberato.</span><span class="sxs-lookup"><span data-stu-id="2e7dd-136">The Close event specifies that a file object is being freed.</span></span> <span data-ttu-id="2e7dd-137">L'evento Flush specifica quando i buffer di file vengono scaricati completamente su disco.</span><span class="sxs-lookup"><span data-stu-id="2e7dd-137">The Flush event specifies when the file buffers are fully flushed to disk.</span></span>

## <a name="requirements"></a><span data-ttu-id="2e7dd-138">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2e7dd-138">Requirements</span></span>



| <span data-ttu-id="2e7dd-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="2e7dd-139">Requirement</span></span> | <span data-ttu-id="2e7dd-140">Valore</span><span class="sxs-lookup"><span data-stu-id="2e7dd-140">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="2e7dd-141">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2e7dd-141">Minimum supported client</span></span><br/> | <span data-ttu-id="2e7dd-142">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2e7dd-142">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="2e7dd-143">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2e7dd-143">Minimum supported server</span></span><br/> | <span data-ttu-id="2e7dd-144">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="2e7dd-144">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2e7dd-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2e7dd-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e7dd-146">**FileIo**</span><span class="sxs-lookup"><span data-stu-id="2e7dd-146">**FileIo**</span></span>](fileio.md)
</dt> </dl>

 

 




