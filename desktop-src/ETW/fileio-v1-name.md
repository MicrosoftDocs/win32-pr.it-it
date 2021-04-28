---
description: 'FileIo_V1_Name classe: questa classe è la classe del tipo di evento per gli eventi di I/O di file. La sintassi seguente è semplificata dal codice MOF.'
ms.assetid: a4ee38df-af75-4aec-89ec-5a1c39302c82
title: FileIo_V1_Name classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FileIo_V1_Name
- FileIo_V1_Name.FileObject
- FileIo_V1_Name.FileName
api_type:
- NA
api_location: ''
ms.openlocfilehash: 62069f8a462499dfbfd9cfa368b9f5985d4775e0
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108106549"
---
# <a name="fileio_v1_name-class"></a><span data-ttu-id="fee08-104">Classe FileIo \_ V1 \_ Name</span><span class="sxs-lookup"><span data-stu-id="fee08-104">FileIo\_V1\_Name class</span></span>

<span data-ttu-id="fee08-105">Questa classe è la classe del tipo di evento per gli eventi di I/O di file.</span><span class="sxs-lookup"><span data-stu-id="fee08-105">This class is the event type class for file I/O events.</span></span>

<span data-ttu-id="fee08-106">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="fee08-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="fee08-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fee08-107">Syntax</span></span>

``` syntax
[EventType{0, 32}, EventTypeName{"Name", "FileCreate"}]
class FileIo_V1_Name : FileIo
{
  uint32 FileObject;
  string FileName;
};
```

## <a name="members"></a><span data-ttu-id="fee08-108">Members</span><span class="sxs-lookup"><span data-stu-id="fee08-108">Members</span></span>

<span data-ttu-id="fee08-109">La **classe FileIo \_ V1 \_ Name** ha questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="fee08-109">The **FileIo\_V1\_Name** class has these types of members:</span></span>

-   [<span data-ttu-id="fee08-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="fee08-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fee08-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="fee08-111">Properties</span></span>

<span data-ttu-id="fee08-112">La **classe FileIo \_ V1 \_ Name** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="fee08-112">The **FileIo\_V1\_Name** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="fee08-113">FileName</span><span class="sxs-lookup"><span data-stu-id="fee08-113">FileName</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fee08-114">Tipo di dati: **stringa**</span><span class="sxs-lookup"><span data-stu-id="fee08-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fee08-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fee08-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fee08-116">Qualificatori: WmiDataId(2), StringTermination("NullTerminated"), Format("w")</span><span class="sxs-lookup"><span data-stu-id="fee08-116">Qualifiers: WmiDataId(2), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="fee08-117">Percorso completo del file, senza includere la lettera di unità.</span><span class="sxs-lookup"><span data-stu-id="fee08-117">Full path to the file, not including the drive letter.</span></span>

</dd> <dt>

<span data-ttu-id="fee08-118">Oggetto FileObject</span><span class="sxs-lookup"><span data-stu-id="fee08-118">FileObject</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fee08-119">Tipo di dati: **uint32**</span><span class="sxs-lookup"><span data-stu-id="fee08-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fee08-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fee08-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fee08-121">Qualificatori: WmiDataId(1), Pointer</span><span class="sxs-lookup"><span data-stu-id="fee08-121">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="fee08-122">Trovare la corrispondenza tra il valore di questo puntatore e il valore del puntatore **FileObject** in un evento [**DiskIo \_ TypeGroup1**](diskio-typegroup1.md) per determinare il tipo di operazione di I/O.</span><span class="sxs-lookup"><span data-stu-id="fee08-122">Match the value of this pointer to the **FileObject** pointer value in a [**DiskIo\_TypeGroup1**](diskio-typegroup1.md) event to determine the type of I/O operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fee08-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="fee08-123">Remarks</span></span>

<span data-ttu-id="fee08-124">**Windows Server 2003:** Per recuperare la lettera di unità per il percorso del nome file, usare il valore della proprietà **FileObject** per eseguire il mapping all'evento [ \_ DiskIo TypeGroup1](diskio-typegroup1.md) corrispondente.</span><span class="sxs-lookup"><span data-stu-id="fee08-124">**Windows Server 2003:** To retrieve the drive letter for the file name path, use the **FileObject** property value to map to the corresponding [DiskIo\_TypeGroup1](diskio-typegroup1.md) event.</span></span> <span data-ttu-id="fee08-125">Dall'evento DiskIo TypeGroup1 usare i valori delle proprietà DiskNumber e ByteOffset per eseguire il mapping all'evento \_ [SystemConfig \_ LogDisk](systemconfig-logdisk.md)  corrispondente (**ByteOffset** esegue il mapping **a StartOffset**). </span><span class="sxs-lookup"><span data-stu-id="fee08-125">From the DiskIo\_TypeGroup1 event, use the **DiskNumber** and **ByteOffset** property values to map to the corresponding [SystemConfig\_LogDisk](systemconfig-logdisk.md) event (**ByteOffset** maps to **StartOffset**).</span></span> <span data-ttu-id="fee08-126">La **proprietà DriveLetterString** contiene la lettera di unità.</span><span class="sxs-lookup"><span data-stu-id="fee08-126">The **DriveLetterString** property contains the drive letter.</span></span>

## <a name="requirements"></a><span data-ttu-id="fee08-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fee08-127">Requirements</span></span>



| <span data-ttu-id="fee08-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="fee08-128">Requirement</span></span> | <span data-ttu-id="fee08-129">Valore</span><span class="sxs-lookup"><span data-stu-id="fee08-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="fee08-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fee08-130">Minimum supported client</span></span><br/> | <span data-ttu-id="fee08-131">Solo app desktop di Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="fee08-131">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="fee08-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fee08-132">Minimum supported server</span></span><br/> | <span data-ttu-id="fee08-133">Solo app desktop di Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="fee08-133">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="fee08-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fee08-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fee08-135">**Fileio**</span><span class="sxs-lookup"><span data-stu-id="fee08-135">**FileIo**</span></span>](fileio.md)
</dt> </dl>

 

 




