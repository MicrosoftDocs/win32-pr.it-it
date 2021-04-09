---
description: Contiene le informazioni sul riconoscimento file system su disco archiviate nel settore di avvio dei volumi (zero del settore del disco logico).
ms.assetid: d9c19e01-ff82-4bbc-9eb6-aac9dc5c34ac
title: Struttura FILE_SYSTEM_RECOGNITION_STRUCTURE
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FILE_SYSTEM_RECOGNITION_STRUCTURE
api_type:
- NA
api_location: ''
ms.openlocfilehash: c542b2b9ee1cd1696c7c95797c7df20aa02180cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049777"
---
# <a name="file_system_recognition_structure-structure"></a><span data-ttu-id="551a2-103">\_Struttura della \_ struttura di riconoscimento del file System \_</span><span class="sxs-lookup"><span data-stu-id="551a2-103">FILE\_SYSTEM\_RECOGNITION\_STRUCTURE structure</span></span>

<span data-ttu-id="551a2-104">Contiene le informazioni sul riconoscimento file system su disco archiviate nel settore di avvio del volume (zero del settore del disco logico).</span><span class="sxs-lookup"><span data-stu-id="551a2-104">Contains the on-disk file system recognition information stored in the volume's boot sector (logical disk sector zero).</span></span>

<span data-ttu-id="551a2-105">Si tratta di una struttura di dati definita internamente non disponibile in un'intestazione pubblica e viene fornita qui per file system sviluppatori che desiderano sfruttare file system il riconoscimento.</span><span class="sxs-lookup"><span data-stu-id="551a2-105">This is an internally-defined data structure not available in a public header and is provided here for file system developers who want to take advantage of file system recognition.</span></span> <span data-ttu-id="551a2-106">Per ulteriori informazioni, vedere [riconoscimento del file System](file-system-recognition.md).</span><span class="sxs-lookup"><span data-stu-id="551a2-106">For more information, see [File System Recognition](file-system-recognition.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="551a2-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="551a2-107">Syntax</span></span>


```C++
typedef struct _FILE_SYSTEM_RECOGNITION_STRUCTURE {
  UCHAR  Jmp[3];
  UCHAR  FsName[8];
  UCHAR  MustBeZero[5];
  ULONG  Identifier;
  USHORT Length;
  USHORT Checksum;
} FILE_SYSTEM_RECOGNITION_STRUCTURE;
```



## <a name="members"></a><span data-ttu-id="551a2-108">Members</span><span class="sxs-lookup"><span data-stu-id="551a2-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="551a2-109">**JMP**</span><span class="sxs-lookup"><span data-stu-id="551a2-109">**Jmp**</span></span>
</dt> <dd>

<span data-ttu-id="551a2-110">Istruzione JMP.</span><span class="sxs-lookup"><span data-stu-id="551a2-110">The JMP instruction.</span></span> <span data-ttu-id="551a2-111">Questo membro dati non è incluso nel valore contenuto nel membro dati di **checksum** .</span><span class="sxs-lookup"><span data-stu-id="551a2-111">This data member is not included in the value contained in the **Checksum** data member.</span></span>

</dd> <dt>

<span data-ttu-id="551a2-112">**FsName**</span><span class="sxs-lookup"><span data-stu-id="551a2-112">**FsName**</span></span>
</dt> <dd>

<span data-ttu-id="551a2-113">Nome del file system.</span><span class="sxs-lookup"><span data-stu-id="551a2-113">The file system name.</span></span> <span data-ttu-id="551a2-114">Si tratta di una sequenza di 8 caratteri ASCII che rappresenta il nome leggibile non localizzabile del file system in cui è formattato il volume.</span><span class="sxs-lookup"><span data-stu-id="551a2-114">This is a sequence of 8 ASCII characters that represents the nonlocalizable human-readable name of the file system the volume is formatted with.</span></span>

<span data-ttu-id="551a2-115">Questa stringa si trova nella stessa posizione del nome del file system OEM su un disco con una normale struttura del blocco di parametri BIOS (BPB).</span><span class="sxs-lookup"><span data-stu-id="551a2-115">This string is in the same place as the OEM file system name on a disk with a normal BIOS parameter block (BPB) structure.</span></span>

</dd> <dt>

<span data-ttu-id="551a2-116">**MustBeZero**</span><span class="sxs-lookup"><span data-stu-id="551a2-116">**MustBeZero**</span></span>
</dt> <dd>

<span data-ttu-id="551a2-117">Spazio riservato che contiene tutti gli zeri.</span><span class="sxs-lookup"><span data-stu-id="551a2-117">Reserved space that contains all zeros.</span></span>

<span data-ttu-id="551a2-118">Questo membro dati si sovrappone a quanto normalmente sono i membri dati seguenti in un BPB:</span><span class="sxs-lookup"><span data-stu-id="551a2-118">This data member overlaps what normally are the following data members in a BPB:</span></span>

