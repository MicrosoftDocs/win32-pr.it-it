---
description: Questa classe è la classe del tipo di evento per l'evento di creazione del file. La sintassi seguente è semplificata dal codice MOF.
ms.assetid: 83465072-3dae-4a39-8a36-1512025b79df
title: Classe FileIo_Create
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FileIo_Create
- FileIo_Create.IrpPtr
- FileIo_Create.TTID
- FileIo_Create.FileObject
- FileIo_Create.CreateOptions
- FileIo_Create.FileAttributes
- FileIo_Create.ShareAccess
- FileIo_Create.OpenPath
api_type:
- NA
api_location: ''
ms.openlocfilehash: 2f8a42e9dee1c49817d578ab73a221c013f69aef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977663"
---
# <a name="fileio_create-class"></a><span data-ttu-id="d276d-104">Classe di creazione FileIO \_</span><span class="sxs-lookup"><span data-stu-id="d276d-104">FileIo\_Create class</span></span>

<span data-ttu-id="d276d-105">Questa classe è la classe del tipo di evento per l'evento di creazione del file.</span><span class="sxs-lookup"><span data-stu-id="d276d-105">This class is the event type class for the file create event.</span></span>

<span data-ttu-id="d276d-106">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="d276d-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="d276d-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d276d-107">Syntax</span></span>

``` syntax
[EventType{64}, EventTypeName{"Create"}]
class FileIo_Create : FileIo
{
  uint32 IrpPtr;
  uint32 TTID;
  uint32 FileObject;
  uint32 CreateOptions;
  uint32 FileAttributes;
  uint32 ShareAccess;
  string OpenPath;
};
```

## <a name="members"></a><span data-ttu-id="d276d-108">Members</span><span class="sxs-lookup"><span data-stu-id="d276d-108">Members</span></span>

<span data-ttu-id="d276d-109">I tipi di membri della classe di **\_ creazione di FileIO** sono:</span><span class="sxs-lookup"><span data-stu-id="d276d-109">The **FileIo\_Create** class has these types of members:</span></span>

