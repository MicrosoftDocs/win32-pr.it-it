---
title: Messaggio TDM_CLICK_RADIO_BUTTON (COMmctrl. h)
description: Simula l'azione di un pulsante di opzione fare clic in una finestra di dialogo attività.
ms.assetid: ad1616fc-f64d-4575-8bd1-7ce63185d725
keywords:
- Controlli di Windows Message TDM_CLICK_RADIO_BUTTON
topic_type:
- apiref
api_name:
- TDM_CLICK_RADIO_BUTTON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b76d465b1b937359a3d312a401914d497f9c9b22
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964851"
---
# <a name="tdm_click_radio_button-message"></a><span data-ttu-id="3a4ce-104">TDM \_ fare clic sul \_ pulsante di opzione \_</span><span class="sxs-lookup"><span data-stu-id="3a4ce-104">TDM\_CLICK\_RADIO\_BUTTON message</span></span>

<span data-ttu-id="3a4ce-105">Simula l'azione di un pulsante di opzione fare clic in una finestra di dialogo attività.</span><span class="sxs-lookup"><span data-stu-id="3a4ce-105">Simulates the action of a radio button click in a task dialog.</span></span>

## <a name="parameters"></a><span data-ttu-id="3a4ce-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="3a4ce-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3a4ce-107">*wParam* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3a4ce-107">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a4ce-108">Valore **int** che specifica l'ID del pulsante di opzione su cui fare clic.</span><span class="sxs-lookup"><span data-stu-id="3a4ce-108">An **int** value that specifies the ID of the radio button to be clicked.</span></span>

</dd> <dt>

<span data-ttu-id="3a4ce-109">*lParam* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3a4ce-109">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a4ce-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="3a4ce-110">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3a4ce-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3a4ce-111">Return value</span></span>

<span data-ttu-id="3a4ce-112">Il valore restituito viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="3a4ce-112">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="3a4ce-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="3a4ce-113">Remarks</span></span>

<span data-ttu-id="3a4ce-114">L'ID del pulsante di opzione specificato viene inviato alla funzione di callback [**TaskDialogCallbackProc**](/windows/win32/api/commctrl/nc-commctrl-pftaskdialogcallback) come parte di un [pulsante di \_ opzione TDN \_ \_ selezionato](tdn-radio-button-clicked.md) .</span><span class="sxs-lookup"><span data-stu-id="3a4ce-114">The specified radio button ID is sent to the [**TaskDialogCallbackProc**](/windows/win32/api/commctrl/nc-commctrl-pftaskdialogcallback) callback function as part of a [TDN\_RADIO\_BUTTON\_CLICKED](tdn-radio-button-clicked.md) notification code.</span></span> <span data-ttu-id="3a4ce-115">Dopo che la funzione di callback viene restituita, il pulsante di opzione verrà selezionato.</span><span class="sxs-lookup"><span data-stu-id="3a4ce-115">After the callback function returns, the radio button will be selected.</span></span>

## <a name="requirements"></a><span data-ttu-id="3a4ce-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3a4ce-116">Requirements</span></span>



| <span data-ttu-id="3a4ce-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="3a4ce-117">Requirement</span></span> | <span data-ttu-id="3a4ce-118">Valore</span><span class="sxs-lookup"><span data-stu-id="3a4ce-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3a4ce-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3a4ce-119">Minimum supported client</span></span><br/> | <span data-ttu-id="3a4ce-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3a4ce-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3a4ce-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3a4ce-121">Minimum supported server</span></span><br/> | <span data-ttu-id="3a4ce-122">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="3a4ce-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3a4ce-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3a4ce-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="3a4ce-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="3a4ce-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

