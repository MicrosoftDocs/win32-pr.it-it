---
title: Messaggio WM_DSA_SHEET_CREATE_NOTIFY
description: Inviato allo snap-in MMC Active Directory per creare una finestra delle proprietà secondaria.
ms.assetid: 878878bf-fb78-4669-b282-1dd3349f35d5
ms.tgt_platform: multiple
keywords:
- Messaggio WM_DSA_SHEET_CREATE_NOTIFY Active Directory
topic_type:
- apiref
api_name:
- WM_DSA_SHEET_CREATE_NOTIFY
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77f08424e7b39449861ec654f1ff7891c6e9c60a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964298"
---
# <a name="wm_dsa_sheet_create_notify-message"></a><span data-ttu-id="6b7f5-104">Creazione di un \_ \_ messaggio di \_ notifica del foglio DSA WM \_</span><span class="sxs-lookup"><span data-stu-id="6b7f5-104">WM\_DSA\_SHEET\_CREATE\_NOTIFY message</span></span>

<span data-ttu-id="6b7f5-105">Per creare una finestra delle proprietà secondaria, viene pubblicato il messaggio di **notifica del foglio DSA WM per Active Directory la creazione di un messaggio di \_ \_ \_ \_ notifica** .</span><span class="sxs-lookup"><span data-stu-id="6b7f5-105">The **WM\_DSA\_SHEET\_CREATE\_NOTIFY** message is posted to the Active Directory MMC snap-in to create a secondary property sheet.</span></span>

> [!Note]  
> <span data-ttu-id="6b7f5-106">Il valore di questo messaggio non è definito in un file di intestazione pubblicato.</span><span class="sxs-lookup"><span data-stu-id="6b7f5-106">This message value is not defined in a published header file.</span></span> <span data-ttu-id="6b7f5-107">Per utilizzare questo valore del messaggio, definirlo nel formato esatto visualizzato.</span><span class="sxs-lookup"><span data-stu-id="6b7f5-107">To use this message value, define it in the exact format shown.</span></span>

 


```C++
#define WM_DSA_SHEET_CREATE_NOTIFY (WM_USER + 6)
LRESULT SendMessage(
    (HWND) hwnd, 
    WM_DSA_SHEET_CREATE_NOTIFY,
    (WPARAM) wParam, 
    (LPARAM) lParam);
```



## <a name="parameters"></a><span data-ttu-id="6b7f5-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="6b7f5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6b7f5-109">*HWND*</span><span class="sxs-lookup"><span data-stu-id="6b7f5-109">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="6b7f5-110">Handle della finestra dello snap-in che elaborerà questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="6b7f5-110">The window handle of the snap-in window that will process this message.</span></span> <span data-ttu-id="6b7f5-111">Questo handle viene ottenuto dal membro **hwndHidden** della struttura [**PROPSHEETCFG**](propsheetcfg.md) .</span><span class="sxs-lookup"><span data-stu-id="6b7f5-111">This handle is obtained from the **hwndHidden** member of the [**PROPSHEETCFG**](propsheetcfg.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="6b7f5-112">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6b7f5-112">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6b7f5-113">Contiene un puntatore a una struttura di [**\_ informazioni della \_ pagina \_ DSA sec**](dsa-sec-page-info.md) che definisce la finestra delle proprietà secondaria da creare.</span><span class="sxs-lookup"><span data-stu-id="6b7f5-113">Contains a pointer to a [**DSA\_SEC\_PAGE\_INFO**](dsa-sec-page-info.md) structure that defines the secondary property sheet to create.</span></span> <span data-ttu-id="6b7f5-114">Il ricevitore del messaggio deve liberare questa memoria con la funzione [**LocalFree**](/windows/desktop/api/winbase/nf-winbase-localfree) quando non è più necessaria.</span><span class="sxs-lookup"><span data-stu-id="6b7f5-114">The message receiver must free this memory with the [**LocalFree**](/windows/desktop/api/winbase/nf-winbase-localfree) function when it is no longer required.</span></span>

</dd> <dt>

<span data-ttu-id="6b7f5-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6b7f5-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6b7f5-116">Non usato.</span><span class="sxs-lookup"><span data-stu-id="6b7f5-116">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6b7f5-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6b7f5-117">Return value</span></span>

<span data-ttu-id="6b7f5-118">Non usato.</span><span class="sxs-lookup"><span data-stu-id="6b7f5-118">Not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="6b7f5-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6b7f5-119">Requirements</span></span>



| <span data-ttu-id="6b7f5-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="6b7f5-120">Requirement</span></span> | <span data-ttu-id="6b7f5-121">Valore</span><span class="sxs-lookup"><span data-stu-id="6b7f5-121">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="6b7f5-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6b7f5-122">Minimum supported client</span></span><br/> | <span data-ttu-id="6b7f5-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6b7f5-123">Windows Vista</span></span><br/>       |
| <span data-ttu-id="6b7f5-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6b7f5-124">Minimum supported server</span></span><br/> | <span data-ttu-id="6b7f5-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6b7f5-125">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6b7f5-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6b7f5-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b7f5-127">**PROPSHEETCFG**</span><span class="sxs-lookup"><span data-stu-id="6b7f5-127">**PROPSHEETCFG**</span></span>](propsheetcfg.md)
</dt> <dt>

[<span data-ttu-id="6b7f5-128">**\_ \_ informazioni pagina di DSA sec \_**</span><span class="sxs-lookup"><span data-stu-id="6b7f5-128">**DSA\_SEC\_PAGE\_INFO**</span></span>](dsa-sec-page-info.md)
</dt> <dt>

[<span data-ttu-id="6b7f5-129">**LocalFree**</span><span class="sxs-lookup"><span data-stu-id="6b7f5-129">**LocalFree**</span></span>](/windows/desktop/api/winbase/nf-winbase-localfree)
</dt> </dl>

 

