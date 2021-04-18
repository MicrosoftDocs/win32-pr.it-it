---
title: Codice di notifica RBN_AUTOSIZE (COMmctrl. h)
description: Inviato da un controllo Rebar creato con lo \_ stile AUTOSIZE di RBS quando il Rebar viene ridimensionato automaticamente. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: d174fe99-13cc-404c-9dc5-d5a93e9807a2
keywords:
- Controlli di Windows per il codice di notifica RBN_AUTOSIZE
topic_type:
- apiref
api_name:
- RBN_AUTOSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18ecfac5a4f84d69d444c25a24956cb911fd90a4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302641"
---
# <a name="rbn_autosize-notification-code"></a><span data-ttu-id="99146-105">\_Codice di notifica AUTOSIZE RBN</span><span class="sxs-lookup"><span data-stu-id="99146-105">RBN\_AUTOSIZE notification code</span></span>

<span data-ttu-id="99146-106">Inviato da un controllo Rebar creato con lo [**stile \_ AUTOSIZE di RBS**](rebar-control-styles.md) quando il Rebar viene ridimensionato automaticamente.</span><span class="sxs-lookup"><span data-stu-id="99146-106">Sent by a rebar control created with the [**RBS\_AUTOSIZE**](rebar-control-styles.md) style when the rebar automatically resizes itself.</span></span> <span data-ttu-id="99146-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="99146-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
RBN_AUTOSIZE

    lpnmas = (LPNMRBAUTOSIZE) lParam;
```



## <a name="parameters"></a><span data-ttu-id="99146-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="99146-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="99146-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="99146-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="99146-110">Puntatore a una struttura [**NMRBAUTOSIZE**](/windows/win32/api/commctrl/ns-commctrl-nmrbautosize) che contiene informazioni sull'operazione di ridimensionamento.</span><span class="sxs-lookup"><span data-stu-id="99146-110">Pointer to an [**NMRBAUTOSIZE**](/windows/win32/api/commctrl/ns-commctrl-nmrbautosize) structure that contains information about the resize operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="99146-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="99146-111">Return value</span></span>

<span data-ttu-id="99146-112">Il valore restituito per questa notifica non viene utilizzato.</span><span class="sxs-lookup"><span data-stu-id="99146-112">The return value for this notification is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="99146-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="99146-113">Requirements</span></span>



| <span data-ttu-id="99146-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="99146-114">Requirement</span></span> | <span data-ttu-id="99146-115">Valore</span><span class="sxs-lookup"><span data-stu-id="99146-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="99146-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="99146-116">Minimum supported client</span></span><br/> | <span data-ttu-id="99146-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="99146-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="99146-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="99146-118">Minimum supported server</span></span><br/> | <span data-ttu-id="99146-119">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="99146-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="99146-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="99146-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="99146-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="99146-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





