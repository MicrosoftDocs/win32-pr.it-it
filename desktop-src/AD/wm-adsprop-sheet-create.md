---
title: Messaggio WM_ADSPROP_SHEET_CREATE
description: Inviato all'oggetto notifica per creare una finestra delle proprietà secondaria in uno snap-in di MMC Active Directory.
ms.assetid: 3efa25f2-cd39-44f8-952e-203f1519ce2c
ms.tgt_platform: multiple
keywords:
- Messaggio WM_ADSPROP_SHEET_CREATE Active Directory
topic_type:
- apiref
api_name:
- WM_ADSPROP_SHEET_CREATE
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b540ffd87d4350a323577ff5fa317e94f9271f2d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517836"
---
# <a name="wm_adsprop_sheet_create-message"></a><span data-ttu-id="66260-104">\_Messaggio di \_ creazione del foglio ADSPROP WM \_</span><span class="sxs-lookup"><span data-stu-id="66260-104">WM\_ADSPROP\_SHEET\_CREATE message</span></span>

<span data-ttu-id="66260-105">Per creare una finestra delle proprietà secondaria in uno snap-in di MMC Active Directory, viene inviato un messaggio di **\_ creazione del \_ foglio \_ WM ADSPROP** all'oggetto notifica.</span><span class="sxs-lookup"><span data-stu-id="66260-105">The **WM\_ADSPROP\_SHEET\_CREATE** message is sent to the notification object to create a secondary property sheet in an Active Directory MMC snap-in.</span></span>

> [!Note]  
> <span data-ttu-id="66260-106">Il valore di questo messaggio non è definito in un file di intestazione pubblicato.</span><span class="sxs-lookup"><span data-stu-id="66260-106">This message value is not defined in a published header file.</span></span> <span data-ttu-id="66260-107">Per usare questo valore del messaggio, è necessario definirlo nel formato esatto indicato.</span><span class="sxs-lookup"><span data-stu-id="66260-107">To use this message value, you must define it yourself in the exact format shown.</span></span>

 


```C++
#define WM_ADSPROP_SHEET_CREATE (WM_USER + 1108)
LRESULT SendMessage( (HWND)   hwnd, 
                     (UINT)   WM_ADSPROP_SHEET_CREATE,
                     (WPARAM) wParam, 
                     (LPARAM) lParam);
```



## <a name="parameters"></a><span data-ttu-id="66260-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="66260-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="66260-109">*HWND*</span><span class="sxs-lookup"><span data-stu-id="66260-109">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="66260-110">Handle dell'oggetto notifica.</span><span class="sxs-lookup"><span data-stu-id="66260-110">The handle of the notification object.</span></span> <span data-ttu-id="66260-111">Per ottenere questo handle, chiamare [**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj).</span><span class="sxs-lookup"><span data-stu-id="66260-111">To obtain this handle, call [**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj).</span></span>

</dd> <dt>

<span data-ttu-id="66260-112">*wParam*</span><span class="sxs-lookup"><span data-stu-id="66260-112">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="66260-113">Contiene un puntatore a una struttura di [**\_ informazioni della \_ pagina \_ DSA sec**](dsa-sec-page-info.md) che definisce la pagina secondaria da creare.</span><span class="sxs-lookup"><span data-stu-id="66260-113">Contains a pointer to a [**DSA\_SEC\_PAGE\_INFO**](dsa-sec-page-info.md) structure that defines the secondary page to create.</span></span> <span data-ttu-id="66260-114">È possibile creare una sola finestra delle proprietà secondaria con il messaggio di **\_ \_ \_ creazione del foglio WM ADSPROP** , quindi la struttura [**DSOBJECTNAMES**](/windows/desktop/api/Dsclient/ns-dsclient-dsobjectnames) può contenere una sola struttura [**DSOBJECT**](/windows/desktop/api/Dsclient/ns-dsclient-dsobject) .</span><span class="sxs-lookup"><span data-stu-id="66260-114">Only one secondary property sheet can be created with the **WM\_ADSPROP\_SHEET\_CREATE** message, so the [**DSOBJECTNAMES**](/windows/desktop/api/Dsclient/ns-dsclient-dsobjectnames) structure can only contain one [**DSOBJECT**](/windows/desktop/api/Dsclient/ns-dsclient-dsobject) structure.</span></span>

</dd> <dt>

<span data-ttu-id="66260-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="66260-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="66260-116">Non usato.</span><span class="sxs-lookup"><span data-stu-id="66260-116">Not used.</span></span> <span data-ttu-id="66260-117">Deve essere **null**.</span><span class="sxs-lookup"><span data-stu-id="66260-117">Must be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="66260-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="66260-118">Return value</span></span>

