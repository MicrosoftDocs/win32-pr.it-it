---
title: Struttura CHANGE_LOG_HEADER
description: Intestazione del log delle modifiche.
ms.assetid: 24fee9a5-b073-474f-afd5-d81f66399936
keywords:
- Ripristino del sistema della struttura CHANGE_LOG_HEADER
- Ripristino del sistema del puntatore della struttura PCHANGE_LOG_HEADER
topic_type:
- apiref
api_name:
- CHANGE_LOG_HEADER
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5512ff9c9e708095f38e3ae1dcf80ce2e0e4443b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400292"
---
# <a name="change_log_header-structure"></a><span data-ttu-id="567cd-105">MODIFICARE \_ la \_ struttura dell'intestazione del log</span><span class="sxs-lookup"><span data-stu-id="567cd-105">CHANGE\_LOG\_HEADER structure</span></span>

<span data-ttu-id="567cd-106">\[Queste informazioni si applicano solo a Windows XP con Service Pack 2 (SP2).\]</span><span class="sxs-lookup"><span data-stu-id="567cd-106">\[This information applies only to Windows XP with Service Pack 2 (SP2).\]</span></span>

<span data-ttu-id="567cd-107">Intestazione del log delle modifiche.</span><span class="sxs-lookup"><span data-stu-id="567cd-107">The change log header.</span></span>

## <a name="syntax"></a><span data-ttu-id="567cd-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="567cd-108">Syntax</span></span>


```C++
typedef struct _CHANGE_LOG_HEADER {
  RECORD_HEADER RecordHeader;
  DWORD         dwMagicNum;
  DWORD         dwLogVersion;
  RECORD_HEADER DataHeader;
  BYTE          byteData[1];
} CHANGE_LOG_HEADER, *PCHANGE_LOG_HEADER;
```



## <a name="members"></a><span data-ttu-id="567cd-109">Members</span><span class="sxs-lookup"><span data-stu-id="567cd-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="567cd-110">**RecordHeader**</span><span class="sxs-lookup"><span data-stu-id="567cd-110">**RecordHeader**</span></span>
</dt> <dd>

<span data-ttu-id="567cd-111">Struttura [**di \_ intestazione**](record-header.md) di un record.</span><span class="sxs-lookup"><span data-stu-id="567cd-111">A [**RECORD\_HEADER**](record-header.md) structure.</span></span> <span data-ttu-id="567cd-112">Il membro **dwRecordType** deve essere impostato su RecordTypeLogHeader (0).</span><span class="sxs-lookup"><span data-stu-id="567cd-112">The **dwRecordType** member should be set to RecordTypeLogHeader (0).</span></span> <span data-ttu-id="567cd-113">Il membro **dwRecordSize** deve tenere conto di tutti i membri, più il valore **DWORD** aggiuntivo che segue questa intestazione.</span><span class="sxs-lookup"><span data-stu-id="567cd-113">The **dwRecordSize** member should account for all the members, plus the extra **DWORD** value that follows this header.</span></span> <span data-ttu-id="567cd-114">Per altre informazioni, vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="567cd-114">For more information, see Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="567cd-115">**dwMagicNum**</span><span class="sxs-lookup"><span data-stu-id="567cd-115">**dwMagicNum**</span></span>
</dt> <dd>

<span data-ttu-id="567cd-116">Questo membro deve essere impostato su 0xabcdef12.</span><span class="sxs-lookup"><span data-stu-id="567cd-116">This member should be set to 0xabcdef12.</span></span>

</dd> <dt>

<span data-ttu-id="567cd-117">**dwLogVersion**</span><span class="sxs-lookup"><span data-stu-id="567cd-117">**dwLogVersion**</span></span>
</dt> <dd>

<span data-ttu-id="567cd-118">Questo membro deve essere impostato su 2.</span><span class="sxs-lookup"><span data-stu-id="567cd-118">This member should be set to 2.</span></span>

</dd> <dt>

<span data-ttu-id="567cd-119">**Dataheader**</span><span class="sxs-lookup"><span data-stu-id="567cd-119">**DataHeader**</span></span>
</dt> <dd>

<span data-ttu-id="567cd-120">Struttura [**di \_ intestazione**](record-header.md) di un record.</span><span class="sxs-lookup"><span data-stu-id="567cd-120">A [**RECORD\_HEADER**](record-header.md) structure.</span></span> <span data-ttu-id="567cd-121">Il membro **dwRecordType** deve essere impostato su **RecordTypeVolumePath** (2).</span><span class="sxs-lookup"><span data-stu-id="567cd-121">The **dwRecordType** member should be set to **RecordTypeVolumePath** (2).</span></span>

</dd> <dt>

<span data-ttu-id="567cd-122">**byteData**</span><span class="sxs-lookup"><span data-stu-id="567cd-122">**byteData**</span></span>
</dt> <dd>

<span data-ttu-id="567cd-123">Inizio di una stringa con terminazione null che specifica il percorso del volume.</span><span class="sxs-lookup"><span data-stu-id="567cd-123">The start of a null-terminated string that specifies the volume path.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="567cd-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="567cd-124">Remarks</span></span>

<span data-ttu-id="567cd-125">Questa intestazione è seguita da un valore **DWORD** che deve essere identico al valore del membro **dwRecordSize** di **RecordHeader**.</span><span class="sxs-lookup"><span data-stu-id="567cd-125">This header is followed by a **DWORD** value that should be identical to the value of the **dwRecordSize** member of **RecordHeader**.</span></span>

## <a name="requirements"></a><span data-ttu-id="567cd-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="567cd-126">Requirements</span></span>



| <span data-ttu-id="567cd-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="567cd-127">Requirement</span></span> | <span data-ttu-id="567cd-128">Valore</span><span class="sxs-lookup"><span data-stu-id="567cd-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="567cd-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="567cd-129">Minimum supported client</span></span><br/> | <span data-ttu-id="567cd-130">Solo app desktop Windows XP con SP2 \[\]</span><span class="sxs-lookup"><span data-stu-id="567cd-130">Windows XP with SP2 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="567cd-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="567cd-131">Minimum supported server</span></span><br/> | <span data-ttu-id="567cd-132">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="567cd-132">None supported</span></span><br/>                            |
| <span data-ttu-id="567cd-133">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="567cd-133">End of client support</span></span><br/>    | <span data-ttu-id="567cd-134">Windows XP con SP2</span><span class="sxs-lookup"><span data-stu-id="567cd-134">Windows XP with SP2</span></span><br/>                       |



 

 





