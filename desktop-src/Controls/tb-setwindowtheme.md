---
title: Messaggio TB_SETWINDOWTHEME (COMmctrl. h)
description: Imposta lo stile di visualizzazione di un controllo Toolbar.
ms.assetid: 8b05c561-af66-47e7-8ef3-7f9f81da4840
keywords:
- Controlli di Windows Message TB_SETWINDOWTHEME
topic_type:
- apiref
api_name:
- TB_SETWINDOWTHEME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e0c293e974eee2e7827225efb06cc439fdf2c39
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121706"
---
# <a name="tb_setwindowtheme-message"></a><span data-ttu-id="1fc3e-104">TB \_ SETWINDOWTHEME messaggio</span><span class="sxs-lookup"><span data-stu-id="1fc3e-104">TB\_SETWINDOWTHEME message</span></span>

<span data-ttu-id="1fc3e-105">Imposta lo stile di visualizzazione di un controllo Toolbar.</span><span class="sxs-lookup"><span data-stu-id="1fc3e-105">Sets the visual style of a toolbar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="1fc3e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="1fc3e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1fc3e-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1fc3e-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="1fc3e-108">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="1fc3e-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="1fc3e-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1fc3e-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1fc3e-110">Puntatore a una stringa Unicode che contiene lo stile di visualizzazione della barra degli strumenti da impostare.</span><span class="sxs-lookup"><span data-stu-id="1fc3e-110">Pointer to a Unicode string that contains the toolbar visual style to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1fc3e-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1fc3e-111">Return value</span></span>

<span data-ttu-id="1fc3e-112">Il valore restituito non viene utilizzato.</span><span class="sxs-lookup"><span data-stu-id="1fc3e-112">The return value is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="1fc3e-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="1fc3e-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="1fc3e-114">Per utilizzare questo messaggio, è necessario fornire un manifesto che specifichi Comclt32.dll versione 6,0.</span><span class="sxs-lookup"><span data-stu-id="1fc3e-114">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="1fc3e-115">Per altre informazioni sui manifesti, vedere [Abilitazione degli stili di visualizzazione](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="1fc3e-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

<span data-ttu-id="1fc3e-116">L'invio di questo messaggio equivale alla chiamata di [**SetWindowTheme**](/windows/desktop/api/Uxtheme/nf-uxtheme-setwindowtheme) sulla barra degli strumenti e del relativo controllo ToolTip, se disponibile.</span><span class="sxs-lookup"><span data-stu-id="1fc3e-116">Sending this message is equivalent to calling [**SetWindowTheme**](/windows/desktop/api/Uxtheme/nf-uxtheme-setwindowtheme) on the toolbar and its tooltip control, if any.</span></span>

## <a name="requirements"></a><span data-ttu-id="1fc3e-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1fc3e-117">Requirements</span></span>



| <span data-ttu-id="1fc3e-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="1fc3e-118">Requirement</span></span> | <span data-ttu-id="1fc3e-119">Valore</span><span class="sxs-lookup"><span data-stu-id="1fc3e-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1fc3e-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1fc3e-120">Minimum supported client</span></span><br/> | <span data-ttu-id="1fc3e-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1fc3e-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1fc3e-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1fc3e-122">Minimum supported server</span></span><br/> | <span data-ttu-id="1fc3e-123">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="1fc3e-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1fc3e-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1fc3e-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="1fc3e-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="1fc3e-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





