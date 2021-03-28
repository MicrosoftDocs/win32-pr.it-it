---
description: L'utente ha fatto clic su una freccia di espansione per espandere l'elemento specificato dalla struttura SMDATA associata.
title: Messaggio SMC_CHEVRONEXPAND (ShObjIdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: cb0b3cf1-1a12-4236-96e9-cc04360d269f
api_name:
- SMC_CHEVRONEXPAND
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 6ecf8f86e111326b3f37f3111c382d2d04ef2fa7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232334"
---
# <a name="smc_chevronexpand-message"></a><span data-ttu-id="d50c5-103">\_Messaggio CHEVRONEXPAND di SMC</span><span class="sxs-lookup"><span data-stu-id="d50c5-103">SMC\_CHEVRONEXPAND message</span></span>

<span data-ttu-id="d50c5-104">L'utente ha fatto clic su una freccia di espansione per espandere l'elemento specificato dalla struttura [**SMDATA**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) associata.</span><span class="sxs-lookup"><span data-stu-id="d50c5-104">The user has clicked a chevron to expand the item specified by the accompanying [**SMDATA**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) structure.</span></span>


```C++
SMC_CHEVRONEXPAND
            
```



## <a name="parameters"></a><span data-ttu-id="d50c5-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="d50c5-105">Parameters</span></span>

<span data-ttu-id="d50c5-106">Questo messaggio non contiene parametri.</span><span class="sxs-lookup"><span data-stu-id="d50c5-106">This message has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d50c5-107">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d50c5-107">Return value</span></span>

<span data-ttu-id="d50c5-108">Restituisce \_ OK.</span><span class="sxs-lookup"><span data-stu-id="d50c5-108">Return S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="d50c5-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="d50c5-109">Remarks</span></span>

<span data-ttu-id="d50c5-110">Questa notifica viene ricevuta dal metodo [**IShellMenuCallback:: CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) .</span><span class="sxs-lookup"><span data-stu-id="d50c5-110">This notification is received by the [**IShellMenuCallback::CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="d50c5-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d50c5-111">Requirements</span></span>



| <span data-ttu-id="d50c5-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="d50c5-112">Requirement</span></span> | <span data-ttu-id="d50c5-113">Valore</span><span class="sxs-lookup"><span data-stu-id="d50c5-113">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d50c5-114">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d50c5-114">Minimum supported client</span></span><br/> | <span data-ttu-id="d50c5-115">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d50c5-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="d50c5-116">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d50c5-116">Minimum supported server</span></span><br/> | <span data-ttu-id="d50c5-117">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d50c5-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d50c5-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d50c5-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="d50c5-119"><dt>ShObjIdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d50c5-119"><dt>Shobjidl.h</dt></span></span> </dl>   |
| <span data-ttu-id="d50c5-120">IDL</span><span class="sxs-lookup"><span data-stu-id="d50c5-120">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d50c5-121"><dt>ShObjIdl. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d50c5-121"><dt>Shobjidl.idl</dt></span></span> </dl> |



 

 




