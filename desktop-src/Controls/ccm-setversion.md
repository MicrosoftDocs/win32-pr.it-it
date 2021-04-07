---
title: Messaggio CCM_SETVERSION (COMmctrl. h)
description: Questo messaggio viene usato per informare il controllo che si prevede un comportamento associato a una particolare versione.
ms.assetid: f87b20bc-0139-4d0a-b38c-32c75743d6f6
keywords:
- Controlli di Windows Message CCM_SETVERSION
topic_type:
- apiref
api_name:
- CCM_SETVERSION
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 349935173c41cd9c90a016ef3d2f3c77df8f159c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048526"
---
# <a name="ccm_setversion-message"></a><span data-ttu-id="354d7-104">\_Messaggio della versione CCM</span><span class="sxs-lookup"><span data-stu-id="354d7-104">CCM\_SETVERSION message</span></span>

<span data-ttu-id="354d7-105">Questo messaggio viene usato per informare il controllo che si prevede un comportamento associato a una particolare versione.</span><span class="sxs-lookup"><span data-stu-id="354d7-105">This message is used to inform the control that you are expecting a behavior associated with a particular version.</span></span>

## <a name="parameters"></a><span data-ttu-id="354d7-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="354d7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="354d7-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="354d7-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="354d7-108">Numero di versione.</span><span class="sxs-lookup"><span data-stu-id="354d7-108">The version number.</span></span>

</dd> <dt>

<span data-ttu-id="354d7-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="354d7-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="354d7-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="354d7-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="354d7-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="354d7-111">Return value</span></span>

<span data-ttu-id="354d7-112">Restituisce la versione specificata nel messaggio precedente **della \_ versione CCM** .</span><span class="sxs-lookup"><span data-stu-id="354d7-112">Returns the version specified in the previous **CCM\_SETVERSION** message.</span></span> <span data-ttu-id="354d7-113">Se *wParam* è impostato su un valore maggiore della versione della dll corrente, restituisce-1.</span><span class="sxs-lookup"><span data-stu-id="354d7-113">If *wParam* is set to a value greater than the current DLL version, it returns -1.</span></span>

## <a name="remarks"></a><span data-ttu-id="354d7-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="354d7-114">Remarks</span></span>

<span data-ttu-id="354d7-115">In alcuni casi, un controllo può comportarsi in modo diverso, a seconda della versione.</span><span class="sxs-lookup"><span data-stu-id="354d7-115">In a few cases, a control may behave differently, depending on the version.</span></span> <span data-ttu-id="354d7-116">Questo vale principalmente per i bug risolti nelle versioni successive.</span><span class="sxs-lookup"><span data-stu-id="354d7-116">This primarily applies to bugs that were fixed in later versions.</span></span> <span data-ttu-id="354d7-117">Il messaggio della **\_ versione CCM** consente di informare il controllo del comportamento previsto.</span><span class="sxs-lookup"><span data-stu-id="354d7-117">The **CCM\_SETVERSION** message enables you to inform the control which behavior is expected.</span></span> <span data-ttu-id="354d7-118">È possibile determinare la versione specificata inviando un messaggio [**CCM \_ GetVersion**](ccm-getversion.md) .</span><span class="sxs-lookup"><span data-stu-id="354d7-118">You can determine which version you have specified by sending a [**CCM\_GETVERSION**](ccm-getversion.md) message.</span></span> <span data-ttu-id="354d7-119">Per un esempio di come usare questo messaggio, vedere [Custom disegnato With List-View and Tree-View Controls](custom-draw.md).</span><span class="sxs-lookup"><span data-stu-id="354d7-119">For an example of how to use this message, see [Custom Draw With List-View and Tree-View Controls](custom-draw.md).</span></span>

<span data-ttu-id="354d7-120">Se ComCtl32.dll versione 6 è installata, indipendentemente dal valore impostato in *wParam*, il messaggio della versione **CCM \_** restituisce la versione 6.</span><span class="sxs-lookup"><span data-stu-id="354d7-120">If you have ComCtl32.dll version 6 installed, regardless of what value you set in *wParam*, the **CCM\_SETVERSION** message returns version 6.</span></span>

> [!Note]  
> <span data-ttu-id="354d7-121">Questo messaggio consente di impostare solo il numero di versione per il controllo a cui viene inviato.</span><span class="sxs-lookup"><span data-stu-id="354d7-121">This message only sets the version number for the control to which it is sent.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="354d7-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="354d7-122">Requirements</span></span>



| <span data-ttu-id="354d7-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="354d7-123">Requirement</span></span> | <span data-ttu-id="354d7-124">Valore</span><span class="sxs-lookup"><span data-stu-id="354d7-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="354d7-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="354d7-125">Minimum supported client</span></span><br/> | <span data-ttu-id="354d7-126">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="354d7-126">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="354d7-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="354d7-127">Minimum supported server</span></span><br/> | <span data-ttu-id="354d7-128">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="354d7-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="354d7-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="354d7-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="354d7-130"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="354d7-130"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





