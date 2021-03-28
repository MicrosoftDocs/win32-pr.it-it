---
description: Questa classe è la classe del tipo di evento per gli eventi enumera directory e notifica directory. La sintassi seguente è semplificata dal codice MOF.
ms.assetid: 08458385-6066-4523-a053-aceb5e5d6f10
title: Classe FileIo_DirEnum
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FileIo_DirEnum
- FileIo_DirEnum.IrpPtr
- FileIo_DirEnum.TTID
- FileIo_DirEnum.FileObject
- FileIo_DirEnum.FileKey
- FileIo_DirEnum.Length
- FileIo_DirEnum.InfoClass
- FileIo_DirEnum.FileIndex
- FileIo_DirEnum.FileName
api_type:
- NA
api_location: ''
ms.openlocfilehash: 12f8fd8b4629ac11e7316caae0690982c210e4bc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977658"
---
# <a name="fileio_direnum-class"></a><span data-ttu-id="40add-104">Classe DirEnum di FileIO \_</span><span class="sxs-lookup"><span data-stu-id="40add-104">FileIo\_DirEnum class</span></span>

<span data-ttu-id="40add-105">Questa classe è la classe del tipo di evento per gli eventi enumera directory e notifica directory.</span><span class="sxs-lookup"><span data-stu-id="40add-105">This class is the event type class for the enumerate directory and directory notification events.</span></span>

<span data-ttu-id="40add-106">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="40add-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="40add-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="40add-107">Syntax</span></span>

``` syntax
[EventType{72, 77}, EventTypeName{"DirEnum", "DirNotify"}]
class FileIo_DirEnum : FileIo
{
  uint32 IrpPtr;
  uint32 TTID;
  uint32 FileObject;
  uint32 FileKey;
  uint32 Length;
  uint32 InfoClass;
  uint32 FileIndex;
  string FileName;
};
```

## <a name="members"></a><span data-ttu-id="40add-108">Members</span><span class="sxs-lookup"><span data-stu-id="40add-108">Members</span></span>

<span data-ttu-id="40add-109">La **classe \_ DirEnum di FileIO** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="40add-109">The **FileIo\_DirEnum** class has these types of members:</span></span>

