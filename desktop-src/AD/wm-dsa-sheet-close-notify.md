---
title: Messaggio WM_DSA_SHEET_CLOSE_NOTIFY
description: Inserito nello snap-in di MMC Active Directory quando viene eliminata definitivamente una finestra delle proprietà secondaria.
ms.assetid: 74271550-e1f7-4576-a04f-52d5b7c619cb
ms.tgt_platform: multiple
keywords:
- Messaggio WM_DSA_SHEET_CLOSE_NOTIFY Active Directory
topic_type:
- apiref
api_name:
- WM_DSA_SHEET_CLOSE_NOTIFY
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36f03cdb6224ae5f55bc995897d766ce61e67693
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301710"
---
# <a name="wm_dsa_sheet_close_notify-message"></a><span data-ttu-id="4167e-104">\_Messaggio di \_ \_ notifica chiusura del foglio DSA WM \_</span><span class="sxs-lookup"><span data-stu-id="4167e-104">WM\_DSA\_SHEET\_CLOSE\_NOTIFY message</span></span>

<span data-ttu-id="4167e-105">Il messaggio di **\_ notifica di \_ \_ chiusura \_ del foglio DSA WM** viene inserito nello snap-in di MMC Active Directory quando una finestra delle proprietà secondaria viene distrutta.</span><span class="sxs-lookup"><span data-stu-id="4167e-105">The **WM\_DSA\_SHEET\_CLOSE\_NOTIFY** message is posted to the Active Directory MMC snap-in when a secondary property sheet is destroyed.</span></span>

> [!Note]  
> <span data-ttu-id="4167e-106">Il valore di questo messaggio non è definito in un file di intestazione pubblicato.</span><span class="sxs-lookup"><span data-stu-id="4167e-106">This message value is not defined in a published header file.</span></span> <span data-ttu-id="4167e-107">Per usare questo valore del messaggio, è necessario definirlo nel formato esatto indicato.</span><span class="sxs-lookup"><span data-stu-id="4167e-107">To use this message value, you must define it yourself in the exact format shown.</span></span>

 


```C++
#define WM_DSA_SHEET_CLOSE_NOTIFY (WM_USER + 5)
```




```C++
LRESULT SendMessage( (HWND)   hwnd, 
                     (UINT)   WM_DSA_SHEET_CLOSE_NOTIFY,
                     (WPARAM) wParam, 
                     (LPARAM) lParam);
```



## <a name="parameters"></a><span data-ttu-id="4167e-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="4167e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4167e-109">*HWND*</span><span class="sxs-lookup"><span data-stu-id="4167e-109">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="4167e-110">Handle della finestra dello snap-in che elaborerà questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="4167e-110">The window handle of the snap-in window that will process this message.</span></span> <span data-ttu-id="4167e-111">Questo handle viene ottenuto dal membro **hwndHidden** della struttura [**PROPSHEETCFG**](propsheetcfg.md) .</span><span class="sxs-lookup"><span data-stu-id="4167e-111">This handle is obtained from the **hwndHidden** member of the [**PROPSHEETCFG**](propsheetcfg.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="4167e-112">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4167e-112">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4167e-113">Contiene un valore definito dall'applicazione a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="4167e-113">Contains an application-defined 32-bit value.</span></span> <span data-ttu-id="4167e-114">Questa operazione viene ottenuta dal membro **wParamSheetClose** della struttura [**PROPSHEETCFG**](propsheetcfg.md) .</span><span class="sxs-lookup"><span data-stu-id="4167e-114">This is obtained from the **wParamSheetClose** member of the [**PROPSHEETCFG**](propsheetcfg.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="4167e-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4167e-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4167e-116">Non usato.</span><span class="sxs-lookup"><span data-stu-id="4167e-116">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4167e-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4167e-117">Return value</span></span>

<span data-ttu-id="4167e-118">Il valore restituito per questo messaggio non viene utilizzato.</span><span class="sxs-lookup"><span data-stu-id="4167e-118">The return value for this message is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="4167e-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4167e-119">Requirements</span></span>



| <span data-ttu-id="4167e-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="4167e-120">Requirement</span></span> | <span data-ttu-id="4167e-121">Valore</span><span class="sxs-lookup"><span data-stu-id="4167e-121">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="4167e-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4167e-122">Minimum supported client</span></span><br/> | <span data-ttu-id="4167e-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4167e-123">Windows Vista</span></span><br/>       |
| <span data-ttu-id="4167e-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4167e-124">Minimum supported server</span></span><br/> | <span data-ttu-id="4167e-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4167e-125">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4167e-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4167e-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4167e-127">**PROPSHEETCFG**</span><span class="sxs-lookup"><span data-stu-id="4167e-127">**PROPSHEETCFG**</span></span>](propsheetcfg.md)
</dt> </dl>

 

 





