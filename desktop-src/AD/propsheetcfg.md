---
title: Struttura PROPSHEETCFG
description: Utilizzato per contenere i dati di configurazione della finestra delle proprietà.
ms.assetid: d3bde744-9d85-4506-894f-f8be3463721f
ms.tgt_platform: multiple
keywords:
- Active Directory della struttura PROPSHEETCFG
- Active Directory puntatore alla struttura PPROPSHEETCFG
topic_type:
- apiref
api_name:
- PROPSHEETCFG
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 33f4a1186cc756435cc49ed7c81592385faaee60
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048400"
---
# <a name="propsheetcfg-structure"></a><span data-ttu-id="659c6-105">Struttura PROPSHEETCFG</span><span class="sxs-lookup"><span data-stu-id="659c6-105">PROPSHEETCFG structure</span></span>

<span data-ttu-id="659c6-106">La struttura **PROPSHEETCFG** viene utilizzata per contenere i dati di configurazione della finestra delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="659c6-106">The **PROPSHEETCFG** structure is used to contain property sheet configuration data.</span></span> <span data-ttu-id="659c6-107">Questa struttura è contenuta nel formato [**CFSTR \_ DS \_ PROPSHEETCONFIG**](cfstr-ds-propsheetconfig.md) Clipboard.</span><span class="sxs-lookup"><span data-stu-id="659c6-107">This structure is contained in the [**CFSTR\_DS\_PROPSHEETCONFIG**](cfstr-ds-propsheetconfig.md) clipboard format.</span></span>

> [!Note]  
> <span data-ttu-id="659c6-108">Questa struttura non è definita in un file di intestazione pubblicato.</span><span class="sxs-lookup"><span data-stu-id="659c6-108">This structure is not defined in a published header file.</span></span> <span data-ttu-id="659c6-109">Per usare questa struttura, è necessario definirla nel formato esatto illustrato.</span><span class="sxs-lookup"><span data-stu-id="659c6-109">To use this structure, you must define it yourself in the exact format shown.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="659c6-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="659c6-110">Syntax</span></span>


```C++
typedef struct {
  LONG_PTR lNotifyHandle;
  HWND     hwndParentSheet;
  HWND     hwndHidden;
  WPARAM   wParamSheetClose;
} PROPSHEETCFG, *PPROPSHEETCFG;
```



## <a name="members"></a><span data-ttu-id="659c6-111">Members</span><span class="sxs-lookup"><span data-stu-id="659c6-111">Members</span></span>

<dl> <dt>

<span data-ttu-id="659c6-112">**lNotifyHandle**</span><span class="sxs-lookup"><span data-stu-id="659c6-112">**lNotifyHandle**</span></span>
</dt> <dd>

<span data-ttu-id="659c6-113">Contiene l'handle di notifica.</span><span class="sxs-lookup"><span data-stu-id="659c6-113">Contains the notification handle.</span></span> <span data-ttu-id="659c6-114">Si tratta di un handle identico a quello passato per il parametro *handle* nel metodo [**IExtendPropertySheet2:: CreatePropertyPages**](/previous-versions/windows/desktop/legacy/aa814847(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="659c6-114">This is identical to the handle passed for the *handle* parameter in the [**IExtendPropertySheet2::CreatePropertyPages**](/previous-versions/windows/desktop/legacy/aa814847(v=vs.85)) method.</span></span>

</dd> <dt>

<span data-ttu-id="659c6-115">**hwndParentSheet**</span><span class="sxs-lookup"><span data-stu-id="659c6-115">**hwndParentSheet**</span></span>
</dt> <dd>

<span data-ttu-id="659c6-116">Contiene l'handle della finestra delle proprietà padre.</span><span class="sxs-lookup"><span data-stu-id="659c6-116">Contains the window handle of the parent property sheet.</span></span>

</dd> <dt>

<span data-ttu-id="659c6-117">**hwndHidden**</span><span class="sxs-lookup"><span data-stu-id="659c6-117">**hwndHidden**</span></span>
</dt> <dd>

<span data-ttu-id="659c6-118">Contiene l'handle della finestra nascosta.</span><span class="sxs-lookup"><span data-stu-id="659c6-118">Contains the handle of the hidden window.</span></span>

</dd> <dt>

<span data-ttu-id="659c6-119">**wParamSheetClose**</span><span class="sxs-lookup"><span data-stu-id="659c6-119">**wParamSheetClose**</span></span>
</dt> <dd>

<span data-ttu-id="659c6-120">Contiene un valore definito dall'applicazione a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="659c6-120">Contains an application-defined 32-bit value.</span></span> <span data-ttu-id="659c6-121">Questo valore viene passato nuovamente all'applicazione nel *wParam* del messaggio di [**notifica di \_ \_ chiusura del \_ foglio \_ DSA WM**](wm-dsa-sheet-close-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="659c6-121">This value is passed back to the application in the *wParam* of the [**WM\_DSA\_SHEET\_CLOSE\_NOTIFY**](wm-dsa-sheet-close-notify.md) message.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="659c6-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="659c6-122">Requirements</span></span>



| <span data-ttu-id="659c6-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="659c6-123">Requirement</span></span> | <span data-ttu-id="659c6-124">Valore</span><span class="sxs-lookup"><span data-stu-id="659c6-124">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="659c6-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="659c6-125">Minimum supported client</span></span><br/> | <span data-ttu-id="659c6-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="659c6-126">Windows Vista</span></span><br/>       |
| <span data-ttu-id="659c6-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="659c6-127">Minimum supported server</span></span><br/> | <span data-ttu-id="659c6-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="659c6-128">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="659c6-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="659c6-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="659c6-130">**\_PROPSHEETCONFIG DS \_ CFSTR**</span><span class="sxs-lookup"><span data-stu-id="659c6-130">**CFSTR\_DS\_PROPSHEETCONFIG**</span></span>](cfstr-ds-propsheetconfig.md)
</dt> <dt>

[<span data-ttu-id="659c6-131">**\_notifica di \_ chiusura del foglio DSA \_ WM \_**</span><span class="sxs-lookup"><span data-stu-id="659c6-131">**WM\_DSA\_SHEET\_CLOSE\_NOTIFY**</span></span>](wm-dsa-sheet-close-notify.md)
</dt> </dl>

 

