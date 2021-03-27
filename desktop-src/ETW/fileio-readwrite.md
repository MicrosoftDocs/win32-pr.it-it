---
description: Questa classe è la classe del tipo di evento per gli eventi di lettura e scrittura di file. La sintassi seguente è semplificata dal codice MOF.
ms.assetid: 88c380fb-e043-40ab-aa74-550bce43c52b
title: Classe FileIo_ReadWrite
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FileIo_ReadWrite
- FileIo_ReadWrite.Offset
- FileIo_ReadWrite.IrpPtr
- FileIo_ReadWrite.TTID
- FileIo_ReadWrite.FileObject
- FileIo_ReadWrite.FileKey
- FileIo_ReadWrite.IoSize
- FileIo_ReadWrite.IoFlags
api_type:
- NA
api_location: ''
ms.openlocfilehash: c684444ea35efe0fee9c38b15be8fe7e45e9a102
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980367"
---
# <a name="fileio_readwrite-class"></a><span data-ttu-id="8a5c5-104">Classe ReadWrite di FileIO \_</span><span class="sxs-lookup"><span data-stu-id="8a5c5-104">FileIo\_ReadWrite class</span></span>

<span data-ttu-id="8a5c5-105">Questa classe è la classe del tipo di evento per gli eventi di lettura e scrittura di file.</span><span class="sxs-lookup"><span data-stu-id="8a5c5-105">This class is the event type class for file read and write events.</span></span>

<span data-ttu-id="8a5c5-106">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="8a5c5-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a5c5-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8a5c5-107">Syntax</span></span>

``` syntax
[EventType{67, 68}, EventTypeName{"Read", "Write"}]
class FileIo_ReadWrite : FileIo
{
  uint64 Offset;
  uint32 IrpPtr;
  uint32 TTID;
  uint32 FileObject;
  uint32 FileKey;
  uint32 IoSize;
  uint32 IoFlags;
};
```

## <a name="members"></a><span data-ttu-id="8a5c5-108">Members</span><span class="sxs-lookup"><span data-stu-id="8a5c5-108">Members</span></span>

<span data-ttu-id="8a5c5-109">La **classe \_ ReadWrite di FileIO** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="8a5c5-109">The **FileIo\_ReadWrite** class has these types of members:</span></span>

