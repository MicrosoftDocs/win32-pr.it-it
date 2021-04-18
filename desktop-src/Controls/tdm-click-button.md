---
title: Messaggio TDM_CLICK_BUTTON (COMmctrl. h)
description: Simula l'azione di un clic su un pulsante in una finestra di dialogo attività.
ms.assetid: cc8a8252-3418-4a28-bfb7-11d6e3fee903
keywords:
- Controlli di Windows Message TDM_CLICK_BUTTON
topic_type:
- apiref
api_name:
- TDM_CLICK_BUTTON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e5933668eca907f36414113091b8901bfb9c110
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301660"
---
# <a name="tdm_click_button-message"></a><span data-ttu-id="c65cf-104">Messaggio del pulsante di \_ clic TDM \_</span><span class="sxs-lookup"><span data-stu-id="c65cf-104">TDM\_CLICK\_BUTTON message</span></span>

<span data-ttu-id="c65cf-105">Simula l'azione di un clic su un pulsante in una finestra di dialogo attività.</span><span class="sxs-lookup"><span data-stu-id="c65cf-105">Simulates the action of a button click in a task dialog.</span></span>

## <a name="parameters"></a><span data-ttu-id="c65cf-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="c65cf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c65cf-107">*wParam* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c65cf-107">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c65cf-108">**Integer** che specifica l'ID del pulsante su cui fare clic.</span><span class="sxs-lookup"><span data-stu-id="c65cf-108">An **int** that specifies the ID of the button to be clicked.</span></span>

</dd> <dt>

<span data-ttu-id="c65cf-109">*lParam* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c65cf-109">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c65cf-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="c65cf-110">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c65cf-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c65cf-111">Return value</span></span>

<span data-ttu-id="c65cf-112">Il valore restituito viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="c65cf-112">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="c65cf-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="c65cf-113">Remarks</span></span>

<span data-ttu-id="c65cf-114">L'ID del pulsante specificato da *wParam* viene inviato alla funzione di callback [**TaskDialogCallbackProc**](/windows/win32/api/commctrl/nc-commctrl-pftaskdialogcallback) come parte di un pulsante TDN che ha [ \_ \_ fatto clic sul](tdn-button-clicked.md) codice di notifica.</span><span class="sxs-lookup"><span data-stu-id="c65cf-114">The button ID specified by *wParam* is sent to the [**TaskDialogCallbackProc**](/windows/win32/api/commctrl/nc-commctrl-pftaskdialogcallback) callback function as part of a [TDN\_BUTTON\_CLICKED](tdn-button-clicked.md) notification code.</span></span> <span data-ttu-id="c65cf-115">Una volta restituita la funzione di callback, la finestra di dialogo attività viene chiusa se \_ dalla funzione di callback viene restituito S OK.</span><span class="sxs-lookup"><span data-stu-id="c65cf-115">After the callback function returns, the task dialog is closed if S\_OK was returned from the callback function.</span></span> <span data-ttu-id="c65cf-116">Se \_ dalla funzione di callback viene restituito S false, la finestra di dialogo attività rimane attiva.</span><span class="sxs-lookup"><span data-stu-id="c65cf-116">If S\_FALSE was returned from the callback function, the task dialog remains active.</span></span>

## <a name="requirements"></a><span data-ttu-id="c65cf-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c65cf-117">Requirements</span></span>



| <span data-ttu-id="c65cf-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="c65cf-118">Requirement</span></span> | <span data-ttu-id="c65cf-119">Valore</span><span class="sxs-lookup"><span data-stu-id="c65cf-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c65cf-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c65cf-120">Minimum supported client</span></span><br/> | <span data-ttu-id="c65cf-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c65cf-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c65cf-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c65cf-122">Minimum supported server</span></span><br/> | <span data-ttu-id="c65cf-123">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c65cf-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c65cf-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c65cf-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="c65cf-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="c65cf-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

