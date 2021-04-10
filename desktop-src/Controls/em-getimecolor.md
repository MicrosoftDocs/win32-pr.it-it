---
title: Messaggio di EM_GETIMECOLOR (RichEdit. h)
description: Recupera il colore di composizione IME (Input Method Editor).
ms.assetid: 788ac56c-f2d8-4e9a-8829-b92dcd76e6de
keywords:
- Controlli di Windows Message EM_GETIMECOLOR
topic_type:
- apiref
api_name:
- EM_GETIMECOLOR
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8a19061651787ff94575f8bc64a69f06d445a7f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964578"
---
# <a name="em_getimecolor-message"></a><span data-ttu-id="79aaf-104">\_Messaggio GETIMECOLOR em</span><span class="sxs-lookup"><span data-stu-id="79aaf-104">EM\_GETIMECOLOR message</span></span>

<span data-ttu-id="79aaf-105">Recupera il colore di composizione IME (Input Method Editor).</span><span class="sxs-lookup"><span data-stu-id="79aaf-105">Retrieves the Input Method Editor (IME) composition color.</span></span>

> [!Note]  
> <span data-ttu-id="79aaf-106">Questo messaggio è supportato solo nelle versioni in lingua asiatica di Microsoft Rich Edit 1,0.</span><span class="sxs-lookup"><span data-stu-id="79aaf-106">This message is supported only in Asian-language versions of Microsoft Rich Edit 1.0.</span></span> <span data-ttu-id="79aaf-107">Non è supportata nelle versioni successive di Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="79aaf-107">It is not supported in any later versions of Rich Edit.</span></span>

 

## <a name="parameters"></a><span data-ttu-id="79aaf-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="79aaf-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="79aaf-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="79aaf-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="79aaf-110">Questo parametro non viene utilizzato. deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="79aaf-110">This parameter is not used; it must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="79aaf-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="79aaf-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="79aaf-112">Matrice di quattro elementi di strutture [**COMPCOLOR**](/windows/desktop/api/Richedit/ns-richedit-compcolor) che riceve il colore di composizione.</span><span class="sxs-lookup"><span data-stu-id="79aaf-112">A four-element array of [**COMPCOLOR**](/windows/desktop/api/Richedit/ns-richedit-compcolor) structures that receives the composition color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="79aaf-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="79aaf-113">Return value</span></span>

<span data-ttu-id="79aaf-114">Se l'operazione ha esito positivo, il valore restituito è un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="79aaf-114">If the operation succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="79aaf-115">Se l'operazione ha esito negativo, il valore restituito è zero.</span><span class="sxs-lookup"><span data-stu-id="79aaf-115">If the operation fails, the return value is zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="79aaf-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="79aaf-116">Requirements</span></span>



| <span data-ttu-id="79aaf-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="79aaf-117">Requirement</span></span> | <span data-ttu-id="79aaf-118">Valore</span><span class="sxs-lookup"><span data-stu-id="79aaf-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="79aaf-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="79aaf-119">Minimum supported client</span></span><br/> | <span data-ttu-id="79aaf-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="79aaf-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="79aaf-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="79aaf-121">Minimum supported server</span></span><br/> | <span data-ttu-id="79aaf-122">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="79aaf-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="79aaf-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="79aaf-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="79aaf-124"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="79aaf-124"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="79aaf-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="79aaf-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79aaf-126">**COMPCOLOR**</span><span class="sxs-lookup"><span data-stu-id="79aaf-126">**COMPCOLOR**</span></span>](/windows/desktop/api/Richedit/ns-richedit-compcolor)
</dt> </dl>

 

 





