---
title: Codice di notifica LVN_GETINFOTIP (COMmctrl. h)
description: Inviato da un controllo di visualizzazione elenco icone grande con lo \_ stile esteso LVS ex \_ INFOTIP.
ms.assetid: 62be5087-7e49-4722-a63a-1768e030af48
keywords:
- Controlli di Windows per il codice di notifica LVN_GETINFOTIP
topic_type:
- apiref
api_name:
- LVN_GETINFOTIP
- LVN_GETINFOTIPA
- LVN_GETINFOTIPW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2b4552456a575e2f03e02b2bfb78f7fcc1d8ca1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519326"
---
# <a name="lvn_getinfotip-notification-code"></a><span data-ttu-id="aef8e-104">\_Codice di notifica GETINFOTIP di LVN</span><span class="sxs-lookup"><span data-stu-id="aef8e-104">LVN\_GETINFOTIP notification code</span></span>

<span data-ttu-id="aef8e-105">Inviato da un controllo di visualizzazione elenco icone grande con lo stile esteso [**LVS \_ ex \_ INFOTIP**](extended-list-view-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="aef8e-105">Sent by a large icon view list-view control that has the [**LVS\_EX\_INFOTIP**](extended-list-view-styles.md) extended style.</span></span> <span data-ttu-id="aef8e-106">Questo codice di notifica viene inviato quando il controllo elenco-visualizzazione richiede informazioni aggiuntive sul testo da visualizzare in una descrizione comando.</span><span class="sxs-lookup"><span data-stu-id="aef8e-106">This notification code is sent when the list-view control is requesting additional text information to be displayed in a tooltip.</span></span> <span data-ttu-id="aef8e-107">Viene inviato sotto forma di un messaggio di [**\_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="aef8e-107">It is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_GETINFOTIP

    pGetInfoTip = (LPNMLVGETINFOTIP) lParam;
```



## <a name="parameters"></a><span data-ttu-id="aef8e-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="aef8e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aef8e-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="aef8e-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="aef8e-110">Puntatore a una struttura [**NMLVGETINFOTIP**](/windows/win32/api/commctrl/ns-commctrl-nmlvgetinfotipa) che contiene informazioni su questo codice di notifica.</span><span class="sxs-lookup"><span data-stu-id="aef8e-110">Pointer to an [**NMLVGETINFOTIP**](/windows/win32/api/commctrl/ns-commctrl-nmlvgetinfotipa) structure that contains information about this notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aef8e-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="aef8e-111">Return value</span></span>

<span data-ttu-id="aef8e-112">Il valore restituito per questa notifica non viene utilizzato.</span><span class="sxs-lookup"><span data-stu-id="aef8e-112">The return value for this notification is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="aef8e-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="aef8e-113">Remarks</span></span>

<span data-ttu-id="aef8e-114">Questo codice di notifica viene inviato solo da controlli di visualizzazione elenco con stile esteso [**LVS \_ ex \_ INFOTIP**](extended-list-view-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="aef8e-114">This notification code is only sent by list-view controls that have the [**LVS\_EX\_INFOTIP**](extended-list-view-styles.md) extended style.</span></span> <span data-ttu-id="aef8e-115">Il \_ codice di notifica GETINFOTIP di LVN viene inviato solo per l'elemento secondario 0.</span><span class="sxs-lookup"><span data-stu-id="aef8e-115">The LVN\_GETINFOTIP notification code is sent only for subitem 0.</span></span>

## <a name="requirements"></a><span data-ttu-id="aef8e-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="aef8e-116">Requirements</span></span>



| <span data-ttu-id="aef8e-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="aef8e-117">Requirement</span></span> | <span data-ttu-id="aef8e-118">Valore</span><span class="sxs-lookup"><span data-stu-id="aef8e-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="aef8e-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="aef8e-119">Minimum supported client</span></span><br/> | <span data-ttu-id="aef8e-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="aef8e-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="aef8e-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="aef8e-121">Minimum supported server</span></span><br/> | <span data-ttu-id="aef8e-122">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="aef8e-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="aef8e-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="aef8e-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="aef8e-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="aef8e-124"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="aef8e-125">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="aef8e-125">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="aef8e-126">**LVN \_ GETINFOTIPW** (Unicode) e **LVN \_ GETINFOTIPA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="aef8e-126">**LVN\_GETINFOTIPW** (Unicode) and **LVN\_GETINFOTIPA** (ANSI)</span></span><br/>             |



 

 





