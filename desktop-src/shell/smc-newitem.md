---
description: Notifica all'utente un nuovo elemento, come specificato dalla struttura SMDATA associata.
title: Messaggio SMC_NEWITEM (ShObjIdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: e0ccf2db-cb46-469f-bc08-4b5100a410ba
api_name:
- SMC_NEWITEM
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: ebd8f1b6454a2fb592374b860811ebfc7a14f09d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980159"
---
# <a name="smc_newitem-message"></a><span data-ttu-id="ad7b1-103">\_Messaggio NEWITEM di SMC</span><span class="sxs-lookup"><span data-stu-id="ad7b1-103">SMC\_NEWITEM message</span></span>

<span data-ttu-id="ad7b1-104">Notifica all'utente un nuovo elemento, come specificato dalla struttura [**SMDATA**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) associata.</span><span class="sxs-lookup"><span data-stu-id="ad7b1-104">Notifies you of a new item, as specified by the accompanying [**SMDATA**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) structure.</span></span>


```C++
SMC_NEWITEM
            
```



## <a name="parameters"></a><span data-ttu-id="ad7b1-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="ad7b1-105">Parameters</span></span>

<span data-ttu-id="ad7b1-106">Questo messaggio non contiene parametri.</span><span class="sxs-lookup"><span data-stu-id="ad7b1-106">This message has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ad7b1-107">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ad7b1-107">Return value</span></span>

<span data-ttu-id="ad7b1-108">Restituisce \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ad7b1-108">Return S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="ad7b1-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="ad7b1-109">Remarks</span></span>

<span data-ttu-id="ad7b1-110">Questa notifica viene ricevuta dal metodo [**IShellMenuCallback:: CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) .</span><span class="sxs-lookup"><span data-stu-id="ad7b1-110">This notification is received by the [**IShellMenuCallback::CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="ad7b1-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ad7b1-111">Requirements</span></span>



| <span data-ttu-id="ad7b1-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="ad7b1-112">Requirement</span></span> | <span data-ttu-id="ad7b1-113">Valore</span><span class="sxs-lookup"><span data-stu-id="ad7b1-113">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ad7b1-114">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ad7b1-114">Minimum supported client</span></span><br/> | <span data-ttu-id="ad7b1-115">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="ad7b1-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="ad7b1-116">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ad7b1-116">Minimum supported server</span></span><br/> | <span data-ttu-id="ad7b1-117">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="ad7b1-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ad7b1-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ad7b1-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="ad7b1-119"><dt>ShObjIdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ad7b1-119"><dt>Shobjidl.h</dt></span></span> </dl>   |
| <span data-ttu-id="ad7b1-120">IDL</span><span class="sxs-lookup"><span data-stu-id="ad7b1-120">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ad7b1-121"><dt>ShObjIdl. idl</dt></span><span class="sxs-lookup"><span data-stu-id="ad7b1-121"><dt>Shobjidl.idl</dt></span></span> </dl> |



 

 




