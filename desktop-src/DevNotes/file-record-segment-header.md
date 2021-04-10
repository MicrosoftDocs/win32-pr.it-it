---
description: Rappresenta il segmento di record del file. Si tratta dell'intestazione per ogni segmento di record di file nella tabella file master (MFT).
ms.assetid: 4548ad49-1924-4888-8966-c45f8e453c6f
title: Struttura FILE_RECORD_SEGMENT_HEADER
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FILE_RECORD_SEGMENT_HEADER
api_type:
- NA
api_location: ''
ms.openlocfilehash: 293bb14dbaee0853aa1ef293502724458e02e26f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225535"
---
# <a name="file_record_segment_header-structure"></a><span data-ttu-id="eb66c-104">\_Struttura di \_ intestazione del segmento di record di file \_</span><span class="sxs-lookup"><span data-stu-id="eb66c-104">FILE\_RECORD\_SEGMENT\_HEADER structure</span></span>

<span data-ttu-id="eb66c-105">\[Questa struttura è valida solo per la versione 3 dei volumi NTFS. potrebbe essere modificato nelle versioni future.\]</span><span class="sxs-lookup"><span data-stu-id="eb66c-105">\[This structure is valid only for version 3 of NTFS volumes; it may be altered in future versions.\]</span></span>

<span data-ttu-id="eb66c-106">Rappresenta il segmento di record del file.</span><span class="sxs-lookup"><span data-stu-id="eb66c-106">Represents the file record segment.</span></span> <span data-ttu-id="eb66c-107">Si tratta dell'intestazione per ogni segmento di record di file nella tabella file master (MFT).</span><span class="sxs-lookup"><span data-stu-id="eb66c-107">This is the header for each file record segment in the master file table (MFT).</span></span>

## <a name="syntax"></a><span data-ttu-id="eb66c-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="eb66c-108">Syntax</span></span>


```C++
typedef struct _FILE_RECORD_SEGMENT_HEADER {
  MULTI_SECTOR_HEADER   MultiSectorHeader;
  ULONGLONG             Reserved1;
  USHORT                SequenceNumber;
  USHORT                Reserved2;
  USHORT                FirstAttributeOffset;
  USHORT                Flags;
  ULONG                 Reserved3[2];
  FILE_REFERENCE        BaseFileRecordSegment;
  USHORT                Reserved4;
  UPDATE_SEQUENCE_ARRAY UpdateSequenceArray;
} FILE_RECORD_SEGMENT_HEADER, *PFILE_RECORD_SEGMENT_HEADER;
```



## <a name="members"></a><span data-ttu-id="eb66c-109">Members</span><span class="sxs-lookup"><span data-stu-id="eb66c-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="eb66c-110">**MultiSectorHeader**</span><span class="sxs-lookup"><span data-stu-id="eb66c-110">**MultiSectorHeader**</span></span>
</dt> <dd>

<span data-ttu-id="eb66c-111">Intestazione multisettore definita dal gestore della cache.</span><span class="sxs-lookup"><span data-stu-id="eb66c-111">The multisector header defined by the cache manager.</span></span> <span data-ttu-id="eb66c-112">La struttura dell' [**\_ \_ intestazione multisettore**](multi-sector-header.md) contiene sempre la firma "file" e una descrizione della posizione e della dimensione della matrice di sequenza di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="eb66c-112">The [**MULTI\_SECTOR\_HEADER**](multi-sector-header.md) structure always contains the signature "FILE" and a description of the location and size of the update sequence array.</span></span>

</dd> <dt>

<span data-ttu-id="eb66c-113">**Reserved1**</span><span class="sxs-lookup"><span data-stu-id="eb66c-113">**Reserved1**</span></span>
</dt> <dd>

<span data-ttu-id="eb66c-114">Riservato.</span><span class="sxs-lookup"><span data-stu-id="eb66c-114">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="eb66c-115">**SequenceNumber**</span><span class="sxs-lookup"><span data-stu-id="eb66c-115">**SequenceNumber**</span></span>
</dt> <dd>

<span data-ttu-id="eb66c-116">Numero di sequenza.</span><span class="sxs-lookup"><span data-stu-id="eb66c-116">The sequence number.</span></span> <span data-ttu-id="eb66c-117">Questo valore viene incrementato ogni volta che viene liberato un segmento di record di file; è 0 se il segmento non viene utilizzato.</span><span class="sxs-lookup"><span data-stu-id="eb66c-117">This value is incremented each time that a file record segment is freed; it is 0 if the segment is not used.</span></span> <span data-ttu-id="eb66c-118">Il campo **SequenceNumber** di un riferimento a file deve corrispondere al contenuto di questo campo; Se non corrispondono, il riferimento al file è errato e probabilmente obsoleto.</span><span class="sxs-lookup"><span data-stu-id="eb66c-118">The **SequenceNumber** field of a file reference must match the contents of this field; if they do not match, the file reference is incorrect and probably obsolete.</span></span>

</dd> <dt>

<span data-ttu-id="eb66c-119">**Reserved2**</span><span class="sxs-lookup"><span data-stu-id="eb66c-119">**Reserved2**</span></span>
</dt> <dd>