-   [<span data-ttu-id="8a5c5-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="8a5c5-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8a5c5-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="8a5c5-111">Properties</span></span>

<span data-ttu-id="8a5c5-112">La **classe \_ ReadWrite di FileIO** presenta queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="8a5c5-112">The **FileIo\_ReadWrite** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8a5c5-113">**FileKey**</span><span class="sxs-lookup"><span data-stu-id="8a5c5-113">**FileKey**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a5c5-114">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8a5c5-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8a5c5-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8a5c5-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8a5c5-116">Qualificatori: WmiDataId (5), puntatore</span><span class="sxs-lookup"><span data-stu-id="8a5c5-116">Qualifiers: WmiDataId(5), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="8a5c5-117">Per determinare il nome del file, trovare la corrispondenza con il valore di questa proprietà con la proprietà **FileObject** di un evento del [**\_ nome**](fileio-name.md) del FileIO.</span><span class="sxs-lookup"><span data-stu-id="8a5c5-117">To determine the file name, match the value of this property to the **FileObject** property of a [**FileIo\_Name**](fileio-name.md) event.</span></span>

</dd> <dt>

<span data-ttu-id="8a5c5-118">**FileObject**</span><span class="sxs-lookup"><span data-stu-id="8a5c5-118">**FileObject**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a5c5-119">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8a5c5-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8a5c5-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8a5c5-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8a5c5-121">Qualificatori: WmiDataId (4), puntatore</span><span class="sxs-lookup"><span data-stu-id="8a5c5-121">Qualifiers: WmiDataId(4), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="8a5c5-122">Identificatore che può essere usato per correlare le operazioni alla stessa istanza dell'oggetto file aperto tra gli eventi di creazione e chiusura di file.</span><span class="sxs-lookup"><span data-stu-id="8a5c5-122">Identifier that can be used for correlating operations to the same opened file object instance between file create and close events.</span></span>

</dd> <dt>

<span data-ttu-id="8a5c5-123">**IoFlags**</span><span class="sxs-lookup"><span data-stu-id="8a5c5-123">**IoFlags**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a5c5-124">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8a5c5-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8a5c5-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8a5c5-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8a5c5-126">Qualificatori: WmiDataId (7)</span><span class="sxs-lookup"><span data-stu-id="8a5c5-126">Qualifiers: WmiDataId(7)</span></span>
</dt> </dl>

<span data-ttu-id="8a5c5-127">I flag di pacchetti della richiesta i/o specificati per questa operazione.</span><span class="sxs-lookup"><span data-stu-id="8a5c5-127">IO request packet flags specified for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="8a5c5-128">**IoSize**</span><span class="sxs-lookup"><span data-stu-id="8a5c5-128">**IoSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a5c5-129">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8a5c5-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8a5c5-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8a5c5-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8a5c5-131">Qualificatori: WmiDataId (6)</span><span class="sxs-lookup"><span data-stu-id="8a5c5-131">Qualifiers: WmiDataId(6)</span></span>
</dt> </dl>

<span data-ttu-id="8a5c5-132">Numero di byte richiesti.</span><span class="sxs-lookup"><span data-stu-id="8a5c5-132">Number of bytes requested.</span></span>

</dd> <dt>

<span data-ttu-id="8a5c5-133">**IrpPtr**</span><span class="sxs-lookup"><span data-stu-id="8a5c5-133">**IrpPtr**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a5c5-134">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8a5c5-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8a5c5-135">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8a5c5-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8a5c5-136">Qualificatori: WmiDataId (2), puntatore</span><span class="sxs-lookup"><span data-stu-id="8a5c5-136">Qualifiers: WmiDataId(2), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="8a5c5-137">Pacchetto di richiesta IO.</span><span class="sxs-lookup"><span data-stu-id="8a5c5-137">IO request packet.</span></span> <span data-ttu-id="8a5c5-138">Questa proprietà identifica l'attività IO.</span><span class="sxs-lookup"><span data-stu-id="8a5c5-138">This property identifies the IO activity.</span></span>

</dd> <dt>

<span data-ttu-id="8a5c5-139">**Offset**</span><span class="sxs-lookup"><span data-stu-id="8a5c5-139">**Offset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a5c5-140">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="8a5c5-140">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="8a5c5-141">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8a5c5-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8a5c5-142">Qualificatori: WmiDataId (1)</span><span class="sxs-lookup"><span data-stu-id="8a5c5-142">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="8a5c5-143">Offset del file iniziale per l'operazione richiesta.</span><span class="sxs-lookup"><span data-stu-id="8a5c5-143">Starting file offset for the requested operation.</span></span>

</dd> <dt>

<span data-ttu-id="8a5c5-144">**TTID**</span><span class="sxs-lookup"><span data-stu-id="8a5c5-144">**TTID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a5c5-145">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8a5c5-145">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8a5c5-146">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8a5c5-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8a5c5-147">Qualificatori: WmiDataId (3), puntatore</span><span class="sxs-lookup"><span data-stu-id="8a5c5-147">Qualifiers: WmiDataId(3), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="8a5c5-148">Identificatore del thread che sta eseguendo l'operazione.</span><span class="sxs-lookup"><span data-stu-id="8a5c5-148">Thread identifier of the thread that is performing the operation.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8a5c5-149">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8a5c5-149">Requirements</span></span>



| <span data-ttu-id="8a5c5-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="8a5c5-150">Requirement</span></span> | <span data-ttu-id="8a5c5-151">Valore</span><span class="sxs-lookup"><span data-stu-id="8a5c5-151">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="8a5c5-152">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8a5c5-152">Minimum supported client</span></span><br/> | <span data-ttu-id="8a5c5-153">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8a5c5-153">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="8a5c5-154">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8a5c5-154">Minimum supported server</span></span><br/> | <span data-ttu-id="8a5c5-155">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="8a5c5-155">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8a5c5-156">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8a5c5-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a5c5-157">**FileIo**</span><span class="sxs-lookup"><span data-stu-id="8a5c5-157">**FileIo**</span></span>](fileio.md)
</dt> </dl>

 

 




