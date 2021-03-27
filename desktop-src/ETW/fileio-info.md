---
description: Questa classe è la classe del tipo di evento per l'evento di informazioni sul file. La sintassi seguente è semplificata dal codice MOF.
ms.assetid: 41ae1f8a-a90f-43d0-a848-a2c095f046d4
title: Classe FileIo_Info
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FileIo_Info
- FileIo_Info.IrpPtr
- FileIo_Info.TTID
- FileIo_Info.FileObject
- FileIo_Info.FileKey
- FileIo_Info.ExtraInfo
- FileIo_Info.InfoClass
api_type:
- NA
api_location: ''
ms.openlocfilehash: 985986132abe432e1adefb51939b8ace1aa48c8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980370"
---
# <a name="fileio_info-class"></a><span data-ttu-id="b609d-104">\_Classe info FileIO</span><span class="sxs-lookup"><span data-stu-id="b609d-104">FileIo\_Info class</span></span>

<span data-ttu-id="b609d-105">Questa classe è la classe del tipo di evento per l'evento di informazioni sul file.</span><span class="sxs-lookup"><span data-stu-id="b609d-105">This class is the event type class for file information event.</span></span>

<span data-ttu-id="b609d-106">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="b609d-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="b609d-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b609d-107">Syntax</span></span>

``` syntax
[EventType{69, 70, 71, 74, 75}, EventTypeName{"SetInfo", "Delete", "Rename", "QueryInfo", "FSControl"}]
class FileIo_Info : FileIo
{
  uint32 IrpPtr;
  uint32 TTID;
  uint32 FileObject;
  uint32 FileKey;
  uint32 ExtraInfo;
  uint32 InfoClass;
};
```

## <a name="members"></a><span data-ttu-id="b609d-108">Members</span><span class="sxs-lookup"><span data-stu-id="b609d-108">Members</span></span>

<span data-ttu-id="b609d-109">La **classe \_ info di FileIO** include questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="b609d-109">The **FileIo\_Info** class has these types of members:</span></span>

