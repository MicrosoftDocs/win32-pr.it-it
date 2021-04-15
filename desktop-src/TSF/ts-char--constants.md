---
title: Costanti TS_CHAR_ (Textstor. h)
description: Le \_ costanti char TS \_ \ descrivono il tipo di carattere.
ms.assetid: b40ca931-d45c-4101-9380-bb2b3ad25fba
topic_type:
- apiref
api_name:
- TS_CHAR_EMBEDDED
- TS_CHAR_REGION
- TS_CHAR_REPLACEMENT
api_location:
- Textstor.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e25f66006dcb37e2504785b2b28ca1f328edfcfd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400480"
---
# <a name="ts_char_-constants"></a><span data-ttu-id="7f015-103">\_Costanti char \_ \* TS</span><span class="sxs-lookup"><span data-stu-id="7f015-103">TS\_CHAR\_\* Constants</span></span>

<span data-ttu-id="7f015-104">Le \_ costanti char TS \_ \* descrivono il tipo di carattere.</span><span class="sxs-lookup"><span data-stu-id="7f015-104">The TS\_CHAR\_\* constants describe the type of character.</span></span>



| <span data-ttu-id="7f015-105">Costante/valore</span><span class="sxs-lookup"><span data-stu-id="7f015-105">Constant/value</span></span>                                                                                                                                                                                                                                   | <span data-ttu-id="7f015-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7f015-106">Description</span></span>                                                                                         |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------|
| <span id="TS_CHAR_EMBEDDED"></span><span id="ts_char_embedded"></span><dl> <span data-ttu-id="7f015-107"><dt>**Servizi terminal \_ CHAR \_ incorporato**</dt> <dt>(0xFFFC)</dt></span><span class="sxs-lookup"><span data-stu-id="7f015-107"><dt>**TS\_CHAR\_EMBEDDED**</dt> <dt>( 0xfffc )</dt></span></span> </dl>          | <span data-ttu-id="7f015-108">Il carattere è un carattere di sostituzione dell'oggetto Unicode 2,1.</span><span class="sxs-lookup"><span data-stu-id="7f015-108">The character is a Unicode 2.1 object-replacement character.</span></span><br/>                             |
| <span id="TS_CHAR_REGION"></span><span id="ts_char_region"></span><dl> <span data-ttu-id="7f015-109"><dt>**Servizi terminal \_ \_Area char**</dt> <dt>(0)</dt></span><span class="sxs-lookup"><span data-stu-id="7f015-109"><dt>**TS\_CHAR\_REGION**</dt> <dt>( 0 )</dt></span></span> </dl>                     | <span data-ttu-id="7f015-110">Il carattere è un limite di area.</span><span class="sxs-lookup"><span data-stu-id="7f015-110">The character is a region boundary.</span></span><br/>                                                      |
| <span id="TS_CHAR_REPLACEMENT"></span><span id="ts_char_replacement"></span><dl> <span data-ttu-id="7f015-111"><dt>**Servizi terminal \_ \_Sostituzione di caratteri**</dt> <dt>(0xFFFD)</dt></span><span class="sxs-lookup"><span data-stu-id="7f015-111"><dt>**TS\_CHAR\_REPLACEMENT**</dt> <dt>( 0xfffd )</dt></span></span> </dl> | <span data-ttu-id="7f015-112">Il carattere è un carattere segnaposto di testo nascosto o un carattere di sostituzione Unicode.</span><span class="sxs-lookup"><span data-stu-id="7f015-112">The character is a hidden-text placeholder character or a Unicode replacement character.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="7f015-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7f015-113">Requirements</span></span>



| <span data-ttu-id="7f015-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="7f015-114">Requirement</span></span> | <span data-ttu-id="7f015-115">Valore</span><span class="sxs-lookup"><span data-stu-id="7f015-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7f015-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7f015-116">Minimum supported client</span></span><br/> | <span data-ttu-id="7f015-117">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="7f015-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="7f015-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7f015-118">Minimum supported server</span></span><br/> | <span data-ttu-id="7f015-119">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="7f015-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="7f015-120">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="7f015-120">Redistributable</span></span><br/>          | <span data-ttu-id="7f015-121">TSF 1,0 su Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="7f015-121">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                         |
| <span data-ttu-id="7f015-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7f015-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="7f015-123"><dt>Textstor. h</dt></span><span class="sxs-lookup"><span data-stu-id="7f015-123"><dt>Textstor.h</dt></span></span> </dl>   |
| <span data-ttu-id="7f015-124">IDL</span><span class="sxs-lookup"><span data-stu-id="7f015-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="7f015-125"><dt>Textstor. idl</dt></span><span class="sxs-lookup"><span data-stu-id="7f015-125"><dt>Textstor.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7f015-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7f015-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f015-127">Oggetti incorporati</span><span class="sxs-lookup"><span data-stu-id="7f015-127">Embedded Objects</span></span>](embedded-objects.md)
</dt> </dl>

 

 





