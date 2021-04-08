---
title: Codice di notifica TBN_GETINFOTIP (COMmctrl. h)
description: Recupera le informazioni infotip per un elemento della barra degli strumenti. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 877de60c-f6e1-440a-81f0-d66ab443c985
keywords:
- Controlli di Windows per il codice di notifica TBN_GETINFOTIP
topic_type:
- apiref
api_name:
- TBN_GETINFOTIP
- TBN_GETINFOTIPA
- TBN_GETINFOTIPW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fda2c1b181ebea1840b153b8b2df8328b3f2cc8d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048109"
---
# <a name="tbn_getinfotip-notification-code"></a><span data-ttu-id="1b438-105">\_Codice di notifica GETINFOTIP di TBN</span><span class="sxs-lookup"><span data-stu-id="1b438-105">TBN\_GETINFOTIP notification code</span></span>

<span data-ttu-id="1b438-106">Recupera le informazioni infotip per un elemento della barra degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="1b438-106">Retrieves infotip information for a toolbar item.</span></span> <span data-ttu-id="1b438-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="1b438-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TBN_GETINFOTIP

    lptbgit = (LPNMTBGETINFOTIP) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="1b438-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="1b438-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1b438-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1b438-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1b438-110">Puntatore a una struttura [**NMTBGETINFOTIP**](/windows/win32/api/commctrl/ns-commctrl-nmtbgetinfotipa) che contiene informazioni sull'elemento e riceve informazioni infotip.</span><span class="sxs-lookup"><span data-stu-id="1b438-110">Pointer to an [**NMTBGETINFOTIP**](/windows/win32/api/commctrl/ns-commctrl-nmtbgetinfotipa) structure that contains item information and receives infotip information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1b438-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1b438-111">Return value</span></span>

<span data-ttu-id="1b438-112">Il valore restituito viene ignorato dal controllo.</span><span class="sxs-lookup"><span data-stu-id="1b438-112">The return value is ignored by the control.</span></span>

## <a name="remarks"></a><span data-ttu-id="1b438-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="1b438-113">Remarks</span></span>

<span data-ttu-id="1b438-114">Il supporto infotip sulla barra degli strumenti consente alla barra degli strumenti di visualizzare le descrizioni comandi per gli elementi con dimensioni pari a INFOTIPSIZE caratteri.</span><span class="sxs-lookup"><span data-stu-id="1b438-114">The infotip support in the toolbar allows the toolbar to display tooltips for items that are as large as INFOTIPSIZE characters.</span></span> <span data-ttu-id="1b438-115">Se il codice di notifica non viene elaborato, la barra degli strumenti utilizzerà il testo dell'elemento per infotip.</span><span class="sxs-lookup"><span data-stu-id="1b438-115">If this notification code is not processed, the toolbar will use the item's text for the infotip.</span></span>

## <a name="requirements"></a><span data-ttu-id="1b438-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1b438-116">Requirements</span></span>



| <span data-ttu-id="1b438-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="1b438-117">Requirement</span></span> | <span data-ttu-id="1b438-118">Valore</span><span class="sxs-lookup"><span data-stu-id="1b438-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1b438-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1b438-119">Minimum supported client</span></span><br/> | <span data-ttu-id="1b438-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1b438-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1b438-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1b438-121">Minimum supported server</span></span><br/> | <span data-ttu-id="1b438-122">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="1b438-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1b438-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1b438-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="1b438-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="1b438-124"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="1b438-125">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="1b438-125">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="1b438-126">**TBN \_ GETINFOTIPW** (Unicode) e **TBN \_ GETINFOTIPA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="1b438-126">**TBN\_GETINFOTIPW** (Unicode) and **TBN\_GETINFOTIPA** (ANSI)</span></span><br/>             |



 

 





