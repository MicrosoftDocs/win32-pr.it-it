---
description: Contiene informazioni sul contesto di ricerca.
ms.assetid: 4b865563-98c2-459b-bb2b-75420d51d6a7
title: Struttura FIND_INFO
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FIND_INFO
api_type:
- NA
api_location: ''
ms.openlocfilehash: 7d6b6dea42c008178c22f6e342a64b2f8d193ec5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304500"
---
# <a name="find_info-structure"></a><span data-ttu-id="2db86-103">TROVA \_ struttura info</span><span class="sxs-lookup"><span data-stu-id="2db86-103">FIND\_INFO structure</span></span>

<span data-ttu-id="2db86-104">Contiene informazioni sul contesto di ricerca.</span><span class="sxs-lookup"><span data-stu-id="2db86-104">Contains search context information.</span></span>

## <a name="syntax"></a><span data-ttu-id="2db86-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2db86-105">Syntax</span></span>


```C++
typedef struct _FIND_INFO {
  TAGID     tiIndex;
  TAGID     tiCurrent;
  TAGID     tiEndIndex;
  TAG       tName;
  DWORD     dwIndexRec;
  DWORD     dwFlags;
  ULONGLONG ullKey;
  union {
    LPCTSTR szName;
    DWORD   dwName;
    GUID    *pguidName;
  };
} FIND_INFO, *PFIND_INFO;
```



## <a name="members"></a><span data-ttu-id="2db86-106">Members</span><span class="sxs-lookup"><span data-stu-id="2db86-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="2db86-107">**tiIndex**</span><span class="sxs-lookup"><span data-stu-id="2db86-107">**tiIndex**</span></span>
</dt> <dd>

<span data-ttu-id="2db86-108">**TagId** per l'indice in cui eseguire la ricerca.</span><span class="sxs-lookup"><span data-stu-id="2db86-108">The **TAGID** for the index to be searched.</span></span>

</dd> <dt>

<span data-ttu-id="2db86-109">**tiCurrent**</span><span class="sxs-lookup"><span data-stu-id="2db86-109">**tiCurrent**</span></span>
</dt> <dd>

<span data-ttu-id="2db86-110">**TagId** per l'elemento corrente che è stato individuato.</span><span class="sxs-lookup"><span data-stu-id="2db86-110">The **TAGID** for the current item that was located.</span></span>

</dd> <dt>

<span data-ttu-id="2db86-111">**tiEndIndex**</span><span class="sxs-lookup"><span data-stu-id="2db86-111">**tiEndIndex**</span></span>
</dt> <dd>

<span data-ttu-id="2db86-112">**TagId** per l'ultimo record dopo FindFirst se l'indice è univoco.</span><span class="sxs-lookup"><span data-stu-id="2db86-112">The **TAGID** for the last record after FindFirst if the index is UNIQUE.</span></span>

</dd> <dt>

<span data-ttu-id="2db86-113">**tName**</span><span class="sxs-lookup"><span data-stu-id="2db86-113">**tName**</span></span>
</dt> <dd>

<span data-ttu-id="2db86-114">Tipo dell'elemento da trovare.</span><span class="sxs-lookup"><span data-stu-id="2db86-114">The type of the item to be located.</span></span> <span data-ttu-id="2db86-115">Vedere [tipi di tag](tag-types.md).</span><span class="sxs-lookup"><span data-stu-id="2db86-115">See [TAG Types](tag-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="2db86-116">**dwIndexRec**</span><span class="sxs-lookup"><span data-stu-id="2db86-116">**dwIndexRec**</span></span>
</dt> <dd>

<span data-ttu-id="2db86-117">Contatore interno utilizzato per tenere traccia della posizione nell'indice in cui dovrebbe iniziare l'operazione di ricerca successiva.</span><span class="sxs-lookup"><span data-stu-id="2db86-117">An internal counter used to track where in the index the next find operation should start.</span></span>

</dd> <dt>

<span data-ttu-id="2db86-118">**dwFlags**</span><span class="sxs-lookup"><span data-stu-id="2db86-118">**dwFlags**</span></span>
</dt> <dd>

<span data-ttu-id="2db86-119">Questo membro può essere 0 o **la \_ \_ \_ chiave univoca dell'indice SHIMDB** (0x00000001), che indica che si tratta di un indice di chiave univoca.</span><span class="sxs-lookup"><span data-stu-id="2db86-119">This member can be 0 or **SHIMDB\_INDEX\_UNIQUE\_KEY** (0x00000001), which indicates that this is a unique-key index.</span></span>

</dd> <dt>

<span data-ttu-id="2db86-120">**ullKey**</span><span class="sxs-lookup"><span data-stu-id="2db86-120">**ullKey**</span></span>
</dt> <dd>

<span data-ttu-id="2db86-121">Chiave per la voce corrente.</span><span class="sxs-lookup"><span data-stu-id="2db86-121">The key for the current entry.</span></span>

</dd> <dt>

<span data-ttu-id="2db86-122">**szName**</span><span class="sxs-lookup"><span data-stu-id="2db86-122">**szName**</span></span>
</dt> <dd>

<span data-ttu-id="2db86-123">Stringa corrente (se il tipo di tag è **il \_ tipo \_ di tag STRINGREF**).</span><span class="sxs-lookup"><span data-stu-id="2db86-123">The current string (if the tag type is **TAG\_TYPE\_STRINGREF**).</span></span>

</dd> <dt>

<span data-ttu-id="2db86-124">**dwName**</span><span class="sxs-lookup"><span data-stu-id="2db86-124">**dwName**</span></span>
</dt> <dd>

<span data-ttu-id="2db86-125">Valore **DWORD** corrente (se il tipo di tag è **il \_ tipo \_ di tag DWORD**).</span><span class="sxs-lookup"><span data-stu-id="2db86-125">The current **DWORD** value (if the tag type is **TAG\_TYPE\_DWORD**).</span></span>

</dd> <dt>

<span data-ttu-id="2db86-126">**pguidName**</span><span class="sxs-lookup"><span data-stu-id="2db86-126">**pguidName**</span></span>
</dt> <dd>

<span data-ttu-id="2db86-127">Il valore GUID corrente (se il tipo di tag è un tipo di tag **\_ \_ Binary** e il tag è **tag \_ database \_ ID**).</span><span class="sxs-lookup"><span data-stu-id="2db86-127">The current GUID value (if the tag type is **TAG\_TYPE\_BINARY** and the TAG is **TAG\_DATABASE\_ID**).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2db86-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2db86-128">Requirements</span></span>



| <span data-ttu-id="2db86-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="2db86-129">Requirement</span></span> | <span data-ttu-id="2db86-130">Valore</span><span class="sxs-lookup"><span data-stu-id="2db86-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="2db86-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2db86-131">Minimum supported client</span></span><br/> | <span data-ttu-id="2db86-132">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2db86-132">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="2db86-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2db86-133">Minimum supported server</span></span><br/> | <span data-ttu-id="2db86-134">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="2db86-134">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2db86-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2db86-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2db86-136">**SdbFindFirstDWORDIndexedTag**</span><span class="sxs-lookup"><span data-stu-id="2db86-136">**SdbFindFirstDWORDIndexedTag**</span></span>](sdbfindfirstdwordindexedtag.md)
</dt> </dl>

 

 




