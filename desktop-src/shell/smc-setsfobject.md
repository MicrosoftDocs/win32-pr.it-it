---
description: Notifica all'utente di salvare l'oggetto passato.
title: Messaggio SMC_SETSFOBJECT (ShObjIdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: f7e2cf12-7f09-45b0-97d3-eed803e57d9f
api_name:
- SMC_SETSFOBJECT
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 44aeb41ab7dcd271f8c84bff4eb8b5525ac66e70
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232328"
---
# <a name="smc_setsfobject-message"></a><span data-ttu-id="a528d-103">\_Messaggio SETSFOBJECT di SMC</span><span class="sxs-lookup"><span data-stu-id="a528d-103">SMC\_SETSFOBJECT message</span></span>

<span data-ttu-id="a528d-104">Notifica all'utente di salvare l'oggetto passato.</span><span class="sxs-lookup"><span data-stu-id="a528d-104">Notifies you to save the passed object.</span></span>


```C++
SMC_GETOBJECT 
    wParam = (WPARAM) (REFIID) iid;
    lParam = (LPARAM) (void **) pv
            
```



## <a name="parameters"></a><span data-ttu-id="a528d-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="a528d-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a528d-106">*IID*</span><span class="sxs-lookup"><span data-stu-id="a528d-106">*iid*</span></span> 
</dt> <dd>

<span data-ttu-id="a528d-107">IID associato all'oggetto.</span><span class="sxs-lookup"><span data-stu-id="a528d-107">The IID associated with the object.</span></span>

</dd> <dt>

<span data-ttu-id="a528d-108">*PV*</span><span class="sxs-lookup"><span data-stu-id="a528d-108">*pv*</span></span> 
</dt> <dd>

<span data-ttu-id="a528d-109">Puntatore all'interfaccia dell'oggetto specificato da *IID*.</span><span class="sxs-lookup"><span data-stu-id="a528d-109">A pointer the interface on the object specified by *iid*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a528d-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a528d-110">Return value</span></span>

<span data-ttu-id="a528d-111">Restituisce \_ OK.</span><span class="sxs-lookup"><span data-stu-id="a528d-111">Return S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="a528d-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="a528d-112">Remarks</span></span>

<span data-ttu-id="a528d-113">Questa notifica viene ricevuta dal metodo [**IShellMenuCallback:: CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) .</span><span class="sxs-lookup"><span data-stu-id="a528d-113">This notification is received by the [**IShellMenuCallback::CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) method.</span></span>

<span data-ttu-id="a528d-114">La **notifica \_ SETSFOBJECT di SMC** viene utilizzata con il \_ flusso IID.</span><span class="sxs-lookup"><span data-stu-id="a528d-114">The **SMC\_SETSFOBJECT** notification is used with IID\_Stream.</span></span> <span data-ttu-id="a528d-115">L'oggetto viene salvato in un formato permanente nel registro di sistema e non viene eseguita alcuna operazione con il conteggio dei riferimenti nell'oggetto passato.</span><span class="sxs-lookup"><span data-stu-id="a528d-115">The object is saved into a persisted form in the registry and nothing is done with the reference count on the object passed in.</span></span>

## <a name="requirements"></a><span data-ttu-id="a528d-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a528d-116">Requirements</span></span>



| <span data-ttu-id="a528d-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="a528d-117">Requirement</span></span> | <span data-ttu-id="a528d-118">Valore</span><span class="sxs-lookup"><span data-stu-id="a528d-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a528d-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a528d-119">Minimum supported client</span></span><br/> | <span data-ttu-id="a528d-120">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="a528d-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="a528d-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a528d-121">Minimum supported server</span></span><br/> | <span data-ttu-id="a528d-122">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="a528d-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a528d-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a528d-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="a528d-124"><dt>ShObjIdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="a528d-124"><dt>Shobjidl.h</dt></span></span> </dl>   |
| <span data-ttu-id="a528d-125">IDL</span><span class="sxs-lookup"><span data-stu-id="a528d-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a528d-126"><dt>ShObjIdl. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a528d-126"><dt>Shobjidl.idl</dt></span></span> </dl> |



 

 




