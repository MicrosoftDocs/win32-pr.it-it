---
description: Notifica all'utente che sta per essere visualizzato un infotip per la freccia di espansione associata all'elemento specificato dalla struttura SMDATA associata.
title: Messaggio SMC_DISPLAYCHEVRONTIP (ShObjIdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: e4ec4839-e49a-4563-9bc9-79f9d4d54658
api_name:
- SMC_DISPLAYCHEVRONTIP
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 09e01fc6ea169d8dcbf5758ace341198166a3a9e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104485508"
---
# <a name="smc_displaychevrontip-message"></a><span data-ttu-id="772c4-103">\_Messaggio DISPLAYCHEVRONTIP di SMC</span><span class="sxs-lookup"><span data-stu-id="772c4-103">SMC\_DISPLAYCHEVRONTIP message</span></span>

<span data-ttu-id="772c4-104">Notifica all'utente che sta per essere visualizzato un infotip per la freccia di espansione associata all'elemento specificato dalla struttura [**SMDATA**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) associata.</span><span class="sxs-lookup"><span data-stu-id="772c4-104">Notifies you that an infotip is about to be displayed for the chevron associated with the item specified by the accompanying [**SMDATA**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) structure.</span></span>


```C++
SMC_DISPLAYCHEVRONTIP
            
```



## <a name="parameters"></a><span data-ttu-id="772c4-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="772c4-105">Parameters</span></span>

<span data-ttu-id="772c4-106">Questo messaggio non contiene parametri.</span><span class="sxs-lookup"><span data-stu-id="772c4-106">This message has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="772c4-107">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="772c4-107">Return value</span></span>

<span data-ttu-id="772c4-108">Restituire S \_ OK per visualizzare il infotip.</span><span class="sxs-lookup"><span data-stu-id="772c4-108">Return S\_OK to display the infotip.</span></span> <span data-ttu-id="772c4-109">Restituisce \_ false per impedire la visualizzazione del infotip.</span><span class="sxs-lookup"><span data-stu-id="772c4-109">Return S\_FALSE to prevent the infotip from being displayed.</span></span>

## <a name="remarks"></a><span data-ttu-id="772c4-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="772c4-110">Remarks</span></span>

<span data-ttu-id="772c4-111">Questa notifica viene ricevuta dal metodo [**IShellMenuCallback:: CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) .</span><span class="sxs-lookup"><span data-stu-id="772c4-111">This notification is received by the [**IShellMenuCallback::CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="772c4-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="772c4-112">Requirements</span></span>



| <span data-ttu-id="772c4-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="772c4-113">Requirement</span></span> | <span data-ttu-id="772c4-114">Valore</span><span class="sxs-lookup"><span data-stu-id="772c4-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="772c4-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="772c4-115">Minimum supported client</span></span><br/> | <span data-ttu-id="772c4-116">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="772c4-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="772c4-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="772c4-117">Minimum supported server</span></span><br/> | <span data-ttu-id="772c4-118">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="772c4-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="772c4-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="772c4-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="772c4-120"><dt>ShObjIdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="772c4-120"><dt>Shobjidl.h</dt></span></span> </dl>   |
| <span data-ttu-id="772c4-121">IDL</span><span class="sxs-lookup"><span data-stu-id="772c4-121">IDL</span></span><br/>                      | <dl> <span data-ttu-id="772c4-122"><dt>ShObjIdl. idl</dt></span><span class="sxs-lookup"><span data-stu-id="772c4-122"><dt>Shobjidl.idl</dt></span></span> </dl> |



 

 




