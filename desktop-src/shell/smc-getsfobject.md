---
description: Richiede un puntatore a un oggetto specificato.
title: Messaggio SMC_GETSFOBJECT (ShObjIdl. h)
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
ms.openlocfilehash: c7fb57ea8e3f02ce4e773e187310530c14d65515
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232330"
---
# <a name="smc_getsfobject-message"></a><span data-ttu-id="6b0fc-103">\_Messaggio GETSFOBJECT di SMC</span><span class="sxs-lookup"><span data-stu-id="6b0fc-103">SMC\_GETSFOBJECT message</span></span>

<span data-ttu-id="6b0fc-104">Richiede un puntatore a un oggetto specificato.</span><span class="sxs-lookup"><span data-stu-id="6b0fc-104">Requests a pointer to a specified object.</span></span>


```C++
SMC_GETSFOBJECT 
    wParam = (WPARAM) (REFIID) iid;
    lParam = (LPARAM) (void **) pv
            
```



## <a name="parameters"></a><span data-ttu-id="6b0fc-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="6b0fc-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6b0fc-106">*IID*</span><span class="sxs-lookup"><span data-stu-id="6b0fc-106">*iid*</span></span> 
</dt> <dd>

<span data-ttu-id="6b0fc-107">IID associato all'oggetto richiesto.</span><span class="sxs-lookup"><span data-stu-id="6b0fc-107">The IID associated with the requested object.</span></span>

</dd> <dt>

<span data-ttu-id="6b0fc-108">*PV*</span><span class="sxs-lookup"><span data-stu-id="6b0fc-108">*pv*</span></span> 
</dt> <dd>

<span data-ttu-id="6b0fc-109">Puntatore void che riceve un puntatore all'interfaccia richiesta.</span><span class="sxs-lookup"><span data-stu-id="6b0fc-109">A void pointer that receives a pointer to the requested interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6b0fc-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6b0fc-110">Return value</span></span>

<span data-ttu-id="6b0fc-111">Restituisce \_ OK.</span><span class="sxs-lookup"><span data-stu-id="6b0fc-111">Return S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="6b0fc-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="6b0fc-112">Remarks</span></span>

<span data-ttu-id="6b0fc-113">Questa notifica viene ricevuta dal metodo [**IShellMenuCallback:: CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) .</span><span class="sxs-lookup"><span data-stu-id="6b0fc-113">This notification is received by the [**IShellMenuCallback::CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) method.</span></span> <span data-ttu-id="6b0fc-114">È simile a [**SMC \_ GetObject**](smc-getobject.md) ma usato per gli elementi della cartella della shell.</span><span class="sxs-lookup"><span data-stu-id="6b0fc-114">It is similar to [**SMC\_GETOBJECT**](smc-getobject.md) but used for Shell folder items.</span></span> <span data-ttu-id="6b0fc-115">Creare l'oggetto richiesto e assegnare un puntatore all'interfaccia richiesta a *PV*.</span><span class="sxs-lookup"><span data-stu-id="6b0fc-115">Create the requested object and assign a pointer to the requested interface to *pv*.</span></span>

<span data-ttu-id="6b0fc-116">È possibile che vengano richieste le interfacce seguenti.</span><span class="sxs-lookup"><span data-stu-id="6b0fc-116">The following interfaces may be requested.</span></span>

-   [<span data-ttu-id="6b0fc-117">**IStream**</span><span class="sxs-lookup"><span data-stu-id="6b0fc-117">**IStream**</span></span>](/windows/win32/api/objidl/nn-objidl-istream)
-   [<span data-ttu-id="6b0fc-118">**IShellMenu**</span><span class="sxs-lookup"><span data-stu-id="6b0fc-118">**IShellMenu**</span></span>](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellmenu)
-   [<span data-ttu-id="6b0fc-119">**IShellMenuCallback**</span><span class="sxs-lookup"><span data-stu-id="6b0fc-119">**IShellMenuCallback**</span></span>](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellmenucallback)

## <a name="requirements"></a><span data-ttu-id="6b0fc-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6b0fc-120">Requirements</span></span>



| <span data-ttu-id="6b0fc-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="6b0fc-121">Requirement</span></span> | <span data-ttu-id="6b0fc-122">Valore</span><span class="sxs-lookup"><span data-stu-id="6b0fc-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6b0fc-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6b0fc-123">Minimum supported client</span></span><br/> | <span data-ttu-id="6b0fc-124">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="6b0fc-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="6b0fc-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6b0fc-125">Minimum supported server</span></span><br/> | <span data-ttu-id="6b0fc-126">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="6b0fc-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="6b0fc-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6b0fc-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="6b0fc-128"><dt>ShObjIdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="6b0fc-128"><dt>Shobjidl.h</dt></span></span> </dl>   |
| <span data-ttu-id="6b0fc-129">IDL</span><span class="sxs-lookup"><span data-stu-id="6b0fc-129">IDL</span></span><br/>                      | <dl> <span data-ttu-id="6b0fc-130"><dt>ShObjIdl. idl</dt></span><span class="sxs-lookup"><span data-stu-id="6b0fc-130"><dt>Shobjidl.idl</dt></span></span> </dl> |



 

 
