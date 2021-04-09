---
description: Contiene i dati dell'attributo per un file.
ms.assetid: f23f801c-826c-4269-bf96-0e01430484f4
title: Struttura ATTRINFO
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ATTRINFO
api_type:
- NA
api_location: ''
ms.openlocfilehash: 01c061330db3e97989e0700452fd4a205488a9fc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877241"
---
# <a name="attrinfo-structure"></a><span data-ttu-id="99619-103">Struttura ATTRINFO</span><span class="sxs-lookup"><span data-stu-id="99619-103">ATTRINFO structure</span></span>

<span data-ttu-id="99619-104">Contiene i dati dell'attributo per un file.</span><span class="sxs-lookup"><span data-stu-id="99619-104">Contains the attribute data for a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="99619-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="99619-105">Syntax</span></span>


```C++
typedef struct tagATTRINFO {
  TAG   tAttrID;
  DWORD dwFlags;
  union {
    ULONGLONG ullAttr;
    DWORD     dwAttr;
    TCHAR     *lpAttr;
  };
} ATTRINFO, *PATTRINFO;
```



## <a name="members"></a><span data-ttu-id="99619-106">Members</span><span class="sxs-lookup"><span data-stu-id="99619-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="99619-107">**tAttrID**</span><span class="sxs-lookup"><span data-stu-id="99619-107">**tAttrID**</span></span>
</dt> <dd>

<span data-ttu-id="99619-108">Tipo di attributo.</span><span class="sxs-lookup"><span data-stu-id="99619-108">The attribute type.</span></span> <span data-ttu-id="99619-109">Vedere [tipi di tag](tag-types.md).</span><span class="sxs-lookup"><span data-stu-id="99619-109">See [TAG Types](tag-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="99619-110">**dwFlags**</span><span class="sxs-lookup"><span data-stu-id="99619-110">**dwFlags**</span></span>
</dt> <dd>

<span data-ttu-id="99619-111">Flag per questo attributo.</span><span class="sxs-lookup"><span data-stu-id="99619-111">The flags for this attribute.</span></span>



| <span data-ttu-id="99619-112">Valore</span><span class="sxs-lookup"><span data-stu-id="99619-112">Value</span></span>                                                                                                                                                                                                                                           | <span data-ttu-id="99619-113">Significato</span><span class="sxs-lookup"><span data-stu-id="99619-113">Meaning</span></span>                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <span id="ATTRIBUTE_AVAILABLE"></span><span id="attribute_available"></span><dl> <span data-ttu-id="99619-114"><dt>**Attributo \_**</dt> <dt>0x00000001</dt> disponibili</span><span class="sxs-lookup"><span data-stu-id="99619-114"><dt>**ATTRIBUTE\_AVAILABLE**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="99619-115">L'attributo è disponibile.</span><span class="sxs-lookup"><span data-stu-id="99619-115">The attribute is available.</span></span><br/>                             |
| <span id="ATTRIBUTE_FAILED"></span><span id="attribute_failed"></span><dl> <span data-ttu-id="99619-116"><dt>**Attributo \_ 0x00000002 non riuscito**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="99619-116"><dt>**ATTRIBUTE\_FAILED**</dt> <dt>0x00000002</dt></span></span> </dl>          | <span data-ttu-id="99619-117">La chiamata non è riuscita perché l'attributo non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="99619-117">The call failed because the attribute is not available.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="99619-118">**ullAttr**</span><span class="sxs-lookup"><span data-stu-id="99619-118">**ullAttr**</span></span>
</dt> <dd>

<span data-ttu-id="99619-119">Valore **QWORD** (se il tipo di tag è **il \_ tipo \_ di tag QWORD**).</span><span class="sxs-lookup"><span data-stu-id="99619-119">A **QWORD** value (if the tag type is **TAG\_TYPE\_QWORD**).</span></span>

</dd> <dt>

<span data-ttu-id="99619-120">**dwAttr**</span><span class="sxs-lookup"><span data-stu-id="99619-120">**dwAttr**</span></span>
</dt> <dd>

<span data-ttu-id="99619-121">Valore **DWORD** (se il tipo di tag è **il \_ tipo \_ di tag DWORD**).</span><span class="sxs-lookup"><span data-stu-id="99619-121">A **DWORD** value (if the tag type is **TAG\_TYPE\_DWORD**).</span></span>

</dd> <dt>

<span data-ttu-id="99619-122">**lpAttr**</span><span class="sxs-lookup"><span data-stu-id="99619-122">**lpAttr**</span></span>
</dt> <dd>

<span data-ttu-id="99619-123">Puntatore a una stringa (se il tipo di tag è **il \_ tipo \_ di tag STRINGREF**).</span><span class="sxs-lookup"><span data-stu-id="99619-123">A pointer to a string (if the tag type is **TAG\_TYPE\_STRINGREF**).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="99619-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="99619-124">Requirements</span></span>



| <span data-ttu-id="99619-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="99619-125">Requirement</span></span> | <span data-ttu-id="99619-126">Valore</span><span class="sxs-lookup"><span data-stu-id="99619-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="99619-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="99619-127">Minimum supported client</span></span><br/> | <span data-ttu-id="99619-128">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="99619-128">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="99619-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="99619-129">Minimum supported server</span></span><br/> | <span data-ttu-id="99619-130">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="99619-130">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="99619-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="99619-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99619-132">**SdbFormatAttribute**</span><span class="sxs-lookup"><span data-stu-id="99619-132">**SdbFormatAttribute**</span></span>](sdbformatattribute.md)
</dt> <dt>

[<span data-ttu-id="99619-133">**SdbFreeFileAttributes**</span><span class="sxs-lookup"><span data-stu-id="99619-133">**SdbFreeFileAttributes**</span></span>](sdbfreefileattributes.md)
</dt> <dt>

[<span data-ttu-id="99619-134">**SdbGetFileAttributes**</span><span class="sxs-lookup"><span data-stu-id="99619-134">**SdbGetFileAttributes**</span></span>](sdbgetfileattributes.md)
</dt> </dl>

 

 




