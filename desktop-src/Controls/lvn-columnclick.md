---
title: Codice di notifica LVN_COLUMNCLICK (COMmctrl. h)
description: Notifica alla finestra padre di un controllo di visualizzazione elenco che è stata fatto clic su un'intestazione di colonna mentre il controllo elenco-visualizzazione era in modalità report. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: a6bfbd6c-4778-47a7-92e9-9140d46d89cc
keywords:
- Controlli di Windows per il codice di notifica LVN_COLUMNCLICK
topic_type:
- apiref
api_name:
- LVN_COLUMNCLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27cfd75d913c62c89c4cfe305333a934fe172fe2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104047926"
---
# <a name="lvn_columnclick-notification-code"></a><span data-ttu-id="2ee0a-105">\_Codice di notifica COLUMNCLICK di LVN</span><span class="sxs-lookup"><span data-stu-id="2ee0a-105">LVN\_COLUMNCLICK notification code</span></span>

<span data-ttu-id="2ee0a-106">Notifica alla finestra padre di un controllo di visualizzazione elenco che è stata fatto clic su un'intestazione di colonna mentre il controllo elenco-visualizzazione era in modalità report.</span><span class="sxs-lookup"><span data-stu-id="2ee0a-106">Notifies a list-view control's parent window that a column header was clicked while the list-view control was in report mode.</span></span> <span data-ttu-id="2ee0a-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="2ee0a-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_COLUMNCLICK

    pnmv = (LPNMLISTVIEW) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="2ee0a-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="2ee0a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2ee0a-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2ee0a-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2ee0a-110">Puntatore a una struttura [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) .</span><span class="sxs-lookup"><span data-stu-id="2ee0a-110">Pointer to an [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) structure.</span></span> <span data-ttu-id="2ee0a-111">Il membro **iItem** è-1 e il membro **iSubItem** identifica la colonna.</span><span class="sxs-lookup"><span data-stu-id="2ee0a-111">The **iItem** member is -1, and the **iSubItem** member identifies the column.</span></span> <span data-ttu-id="2ee0a-112">Tutti gli altri membri sono pari a zero.</span><span class="sxs-lookup"><span data-stu-id="2ee0a-112">All other members are zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2ee0a-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2ee0a-113">Return value</span></span>

<span data-ttu-id="2ee0a-114">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="2ee0a-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2ee0a-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="2ee0a-115">Remarks</span></span>

<span data-ttu-id="2ee0a-116">L'uso di formati di controllo intestazione, ad esempio HDF \_ CheckBox per modificare il formato delle intestazioni di colonna in un controllo visualizzazione elenco, fa sì che il controllo invii il codice di notifica [ \_ ITEMSTATEICONCLICK HDN](hdn-itemstateiconclick.md) anziché LVN \_ COLUMNCLICK quando si fa clic su un elemento di intestazione.</span><span class="sxs-lookup"><span data-stu-id="2ee0a-116">Using header control formats such as HDF\_CHECKBOX to modify the format of column headers in a list-view control causes the control to send the [HDN\_ITEMSTATEICONCLICK](hdn-itemstateiconclick.md) notification code instead of LVN\_COLUMNCLICK when a header item is clicked.</span></span>

## <a name="requirements"></a><span data-ttu-id="2ee0a-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2ee0a-117">Requirements</span></span>



| <span data-ttu-id="2ee0a-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="2ee0a-118">Requirement</span></span> | <span data-ttu-id="2ee0a-119">Valore</span><span class="sxs-lookup"><span data-stu-id="2ee0a-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2ee0a-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2ee0a-120">Minimum supported client</span></span><br/> | <span data-ttu-id="2ee0a-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2ee0a-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2ee0a-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2ee0a-122">Minimum supported server</span></span><br/> | <span data-ttu-id="2ee0a-123">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="2ee0a-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2ee0a-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2ee0a-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="2ee0a-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="2ee0a-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