-   [<span data-ttu-id="40add-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="40add-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="40add-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="40add-111">Properties</span></span>

<span data-ttu-id="40add-112">La **classe \_ DirEnum di FileIO** presenta queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="40add-112">The **FileIo\_DirEnum** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="40add-113">**FileIndex**</span><span class="sxs-lookup"><span data-stu-id="40add-113">**FileIndex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40add-114">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="40add-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="40add-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="40add-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="40add-116">Qualificatori: WmiDataId (7)</span><span class="sxs-lookup"><span data-stu-id="40add-116">Qualifiers: WmiDataId(7)</span></span>
</dt> </dl>

<span data-ttu-id="40add-117">Indice del file da cui continuare l'enumerazione di directory.</span><span class="sxs-lookup"><span data-stu-id="40add-117">File index from which to continue directory enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="40add-118">**FileKey**</span><span class="sxs-lookup"><span data-stu-id="40add-118">**FileKey**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40add-119">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="40add-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="40add-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="40add-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="40add-121">Qualificatori: WmiDataId (4), puntatore</span><span class="sxs-lookup"><span data-stu-id="40add-121">Qualifiers: WmiDataId(4), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="40add-122">Per determinare il nome della directory, associare il valore di questa proprietà alla proprietà **FileObject** di un evento del [**\_ nome del FileIO**](fileio-name.md) .</span><span class="sxs-lookup"><span data-stu-id="40add-122">To determine the directory name, match the value of this property to the **FileObject** property of a [**FileIo\_Name**](fileio-name.md) event.</span></span>

</dd> <dt>

<span data-ttu-id="40add-123">**FileName**</span><span class="sxs-lookup"><span data-stu-id="40add-123">**FileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40add-124">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="40add-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40add-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="40add-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="40add-126">Qualificatori: WmiDataId (8), StringTermination ("NullTerminated"), Format ("w")</span><span class="sxs-lookup"><span data-stu-id="40add-126">Qualifiers: WmiDataId(8), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="40add-127">Modello specificato per l'enumerazione di directory.</span><span class="sxs-lookup"><span data-stu-id="40add-127">Pattern specified for directory enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="40add-128">**FileObject**</span><span class="sxs-lookup"><span data-stu-id="40add-128">**FileObject**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40add-129">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="40add-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="40add-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="40add-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="40add-131">Qualificatori: WmiDataId (3), puntatore</span><span class="sxs-lookup"><span data-stu-id="40add-131">Qualifiers: WmiDataId(3), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="40add-132">Identificatore che può essere usato per correlare le operazioni alla stessa istanza dell'oggetto file aperto tra gli eventi di creazione e chiusura di file.</span><span class="sxs-lookup"><span data-stu-id="40add-132">Identifier that can be used for correlating operations to the same opened file object instance between file create and close events.</span></span>

</dd> <dt>

<span data-ttu-id="40add-133">**InfoClass**</span><span class="sxs-lookup"><span data-stu-id="40add-133">**InfoClass**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40add-134">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="40add-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="40add-135">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="40add-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="40add-136">Qualificatori: WmiDataId (6), puntatore</span><span class="sxs-lookup"><span data-stu-id="40add-136">Qualifiers: WmiDataId(6), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="40add-137">Classe di informazioni enumerazione directory richiesta.</span><span class="sxs-lookup"><span data-stu-id="40add-137">Requested directory enumeration information class.</span></span>

</dd> <dt>

<span data-ttu-id="40add-138">**IrpPtr**</span><span class="sxs-lookup"><span data-stu-id="40add-138">**IrpPtr**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40add-139">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="40add-139">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="40add-140">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="40add-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="40add-141">Qualificatori: WmiDataId (1), puntatore</span><span class="sxs-lookup"><span data-stu-id="40add-141">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="40add-142">Pacchetto di richiesta IO.</span><span class="sxs-lookup"><span data-stu-id="40add-142">IO request packet.</span></span> <span data-ttu-id="40add-143">Questa proprietà identifica l'attività IO.</span><span class="sxs-lookup"><span data-stu-id="40add-143">This property identifies the IO activity.</span></span>

</dd> <dt>

<span data-ttu-id="40add-144">**Length**</span><span class="sxs-lookup"><span data-stu-id="40add-144">**Length**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40add-145">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="40add-145">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="40add-146">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="40add-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="40add-147">Qualificatori: WmiDataId (5)</span><span class="sxs-lookup"><span data-stu-id="40add-147">Qualifiers: WmiDataId(5)</span></span>
</dt> </dl>

<span data-ttu-id="40add-148">Dimensioni in byte del buffer di query.</span><span class="sxs-lookup"><span data-stu-id="40add-148">Size of the query buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="40add-149">**TTID**</span><span class="sxs-lookup"><span data-stu-id="40add-149">**TTID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40add-150">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="40add-150">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="40add-151">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="40add-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="40add-152">Qualificatori: WmiDataId (2), puntatore</span><span class="sxs-lookup"><span data-stu-id="40add-152">Qualifiers: WmiDataId(2), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="40add-153">Identificatore del thread che sta eseguendo l'operazione.</span><span class="sxs-lookup"><span data-stu-id="40add-153">Thread identifier of the thread that is performing the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="40add-154">Commenti</span><span class="sxs-lookup"><span data-stu-id="40add-154">Remarks</span></span>

<span data-ttu-id="40add-155">L'enumerazione di directory e gli eventi di notifica della directory vengono registrati quando una directory viene enumerata o viene inviata una notifica di modifica della directory ai listener registrati, rispettivamente.</span><span class="sxs-lookup"><span data-stu-id="40add-155">Directory enumeration and directory notification events are recorded when a directory is enumerated or a directory change notification is sent to registered listeners, respectively.</span></span>

## <a name="requirements"></a><span data-ttu-id="40add-156">Requisiti</span><span class="sxs-lookup"><span data-stu-id="40add-156">Requirements</span></span>



| <span data-ttu-id="40add-157">Requisito</span><span class="sxs-lookup"><span data-stu-id="40add-157">Requirement</span></span> | <span data-ttu-id="40add-158">Valore</span><span class="sxs-lookup"><span data-stu-id="40add-158">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="40add-159">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="40add-159">Minimum supported client</span></span><br/> | <span data-ttu-id="40add-160">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="40add-160">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="40add-161">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="40add-161">Minimum supported server</span></span><br/> | <span data-ttu-id="40add-162">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="40add-162">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="40add-163">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="40add-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40add-164">**FileIo**</span><span class="sxs-lookup"><span data-stu-id="40add-164">**FileIo**</span></span>](fileio.md)
</dt> </dl>

 

 




