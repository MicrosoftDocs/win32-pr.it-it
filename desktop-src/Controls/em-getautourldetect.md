---
title: Messaggio di EM_GETAUTOURLDETECT (RichEdit. h)
description: Indica se il rilevamento URL automatico è attivato nel controllo Rich Edit.
ms.assetid: f723f15c-bf8f-41ab-aef0-bd8f2c0b9e5d
keywords:
- Controlli di Windows Message EM_GETAUTOURLDETECT
topic_type:
- apiref
api_name:
- EM_GETAUTOURLDETECT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e68e4f2991c5f8780cb587594289674e07ec992
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048449"
---
# <a name="em_getautourldetect-message"></a><span data-ttu-id="2d821-104">\_Messaggio GETAUTOURLDETECT em</span><span class="sxs-lookup"><span data-stu-id="2d821-104">EM\_GETAUTOURLDETECT message</span></span>

<span data-ttu-id="2d821-105">Indica se il rilevamento URL automatico è attivato nel controllo Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="2d821-105">Indicates whether the auto URL detection is turned on in the rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="2d821-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="2d821-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2d821-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2d821-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2d821-108">Non utilizzato; deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="2d821-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="2d821-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2d821-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2d821-110">Non utilizzato; deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="2d821-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2d821-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2d821-111">Return value</span></span>

<span data-ttu-id="2d821-112">Se il rilevamento URL automatico è attivo, il valore restituito è 1.</span><span class="sxs-lookup"><span data-stu-id="2d821-112">If auto-URL detection is active, the return value is 1.</span></span>

<span data-ttu-id="2d821-113">Se il rilevamento URL automatico è inattivo, il valore restituito è 0.</span><span class="sxs-lookup"><span data-stu-id="2d821-113">If auto-URL detection is inactive, the return value is 0.</span></span>

## <a name="remarks"></a><span data-ttu-id="2d821-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="2d821-114">Remarks</span></span>

<span data-ttu-id="2d821-115">Quando il rilevamento URL automatico è acceso, Microsoft Rich Edit controlla costantemente il testo tipizzato per un URL valido.</span><span class="sxs-lookup"><span data-stu-id="2d821-115">When auto URL detection is on, Microsoft Rich Edit is constantly checking typed text for a valid URL.</span></span> <span data-ttu-id="2d821-116">Rich Edit riconosce gli URL che iniziano con i prefissi seguenti:</span><span class="sxs-lookup"><span data-stu-id="2d821-116">Rich Edit recognizes URLs that start with these prefixes:</span></span>

-   <span data-ttu-id="2d821-117">http:</span><span class="sxs-lookup"><span data-stu-id="2d821-117">http:</span></span>
-   <span data-ttu-id="2d821-118">file:</span><span class="sxs-lookup"><span data-stu-id="2d821-118">file:</span></span>
-   <span data-ttu-id="2d821-119">mailto:</span><span class="sxs-lookup"><span data-stu-id="2d821-119">mailto:</span></span>
-   <span data-ttu-id="2d821-120">FTP</span><span class="sxs-lookup"><span data-stu-id="2d821-120">ftp:</span></span>
-   <span data-ttu-id="2d821-121">https</span><span class="sxs-lookup"><span data-stu-id="2d821-121">https:</span></span>
-   <span data-ttu-id="2d821-122">Gopher</span><span class="sxs-lookup"><span data-stu-id="2d821-122">gopher:</span></span>
-   <span data-ttu-id="2d821-123">NNTP</span><span class="sxs-lookup"><span data-stu-id="2d821-123">nntp:</span></span>
-   <span data-ttu-id="2d821-124">Prospero</span><span class="sxs-lookup"><span data-stu-id="2d821-124">prospero:</span></span>
-   <span data-ttu-id="2d821-125">Telnet</span><span class="sxs-lookup"><span data-stu-id="2d821-125">telnet:</span></span>
-   <span data-ttu-id="2d821-126">Notizie</span><span class="sxs-lookup"><span data-stu-id="2d821-126">news:</span></span>
-   <span data-ttu-id="2d821-127">WAIS</span><span class="sxs-lookup"><span data-stu-id="2d821-127">wais:</span></span>
-   <span data-ttu-id="2d821-128">Outlook</span><span class="sxs-lookup"><span data-stu-id="2d821-128">outlook:</span></span>

<span data-ttu-id="2d821-129">Rich Edit riconosce inoltre i nomi di percorso standard che iniziano con \\ \\ .</span><span class="sxs-lookup"><span data-stu-id="2d821-129">Rich Edit also recognizes standard path names that start with \\\\.</span></span> <span data-ttu-id="2d821-130">Quando Rich Edit individua un URL, modifica il colore del testo dell'URL, sottolinea il testo e invia una notifica al client usando il [ \_ collegamento it](en-link.md).</span><span class="sxs-lookup"><span data-stu-id="2d821-130">When Rich Edit locates a URL, it changes the URL text color, underlines the text, and notifies the client using [EN\_LINK](en-link.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2d821-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2d821-131">Requirements</span></span>



| <span data-ttu-id="2d821-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="2d821-132">Requirement</span></span> | <span data-ttu-id="2d821-133">Valore</span><span class="sxs-lookup"><span data-stu-id="2d821-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2d821-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2d821-134">Minimum supported client</span></span><br/> | <span data-ttu-id="2d821-135">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2d821-135">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2d821-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2d821-136">Minimum supported server</span></span><br/> | <span data-ttu-id="2d821-137">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="2d821-137">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2d821-138">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2d821-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="2d821-139"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="2d821-139"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2d821-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2d821-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d821-141">\_collegamento en</span><span class="sxs-lookup"><span data-stu-id="2d821-141">EN\_LINK</span></span>](en-link.md)
</dt> </dl>

 

 





