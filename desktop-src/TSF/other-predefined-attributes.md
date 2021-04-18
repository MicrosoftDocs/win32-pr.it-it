---
title: Altri attributi predefiniti (TsAttrid. h)
description: I valori seguenti identificano gli attributi vari ottenuti con il metodo GetAppProperty di ITfContext. Il formato dei dati e il contenuto di ogni tipo di proprietà sono inclusi.
ms.assetid: 8536938b-98a1-415b-b5f2-45b90215c270
keywords:
- Altri attributi predefiniti Framework servizi di testo
topic_type:
- apiref
api_name:
- Other Predefined Attributes
api_location:
- TsAttrid.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0d0a3ff72a5ea84a6b9e5b47106012a945dbf45
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302244"
---
# <a name="other-predefined-attributes"></a><span data-ttu-id="00bc9-105">Altri attributi predefiniti</span><span class="sxs-lookup"><span data-stu-id="00bc9-105">Other Predefined Attributes</span></span>

<span data-ttu-id="00bc9-106">I valori seguenti identificano gli attributi vari ottenuti con il metodo [ITfContext:: GetAppProperty](/windows/desktop/api/msctf/nf-msctf-itfcontext-getappproperty) .</span><span class="sxs-lookup"><span data-stu-id="00bc9-106">The following values identify miscellaneous attributes obtained with the [ITfContext::GetAppProperty](/windows/desktop/api/msctf/nf-msctf-itfcontext-getappproperty) method.</span></span> <span data-ttu-id="00bc9-107">Il formato dei dati e il contenuto di ogni tipo di proprietà sono inclusi.</span><span class="sxs-lookup"><span data-stu-id="00bc9-107">The data format and contents of each property type are included.</span></span>

## <a name="properties"></a><span data-ttu-id="00bc9-108">Proprietà</span><span class="sxs-lookup"><span data-stu-id="00bc9-108">Properties</span></span>



| <span data-ttu-id="00bc9-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="00bc9-109">Property</span></span>                             | <span data-ttu-id="00bc9-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="00bc9-110">Description</span></span>                                                                       |
|--------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="00bc9-111">**\_App TSATTRID**</span><span class="sxs-lookup"><span data-stu-id="00bc9-111">**TSATTRID\_App**</span></span>                    | <span data-ttu-id="00bc9-112">Non usato.</span><span class="sxs-lookup"><span data-stu-id="00bc9-112">Not used.</span></span>                                                                         |
| <span data-ttu-id="00bc9-113">**\_App TSATTRID \_ IncorrectGrammar**</span><span class="sxs-lookup"><span data-stu-id="00bc9-113">**TSATTRID\_App\_IncorrectGrammar**</span></span>  | <span data-ttu-id="00bc9-114">Contiene un valore diverso da zero se il testo contiene un errore di grammatica o zero in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="00bc9-114">Contains a nonzero value if the text contains a grammar error or zero otherwise.</span></span>  |
| <span data-ttu-id="00bc9-115">**\_App TSATTRID \_ IncorrectSpelling**</span><span class="sxs-lookup"><span data-stu-id="00bc9-115">**TSATTRID\_App\_IncorrectSpelling**</span></span> | <span data-ttu-id="00bc9-116">Contiene un valore diverso da zero se il testo contiene un errore di ortografia o zero in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="00bc9-116">Contains a nonzero value if the text contains a spelling error or zero otherwise.</span></span> |
| <span data-ttu-id="00bc9-117">**TSATTRID \_ altri**</span><span class="sxs-lookup"><span data-stu-id="00bc9-117">**TSATTRID\_OTHERS**</span></span>                 | <span data-ttu-id="00bc9-118">Non usato.</span><span class="sxs-lookup"><span data-stu-id="00bc9-118">Not used.</span></span>                                                                         |



 

## <a name="requirements"></a><span data-ttu-id="00bc9-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="00bc9-119">Requirements</span></span>



| <span data-ttu-id="00bc9-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="00bc9-120">Requirement</span></span> | <span data-ttu-id="00bc9-121">Valore</span><span class="sxs-lookup"><span data-stu-id="00bc9-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="00bc9-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="00bc9-122">Minimum supported client</span></span><br/> | <span data-ttu-id="00bc9-123">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="00bc9-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="00bc9-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="00bc9-124">Minimum supported server</span></span><br/> | <span data-ttu-id="00bc9-125">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="00bc9-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="00bc9-126">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="00bc9-126">Redistributable</span></span><br/>          | <span data-ttu-id="00bc9-127">TSF 1,0 su Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="00bc9-127">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                       |
| <span data-ttu-id="00bc9-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="00bc9-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="00bc9-129"><dt>TsAttrid. h</dt></span><span class="sxs-lookup"><span data-stu-id="00bc9-129"><dt>TsAttrid.h</dt></span></span> </dl> |



 

