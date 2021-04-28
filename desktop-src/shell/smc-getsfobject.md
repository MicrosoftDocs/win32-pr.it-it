---
description: 'SMC_GETSFOBJECT messaggio: richiede un puntatore a un oggetto specificato.'
title: SMC_GETSFOBJECT messaggio (Shobjidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: a8478f10-77ce-4e71-a5dc-89d8a90cf513
api_name:
- SMC_GETSFOBJECT
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 612b43c193cd1919db4a5cf9dba3a8fdba1c81c7
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086609"
---
# <a name="smc_getsfobject-message"></a><span data-ttu-id="38592-103">Messaggio GETSFOBJECT di SMC \_</span><span class="sxs-lookup"><span data-stu-id="38592-103">SMC\_GETSFOBJECT message</span></span>

<span data-ttu-id="38592-104">Richiede un puntatore a un oggetto specificato.</span><span class="sxs-lookup"><span data-stu-id="38592-104">Requests a pointer to a specified object.</span></span>


```C++
SMC_GETSFOBJECT 
    wParam = (WPARAM) (REFIID) iid;
    lParam = (LPARAM) (void **) pv
            
```



## <a name="parameters"></a><span data-ttu-id="38592-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="38592-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="38592-106">*Iid*</span><span class="sxs-lookup"><span data-stu-id="38592-106">*iid*</span></span> 
</dt> <dd>

<span data-ttu-id="38592-107">IID associato all'oggetto richiesto.</span><span class="sxs-lookup"><span data-stu-id="38592-107">The IID associated with the requested object.</span></span>

</dd> <dt>

<span data-ttu-id="38592-108">*Pv*</span><span class="sxs-lookup"><span data-stu-id="38592-108">*pv*</span></span> 
</dt> <dd>

<span data-ttu-id="38592-109">Puntatore void che riceve un puntatore all'interfaccia richiesta.</span><span class="sxs-lookup"><span data-stu-id="38592-109">A void pointer that receives a pointer to the requested interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="38592-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="38592-110">Return value</span></span>

<span data-ttu-id="38592-111">Restituire S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="38592-111">Return S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="38592-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="38592-112">Remarks</span></span>

<span data-ttu-id="38592-113">Questa notifica viene ricevuta dal [**metodo IShellMenuCallback::CallbackSM.**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm)</span><span class="sxs-lookup"><span data-stu-id="38592-113">This notification is received by the [**IShellMenuCallback::CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) method.</span></span> <span data-ttu-id="38592-114">È simile a [**SMC \_ GETOBJECT,**](smc-getobject.md) ma usato per gli elementi della cartella shell.</span><span class="sxs-lookup"><span data-stu-id="38592-114">It is similar to [**SMC\_GETOBJECT**](smc-getobject.md) but used for Shell folder items.</span></span> <span data-ttu-id="38592-115">Creare l'oggetto richiesto e assegnare un puntatore all'interfaccia richiesta a *pv*.</span><span class="sxs-lookup"><span data-stu-id="38592-115">Create the requested object and assign a pointer to the requested interface to *pv*.</span></span>

<span data-ttu-id="38592-116">Possono essere richieste le interfacce seguenti.</span><span class="sxs-lookup"><span data-stu-id="38592-116">The following interfaces may be requested.</span></span>

-   [<span data-ttu-id="38592-117">**Istream**</span><span class="sxs-lookup"><span data-stu-id="38592-117">**IStream**</span></span>](/windows/win32/api/objidl/nn-objidl-istream)
-   [<span data-ttu-id="38592-118">**IShellMenu**</span><span class="sxs-lookup"><span data-stu-id="38592-118">**IShellMenu**</span></span>](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellmenu)
-   [<span data-ttu-id="38592-119">**IShellMenuCallback**</span><span class="sxs-lookup"><span data-stu-id="38592-119">**IShellMenuCallback**</span></span>](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellmenucallback)

## <a name="requirements"></a><span data-ttu-id="38592-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="38592-120">Requirements</span></span>



| <span data-ttu-id="38592-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="38592-121">Requirement</span></span> | <span data-ttu-id="38592-122">Valore</span><span class="sxs-lookup"><span data-stu-id="38592-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="38592-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="38592-123">Minimum supported client</span></span><br/> | <span data-ttu-id="38592-124">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="38592-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="38592-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="38592-125">Minimum supported server</span></span><br/> | <span data-ttu-id="38592-126">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="38592-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="38592-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="38592-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="38592-128"><dt>Shobjidl.h</dt></span><span class="sxs-lookup"><span data-stu-id="38592-128"><dt>Shobjidl.h</dt></span></span> </dl>   |
| <span data-ttu-id="38592-129">Idl</span><span class="sxs-lookup"><span data-stu-id="38592-129">IDL</span></span><br/>                      | <dl> <span data-ttu-id="38592-130"><dt>Shobjidl.idl</dt></span><span class="sxs-lookup"><span data-stu-id="38592-130"><dt>Shobjidl.idl</dt></span></span> </dl> |



 

 