-   [<span data-ttu-id="d276d-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="d276d-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d276d-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="d276d-111">Properties</span></span>

<span data-ttu-id="d276d-112">Questa proprietà è presente nella classe **FileIO \_ create** .</span><span class="sxs-lookup"><span data-stu-id="d276d-112">The **FileIo\_Create** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d276d-113">**CreateOptions**</span><span class="sxs-lookup"><span data-stu-id="d276d-113">**CreateOptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d276d-114">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d276d-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d276d-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d276d-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d276d-116">Qualificatori: WmiDataId (4)</span><span class="sxs-lookup"><span data-stu-id="d276d-116">Qualifiers: WmiDataId(4)</span></span>
</dt> </dl>

<span data-ttu-id="d276d-117">Valori passati nei parametri *createOptions* e *CreateDispositions* alla funzione [**NTCreateFile**](/windows/win32/api/winternl/nf-winternl-ntcreatefile) .</span><span class="sxs-lookup"><span data-stu-id="d276d-117">Values passed in the *CreateOptions* and *CreateDispositions* parameters to the [**NtCreateFile**](/windows/win32/api/winternl/nf-winternl-ntcreatefile) function.</span></span>

</dd> <dt>

<span data-ttu-id="d276d-118">**FileAttributes**</span><span class="sxs-lookup"><span data-stu-id="d276d-118">**FileAttributes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d276d-119">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d276d-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d276d-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d276d-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d276d-121">Qualificatori: WmiDataId (5)</span><span class="sxs-lookup"><span data-stu-id="d276d-121">Qualifiers: WmiDataId(5)</span></span>
</dt> </dl>

<span data-ttu-id="d276d-122">Valore passato nel parametro *FileAttributes* alla funzione [**NTCreateFile**](/windows/win32/api/winternl/nf-winternl-ntcreatefile) .</span><span class="sxs-lookup"><span data-stu-id="d276d-122">Value passed in the *FileAttributes* parameter to the [**NtCreateFile**](/windows/win32/api/winternl/nf-winternl-ntcreatefile) function.</span></span>

</dd> <dt>

<span data-ttu-id="d276d-123">**FileObject**</span><span class="sxs-lookup"><span data-stu-id="d276d-123">**FileObject**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d276d-124">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d276d-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d276d-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d276d-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d276d-126">Qualificatori: WmiDataId (3), puntatore</span><span class="sxs-lookup"><span data-stu-id="d276d-126">Qualifiers: WmiDataId(3), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="d276d-127">Identificatore che può essere usato per correlare le operazioni alla stessa istanza dell'oggetto file aperto tra gli eventi di creazione e chiusura di file.</span><span class="sxs-lookup"><span data-stu-id="d276d-127">Identifier that can be used for correlating operations to the same opened file object instance between file create and close events.</span></span>

</dd> <dt>

<span data-ttu-id="d276d-128">**IrpPtr**</span><span class="sxs-lookup"><span data-stu-id="d276d-128">**IrpPtr**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d276d-129">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d276d-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d276d-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d276d-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d276d-131">Qualificatori: WmiDataId (1), puntatore</span><span class="sxs-lookup"><span data-stu-id="d276d-131">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="d276d-132">Pacchetto di richiesta IO.</span><span class="sxs-lookup"><span data-stu-id="d276d-132">IO request packet.</span></span> <span data-ttu-id="d276d-133">Questa proprietà identifica l'attività IO.</span><span class="sxs-lookup"><span data-stu-id="d276d-133">This property identifies the IO activity.</span></span>

</dd> <dt>

<span data-ttu-id="d276d-134">**OpenPath**</span><span class="sxs-lookup"><span data-stu-id="d276d-134">**OpenPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d276d-135">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d276d-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d276d-136">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d276d-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d276d-137">Qualificatori: WmiDataId (7), StringTermination ("NullTerminated"), Format ("w")</span><span class="sxs-lookup"><span data-stu-id="d276d-137">Qualifiers: WmiDataId(7), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="d276d-138">Percorso del file.</span><span class="sxs-lookup"><span data-stu-id="d276d-138">Path to the file.</span></span>

</dd> <dt>

<span data-ttu-id="d276d-139">**ShareAccess**</span><span class="sxs-lookup"><span data-stu-id="d276d-139">**ShareAccess**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d276d-140">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d276d-140">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d276d-141">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d276d-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d276d-142">Qualificatori: WmiDataId (6)</span><span class="sxs-lookup"><span data-stu-id="d276d-142">Qualifiers: WmiDataId(6)</span></span>
</dt> </dl>

<span data-ttu-id="d276d-143">Valore passato nel parametro *ShareAccess* alla funzione [**NTCreateFile**](/windows/win32/api/winternl/nf-winternl-ntcreatefile) .</span><span class="sxs-lookup"><span data-stu-id="d276d-143">Value passed in the *ShareAccess* parameter to the [**NtCreateFile**](/windows/win32/api/winternl/nf-winternl-ntcreatefile) function.</span></span>

</dd> <dt>

<span data-ttu-id="d276d-144">**TTID**</span><span class="sxs-lookup"><span data-stu-id="d276d-144">**TTID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d276d-145">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d276d-145">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d276d-146">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d276d-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d276d-147">Qualificatori: WmiDataId (2), puntatore</span><span class="sxs-lookup"><span data-stu-id="d276d-147">Qualifiers: WmiDataId(2), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="d276d-148">Identificatore del thread che sta creando il file.</span><span class="sxs-lookup"><span data-stu-id="d276d-148">Thread identifier of the thread that is creating the file.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d276d-149">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d276d-149">Requirements</span></span>



| <span data-ttu-id="d276d-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="d276d-150">Requirement</span></span> | <span data-ttu-id="d276d-151">Valore</span><span class="sxs-lookup"><span data-stu-id="d276d-151">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="d276d-152">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d276d-152">Minimum supported client</span></span><br/> | <span data-ttu-id="d276d-153">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d276d-153">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="d276d-154">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d276d-154">Minimum supported server</span></span><br/> | <span data-ttu-id="d276d-155">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d276d-155">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d276d-156">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d276d-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d276d-157">**FileIo**</span><span class="sxs-lookup"><span data-stu-id="d276d-157">**FileIo**</span></span>](fileio.md)
</dt> </dl>

 

 
