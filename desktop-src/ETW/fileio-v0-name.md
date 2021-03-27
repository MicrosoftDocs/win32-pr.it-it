---
description: La classe del nome FileIO \_ V0 \_ è una versione precedente della classe del tipo di evento per gli eventi di I/O di file. La sintassi seguente è semplificata dal codice MOF.
ms.assetid: dcbe37f2-6df0-41a5-b85f-dcd06cbd5901
title: Classe FileIo_V0_Name
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FileIo_V0_Name
- FileIo_V0_Name.FileObject
- FileIo_V0_Name.FileName
api_type:
- NA
api_location: ''
ms.openlocfilehash: 6e88d1b9b5b36815b1a833062c30e804e4db744a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758426"
---
# <a name="fileio_v0_name-class"></a><span data-ttu-id="ef48d-104">FileIO \_ V0 \_ nome classe</span><span class="sxs-lookup"><span data-stu-id="ef48d-104">FileIo\_V0\_Name class</span></span>

<span data-ttu-id="ef48d-105">La classe del **\_ \_ nome FileIO V0** è una versione precedente della classe del tipo di evento per gli eventi di I/O di file.</span><span class="sxs-lookup"><span data-stu-id="ef48d-105">The **FileIo\_V0\_Name** class is an older version of the event type class for file I/O events.</span></span>

<span data-ttu-id="ef48d-106">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="ef48d-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef48d-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ef48d-107">Syntax</span></span>

``` syntax
[EventType(0), EventTypeName("Name")]
class FileIo_V0_Name : FileIo_V0
{
  uint32 FileObject;
  string FileName;
};
```

## <a name="members"></a><span data-ttu-id="ef48d-108">Members</span><span class="sxs-lookup"><span data-stu-id="ef48d-108">Members</span></span>

<span data-ttu-id="ef48d-109">I tipi di membri della classe del **\_ \_ nome di FileIO V0** sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="ef48d-109">The **FileIo\_V0\_Name** class has these types of members:</span></span>

-   [<span data-ttu-id="ef48d-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ef48d-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ef48d-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ef48d-111">Properties</span></span>

<span data-ttu-id="ef48d-112">La classe del **\_ \_ nome FileIO V0** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="ef48d-112">The **FileIo\_V0\_Name** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ef48d-113">FileName</span><span class="sxs-lookup"><span data-stu-id="ef48d-113">FileName</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef48d-114">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ef48d-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ef48d-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ef48d-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef48d-116">Qualificatori: WmiDataId (2), StringTermination ("NullTerminated"), Format ("w")</span><span class="sxs-lookup"><span data-stu-id="ef48d-116">Qualifiers: WmiDataId(2), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="ef48d-117">Percorso completo del file, esclusa la lettera di unità.</span><span class="sxs-lookup"><span data-stu-id="ef48d-117">Full path to the file, not including the drive letter.</span></span>

</dd> <dt>

<span data-ttu-id="ef48d-118">FileObject</span><span class="sxs-lookup"><span data-stu-id="ef48d-118">FileObject</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef48d-119">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ef48d-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ef48d-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ef48d-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef48d-121">Qualificatori: WmiDataId (1), puntatore</span><span class="sxs-lookup"><span data-stu-id="ef48d-121">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="ef48d-122">Corrisponde al valore di questo puntatore al valore del puntatore **FileObject** in un evento [**DiskIo \_ TypeGroup1**](diskio-typegroup1.md) per determinare il tipo di operazione di i/O.</span><span class="sxs-lookup"><span data-stu-id="ef48d-122">Match the value of this pointer to the **FileObject** pointer value in a [**DiskIo\_TypeGroup1**](diskio-typegroup1.md) event to determine the type of I/O operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ef48d-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="ef48d-123">Remarks</span></span>

<span data-ttu-id="ef48d-124">**Windows Server 2003:** Per recuperare la lettera di unità per il percorso del nome file, usare il valore della proprietà **FileObject** per eseguire il mapping all'evento [**DiskIo \_ TypeGroup1**](diskio-typegroup1.md) corrispondente.</span><span class="sxs-lookup"><span data-stu-id="ef48d-124">**Windows Server 2003:** To retrieve the drive letter for the file name path, use the **FileObject** property value to map to the corresponding [**DiskIo\_TypeGroup1**](diskio-typegroup1.md) event.</span></span> <span data-ttu-id="ef48d-125">Dall'evento **DiskIo \_ TypeGroup1** usare i valori della proprietà **numerodisco** e **ByteOffset** per eseguire il mapping all'evento [**SystemConfig \_**](systemconfig-logdisk.md) LogDisk corrispondente.</span><span class="sxs-lookup"><span data-stu-id="ef48d-125">From the **DiskIo\_TypeGroup1** event, use the **DiskNumber** and **ByteOffset** property values to map to the corresponding [**SystemConfig\_LogDisk**](systemconfig-logdisk.md) event.</span></span> <span data-ttu-id="ef48d-126">La proprietà **DriveLetterString** contiene la lettera di unità.</span><span class="sxs-lookup"><span data-stu-id="ef48d-126">The **DriveLetterString** property contains the drive letter.</span></span>

## <a name="requirements"></a><span data-ttu-id="ef48d-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ef48d-127">Requirements</span></span>



| <span data-ttu-id="ef48d-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="ef48d-128">Requirement</span></span> | <span data-ttu-id="ef48d-129">Valore</span><span class="sxs-lookup"><span data-stu-id="ef48d-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="ef48d-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ef48d-130">Minimum supported client</span></span><br/> | <span data-ttu-id="ef48d-131">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="ef48d-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="ef48d-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ef48d-132">Minimum supported server</span></span><br/> | <span data-ttu-id="ef48d-133">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="ef48d-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="ef48d-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ef48d-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef48d-135">**FileIO \_ V0**</span><span class="sxs-lookup"><span data-stu-id="ef48d-135">**FileIo\_V0**</span></span>](fileio-v0.md)
</dt> </dl>

 

 




