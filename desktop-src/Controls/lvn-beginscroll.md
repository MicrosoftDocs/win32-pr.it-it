---
title: Codice di notifica LVN_BEGINSCROLL (COMmctrl. h)
description: Notifica alla finestra padre di un controllo di visualizzazione elenco quando viene avviata un'operazione di scorrimento. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 67123db1-118c-43d7-8511-12a3c4413958
keywords:
- Controlli di Windows per il codice di notifica LVN_BEGINSCROLL
topic_type:
- apiref
api_name:
- LVN_BEGINSCROLL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae09a05525ac6e9f08d8cc7a0b7de6ef51329baa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475364"
---
# <a name="lvn_beginscroll-notification-code"></a><span data-ttu-id="d9020-105">\_Codice di notifica BEGINSCROLL di LVN</span><span class="sxs-lookup"><span data-stu-id="d9020-105">LVN\_BEGINSCROLL notification code</span></span>

<span data-ttu-id="d9020-106">Notifica alla finestra padre di un controllo di visualizzazione elenco quando viene avviata un'operazione di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="d9020-106">Notifies a list-view control's parent window when a scrolling operation starts.</span></span> <span data-ttu-id="d9020-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="d9020-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_BEGINSCROLL

    pnmLVScroll = (LPNMLVSCROLL) lParam;
```



## <a name="parameters"></a><span data-ttu-id="d9020-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="d9020-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d9020-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d9020-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d9020-110">Puntatore a una struttura [**NMLVSCROLL**](/windows/win32/api/commctrl/ns-commctrl-nmlvscroll) che contiene la posizione orizzontale o verticale della posizione in cui inizia l'operazione di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="d9020-110">Pointer to a [**NMLVSCROLL**](/windows/win32/api/commctrl/ns-commctrl-nmlvscroll) structure that contains the horizontal or vertical position of where the scroll operation starts.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d9020-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d9020-111">Return value</span></span>

<span data-ttu-id="d9020-112">Valore restituito non utilizzato.</span><span class="sxs-lookup"><span data-stu-id="d9020-112">Return value not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="d9020-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="d9020-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="d9020-114">Per usare questo codice di notifica, è necessario fornire un manifesto che specifichi Comclt32.dll versione 6,0.</span><span class="sxs-lookup"><span data-stu-id="d9020-114">To use this notification code, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="d9020-115">Per altre informazioni sui manifesti, vedere [Abilitazione degli stili di visualizzazione](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="d9020-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="d9020-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d9020-116">Requirements</span></span>



| <span data-ttu-id="d9020-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="d9020-117">Requirement</span></span> | <span data-ttu-id="d9020-118">Valore</span><span class="sxs-lookup"><span data-stu-id="d9020-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d9020-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d9020-119">Minimum supported client</span></span><br/> | <span data-ttu-id="d9020-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d9020-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d9020-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d9020-121">Minimum supported server</span></span><br/> | <span data-ttu-id="d9020-122">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d9020-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d9020-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d9020-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="d9020-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d9020-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