-   [<span data-ttu-id="b609d-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b609d-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b609d-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b609d-111">Properties</span></span>

<span data-ttu-id="b609d-112">La **classe \_ info del FileIO** contiene queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="b609d-112">The **FileIo\_Info** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b609d-113">**ExtraInfo**</span><span class="sxs-lookup"><span data-stu-id="b609d-113">**ExtraInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b609d-114">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b609d-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b609d-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b609d-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b609d-116">Qualificatori: WmiDataId (5), puntatore</span><span class="sxs-lookup"><span data-stu-id="b609d-116">Qualifiers: WmiDataId(5), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="b609d-117">Per le richieste FileDispositionInformation, questo campo contiene la disposizione richiesta.</span><span class="sxs-lookup"><span data-stu-id="b609d-117">For FileDispositionInformation requests, this field contains the requested disposition.</span></span> <span data-ttu-id="b609d-118">Per le richieste FileEndOfFileInformation e FileAllocationInformation, questo campo contiene le dimensioni del file specificato.</span><span class="sxs-lookup"><span data-stu-id="b609d-118">For FileEndOfFileInformation and FileAllocationInformation requests, this field contains the specified file size.</span></span>

</dd> <dt>

<span data-ttu-id="b609d-119">**FileKey**</span><span class="sxs-lookup"><span data-stu-id="b609d-119">**FileKey**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b609d-120">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b609d-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b609d-121">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b609d-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b609d-122">Qualificatori: WmiDataId (4), puntatore</span><span class="sxs-lookup"><span data-stu-id="b609d-122">Qualifiers: WmiDataId(4), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="b609d-123">Per determinare il nome del file, trovare la corrispondenza con il valore di questa proprietà con la proprietà **FileObject** di un evento del [**\_ nome**](fileio-name.md) del FileIO.</span><span class="sxs-lookup"><span data-stu-id="b609d-123">To determine the file name, match the value of this property to the **FileObject** property of a [**FileIo\_Name**](fileio-name.md) event.</span></span>

</dd> <dt>

<span data-ttu-id="b609d-124">**FileObject**</span><span class="sxs-lookup"><span data-stu-id="b609d-124">**FileObject**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b609d-125">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b609d-125">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b609d-126">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b609d-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b609d-127">Qualificatori: WmiDataId (3), puntatore</span><span class="sxs-lookup"><span data-stu-id="b609d-127">Qualifiers: WmiDataId(3), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="b609d-128">Identificatore che può essere usato per correlare le operazioni alla stessa istanza dell'oggetto file aperto tra gli eventi di creazione e chiusura di file.</span><span class="sxs-lookup"><span data-stu-id="b609d-128">Identifier that can be used for correlating operations to the same opened file object instance between file create and close events.</span></span>

</dd> <dt>

<span data-ttu-id="b609d-129">**InfoClass**</span><span class="sxs-lookup"><span data-stu-id="b609d-129">**InfoClass**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b609d-130">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b609d-130">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b609d-131">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b609d-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b609d-132">Qualificatori: WmiDataId (6)</span><span class="sxs-lookup"><span data-stu-id="b609d-132">Qualifiers: WmiDataId(6)</span></span>
</dt> </dl>

<span data-ttu-id="b609d-133">Classe di informazioni sui file richiesta.</span><span class="sxs-lookup"><span data-stu-id="b609d-133">Requested file information class.</span></span>

</dd> <dt>

<span data-ttu-id="b609d-134">**IrpPtr**</span><span class="sxs-lookup"><span data-stu-id="b609d-134">**IrpPtr**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b609d-135">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b609d-135">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b609d-136">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b609d-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b609d-137">Qualificatori: WmiDataId (1), puntatore</span><span class="sxs-lookup"><span data-stu-id="b609d-137">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="b609d-138">Pacchetto di richiesta IO.</span><span class="sxs-lookup"><span data-stu-id="b609d-138">IO request packet.</span></span> <span data-ttu-id="b609d-139">Questa proprietà identifica l'attività IO.</span><span class="sxs-lookup"><span data-stu-id="b609d-139">This property identifies the IO activity.</span></span>

</dd> <dt>

<span data-ttu-id="b609d-140">**TTID**</span><span class="sxs-lookup"><span data-stu-id="b609d-140">**TTID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b609d-141">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b609d-141">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b609d-142">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b609d-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b609d-143">Qualificatori: WmiDataId (2), puntatore</span><span class="sxs-lookup"><span data-stu-id="b609d-143">Qualifiers: WmiDataId(2), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="b609d-144">Identificatore del thread che sta eseguendo l'operazione.</span><span class="sxs-lookup"><span data-stu-id="b609d-144">Thread identifier of the thread that is performing the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b609d-145">Commenti</span><span class="sxs-lookup"><span data-stu-id="b609d-145">Remarks</span></span>

<span data-ttu-id="b609d-146">Set information and query Information Events indica che gli attributi di file sono stati impostati o sottoposti a query.</span><span class="sxs-lookup"><span data-stu-id="b609d-146">Set information and query information events indicate that the file attributes were set or queried.</span></span> <span data-ttu-id="b609d-147">Quando viene emesso un comando FSCTL, viene registrato un evento di controllo file system (FSControl).</span><span class="sxs-lookup"><span data-stu-id="b609d-147">A file system control (FSControl) event is recorded when a FSCTL command is issued.</span></span>

## <a name="requirements"></a><span data-ttu-id="b609d-148">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b609d-148">Requirements</span></span>



| <span data-ttu-id="b609d-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="b609d-149">Requirement</span></span> | <span data-ttu-id="b609d-150">Valore</span><span class="sxs-lookup"><span data-stu-id="b609d-150">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="b609d-151">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b609d-151">Minimum supported client</span></span><br/> | <span data-ttu-id="b609d-152">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b609d-152">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="b609d-153">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b609d-153">Minimum supported server</span></span><br/> | <span data-ttu-id="b609d-154">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b609d-154">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b609d-155">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b609d-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b609d-156">**FileIo**</span><span class="sxs-lookup"><span data-stu-id="b609d-156">**FileIo**</span></span>](fileio.md)
</dt> </dl>

 

 




