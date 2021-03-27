---
description: Invia una notifica che i menu sono stati aggiornati completamente ed è possibile reimpostare lo stato.
title: Messaggio SMC_REFRESH (ShObjIdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 8c79d9d5-b7dc-4271-9edb-93b40606c9be
api_name:
- SMC_REFRESH
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: aab18245c6502d4d3424e6ed6727eceb5a329d48
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883182"
---
# <a name="smc_refresh-message"></a><span data-ttu-id="14438-103">\_Messaggio di aggiornamento SMC</span><span class="sxs-lookup"><span data-stu-id="14438-103">SMC\_REFRESH message</span></span>

<span data-ttu-id="14438-104">Invia una notifica che i menu sono stati aggiornati completamente ed è possibile reimpostare lo stato.</span><span class="sxs-lookup"><span data-stu-id="14438-104">Sends notification that the menus have completely refreshed and you can reset your state.</span></span>


```C++
SMC_REFRESH
            
```



## <a name="parameters"></a><span data-ttu-id="14438-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="14438-105">Parameters</span></span>

<span data-ttu-id="14438-106">Questo messaggio non contiene parametri.</span><span class="sxs-lookup"><span data-stu-id="14438-106">This message has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="14438-107">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="14438-107">Return value</span></span>

<span data-ttu-id="14438-108">Restituisce \_ OK.</span><span class="sxs-lookup"><span data-stu-id="14438-108">Return S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="14438-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="14438-109">Remarks</span></span>

<span data-ttu-id="14438-110">Questa notifica viene ricevuta dal metodo [**IShellMenuCallback:: CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) .</span><span class="sxs-lookup"><span data-stu-id="14438-110">This notification is received by the [**IShellMenuCallback::CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="14438-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="14438-111">Requirements</span></span>



| <span data-ttu-id="14438-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="14438-112">Requirement</span></span> | <span data-ttu-id="14438-113">Valore</span><span class="sxs-lookup"><span data-stu-id="14438-113">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="14438-114">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="14438-114">Minimum supported client</span></span><br/> | <span data-ttu-id="14438-115">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="14438-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="14438-116">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="14438-116">Minimum supported server</span></span><br/> | <span data-ttu-id="14438-117">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="14438-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="14438-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="14438-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="14438-119"><dt>ShObjIdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="14438-119"><dt>Shobjidl.h</dt></span></span> </dl>   |
| <span data-ttu-id="14438-120">IDL</span><span class="sxs-lookup"><span data-stu-id="14438-120">IDL</span></span><br/>                      | <dl> <span data-ttu-id="14438-121"><dt>ShObjIdl. idl</dt></span><span class="sxs-lookup"><span data-stu-id="14438-121"><dt>Shobjidl.idl</dt></span></span> </dl> |



 

 




