---
description: Questa classe è la classe del tipo di evento per gli eventi di I/O di file. La sintassi seguente è semplificata dal codice MOF.
ms.assetid: ed72daa3-06c0-46f1-bb9d-c0b343228f28
title: Classe FileIo_Name
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FileIo_Name
- FileIo_Name.FileObject
- FileIo_Name.FileName
api_type:
- NA
api_location: ''
ms.openlocfilehash: a25c96a8a3db11f577e7780d9f12448a8a0039dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977519"
---
# <a name="fileio_name-class"></a><span data-ttu-id="32790-104">\_Classe nome FileIO</span><span class="sxs-lookup"><span data-stu-id="32790-104">FileIo\_Name class</span></span>

<span data-ttu-id="32790-105">Questa classe è la classe del tipo di evento per gli eventi di I/O di file.</span><span class="sxs-lookup"><span data-stu-id="32790-105">This class is the event type class for file I/O events.</span></span>

<span data-ttu-id="32790-106">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="32790-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="32790-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="32790-107">Syntax</span></span>

``` syntax
[EventType{0, 32, 35, 36}, EventTypeName{"Name", "FileCreate", "FileDelete", "FileRundown"}]
class FileIo_Name : FileIo
{
  uint32 FileObject;
  string FileName;
};
```

## <a name="members"></a><span data-ttu-id="32790-108">Members</span><span class="sxs-lookup"><span data-stu-id="32790-108">Members</span></span>

<span data-ttu-id="32790-109">La classe del **\_ nome FileIO** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="32790-109">The **FileIo\_Name** class has these types of members:</span></span>

-   [<span data-ttu-id="32790-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="32790-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="32790-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="32790-111">Properties</span></span>

<span data-ttu-id="32790-112">La classe del **\_ nome FileIO** presenta queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="32790-112">The **FileIo\_Name** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="32790-113">FileName</span><span class="sxs-lookup"><span data-stu-id="32790-113">FileName</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32790-114">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="32790-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="32790-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="32790-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="32790-116">Qualificatori: WmiDataId (2), StringTermination ("NullTerminated"), Format ("w")</span><span class="sxs-lookup"><span data-stu-id="32790-116">Qualifiers: WmiDataId(2), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="32790-117">Percorso completo del file, esclusa la lettera di unità.</span><span class="sxs-lookup"><span data-stu-id="32790-117">Full path to the file, not including the drive letter.</span></span>

</dd> <dt>

<span data-ttu-id="32790-118">FileObject</span><span class="sxs-lookup"><span data-stu-id="32790-118">FileObject</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32790-119">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="32790-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="32790-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="32790-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="32790-121">Qualificatori: WmiDataId (1), puntatore</span><span class="sxs-lookup"><span data-stu-id="32790-121">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="32790-122">Corrisponde al valore di questo puntatore al valore del puntatore **FileObject** in un evento [**DiskIo \_ TypeGroup1**](diskio-typegroup1.md) per determinare il tipo di operazione di i/O.</span><span class="sxs-lookup"><span data-stu-id="32790-122">Match the value of this pointer to the **FileObject** pointer value in a [**DiskIo\_TypeGroup1**](diskio-typegroup1.md) event to determine the type of I/O operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="32790-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="32790-123">Remarks</span></span>

<span data-ttu-id="32790-124">**Windows Server 2003:** Per recuperare la lettera di unità per il percorso del nome file, usare il valore della proprietà **FileObject** per eseguire il mapping all'evento [DiskIo \_ TypeGroup1](diskio-typegroup1.md) corrispondente.</span><span class="sxs-lookup"><span data-stu-id="32790-124">**Windows Server 2003:** To retrieve the drive letter for the file name path, use the **FileObject** property value to map to the corresponding [DiskIo\_TypeGroup1](diskio-typegroup1.md) event.</span></span> <span data-ttu-id="32790-125">Dall' \_ evento TypeGroup1 di DiskIo, usare i valori della proprietà **numerodisco** e **ByteOffset** per eseguire il mapping all'evento [SystemConfig LogDisk \_](systemconfig-logdisk.md) corrispondente (**ByteOffset** viene mappato a **startOffset**).</span><span class="sxs-lookup"><span data-stu-id="32790-125">From the DiskIo\_TypeGroup1 event, use the **DiskNumber** and **ByteOffset** property values to map to the corresponding [SystemConfig\_LogDisk](systemconfig-logdisk.md) event (**ByteOffset** maps to **StartOffset**).</span></span> <span data-ttu-id="32790-126">La proprietà **DriveLetterString** contiene la lettera di unità.</span><span class="sxs-lookup"><span data-stu-id="32790-126">The **DriveLetterString** property contains the drive letter.</span></span>

## <a name="requirements"></a><span data-ttu-id="32790-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="32790-127">Requirements</span></span>



| <span data-ttu-id="32790-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="32790-128">Requirement</span></span> | <span data-ttu-id="32790-129">Valore</span><span class="sxs-lookup"><span data-stu-id="32790-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="32790-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="32790-130">Minimum supported client</span></span><br/> | <span data-ttu-id="32790-131">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="32790-131">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="32790-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="32790-132">Minimum supported server</span></span><br/> | <span data-ttu-id="32790-133">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="32790-133">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="32790-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="32790-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32790-135">**FileIo**</span><span class="sxs-lookup"><span data-stu-id="32790-135">**FileIo**</span></span>](fileio.md)
</dt> </dl>

 

 