-   <span data-ttu-id="551a2-119">**BytesPerSector**</span><span class="sxs-lookup"><span data-stu-id="551a2-119">**BytesPerSector**</span></span>
-   <span data-ttu-id="551a2-120">**SectorsPerCluster**</span><span class="sxs-lookup"><span data-stu-id="551a2-120">**SectorsPerCluster**</span></span>
-   <span data-ttu-id="551a2-121">**ReservedSectorCount**</span><span class="sxs-lookup"><span data-stu-id="551a2-121">**ReservedSectorCount**</span></span>

<span data-ttu-id="551a2-122">Poiché questi membri dati sono impostati su zero, questo dovrebbe essere sufficiente per fare in modo che gli OSs precedenti concludano che non si tratta di un BPB valido e pertanto riconoscono il volume.</span><span class="sxs-lookup"><span data-stu-id="551a2-122">Because these data members are set to zero, this should be sufficient to cause earlier OSs to conclude that this is not a valid BPB and therefore recognize the volume.</span></span>

</dd> <dt>

<span data-ttu-id="551a2-123">**Identificatore**</span><span class="sxs-lookup"><span data-stu-id="551a2-123">**Identifier**</span></span>
</dt> <dd>

<span data-ttu-id="551a2-124">Identificatore della struttura.</span><span class="sxs-lookup"><span data-stu-id="551a2-124">A structure identifier.</span></span> <span data-ttu-id="551a2-125">Deve contenere il valore 0x53525346 disposto in ordine dei byte little-endian.</span><span class="sxs-lookup"><span data-stu-id="551a2-125">Must contain the value 0x53525346 arranged in little-endian byte order.</span></span>

<span data-ttu-id="551a2-126">A questo punto della struttura, i dati sono allineati a 16 byte.</span><span class="sxs-lookup"><span data-stu-id="551a2-126">At this point in the structure, the data is aligned to 16 bytes.</span></span>

</dd> <dt>

<span data-ttu-id="551a2-127">**Length**</span><span class="sxs-lookup"><span data-stu-id="551a2-127">**Length**</span></span>
</dt> <dd>

<span data-ttu-id="551a2-128">Numero di byte in questa struttura, dall'inizio alla fine, incluso il membro dati **JMP** .</span><span class="sxs-lookup"><span data-stu-id="551a2-128">The number of bytes in this structure, from the beginning to the end, including the **Jmp** data member.</span></span>

</dd> <dt>

<span data-ttu-id="551a2-129">**Checksum**</span><span class="sxs-lookup"><span data-stu-id="551a2-129">**Checksum**</span></span>
</dt> <dd>

<span data-ttu-id="551a2-130">Checksum a due byte calcolato sui byte a partire dal membro dati **FsName** e terminando con l'ultimo byte di questa struttura, esclusi i membri dati **JMP** e **checksum** .</span><span class="sxs-lookup"><span data-stu-id="551a2-130">A two-byte checksum calculated over the bytes starting at the **FsName** data member and ending at the last byte of this structure, excluding the **Jmp** and **Checksum** data members.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="551a2-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="551a2-131">Requirements</span></span>



| <span data-ttu-id="551a2-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="551a2-132">Requirement</span></span> | <span data-ttu-id="551a2-133">Valore</span><span class="sxs-lookup"><span data-stu-id="551a2-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="551a2-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="551a2-134">Minimum supported client</span></span><br/> | <span data-ttu-id="551a2-135">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="551a2-135">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="551a2-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="551a2-136">Minimum supported server</span></span><br/> | <span data-ttu-id="551a2-137">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="551a2-137">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="551a2-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="551a2-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="551a2-139">Calcolo di un checksum di riconoscimento del file System</span><span class="sxs-lookup"><span data-stu-id="551a2-139">Computing a File System Recognition Checksum</span></span>](computing-a-file-system-recognition-checksum.md)
</dt> <dt>

[<span data-ttu-id="551a2-140">Riconoscimento del file System</span><span class="sxs-lookup"><span data-stu-id="551a2-140">File System Recognition</span></span>](file-system-recognition.md)
</dt> <dt>

[<span data-ttu-id="551a2-141">**\_ \_ informazioni sul riconoscimento del file System \_**</span><span class="sxs-lookup"><span data-stu-id="551a2-141">**FILE\_SYSTEM\_RECOGNITION\_INFORMATION**</span></span>](/windows/desktop/api/WinIoCtl/ns-winioctl-file_system_recognition_information)
</dt> <dt>

[<span data-ttu-id="551a2-142">**\_riconoscimento del \_ file \_ System di query \_ FSCTL**</span><span class="sxs-lookup"><span data-stu-id="551a2-142">**FSCTL\_QUERY\_FILE\_SYSTEM\_RECOGNITION**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_query_file_system_recognition)
</dt> </dl>

 