<span data-ttu-id="66260-119">Il valore restituito per questo messaggio è sempre zero.</span><span class="sxs-lookup"><span data-stu-id="66260-119">The return value for this message is always zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="66260-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="66260-120">Remarks</span></span>

<span data-ttu-id="66260-121">Il chiamante deve allocare la struttura delle [**\_ \_ \_ informazioni della pagina DSA sec**](dsa-sec-page-info.md) , la stringa del titolo e tutte le stringhe [**DSOBJECT**](/windows/desktop/api/Dsclient/ns-dsclient-dsobject) usando una singola chiamata alla funzione [**LocalAlloc**](/windows/desktop/api/winbase/nf-winbase-localalloc) .</span><span class="sxs-lookup"><span data-stu-id="66260-121">The caller must allocate the [**DSA\_SEC\_PAGE\_INFO**](dsa-sec-page-info.md) structure, the title string and all [**DSOBJECT**](/windows/desktop/api/Dsclient/ns-dsclient-dsobject) strings using a single call to the [**LocalAlloc**](/windows/desktop/api/winbase/nf-winbase-localalloc) function.</span></span> <span data-ttu-id="66260-122">Il messaggio di **\_ creazione del \_ foglio \_ WM ADSPROP** è un messaggio asincrono, che verrà restituito prima della creazione del foglio secondario.</span><span class="sxs-lookup"><span data-stu-id="66260-122">The **WM\_ADSPROP\_SHEET\_CREATE** message is an asynchronous message, so it will return before the secondary sheet is created.</span></span> <span data-ttu-id="66260-123">Per questo motivo, la memoria deve rimanere intatta dopo la restituzione del messaggio.</span><span class="sxs-lookup"><span data-stu-id="66260-123">Because of this, the memory must remain intact after the message returns.</span></span> <span data-ttu-id="66260-124">Il ricevitore libera questa memoria con una sola chiamata alla funzione [**LocalFree**](/windows/desktop/api/winbase/nf-winbase-localfree) dopo la creazione del foglio secondario.</span><span class="sxs-lookup"><span data-stu-id="66260-124">The receiver will free this memory with a single call to the [**LocalFree**](/windows/desktop/api/winbase/nf-winbase-localfree) function after the secondary sheet is created.</span></span>

## <a name="requirements"></a><span data-ttu-id="66260-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="66260-125">Requirements</span></span>



| <span data-ttu-id="66260-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="66260-126">Requirement</span></span> | <span data-ttu-id="66260-127">Valore</span><span class="sxs-lookup"><span data-stu-id="66260-127">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="66260-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="66260-128">Minimum supported client</span></span><br/> | <span data-ttu-id="66260-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="66260-129">Windows Vista</span></span><br/>       |
| <span data-ttu-id="66260-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="66260-130">Minimum supported server</span></span><br/> | <span data-ttu-id="66260-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="66260-131">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="66260-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="66260-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66260-133">**\_PARENTHWND DS \_ CFSTR**</span><span class="sxs-lookup"><span data-stu-id="66260-133">**CFSTR\_DS\_PARENTHWND**</span></span>](cfstr-ds-parenthwnd.md)
</dt> <dt>

[<span data-ttu-id="66260-134">**\_ \_ informazioni pagina di DSA sec \_**</span><span class="sxs-lookup"><span data-stu-id="66260-134">**DSA\_SEC\_PAGE\_INFO**</span></span>](dsa-sec-page-info.md)
</dt> <dt>

[<span data-ttu-id="66260-135">**DSOBJECTNAMES**</span><span class="sxs-lookup"><span data-stu-id="66260-135">**DSOBJECTNAMES**</span></span>](/windows/desktop/api/Dsclient/ns-dsclient-dsobjectnames)
</dt> <dt>

[<span data-ttu-id="66260-136">**DSOBJECT**</span><span class="sxs-lookup"><span data-stu-id="66260-136">**DSOBJECT**</span></span>](/windows/desktop/api/Dsclient/ns-dsclient-dsobject)
</dt> <dt>

[<span data-ttu-id="66260-137">**LocalAlloc**</span><span class="sxs-lookup"><span data-stu-id="66260-137">**LocalAlloc**</span></span>](/windows/desktop/api/winbase/nf-winbase-localalloc)
</dt> <dt>

[<span data-ttu-id="66260-138">**LocalFree**</span><span class="sxs-lookup"><span data-stu-id="66260-138">**LocalFree**</span></span>](/windows/desktop/api/winbase/nf-winbase-localfree)
</dt> </dl>

 

