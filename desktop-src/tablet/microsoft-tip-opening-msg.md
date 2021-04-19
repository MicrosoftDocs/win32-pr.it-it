---
description: Notifica alla finestra l'apertura del pannello input di testo.
ms.assetid: 6eadd648-bffb-4227-bdcd-cd733f692734
title: Messaggio di MICROSOFT_TIP_OPENING_MSG (PenInputPanel. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f0938b8a00e39f54817b8ec52e86e00aae52111
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333224"
---
# <a name="microsoft_tip_opening_msg-message"></a><span data-ttu-id="92187-103">\_Messaggio di \_ apertura \_ messaggio Microsoft Tip</span><span class="sxs-lookup"><span data-stu-id="92187-103">MICROSOFT\_TIP\_OPENING\_MSG message</span></span>

<span data-ttu-id="92187-104">Notifica alla finestra l'apertura del pannello input di testo.</span><span class="sxs-lookup"><span data-stu-id="92187-104">Notifies the window when the Text Input Panel is opening.</span></span>

## <a name="parameters"></a><span data-ttu-id="92187-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="92187-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="92187-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="92187-106">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="92187-107">Attualmente non utilizzato, deve essere **null**.</span><span class="sxs-lookup"><span data-stu-id="92187-107">Currently not used, should be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="92187-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="92187-108">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="92187-109">Attualmente non utilizzato, deve essere **null**.</span><span class="sxs-lookup"><span data-stu-id="92187-109">Currently not used, should be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="92187-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="92187-110">Return value</span></span>

<span data-ttu-id="92187-111">Le applicazioni devono chiamare [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) dopo aver gestito questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="92187-111">Applications should call [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) after handling this message.</span></span> <span data-ttu-id="92187-112">Per informazioni sui valori restituiti, vedere **DefWindowProc** .</span><span class="sxs-lookup"><span data-stu-id="92187-112">See **DefWindowProc** for information about its return values.</span></span>

## <a name="remarks"></a><span data-ttu-id="92187-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="92187-113">Remarks</span></span>

<span data-ttu-id="92187-114">Questa notifica consente di stabilire quando il pannello di input viene aperto.</span><span class="sxs-lookup"><span data-stu-id="92187-114">This notification lets you know when the input panel is opening.</span></span> <span data-ttu-id="92187-115">Se si desidera eseguire un'azione quando si verifica questo problema, gestire il messaggio, eseguire l'operazione nel gestore e quindi passare il messaggio a [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).</span><span class="sxs-lookup"><span data-stu-id="92187-115">If you want to perform an action when this happens, handle the message, perform your operation in the handler, and then pass on the message to [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).</span></span>

> [!Note]  
> <span data-ttu-id="92187-116">Questo messaggio viene inviato anche quando il pannello input di testo è già visibile e l'utente passa dalla tastiera all'interfaccia della grafia.</span><span class="sxs-lookup"><span data-stu-id="92187-116">This message is also sent when the Text Input Panel is already visible and the user switches from the keyboard to the handwriting skin.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="92187-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="92187-117">Requirements</span></span>



| <span data-ttu-id="92187-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="92187-118">Requirement</span></span> | <span data-ttu-id="92187-119">Valore</span><span class="sxs-lookup"><span data-stu-id="92187-119">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="92187-120">Client</span><span class="sxs-lookup"><span data-stu-id="92187-120">Client</span></span><br/> | <span data-ttu-id="92187-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="92187-121">Windows Vista</span></span><br/>                                                                   |
| <span data-ttu-id="92187-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="92187-122">Header</span></span><br/> | <dl> <span data-ttu-id="92187-123"><dt>PenInputPanel. h</dt></span><span class="sxs-lookup"><span data-stu-id="92187-123"><dt>Peninputpanel.h</dt></span></span> </dl> |



 

