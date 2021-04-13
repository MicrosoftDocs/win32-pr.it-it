---
title: Messaggio di EM_GETWORDWRAPMODE (RichEdit. h)
description: Ottiene il ritorno a capo automatico e le opzioni di Word break per il controllo Rich Edit.
ms.assetid: a87d80d6-2e9e-40ba-9348-a1cc1ef8ec10
keywords:
- Controlli di Windows Message EM_GETWORDWRAPMODE
topic_type:
- apiref
api_name:
- EM_GETWORDWRAPMODE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: efc8a2b6d17623964eb0d3714c1c099f47fc788a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475568"
---
# <a name="em_getwordwrapmode-message"></a><span data-ttu-id="0d3ef-104">\_Messaggio GETWORDWRAPMODE em</span><span class="sxs-lookup"><span data-stu-id="0d3ef-104">EM\_GETWORDWRAPMODE message</span></span>

<span data-ttu-id="0d3ef-105">Ottiene il ritorno a capo automatico e le opzioni di Word break per il controllo Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="0d3ef-105">Gets the current word wrap and word-break options for the rich edit control.</span></span>

> [!Note]  
> <span data-ttu-id="0d3ef-106">Questo messaggio è supportato solo nelle versioni in lingua asiatica di Microsoft Rich Edit 1,0.</span><span class="sxs-lookup"><span data-stu-id="0d3ef-106">This message is supported only in Asian-language versions of Microsoft Rich Edit 1.0.</span></span> <span data-ttu-id="0d3ef-107">Non è supportata nelle versioni successive di Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="0d3ef-107">It is not supported in any later versions of Rich Edit.</span></span>

 

## <a name="parameters"></a><span data-ttu-id="0d3ef-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="0d3ef-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0d3ef-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0d3ef-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0d3ef-110">Non utilizzato; deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="0d3ef-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="0d3ef-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0d3ef-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0d3ef-112">Non utilizzato; deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="0d3ef-112">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0d3ef-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0d3ef-113">Return value</span></span>

<span data-ttu-id="0d3ef-114">Il messaggio restituisce le opzioni di ritorno a capo e di Word Breaking correnti.</span><span class="sxs-lookup"><span data-stu-id="0d3ef-114">The message returns the current word wrap and word-break options.</span></span>

## <a name="remarks"></a><span data-ttu-id="0d3ef-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="0d3ef-115">Remarks</span></span>

<span data-ttu-id="0d3ef-116">Questo messaggio non deve essere inviato dalla procedura di Word break definita dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="0d3ef-116">This message must not be sent by the application-defined, word-break procedure.</span></span>

## <a name="requirements"></a><span data-ttu-id="0d3ef-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0d3ef-117">Requirements</span></span>



| <span data-ttu-id="0d3ef-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="0d3ef-118">Requirement</span></span> | <span data-ttu-id="0d3ef-119">Valore</span><span class="sxs-lookup"><span data-stu-id="0d3ef-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0d3ef-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0d3ef-120">Minimum supported client</span></span><br/> | <span data-ttu-id="0d3ef-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0d3ef-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0d3ef-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0d3ef-122">Minimum supported server</span></span><br/> | <span data-ttu-id="0d3ef-123">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="0d3ef-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0d3ef-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0d3ef-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="0d3ef-125"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="0d3ef-125"><dt>Richedit.h</dt></span></span> </dl> |



 

 





