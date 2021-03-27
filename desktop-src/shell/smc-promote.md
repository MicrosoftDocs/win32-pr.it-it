---
description: Alzare di livello l'elemento specificato dalla struttura SMDATA associata.
title: Messaggio SMC_PROMOTE (ShObjIdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: b1208673-06b4-42b2-b4ac-872fd22927df
api_name:
- SMC_PROMOTE
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 22718e51d6ef1bf7e3c5652741b95cadb4db9937
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980151"
---
# <a name="smc_promote-message"></a><span data-ttu-id="f2a5e-103">\_Messaggio di promozione SMC</span><span class="sxs-lookup"><span data-stu-id="f2a5e-103">SMC\_PROMOTE message</span></span>

<span data-ttu-id="f2a5e-104">Alzare di livello l'elemento specificato dalla struttura [**SMDATA**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) associata.</span><span class="sxs-lookup"><span data-stu-id="f2a5e-104">Promote the item specified by the accompanying [**SMDATA**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) structure.</span></span>


```C++
SMC_PROMOTE
```



## <a name="parameters"></a><span data-ttu-id="f2a5e-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="f2a5e-105">Parameters</span></span>

<span data-ttu-id="f2a5e-106">Questo messaggio non contiene parametri.</span><span class="sxs-lookup"><span data-stu-id="f2a5e-106">This message has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f2a5e-107">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f2a5e-107">Return value</span></span>

<span data-ttu-id="f2a5e-108">Restituisce \_ OK.</span><span class="sxs-lookup"><span data-stu-id="f2a5e-108">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="f2a5e-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="f2a5e-109">Remarks</span></span>

<span data-ttu-id="f2a5e-110">Questa notifica viene ricevuta dal metodo [**IShellMenuCallback:: CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) .</span><span class="sxs-lookup"><span data-stu-id="f2a5e-110">This notification is received by the [**IShellMenuCallback::CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="f2a5e-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f2a5e-111">Requirements</span></span>



| <span data-ttu-id="f2a5e-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="f2a5e-112">Requirement</span></span> | <span data-ttu-id="f2a5e-113">Valore</span><span class="sxs-lookup"><span data-stu-id="f2a5e-113">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f2a5e-114">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f2a5e-114">Minimum supported client</span></span><br/> | <span data-ttu-id="f2a5e-115">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="f2a5e-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="f2a5e-116">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f2a5e-116">Minimum supported server</span></span><br/> | <span data-ttu-id="f2a5e-117">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="f2a5e-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f2a5e-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f2a5e-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="f2a5e-119"><dt>ShObjIdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f2a5e-119"><dt>Shobjidl.h</dt></span></span> </dl>   |
| <span data-ttu-id="f2a5e-120">IDL</span><span class="sxs-lookup"><span data-stu-id="f2a5e-120">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f2a5e-121"><dt>ShObjIdl. idl</dt></span><span class="sxs-lookup"><span data-stu-id="f2a5e-121"><dt>Shobjidl.idl</dt></span></span> </dl> |



 

 




