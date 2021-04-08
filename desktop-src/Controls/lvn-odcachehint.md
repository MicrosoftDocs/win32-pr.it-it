---
title: Codice di notifica LVN_ODCACHEHINT (COMmctrl. h)
description: Inviato da un controllo di visualizzazione elenco virtuale quando il contenuto dell'area di visualizzazione è stato modificato.
ms.assetid: 2fac6a16-f65e-402f-9295-f2beb23db924
keywords:
- Controlli di Windows per il codice di notifica LVN_ODCACHEHINT
topic_type:
- apiref
api_name:
- LVN_ODCACHEHINT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 827ad81b6ebb66a4fbe5c1a3b283175818b99e98
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103965010"
---
# <a name="lvn_odcachehint-notification-code"></a><span data-ttu-id="6fc67-104">\_Codice di notifica ODCACHEHINT di LVN</span><span class="sxs-lookup"><span data-stu-id="6fc67-104">LVN\_ODCACHEHINT notification code</span></span>

<span data-ttu-id="6fc67-105">Inviato da un controllo di visualizzazione elenco virtuale quando il contenuto dell'area di visualizzazione è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="6fc67-105">Sent by a virtual list-view control when the contents of its display area have changed.</span></span> <span data-ttu-id="6fc67-106">Ad esempio, un controllo di visualizzazione elenco Invia questo codice di notifica quando l'utente scorre la visualizzazione del controllo.</span><span class="sxs-lookup"><span data-stu-id="6fc67-106">For example, a list-view control sends this notification code when the user scrolls the control's display.</span></span> <span data-ttu-id="6fc67-107">Il \_ codice di notifica ODCACHEHINT di LVN viene inviato sotto forma di messaggio di [**\_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="6fc67-107">The LVN\_ODCACHEHINT notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_ODCACHEHINT

    pCachehint = (NMLVCACHEHINT *) lParam;
```



## <a name="parameters"></a><span data-ttu-id="6fc67-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="6fc67-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6fc67-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6fc67-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6fc67-110">Puntatore a una struttura [**NMLVCACHEHINT**](/windows/win32/api/commctrl/ns-commctrl-nmlvcachehint) contenente informazioni sull'intervallo di elementi da memorizzare nella cache.</span><span class="sxs-lookup"><span data-stu-id="6fc67-110">Pointer to an [**NMLVCACHEHINT**](/windows/win32/api/commctrl/ns-commctrl-nmlvcachehint) structure containing information about the range of items to be cached.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6fc67-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6fc67-111">Return value</span></span>

<span data-ttu-id="6fc67-112">L'applicazione che riceve il codice di notifica deve restituire zero.</span><span class="sxs-lookup"><span data-stu-id="6fc67-112">The application receiving this notification code must return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="6fc67-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="6fc67-113">Remarks</span></span>

<span data-ttu-id="6fc67-114">La gestione di questo messaggio consente all'applicazione di aggiornare le informazioni sull'elemento contenute nella cache in modo che sia prontamente disponibile quando viene inviato un codice di notifica [ \_ GETDISPINFO LVN](lvn-getdispinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="6fc67-114">Handling this message allows the application to update the item information held in cache so that it is readily available when an [LVN\_GETDISPINFO](lvn-getdispinfo.md) notification code is sent.</span></span>

<span data-ttu-id="6fc67-115">Si noti che questo codice di notifica non è sempre una rappresentazione esatta degli elementi che verranno richiesti da [LVN \_ GETDISPINFO](lvn-getdispinfo.md).</span><span class="sxs-lookup"><span data-stu-id="6fc67-115">Note that this notification code is not always an exact representation of the items that will be requested by [LVN\_GETDISPINFO](lvn-getdispinfo.md).</span></span> <span data-ttu-id="6fc67-116">Se pertanto l'elemento richiesto non viene memorizzato nella cache durante la gestione \_ di LVN GETDISPINFO, l'applicazione deve essere preparata a fornire le informazioni richieste da un'origine esterna alla cache.</span><span class="sxs-lookup"><span data-stu-id="6fc67-116">Therefore, if the requested item is not cached while handling LVN\_GETDISPINFO, the application must be prepared to supply the requested information from a source outside the cache.</span></span>

## <a name="requirements"></a><span data-ttu-id="6fc67-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6fc67-117">Requirements</span></span>



| <span data-ttu-id="6fc67-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="6fc67-118">Requirement</span></span> | <span data-ttu-id="6fc67-119">Valore</span><span class="sxs-lookup"><span data-stu-id="6fc67-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6fc67-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6fc67-120">Minimum supported client</span></span><br/> | <span data-ttu-id="6fc67-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6fc67-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6fc67-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6fc67-122">Minimum supported server</span></span><br/> | <span data-ttu-id="6fc67-123">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="6fc67-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6fc67-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6fc67-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="6fc67-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="6fc67-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





