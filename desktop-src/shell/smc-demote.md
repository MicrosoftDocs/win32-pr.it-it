---
description: Abbassare di più l'elemento specificato dalla struttura SMDATA associata.
title: Messaggio SMC_DEMOTE (ShObjIdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 4809fbd1-da66-4453-b4f2-e75cb5b3457c
api_name:
- SMC_DEMOTE
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 46e5505571402feec24d81a9184b713e1c61ae0f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104994856"
---
# <a name="smc_demote-message"></a><span data-ttu-id="88029-103">\_Messaggio SMC ABbassamento di pagina</span><span class="sxs-lookup"><span data-stu-id="88029-103">SMC\_DEMOTE message</span></span>

<span data-ttu-id="88029-104">Abbassare di più l'elemento specificato dalla struttura [**SMDATA**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) associata.</span><span class="sxs-lookup"><span data-stu-id="88029-104">Demote the item specified by the accompanying [**SMDATA**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) structure.</span></span>


```C++
SMC_DEMOTE
            
```



## <a name="parameters"></a><span data-ttu-id="88029-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="88029-105">Parameters</span></span>

<span data-ttu-id="88029-106">Questo messaggio non contiene parametri.</span><span class="sxs-lookup"><span data-stu-id="88029-106">This message has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="88029-107">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="88029-107">Return value</span></span>

<span data-ttu-id="88029-108">Restituisce \_ OK.</span><span class="sxs-lookup"><span data-stu-id="88029-108">Return S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="88029-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="88029-109">Remarks</span></span>

<span data-ttu-id="88029-110">Questa notifica viene ricevuta dal metodo [**IShellMenuCallback:: CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) .</span><span class="sxs-lookup"><span data-stu-id="88029-110">This notification is received by the [**IShellMenuCallback::CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="88029-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="88029-111">Requirements</span></span>



| <span data-ttu-id="88029-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="88029-112">Requirement</span></span> | <span data-ttu-id="88029-113">Valore</span><span class="sxs-lookup"><span data-stu-id="88029-113">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="88029-114">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="88029-114">Minimum supported client</span></span><br/> | <span data-ttu-id="88029-115">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="88029-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="88029-116">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="88029-116">Minimum supported server</span></span><br/> | <span data-ttu-id="88029-117">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="88029-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="88029-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="88029-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="88029-119"><dt>ShObjIdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="88029-119"><dt>Shobjidl.h</dt></span></span> </dl>   |
| <span data-ttu-id="88029-120">IDL</span><span class="sxs-lookup"><span data-stu-id="88029-120">IDL</span></span><br/>                      | <dl> <span data-ttu-id="88029-121"><dt>ShObjIdl. idl</dt></span><span class="sxs-lookup"><span data-stu-id="88029-121"><dt>Shobjidl.idl</dt></span></span> </dl> |



 

 




