---
description: Rappresenta un indirizzo nella tabella file master (MFT). L'indirizzo è contrassegnato con un numero di sequenza riutilizzato circolare che viene impostato al momento della validità del riferimento del segmento MFT.
ms.assetid: 59d83b95-83fb-4630-8ce4-f58441c748ab
title: Struttura MFT_SEGMENT_REFERENCE
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MFT_SEGMENT_REFERENCE
api_type:
- NA
api_location: ''
ms.openlocfilehash: beabe7620dadd01b25b3556715b33e2f10c2c230
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104125643"
---
# <a name="mft_segment_reference-structure"></a><span data-ttu-id="e67d8-104">Struttura di riferimento del \_ segmento MFT \_</span><span class="sxs-lookup"><span data-stu-id="e67d8-104">MFT\_SEGMENT\_REFERENCE structure</span></span>

<span data-ttu-id="e67d8-105">\[Questa struttura è valida solo per la versione 3 dei volumi NTFS. potrebbe essere modificato nelle versioni future.\]</span><span class="sxs-lookup"><span data-stu-id="e67d8-105">\[This structure is valid only for version 3 of NTFS volumes; it may be altered in future versions.\]</span></span>

<span data-ttu-id="e67d8-106">Rappresenta un indirizzo nella tabella file master (MFT).</span><span class="sxs-lookup"><span data-stu-id="e67d8-106">Represents an address in the master file table (MFT).</span></span> <span data-ttu-id="e67d8-107">L'indirizzo è contrassegnato con un numero di sequenza riutilizzato circolare che viene impostato al momento della validità del riferimento del segmento MFT.</span><span class="sxs-lookup"><span data-stu-id="e67d8-107">The address is tagged with a circularly reused sequence number that is set at the time the MFT segment reference was valid.</span></span>

## <a name="syntax"></a><span data-ttu-id="e67d8-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e67d8-108">Syntax</span></span>


```C++
typedef struct _MFT_SEGMENT_REFERENCE {
  ULONG  SegmentNumberLowPart;
  USHORT SegmentNumberHighPart;
  USHORT SequenceNumber;
} MFT_SEGMENT_REFERENCE, *PMFT_SEGMENT_REFERENCE;
```



## <a name="members"></a><span data-ttu-id="e67d8-109">Members</span><span class="sxs-lookup"><span data-stu-id="e67d8-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="e67d8-110">**SegmentNumberLowPart**</span><span class="sxs-lookup"><span data-stu-id="e67d8-110">**SegmentNumberLowPart**</span></span>
</dt> <dd>

<span data-ttu-id="e67d8-111">Parte inferiore del numero di segmento.</span><span class="sxs-lookup"><span data-stu-id="e67d8-111">The low part of the segment number.</span></span>

</dd> <dt>

<span data-ttu-id="e67d8-112">**SegmentNumberHighPart**</span><span class="sxs-lookup"><span data-stu-id="e67d8-112">**SegmentNumberHighPart**</span></span>
</dt> <dd>

<span data-ttu-id="e67d8-113">Parte superiore del numero di segmento.</span><span class="sxs-lookup"><span data-stu-id="e67d8-113">The high part of the segment number.</span></span>

</dd> <dt>

<span data-ttu-id="e67d8-114">**SequenceNumber**</span><span class="sxs-lookup"><span data-stu-id="e67d8-114">**SequenceNumber**</span></span>
</dt> <dd>

<span data-ttu-id="e67d8-115">Numero di sequenza diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="e67d8-115">The nonzero sequence number.</span></span> <span data-ttu-id="e67d8-116">Il valore 0 è riservato.</span><span class="sxs-lookup"><span data-stu-id="e67d8-116">The value 0 is reserved.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e67d8-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="e67d8-117">Remarks</span></span>

<span data-ttu-id="e67d8-118">Si noti che non è presente alcun file di intestazione associato per questa struttura.</span><span class="sxs-lookup"><span data-stu-id="e67d8-118">Note that there is no associated header file for this structure.</span></span>

<span data-ttu-id="e67d8-119">Questa definizione di struttura è valida solo per la versione principale 3 e secondaria 0 o 1, come indicato [**da \_ FSCTL \_ ottenere \_ \_ i dati del volume NTFS**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data).</span><span class="sxs-lookup"><span data-stu-id="e67d8-119">This structure definition is valid only for major version 3 and minor version 0 or 1, as reported by [**FSCTL\_GET\_NTFS\_VOLUME\_DATA**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data).</span></span>

<span data-ttu-id="e67d8-120">Il tipo di dati di **\_ riferimento del file** è definito nel modo seguente.</span><span class="sxs-lookup"><span data-stu-id="e67d8-120">The **FILE\_REFERENCE** data type is defined as follows.</span></span>

``` syntax
typedef MFT_SEGMENT_REFERENCE FILE_REFERENCE, *PFILE_REFERENCE;
```

## <a name="see-also"></a><span data-ttu-id="e67d8-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e67d8-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e67d8-122">Tabella file master</span><span class="sxs-lookup"><span data-stu-id="e67d8-122">Master File Table</span></span>](master-file-table.md)
</dt> </dl>

 

 
