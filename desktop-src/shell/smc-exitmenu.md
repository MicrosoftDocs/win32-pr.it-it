---
description: Notifica all'utente che il menu è in compressione.
title: Messaggio SMC_EXITMENU (ShObjIdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 868b4819-1dbf-497a-9c79-5935f503969a
api_name:
- SMC_EXITMENU
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: e9a8680617a17ce0069a8633e1c70ff6b32a4be7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967836"
---
# <a name="smc_exitmenu-message"></a><span data-ttu-id="2158d-103">\_Messaggio EXITMENU di SMC</span><span class="sxs-lookup"><span data-stu-id="2158d-103">SMC\_EXITMENU message</span></span>

<span data-ttu-id="2158d-104">Notifica all'utente che il menu è in compressione.</span><span class="sxs-lookup"><span data-stu-id="2158d-104">Notifies you that the menu is collapsing.</span></span>


```C++
SMC_EXITMENU
            
```



## <a name="parameters"></a><span data-ttu-id="2158d-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="2158d-105">Parameters</span></span>

<span data-ttu-id="2158d-106">Questo messaggio non contiene parametri.</span><span class="sxs-lookup"><span data-stu-id="2158d-106">This message has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2158d-107">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2158d-107">Return value</span></span>

<span data-ttu-id="2158d-108">Restituisce \_ OK.</span><span class="sxs-lookup"><span data-stu-id="2158d-108">Return S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="2158d-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="2158d-109">Remarks</span></span>

<span data-ttu-id="2158d-110">Questa notifica viene ricevuta dal metodo [**IShellMenuCallback:: CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) .</span><span class="sxs-lookup"><span data-stu-id="2158d-110">This notification is received by the [**IShellMenuCallback::CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="2158d-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2158d-111">Requirements</span></span>



| <span data-ttu-id="2158d-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="2158d-112">Requirement</span></span> | <span data-ttu-id="2158d-113">Valore</span><span class="sxs-lookup"><span data-stu-id="2158d-113">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2158d-114">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2158d-114">Minimum supported client</span></span><br/> | <span data-ttu-id="2158d-115">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="2158d-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="2158d-116">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2158d-116">Minimum supported server</span></span><br/> | <span data-ttu-id="2158d-117">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="2158d-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="2158d-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2158d-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="2158d-119"><dt>ShObjIdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="2158d-119"><dt>Shobjidl.h</dt></span></span> </dl>   |
| <span data-ttu-id="2158d-120">IDL</span><span class="sxs-lookup"><span data-stu-id="2158d-120">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2158d-121"><dt>ShObjIdl. idl</dt></span><span class="sxs-lookup"><span data-stu-id="2158d-121"><dt>Shobjidl.idl</dt></span></span> </dl> |



 

 




