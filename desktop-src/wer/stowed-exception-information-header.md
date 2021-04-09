---
title: Struttura STOWED_EXCEPTION_INFORMATION_HEADER
description: Contiene informazioni che identificano la struttura padre.
ms.assetid: 0BC1FDAA-C750-4DEC-AF6A-B2CB3240B67C
keywords:
- Struttura STOWED_EXCEPTION_INFORMATION_HEADER Segnalazione errori Windows
- Puntatore alla struttura PSTOWED_EXCEPTION_INFORMATION_HEADER Segnalazione errori Windows
topic_type:
- apiref
api_name:
- STOWED_EXCEPTION_INFORMATION_HEADER
api_location:
- none
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 101bb1fb1555c829622a42c17fdfb01488c57636
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048672"
---
# <a name="stowed_exception_information_header-structure"></a><span data-ttu-id="28566-105">\_Struttura dell' \_ intestazione delle informazioni sulle eccezioni riposte \_</span><span class="sxs-lookup"><span data-stu-id="28566-105">STOWED\_EXCEPTION\_INFORMATION\_HEADER structure</span></span>

<span data-ttu-id="28566-106">Contiene informazioni che identificano la struttura padre.</span><span class="sxs-lookup"><span data-stu-id="28566-106">Contains info that identifies the parent structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="28566-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="28566-107">Syntax</span></span>


```C++
typedef struct _STOWED_EXCEPTION_INFORMATION_HEADER {
  ULONG Size;
  ULONG Signature;
} STOWED_EXCEPTION_INFORMATION_HEADER, *PSTOWED_EXCEPTION_INFORMATION_HEADER;
```



## <a name="members"></a><span data-ttu-id="28566-108">Members</span><span class="sxs-lookup"><span data-stu-id="28566-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="28566-109">**Dimensioni**</span><span class="sxs-lookup"><span data-stu-id="28566-109">**Size**</span></span>
</dt> <dd>

<span data-ttu-id="28566-110">Tipo: **[ **ULONG**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="28566-110">Type: **[**ULONG**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="28566-111">Dimensione, in byte, della struttura padre.</span><span class="sxs-lookup"><span data-stu-id="28566-111">Size, in bytes, of the parent structure.</span></span>

</dd> <dt>

<span data-ttu-id="28566-112">**Firma**</span><span class="sxs-lookup"><span data-stu-id="28566-112">**Signature**</span></span>
</dt> <dd>

<span data-ttu-id="28566-113">Tipo: **[ **ULONG**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="28566-113">Type: **[**ULONG**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="28566-114">Valore a 32 bit che specifica la firma della struttura padre.</span><span class="sxs-lookup"><span data-stu-id="28566-114">A 32-bit value that specifies the signature of the parent structure.</span></span>



| <span data-ttu-id="28566-115">Valore</span><span class="sxs-lookup"><span data-stu-id="28566-115">Value</span></span>                                                                                                                                                                                                                                                                                                            | <span data-ttu-id="28566-116">Significato</span><span class="sxs-lookup"><span data-stu-id="28566-116">Meaning</span></span>                                                                                                                                       |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="STOWED_EXCEPTION_INFORMATION_V1_SIGNATURE"></span><span id="stowed_exception_information_v1_signature"></span><dl> <span data-ttu-id="28566-117">Ricollocato <dt>**\_ \_Informazioni sull'eccezione \_ V1 \_ firma**</dt> <dt>' SE01'</dt></span><span class="sxs-lookup"><span data-stu-id="28566-117"><dt>**STOWED\_EXCEPTION\_INFORMATION\_V1\_SIGNATURE**</dt> <dt>'SE01'</dt></span></span> </dl> | <span data-ttu-id="28566-118">Questo valore indica che l'elemento padre è una struttura di **\_ \_ informazioni sull' \_ eccezione ristivata** .</span><span class="sxs-lookup"><span data-stu-id="28566-118">This value indicates that the parent is a **STOWED\_EXCEPTION\_INFORMATION\_V1** structure.</span></span><br/>                                        |
| <span id="STOWED_EXCEPTION_INFORMATION_V2_SIGNATURE"></span><span id="stowed_exception_information_v2_signature"></span><dl> <span data-ttu-id="28566-119">Ricollocato <dt>**\_ \_Informazioni sull'eccezione \_ v2 \_ firma**</dt> <dt>' SE02'</dt></span><span class="sxs-lookup"><span data-stu-id="28566-119"><dt>**STOWED\_EXCEPTION\_INFORMATION\_V2\_SIGNATURE**</dt> <dt>'SE02'</dt></span></span> </dl> | <span data-ttu-id="28566-120">Questo valore indica che l'elemento padre è una struttura di [**\_ \_ informazioni sull' \_ eccezione ristivata V2**](stowed-exception-information-v2.md) .</span><span class="sxs-lookup"><span data-stu-id="28566-120">This value indicates that the parent is a [**STOWED\_EXCEPTION\_INFORMATION\_V2**](stowed-exception-information-v2.md) structure.</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="28566-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="28566-121">Remarks</span></span>

<span data-ttu-id="28566-122">Ricollocato [**\_ \_Le informazioni sull'eccezione \_ v2**](stowed-exception-information-v2.md) e l' **\_ \_ \_ intestazione delle informazioni sulle eccezioni** riposte non sono attualmente definite in un'intestazione disponibile pubblicamente, pertanto è necessario definirle nel codice sorgente prima di utilizzarle.</span><span class="sxs-lookup"><span data-stu-id="28566-122">[**STOWED\_EXCEPTION\_INFORMATION\_V2**](stowed-exception-information-v2.md) and **STOWED\_EXCEPTION\_INFORMATION\_HEADER** currently aren't defined in a header that is publicly available so you need to define them in your source code before you use them.</span></span>

<span data-ttu-id="28566-123">La struttura di **\_ \_ informazioni \_ sull'eccezione ristivata** è identica a questa struttura, ad eccezione del fatto che non contiene i membri **NestedExceptionType** e **annidaexception** .</span><span class="sxs-lookup"><span data-stu-id="28566-123">The **STOWED\_EXCEPTION\_INFORMATION\_V1** structure is identical to this structure except it doesn't contain the **NestedExceptionType** and **NestedException** members.</span></span>

## <a name="requirements"></a><span data-ttu-id="28566-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="28566-124">Requirements</span></span>



| <span data-ttu-id="28566-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="28566-125">Requirement</span></span> | <span data-ttu-id="28566-126">Valore</span><span class="sxs-lookup"><span data-stu-id="28566-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="28566-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="28566-127">Minimum supported client</span></span><br/> | <span data-ttu-id="28566-128">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="28566-128">Windows 8 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="28566-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="28566-129">Minimum supported server</span></span><br/> | <span data-ttu-id="28566-130">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="28566-130">Windows Server 2012 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="28566-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="28566-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="28566-132"><dt>Nessuno</dt></span><span class="sxs-lookup"><span data-stu-id="28566-132"><dt>None</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="28566-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="28566-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28566-134">**\_Informazioni sulle eccezioni riposte \_ \_ v2**</span><span class="sxs-lookup"><span data-stu-id="28566-134">**STOWED\_EXCEPTION\_INFORMATION\_V2**</span></span>](stowed-exception-information-v2.md)
</dt> </dl>

 

