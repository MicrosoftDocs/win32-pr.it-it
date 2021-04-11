---
title: Struttura DSA_SEC_PAGE_INFO
description: Usato con il foglio \_ ADSPROP \_ WM \_ Crea e WM \_ DSA \_ foglio \_ Crea \_ notifica messaggi per definire una finestra delle proprietà secondaria in uno snap-in di MMC Active Directory.
ms.assetid: 422d84dc-6b5e-43bf-ac4f-3b99cb59f9df
ms.tgt_platform: multiple
keywords:
- Struttura DSA_SEC_PAGE_INFO Active Directory
- Puntatore alla struttura PDSA_SEC_PAGE_INFO Active Directory
topic_type:
- apiref
api_name:
- DSA_SEC_PAGE_INFO
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e4c8602a958c50c72942d89657a812d24f64571d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964484"
---
# <a name="dsa_sec_page_info-structure"></a><span data-ttu-id="0deee-105">\_Struttura delle \_ informazioni di pagina di DSA sec \_</span><span class="sxs-lookup"><span data-stu-id="0deee-105">DSA\_SEC\_PAGE\_INFO structure</span></span>

<span data-ttu-id="0deee-106">La struttura delle **\_ informazioni della \_ pagina \_ DSA sec** viene usata con il foglio [**ADSPROP di WM \_ \_ \_ Crea**](wm-adsprop-sheet-create.md) e il [**\_ foglio DSA WM \_ \_ Crea \_ notifica**](wm-dsa-sheet-create-notify.md) messaggi per definire una finestra delle proprietà secondaria in uno snap-in di MMC Active Directory.</span><span class="sxs-lookup"><span data-stu-id="0deee-106">The **DSA\_SEC\_PAGE\_INFO** structure is used with the [**WM\_ADSPROP\_SHEET\_CREATE**](wm-adsprop-sheet-create.md) and [**WM\_DSA\_SHEET\_CREATE\_NOTIFY**](wm-dsa-sheet-create-notify.md) messages to define a secondary property sheet in an Active Directory MMC snap-in.</span></span>

> [!Note]  
> <span data-ttu-id="0deee-107">Questa struttura non è definita in un file di intestazione pubblicato.</span><span class="sxs-lookup"><span data-stu-id="0deee-107">This structure is not defined in a published header file.</span></span> <span data-ttu-id="0deee-108">Per usare questa struttura, definirla nel formato esatto illustrato.</span><span class="sxs-lookup"><span data-stu-id="0deee-108">To use this structure, define it in the exact format shown.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="0deee-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0deee-109">Syntax</span></span>


```C++
typedef struct _DSA_SEC_PAGE_INFO {
  HWND          hwndParentSheet;
  DWORD         offsetTitle;
  DSOBJECTNAMES dsObjectNames;
} DSA_SEC_PAGE_INFO, *PDSA_SEC_PAGE_INFO;
```



## <a name="members"></a><span data-ttu-id="0deee-110">Members</span><span class="sxs-lookup"><span data-stu-id="0deee-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="0deee-111">**hwndParentSheet**</span><span class="sxs-lookup"><span data-stu-id="0deee-111">**hwndParentSheet**</span></span>
</dt> <dd>

<span data-ttu-id="0deee-112">Contiene l'handle della finestra padre della finestra delle proprietà secondaria.</span><span class="sxs-lookup"><span data-stu-id="0deee-112">Contains the window handle of the parent of the secondary property sheet.</span></span>

</dd> <dt>

<span data-ttu-id="0deee-113">**offsetTitle**</span><span class="sxs-lookup"><span data-stu-id="0deee-113">**offsetTitle**</span></span>
</dt> <dd>

<span data-ttu-id="0deee-114">Contiene l'offset, in byte, dall'inizio della struttura di **\_ informazioni della \_ pagina \_ DSA sec** a una stringa Unicode con terminazione null che contiene il titolo della finestra delle proprietà secondaria.</span><span class="sxs-lookup"><span data-stu-id="0deee-114">Contains the offset, in bytes, from the start of the **DSA\_SEC\_PAGE\_INFO** structure to a NULL-terminated, Unicode string that contains the title of the secondary property sheet.</span></span>

</dd> <dt>

<span data-ttu-id="0deee-115">**dsObjectNames**</span><span class="sxs-lookup"><span data-stu-id="0deee-115">**dsObjectNames**</span></span>
</dt> <dd>

<span data-ttu-id="0deee-116">Contiene una struttura [**DSOBJECTNAMES**](/windows/desktop/api/Dsclient/ns-dsclient-dsobjectnames) che definisce la finestra delle proprietà secondaria.</span><span class="sxs-lookup"><span data-stu-id="0deee-116">Contains a [**DSOBJECTNAMES**](/windows/desktop/api/Dsclient/ns-dsclient-dsobjectnames) structure that defines the secondary property sheet.</span></span> <span data-ttu-id="0deee-117">È possibile creare una sola finestra delle proprietà secondaria alla volta, quindi la struttura **DSOBJECTNAMES** può contenere solo una struttura [**DSOBJECT**](/windows/desktop/api/Dsclient/ns-dsclient-dsobject) .</span><span class="sxs-lookup"><span data-stu-id="0deee-117">Only one secondary property sheet can be created at a time, so the **DSOBJECTNAMES** structure can only contain one [**DSOBJECT**](/windows/desktop/api/Dsclient/ns-dsclient-dsobject) structure.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0deee-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0deee-118">Requirements</span></span>



| <span data-ttu-id="0deee-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="0deee-119">Requirement</span></span> | <span data-ttu-id="0deee-120">Valore</span><span class="sxs-lookup"><span data-stu-id="0deee-120">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="0deee-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0deee-121">Minimum supported client</span></span><br/> | <span data-ttu-id="0deee-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0deee-122">Windows Vista</span></span><br/>       |
| <span data-ttu-id="0deee-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0deee-123">Minimum supported server</span></span><br/> | <span data-ttu-id="0deee-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0deee-124">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0deee-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0deee-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0deee-126">**\_ \_ creazione foglio ADSPROP \_ WM**</span><span class="sxs-lookup"><span data-stu-id="0deee-126">**WM\_ADSPROP\_SHEET\_CREATE**</span></span>](wm-adsprop-sheet-create.md)
</dt> <dt>

[<span data-ttu-id="0deee-127">**\_ \_ \_ creazione \_ notifica foglio DSA WM**</span><span class="sxs-lookup"><span data-stu-id="0deee-127">**WM\_DSA\_SHEET\_CREATE\_NOTIFY**</span></span>](wm-dsa-sheet-create-notify.md)
</dt> <dt>

[<span data-ttu-id="0deee-128">**DSOBJECTNAMES**</span><span class="sxs-lookup"><span data-stu-id="0deee-128">**DSOBJECTNAMES**</span></span>](/windows/desktop/api/Dsclient/ns-dsclient-dsobjectnames)
</dt> <dt>

[<span data-ttu-id="0deee-129">**DSOBJECT**</span><span class="sxs-lookup"><span data-stu-id="0deee-129">**DSOBJECT**</span></span>](/windows/desktop/api/Dsclient/ns-dsclient-dsobject)
</dt> </dl>

 

 





