---
title: Attributi elenco predefiniti (TsAttrid. h)
description: I valori seguenti identificano gli attributi dell'elenco ottenuti con il metodo ITfContext GetAppProperty. Il formato dei dati e il contenuto di ogni tipo di proprietà sono inclusi.
ms.assetid: 9a9e1912-51c0-40e0-9e3a-b84ea7077dbe
keywords:
- Framework dei servizi di testo attributi elenco predefiniti
topic_type:
- apiref
api_name:
- Predefined List Attributes
api_location:
- TsAttrid.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81ade2403e124b934c6872f39c01fc7fc1ea6f6b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120907"
---
# <a name="predefined-list-attributes"></a><span data-ttu-id="a2422-105">Attributi elenco predefiniti</span><span class="sxs-lookup"><span data-stu-id="a2422-105">Predefined List Attributes</span></span>

<span data-ttu-id="a2422-106">I valori seguenti identificano gli attributi dell'elenco ottenuti con il metodo [ITfContext:: GetAppProperty](/windows/desktop/api/msctf/nf-msctf-itfcontext-getappproperty) .</span><span class="sxs-lookup"><span data-stu-id="a2422-106">The following values identify list attributes obtained with the [ITfContext::GetAppProperty](/windows/desktop/api/msctf/nf-msctf-itfcontext-getappproperty) method.</span></span> <span data-ttu-id="a2422-107">Il formato dei dati e il contenuto di ogni tipo di proprietà sono inclusi.</span><span class="sxs-lookup"><span data-stu-id="a2422-107">The data format and contents of each property type are included.</span></span>

## <a name="properties"></a><span data-ttu-id="a2422-108">Proprietà</span><span class="sxs-lookup"><span data-stu-id="a2422-108">Properties</span></span>



| <span data-ttu-id="a2422-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="a2422-109">Property</span></span>                          | <span data-ttu-id="a2422-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a2422-110">Description</span></span>                                                                                     |
|-----------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a2422-111">\_Elenco TSATTRID</span><span class="sxs-lookup"><span data-stu-id="a2422-111">TSATTRID\_List</span></span>                    | <span data-ttu-id="a2422-112">Non usato.</span><span class="sxs-lookup"><span data-stu-id="a2422-112">Not used.</span></span>                                                                                       |
| <span data-ttu-id="a2422-113">\_Elenco TSATTRID \_ LevelIndel</span><span class="sxs-lookup"><span data-stu-id="a2422-113">TSATTRID\_List\_LevelIndel</span></span>        | <span data-ttu-id="a2422-114">Contiene il livello di indice dell'elenco.</span><span class="sxs-lookup"><span data-stu-id="a2422-114">Contains the index level of the list.</span></span> <span data-ttu-id="a2422-115">1 è il livello più esterno, 2 è il livello successivo e così via.</span><span class="sxs-lookup"><span data-stu-id="a2422-115">1 is the outermost level, 2 is the next level, and so on.</span></span> |
| <span data-ttu-id="a2422-116">\_Tipo di elenco TSATTRID \_</span><span class="sxs-lookup"><span data-stu-id="a2422-116">TSATTRID\_List\_Type</span></span>              | <span data-ttu-id="a2422-117">Non usato.</span><span class="sxs-lookup"><span data-stu-id="a2422-117">Not used.</span></span>                                                                                       |
| <span data-ttu-id="a2422-118">\_Tipo di elenco TSATTRID \_ \_ arabo</span><span class="sxs-lookup"><span data-stu-id="a2422-118">TSATTRID\_List\_Type\_Arabic</span></span>      | <span data-ttu-id="a2422-119">Contiene un valore diverso da zero se l'elenco è un elenco di numeri arabi o zero in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="a2422-119">Contains a nonzero value if the list is an arabic numeral list or zero otherwise.</span></span>               |
| <span data-ttu-id="a2422-120">\_Elenco TSATTRID \_ tipo \_ elenco</span><span class="sxs-lookup"><span data-stu-id="a2422-120">TSATTRID\_List\_Type\_Bullet</span></span>      | <span data-ttu-id="a2422-121">Contiene un valore diverso da zero se l'elenco è un elenco puntato o zero in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="a2422-121">Contains a nonzero value if the list is a bulleted list or zero otherwise.</span></span>                      |
| <span data-ttu-id="a2422-122">\_Tipo di elenco TSATTRID \_ \_ LowerLetter</span><span class="sxs-lookup"><span data-stu-id="a2422-122">TSATTRID\_List\_Type\_LowerLetter</span></span> | <span data-ttu-id="a2422-123">Contiene un valore diverso da zero se l'elenco è un elenco con lettere minuscole o zero in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="a2422-123">Contains a nonzero value if the list is a lowercase lettered list or zero otherwise.</span></span>            |
| <span data-ttu-id="a2422-124">\_Tipo di elenco TSATTRID \_ \_ LowerRoman</span><span class="sxs-lookup"><span data-stu-id="a2422-124">TSATTRID\_List\_Type\_LowerRoman</span></span>  | <span data-ttu-id="a2422-125">Contiene un valore diverso da zero se l'elenco è un elenco di numeri romani minuscoli oppure zero in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="a2422-125">Contains a nonzero value if the list is a lowercase roman numeral list or zero otherwise.</span></span>       |
| <span data-ttu-id="a2422-126">\_Tipo di elenco TSATTRID \_ \_ UpperLetter</span><span class="sxs-lookup"><span data-stu-id="a2422-126">TSATTRID\_List\_Type\_UpperLetter</span></span> | <span data-ttu-id="a2422-127">Contiene un valore diverso da zero se l'elenco è un elenco con lettere maiuscole o zero in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="a2422-127">Contains a nonzero value if the list is an upper-case lettered list or zero otherwise.</span></span>          |
| <span data-ttu-id="a2422-128">\_Tipo di elenco TSATTRID \_ \_ UpperRoman</span><span class="sxs-lookup"><span data-stu-id="a2422-128">TSATTRID\_List\_Type\_UpperRoman</span></span>  | <span data-ttu-id="a2422-129">Contiene un valore diverso da zero se l'elenco è un elenco di numeri romani in maiuscolo o zero in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="a2422-129">Contains a nonzero value if the list is an uppercase roman numeral list or zero otherwise.</span></span>      |



 

## <a name="requirements"></a><span data-ttu-id="a2422-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a2422-130">Requirements</span></span>



| <span data-ttu-id="a2422-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="a2422-131">Requirement</span></span> | <span data-ttu-id="a2422-132">Valore</span><span class="sxs-lookup"><span data-stu-id="a2422-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a2422-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a2422-133">Minimum supported client</span></span><br/> | <span data-ttu-id="a2422-134">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="a2422-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="a2422-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a2422-135">Minimum supported server</span></span><br/> | <span data-ttu-id="a2422-136">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="a2422-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a2422-137">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="a2422-137">Redistributable</span></span><br/>          | <span data-ttu-id="a2422-138">TSF 1,0 su Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="a2422-138">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                       |
| <span data-ttu-id="a2422-139">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a2422-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="a2422-140"><dt>TsAttrid. h</dt></span><span class="sxs-lookup"><span data-stu-id="a2422-140"><dt>TsAttrid.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a2422-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a2422-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2422-142">ITfContext:: GetAppProperty</span><span class="sxs-lookup"><span data-stu-id="a2422-142">ITfContext::GetAppProperty</span></span>](/windows/desktop/api/msctf/nf-msctf-itfcontext-getappproperty)
</dt> </dl>

 

