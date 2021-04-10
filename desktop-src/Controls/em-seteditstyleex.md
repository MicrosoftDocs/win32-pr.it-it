---
title: Messaggio di EM_SETEDITSTYLEEX (RichEdit. h)
description: Imposta i flag di stile di modifica estesa correnti.
ms.assetid: C5CECC7C-6418-4A72-9F0B-6F55BE89E302
keywords:
- Controlli di Windows Message EM_SETEDITSTYLEEX
topic_type:
- apiref
api_name:
- EM_SETEDITSTYLEEX
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72fe7a1ff420048f620d69196360678e9718a510
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964755"
---
# <a name="em_seteditstyleex-message"></a><span data-ttu-id="0b7d0-104">\_Messaggio SETEDITSTYLEEX em</span><span class="sxs-lookup"><span data-stu-id="0b7d0-104">EM\_SETEDITSTYLEEX message</span></span>

<span data-ttu-id="0b7d0-105">Imposta i flag di stile di modifica estesa correnti.</span><span class="sxs-lookup"><span data-stu-id="0b7d0-105">Sets the current extended edit style flags.</span></span>


```C++
#define EM_SETEDITSTYLEEX       (WM_USER + 275)
```



## <a name="parameters"></a><span data-ttu-id="0b7d0-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="0b7d0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0b7d0-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0b7d0-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0b7d0-108">Specifica uno o più flag di stile di modifica estesa.</span><span class="sxs-lookup"><span data-stu-id="0b7d0-108">Specifies one or more extended edit style flags.</span></span> <span data-ttu-id="0b7d0-109">Per un elenco di valori possibili, vedere [**em \_ GETEDITSTYLEEX**](/windows/desktop/Controls/em-geteditstyleex).</span><span class="sxs-lookup"><span data-stu-id="0b7d0-109">For a list of possible values, see [**EM\_GETEDITSTYLEEX**](/windows/desktop/Controls/em-geteditstyleex).</span></span>

</dd> <dt>

<span data-ttu-id="0b7d0-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0b7d0-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0b7d0-111">Maschera costituita da uno o più valori *wParam* .</span><span class="sxs-lookup"><span data-stu-id="0b7d0-111">A mask consisting of one or more of the *wParam* values.</span></span> <span data-ttu-id="0b7d0-112">Verranno impostati o cancellati solo i valori specificati in questa maschera.</span><span class="sxs-lookup"><span data-stu-id="0b7d0-112">Only the values specified in this mask will be set or cleared.</span></span> <span data-ttu-id="0b7d0-113">In questo modo è possibile impostare o cancellare un flag singolo senza leggere gli Stati del flag corrente.</span><span class="sxs-lookup"><span data-stu-id="0b7d0-113">This allows a single flag to be set or cleared without reading the current flag states.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0b7d0-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0b7d0-114">Return value</span></span>

<span data-ttu-id="0b7d0-115">Il valore restituito è lo stato dei flag di stile di modifica estesa dopo che Rich Edit ha tentato di implementare le modifiche dello stile di modifica.</span><span class="sxs-lookup"><span data-stu-id="0b7d0-115">The return value is the state of the extended edit style flags after rich edit has attempted to implement your edit style changes.</span></span> <span data-ttu-id="0b7d0-116">I flag di stile di modifica sono un set di flag che indicano lo stile di modifica corrente.</span><span class="sxs-lookup"><span data-stu-id="0b7d0-116">The edit style flags are a set of flags that indicate the current edit style.</span></span>

## <a name="requirements"></a><span data-ttu-id="0b7d0-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0b7d0-117">Requirements</span></span>



| <span data-ttu-id="0b7d0-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="0b7d0-118">Requirement</span></span> | <span data-ttu-id="0b7d0-119">Valore</span><span class="sxs-lookup"><span data-stu-id="0b7d0-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0b7d0-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0b7d0-120">Minimum supported client</span></span><br/> | <span data-ttu-id="0b7d0-121">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="0b7d0-121">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="0b7d0-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0b7d0-122">Minimum supported server</span></span><br/> | <span data-ttu-id="0b7d0-123">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="0b7d0-123">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0b7d0-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0b7d0-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="0b7d0-125"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="0b7d0-125"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0b7d0-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0b7d0-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b7d0-127">**\_GETEDITSTYLEEX em**</span><span class="sxs-lookup"><span data-stu-id="0b7d0-127">**EM\_GETEDITSTYLEEX**</span></span>](em-geteditstyleex.md)
</dt> </dl>

 

