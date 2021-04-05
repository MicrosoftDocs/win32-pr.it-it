---
title: Codice di notifica RBN_GETOBJECT (COMmctrl. h)
description: Inviato da un controllo Rebar creato con lo \_ stile REGISTERDROP di RBS quando un oggetto viene trascinato su una banda nel controllo. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 057474c1-5f65-4290-973e-4366b760365a
keywords:
- Controlli di Windows per il codice di notifica RBN_GETOBJECT
topic_type:
- apiref
api_name:
- RBN_GETOBJECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a390bc5c5f74a577805ca8ae1128fbb24e6b10b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120502"
---
# <a name="rbn_getobject-notification-code"></a><span data-ttu-id="2e235-105">RBN \_ codice di notifica GETobject</span><span class="sxs-lookup"><span data-stu-id="2e235-105">RBN\_GETOBJECT notification code</span></span>

<span data-ttu-id="2e235-106">Inviato da un controllo Rebar creato con lo [**stile \_ REGISTERDROP di RBS**](rebar-control-styles.md) quando un oggetto viene trascinato su una banda nel controllo.</span><span class="sxs-lookup"><span data-stu-id="2e235-106">Sent by a rebar control created with the [**RBS\_REGISTERDROP**](rebar-control-styles.md) style when an object is dragged over a band in the control.</span></span> <span data-ttu-id="2e235-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="2e235-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
RBN_GETOBJECT

    lpnmon = (LPNMOBJECTNOTIFY) lParam;
```



## <a name="parameters"></a><span data-ttu-id="2e235-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="2e235-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2e235-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2e235-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2e235-110">Puntatore a una struttura [**NMOBJECTNOTIFY**](/windows/win32/api/commctrl/ns-commctrl-nmobjectnotify) contenente informazioni sulla banda su cui viene trascinato l'oggetto e riceve anche i dati forniti dall'applicazione ricevente in risposta a questo codice di notifica.</span><span class="sxs-lookup"><span data-stu-id="2e235-110">Pointer to an [**NMOBJECTNOTIFY**](/windows/win32/api/commctrl/ns-commctrl-nmobjectnotify) structure that contains information about the band that the object is dragged over and also receives the data provided by the receiving application in response to this notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2e235-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2e235-111">Return value</span></span>

<span data-ttu-id="2e235-112">Il valore restituito per questo codice di notifica deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="2e235-112">The return value for this notification code must be zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="2e235-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="2e235-113">Remarks</span></span>

<span data-ttu-id="2e235-114">Per ricevere il \_ codice di notifica GetObject RBN, inizializzare OLE con una chiamata a [**OleInitialize**](/windows/desktop/api/ole2/nf-ole2-oleinitialize) o [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize).</span><span class="sxs-lookup"><span data-stu-id="2e235-114">To receive the RBN\_GETOBJECT notification code, initialize OLE with a call to [**OleInitialize**](/windows/desktop/api/ole2/nf-ole2-oleinitialize) or [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize).</span></span>

## <a name="requirements"></a><span data-ttu-id="2e235-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2e235-115">Requirements</span></span>



| <span data-ttu-id="2e235-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="2e235-116">Requirement</span></span> | <span data-ttu-id="2e235-117">Valore</span><span class="sxs-lookup"><span data-stu-id="2e235-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2e235-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2e235-118">Minimum supported client</span></span><br/> | <span data-ttu-id="2e235-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2e235-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2e235-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2e235-120">Minimum supported server</span></span><br/> | <span data-ttu-id="2e235-121">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="2e235-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2e235-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2e235-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="2e235-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="2e235-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

