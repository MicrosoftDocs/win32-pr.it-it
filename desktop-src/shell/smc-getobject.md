---
description: 'SMC_GETOBJECT messaggio: richiede un puntatore a un oggetto specificato.'
title: SMC_GETOBJECT messaggio (Shobjidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 36e8f304-a92a-485f-8413-b9c416087ec9
api_name:
- SMC_GETOBJECT
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 58741290d741cc18fd788282d0f302ef87bb15dd
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108100439"
---
# <a name="smc_getobject-message"></a><span data-ttu-id="3421c-103">Messaggio GETOBJECT di SMC \_</span><span class="sxs-lookup"><span data-stu-id="3421c-103">SMC\_GETOBJECT message</span></span>

<span data-ttu-id="3421c-104">Richiede un puntatore a un oggetto specificato.</span><span class="sxs-lookup"><span data-stu-id="3421c-104">Requests a pointer to a specified object.</span></span>


```C++
SMC_GETOBJECT 
    wParam = (WPARAM) (REFIID) iid;
    lParam = (LPARAM) (void **) pv
            
```



## <a name="parameters"></a><span data-ttu-id="3421c-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="3421c-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3421c-106">*Iid*</span><span class="sxs-lookup"><span data-stu-id="3421c-106">*iid*</span></span> 
</dt> <dd>

<span data-ttu-id="3421c-107">IID associato all'oggetto richiesto.</span><span class="sxs-lookup"><span data-stu-id="3421c-107">The IID associated with the requested object.</span></span>

</dd> <dt>

<span data-ttu-id="3421c-108">*Pv*</span><span class="sxs-lookup"><span data-stu-id="3421c-108">*pv*</span></span> 
</dt> <dd>

<span data-ttu-id="3421c-109">Puntatore void che riceve un puntatore all'interfaccia richiesta.</span><span class="sxs-lookup"><span data-stu-id="3421c-109">A void pointer that receives a pointer to the requested interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3421c-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3421c-110">Return value</span></span>

<span data-ttu-id="3421c-111">Restituire S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="3421c-111">Return S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="3421c-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="3421c-112">Remarks</span></span>

<span data-ttu-id="3421c-113">Questa notifica viene ricevuta dal [**metodo IShellMenuCallback::CallbackSM.**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm)</span><span class="sxs-lookup"><span data-stu-id="3421c-113">This notification is received by the [**IShellMenuCallback::CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) method.</span></span> <span data-ttu-id="3421c-114">Creare l'oggetto richiesto e assegnare un puntatore all'interfaccia richiesta *a pv*.</span><span class="sxs-lookup"><span data-stu-id="3421c-114">Create the requested object and assign a pointer to the requested interface to *pv*.</span></span>

<span data-ttu-id="3421c-115">Possono essere richieste le interfacce seguenti.</span><span class="sxs-lookup"><span data-stu-id="3421c-115">The following interfaces may be requested.</span></span>

-   [<span data-ttu-id="3421c-116">**IShellMenu**</span><span class="sxs-lookup"><span data-stu-id="3421c-116">**IShellMenu**</span></span>](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellmenu)
-   [<span data-ttu-id="3421c-117">**IContextMenu**</span><span class="sxs-lookup"><span data-stu-id="3421c-117">**IContextMenu**</span></span>](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu)
-   [<span data-ttu-id="3421c-118">**IShellMenuCallback**</span><span class="sxs-lookup"><span data-stu-id="3421c-118">**IShellMenuCallback**</span></span>](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellmenucallback)
-   [<span data-ttu-id="3421c-119">**Idroptarget**</span><span class="sxs-lookup"><span data-stu-id="3421c-119">**IDropTarget**</span></span>](/windows/win32/api/oleidl/nn-oleidl-idroptarget)

## <a name="requirements"></a><span data-ttu-id="3421c-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3421c-120">Requirements</span></span>



| <span data-ttu-id="3421c-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="3421c-121">Requirement</span></span> | <span data-ttu-id="3421c-122">Valore</span><span class="sxs-lookup"><span data-stu-id="3421c-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3421c-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3421c-123">Minimum supported client</span></span><br/> | <span data-ttu-id="3421c-124">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="3421c-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="3421c-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3421c-125">Minimum supported server</span></span><br/> | <span data-ttu-id="3421c-126">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="3421c-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="3421c-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3421c-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="3421c-128"><dt>Shobjidl.h</dt></span><span class="sxs-lookup"><span data-stu-id="3421c-128"><dt>Shobjidl.h</dt></span></span> </dl>   |
| <span data-ttu-id="3421c-129">Idl</span><span class="sxs-lookup"><span data-stu-id="3421c-129">IDL</span></span><br/>                      | <dl> <span data-ttu-id="3421c-130"><dt>Shobjidl.idl</dt></span><span class="sxs-lookup"><span data-stu-id="3421c-130"><dt>Shobjidl.idl</dt></span></span> </dl> |



 

 
