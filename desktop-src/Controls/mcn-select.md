---
title: Codice di notifica MCN_SELECT (COMmctrl. h)
description: Inviato da un controllo di calendario mensile quando l'utente crea una selezione di data esplicita all'interno di un controllo di calendario mensile. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 3cabb4b2-9422-4190-85d3-ab6593891e3d
keywords:
- Controlli di Windows per il codice di notifica MCN_SELECT
topic_type:
- apiref
api_name:
- MCN_SELECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9252133267b9c552542df17ed73caa8c34a69641
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104047995"
---
# <a name="mcn_select-notification-code"></a><span data-ttu-id="d7efe-105">MCN \_ selezionare il codice di notifica</span><span class="sxs-lookup"><span data-stu-id="d7efe-105">MCN\_SELECT notification code</span></span>

<span data-ttu-id="d7efe-106">Inviato da un controllo di calendario mensile quando l'utente crea una selezione di data esplicita all'interno di un controllo di calendario mensile.</span><span class="sxs-lookup"><span data-stu-id="d7efe-106">Sent by a month calendar control when the user makes an explicit date selection within a month calendar control.</span></span> <span data-ttu-id="d7efe-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="d7efe-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
MCN_SELECT

    lpNMSelChange = (LPNMSELCHANGE) lParam;
```



## <a name="parameters"></a><span data-ttu-id="d7efe-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="d7efe-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d7efe-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d7efe-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d7efe-110">Puntatore a una struttura [**NMSELCHANGE**](/windows/win32/api/commctrl/ns-commctrl-nmselchange) che contiene informazioni sull'intervallo di date attualmente selezionato.</span><span class="sxs-lookup"><span data-stu-id="d7efe-110">Pointer to an [**NMSELCHANGE**](/windows/win32/api/commctrl/ns-commctrl-nmselchange) structure that contains information about the currently selected date range.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d7efe-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d7efe-111">Return value</span></span>

<span data-ttu-id="d7efe-112">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="d7efe-112">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d7efe-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="d7efe-113">Remarks</span></span>

<span data-ttu-id="d7efe-114">Il codice di notifica **\_ Select di MCN** è simile a [**MCN \_ selChange**](mcn-selchange.md), ma **MCN \_ Select** viene inviato solo in risposta alle selezioni di data esplicite di un utente.</span><span class="sxs-lookup"><span data-stu-id="d7efe-114">The **MCN\_SELECT** notification code is similar to [**MCN\_SELCHANGE**](mcn-selchange.md), but **MCN\_SELECT** is sent only in response to a user's explicit date selections.</span></span> <span data-ttu-id="d7efe-115">**MCN \_ SELCHANGE** si applica a qualsiasi modifica di selezione.</span><span class="sxs-lookup"><span data-stu-id="d7efe-115">**MCN\_SELCHANGE** applies to any selection change.</span></span>

## <a name="requirements"></a><span data-ttu-id="d7efe-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d7efe-116">Requirements</span></span>



| <span data-ttu-id="d7efe-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="d7efe-117">Requirement</span></span> | <span data-ttu-id="d7efe-118">Valore</span><span class="sxs-lookup"><span data-stu-id="d7efe-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d7efe-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d7efe-119">Minimum supported client</span></span><br/> | <span data-ttu-id="d7efe-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d7efe-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d7efe-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d7efe-121">Minimum supported server</span></span><br/> | <span data-ttu-id="d7efe-122">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d7efe-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d7efe-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d7efe-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="d7efe-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d7efe-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





