---
title: Messaggio SB_SETTIPTEXT (COMmctrl. h)
description: Imposta il testo della descrizione comando per una parte in una barra di stato. La barra di stato deve essere stata creata con lo \_ stile SBT Tooltips per abilitare le descrizioni comandi.
ms.assetid: 8fc3cc00-9742-4861-b2c2-b8aa30f75aaa
keywords:
- Controlli di Windows Message SB_SETTIPTEXT
topic_type:
- apiref
api_name:
- SB_SETTIPTEXT
- SB_SETTIPTEXTA
- SB_SETTIPTEXTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 52d5ddb3f4fdfe18525e2b444438295f8a926180
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478095"
---
# <a name="sb_settiptext-message"></a><span data-ttu-id="ca4fe-105">\_Messaggio SETTIPTEXT SB</span><span class="sxs-lookup"><span data-stu-id="ca4fe-105">SB\_SETTIPTEXT message</span></span>

<span data-ttu-id="ca4fe-106">Imposta il testo della descrizione comando per una parte in una barra di stato.</span><span class="sxs-lookup"><span data-stu-id="ca4fe-106">Sets the tooltip text for a part in a status bar.</span></span> <span data-ttu-id="ca4fe-107">La barra di stato deve essere stata creata con lo stile [**SBT \_ Tooltips**](status-bar-styles.md) per abilitare le descrizioni comandi.</span><span class="sxs-lookup"><span data-stu-id="ca4fe-107">The status bar must have been created with the [**SBT\_TOOLTIPS**](status-bar-styles.md) style to enable tooltips.</span></span>

## <a name="parameters"></a><span data-ttu-id="ca4fe-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="ca4fe-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ca4fe-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ca4fe-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ca4fe-110">Indice in base zero della parte che riceverà il testo della descrizione comando.</span><span class="sxs-lookup"><span data-stu-id="ca4fe-110">Zero-based index of the part that will receive the tooltip text.</span></span>

</dd> <dt>

<span data-ttu-id="ca4fe-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ca4fe-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ca4fe-112">Puntatore a un buffer di caratteri che contiene il nuovo testo della descrizione comando.</span><span class="sxs-lookup"><span data-stu-id="ca4fe-112">Pointer to a character buffer that contains the new tooltip text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ca4fe-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ca4fe-113">Return value</span></span>

<span data-ttu-id="ca4fe-114">Il valore restituito non viene utilizzato.</span><span class="sxs-lookup"><span data-stu-id="ca4fe-114">The return value is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="ca4fe-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="ca4fe-115">Remarks</span></span>

<span data-ttu-id="ca4fe-116">Questo testo della descrizione comando viene visualizzato in due situazioni:</span><span class="sxs-lookup"><span data-stu-id="ca4fe-116">This tooltip text is displayed in two situations:</span></span>

-   <span data-ttu-id="ca4fe-117">Quando il riquadro corrispondente nella barra di stato contiene solo un'icona.</span><span class="sxs-lookup"><span data-stu-id="ca4fe-117">When the corresponding pane in the status bar contains only an icon.</span></span>
-   <span data-ttu-id="ca4fe-118">Quando il riquadro corrispondente nella barra di stato contiene testo troncato a causa delle dimensioni del riquadro.</span><span class="sxs-lookup"><span data-stu-id="ca4fe-118">When the corresponding pane in the status bar contains text that is truncated due to the size of the pane.</span></span>

## <a name="requirements"></a><span data-ttu-id="ca4fe-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ca4fe-119">Requirements</span></span>



| <span data-ttu-id="ca4fe-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="ca4fe-120">Requirement</span></span> | <span data-ttu-id="ca4fe-121">Valore</span><span class="sxs-lookup"><span data-stu-id="ca4fe-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ca4fe-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ca4fe-122">Minimum supported client</span></span><br/> | <span data-ttu-id="ca4fe-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ca4fe-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ca4fe-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ca4fe-124">Minimum supported server</span></span><br/> | <span data-ttu-id="ca4fe-125">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ca4fe-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ca4fe-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ca4fe-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="ca4fe-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ca4fe-127"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="ca4fe-128">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="ca4fe-128">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="ca4fe-129">**SB \_ SETTIPTEXTW** (Unicode) e **SB \_ SETTIPTEXTA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="ca4fe-129">**SB\_SETTIPTEXTW** (Unicode) and **SB\_SETTIPTEXTA** (ANSI)</span></span><br/>               |



 

 