<span data-ttu-id="eb66c-120">Riservato.</span><span class="sxs-lookup"><span data-stu-id="eb66c-120">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="eb66c-121">**FirstAttributeOffset**</span><span class="sxs-lookup"><span data-stu-id="eb66c-121">**FirstAttributeOffset**</span></span>
</dt> <dd>

<span data-ttu-id="eb66c-122">Offset del primo record di attributo, espresso in byte.</span><span class="sxs-lookup"><span data-stu-id="eb66c-122">The offset of the first attribute record, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="eb66c-123">**Flag**</span><span class="sxs-lookup"><span data-stu-id="eb66c-123">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="eb66c-124">Flag del file.</span><span class="sxs-lookup"><span data-stu-id="eb66c-124">The file flags.</span></span>

<dl> <dt>

<span data-ttu-id="eb66c-125"><span id="FILE_RECORD_SEGMENT_IN_USE"></span><span id="file_record_segment_in_use"></span>**File \_ \_Segmento \_ di record in \_ uso** (0x0001)</span><span class="sxs-lookup"><span data-stu-id="eb66c-125"><span id="FILE_RECORD_SEGMENT_IN_USE"></span><span id="file_record_segment_in_use"></span>**FILE\_RECORD\_SEGMENT\_IN\_USE** (0x0001)</span></span>
</dt> <dt>

<span data-ttu-id="eb66c-126"><span id="FILE_FILE_NAME_INDEX_PRESENT"></span><span id="file_file_name_index_present"></span>**File \_ \_Indice nome \_ file \_ presente** (0x0002)</span><span class="sxs-lookup"><span data-stu-id="eb66c-126"><span id="FILE_FILE_NAME_INDEX_PRESENT"></span><span id="file_file_name_index_present"></span>**FILE\_FILE\_NAME\_INDEX\_PRESENT** (0x0002)</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="eb66c-127">**Reserved3**</span><span class="sxs-lookup"><span data-stu-id="eb66c-127">**Reserved3**</span></span>
</dt> <dd>

<span data-ttu-id="eb66c-128">Riservato.</span><span class="sxs-lookup"><span data-stu-id="eb66c-128">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="eb66c-129">**BaseFileRecordSegment**</span><span class="sxs-lookup"><span data-stu-id="eb66c-129">**BaseFileRecordSegment**</span></span>
</dt> <dd>

<span data-ttu-id="eb66c-130">Un riferimento di file al segmento di record del file di base per il file.</span><span class="sxs-lookup"><span data-stu-id="eb66c-130">A file reference to the base file record segment for this file.</span></span> <span data-ttu-id="eb66c-131">Se si tratta del record del file di base, il valore è 0.</span><span class="sxs-lookup"><span data-stu-id="eb66c-131">If this is the base file record, the value is 0.</span></span> <span data-ttu-id="eb66c-132">Vedere informazioni di [**\_ \_ riferimento sul segmento MFT**](mft-segment-reference.md).</span><span class="sxs-lookup"><span data-stu-id="eb66c-132">See [**MFT\_SEGMENT\_REFERENCE**](mft-segment-reference.md).</span></span>

</dd> <dt>

<span data-ttu-id="eb66c-133">**Reserved4**</span><span class="sxs-lookup"><span data-stu-id="eb66c-133">**Reserved4**</span></span>
</dt> <dd>

<span data-ttu-id="eb66c-134">Riservato.</span><span class="sxs-lookup"><span data-stu-id="eb66c-134">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="eb66c-135">**UpdateSequenceArray**</span><span class="sxs-lookup"><span data-stu-id="eb66c-135">**UpdateSequenceArray**</span></span>
</dt> <dd>

<span data-ttu-id="eb66c-136">Matrice di sequenza di aggiornamento per proteggere i trasferimenti multisettore del segmento di record di file.</span><span class="sxs-lookup"><span data-stu-id="eb66c-136">The update sequence array to protect multisector transfers of the file record segment.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="eb66c-137">Commenti</span><span class="sxs-lookup"><span data-stu-id="eb66c-137">Remarks</span></span>

<span data-ttu-id="eb66c-138">Si noti che non è presente alcun file di intestazione associato per questa struttura.</span><span class="sxs-lookup"><span data-stu-id="eb66c-138">Note that there is no associated header file for this structure.</span></span>

<span data-ttu-id="eb66c-139">Questa definizione di struttura è valida solo per la versione principale 3 e secondaria 0 o 1, come indicato [**da \_ FSCTL \_ ottenere \_ \_ i dati del volume NTFS**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data).</span><span class="sxs-lookup"><span data-stu-id="eb66c-139">This structure definition is valid only for major version 3 and minor version 0 or 1, as reported by [**FSCTL\_GET\_NTFS\_VOLUME\_DATA**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data).</span></span>

## <a name="see-also"></a><span data-ttu-id="eb66c-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="eb66c-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb66c-141">Tabella file master</span><span class="sxs-lookup"><span data-stu-id="eb66c-141">Master File Table</span></span>](master-file-table.md)
</dt> </dl>

 

 
