---
title: Codice di notifica RBN_CHEVRONPUSHED (COMmctrl. h)
description: Inviato da un controllo Rebar quando viene eseguito il push di una freccia di espansione. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 58aa2c9d-8ab6-46ee-b32f-5c04fb7afa84
keywords:
- Controlli di Windows per il codice di notifica RBN_CHEVRONPUSHED
topic_type:
- apiref
api_name:
- RBN_CHEVRONPUSHED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab28d992b6d4a617b7aa7ee144eb50aef3b0e834
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048344"
---
# <a name="rbn_chevronpushed-notification-code"></a><span data-ttu-id="1048e-105">\_Codice di notifica CHEVRONPUSHED di RBN</span><span class="sxs-lookup"><span data-stu-id="1048e-105">RBN\_CHEVRONPUSHED notification code</span></span>

<span data-ttu-id="1048e-106">Inviato da un controllo Rebar quando viene eseguito il push di una freccia di espansione.</span><span class="sxs-lookup"><span data-stu-id="1048e-106">Sent by a rebar control when a chevron is pushed.</span></span> <span data-ttu-id="1048e-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="1048e-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
RBN_CHEVRONPUSHED

    lpnm = (NMREBARCHEVRON) lParam;
```



## <a name="parameters"></a><span data-ttu-id="1048e-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="1048e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1048e-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1048e-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1048e-110">Puntatore alla struttura [**NMREBARCHEVRON**](/windows/win32/api/commctrl/ns-commctrl-nmrebarchevron) della banda.</span><span class="sxs-lookup"><span data-stu-id="1048e-110">Pointer to the band's [**NMREBARCHEVRON**](/windows/win32/api/commctrl/ns-commctrl-nmrebarchevron) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1048e-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1048e-111">Return value</span></span>

<span data-ttu-id="1048e-112">Il valore restituito per questa notifica non viene utilizzato.</span><span class="sxs-lookup"><span data-stu-id="1048e-112">The return value for this notification is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="1048e-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="1048e-113">Remarks</span></span>

<span data-ttu-id="1048e-114">Quando un'applicazione riceve il codice di notifica, è responsabile della visualizzazione di un menu popup con elementi per ogni strumento nascosto.</span><span class="sxs-lookup"><span data-stu-id="1048e-114">When an application receives this notification code, it is responsible for displaying a popup menu with items for each hidden tool.</span></span> <span data-ttu-id="1048e-115">Usare il membro **RC** della struttura [**NMREBARCHEVRON**](/windows/win32/api/commctrl/ns-commctrl-nmrebarchevron) per trovare la posizione corretta per il menu di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="1048e-115">Use the **rc** member of the [**NMREBARCHEVRON**](/windows/win32/api/commctrl/ns-commctrl-nmrebarchevron) structure to find the correct position for the popup menu.</span></span>

## <a name="requirements"></a><span data-ttu-id="1048e-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1048e-116">Requirements</span></span>



| <span data-ttu-id="1048e-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="1048e-117">Requirement</span></span> | <span data-ttu-id="1048e-118">Valore</span><span class="sxs-lookup"><span data-stu-id="1048e-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1048e-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1048e-119">Minimum supported client</span></span><br/> | <span data-ttu-id="1048e-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1048e-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1048e-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1048e-121">Minimum supported server</span></span><br/> | <span data-ttu-id="1048e-122">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="1048e-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1048e-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1048e-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="1048e-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="1048e-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





