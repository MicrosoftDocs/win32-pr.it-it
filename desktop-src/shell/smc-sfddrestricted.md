---
description: Richiede se è accettabile eliminare un oggetto dati nell'elemento specificato dalla struttura SMDATA associata.
ms.assetid: 777bbc7e-6b0f-4627-9d92-4aa8209082ca
title: Messaggio SMC_SFDDRESTRICTED (ShObjIdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77ae6a852fd342e67edf42429f31eb7e1ba3b566
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980146"
---
# <a name="smc_sfddrestricted-message"></a><span data-ttu-id="65dda-103">\_Messaggio SFDDRESTRICTED di SMC</span><span class="sxs-lookup"><span data-stu-id="65dda-103">SMC\_SFDDRESTRICTED message</span></span>

<span data-ttu-id="65dda-104">Richiede se è accettabile eliminare un oggetto dati nell'elemento specificato dalla struttura [**SMDATA**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) associata.</span><span class="sxs-lookup"><span data-stu-id="65dda-104">Requests whether it is acceptable to drop a data object on the item specified by the accompanying [**SMDATA**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) structure.</span></span>


```C++
SMC_SFDDRESTRICTED 
    wParam = (WPARAM) (void **) pDropTarget
            
```



## <a name="parameters"></a><span data-ttu-id="65dda-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="65dda-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="65dda-106">*pDropTarget*</span><span class="sxs-lookup"><span data-stu-id="65dda-106">*pDropTarget*</span></span> 
</dt> <dd>

<span data-ttu-id="65dda-107">Indirizzo di un puntatore void che riceve un puntatore all'interfaccia [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) .</span><span class="sxs-lookup"><span data-stu-id="65dda-107">The address of a void pointer that receives a pointer to your [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) interface.</span></span> <span data-ttu-id="65dda-108">Impostare questo valore su **null** se non si desidera accettare l'oggetto dati.</span><span class="sxs-lookup"><span data-stu-id="65dda-108">Set this value to **NULL** if you do not want to accept the data object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="65dda-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="65dda-109">Return value</span></span>

<span data-ttu-id="65dda-110">Restituisce \_ OK.</span><span class="sxs-lookup"><span data-stu-id="65dda-110">Return S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="65dda-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="65dda-111">Remarks</span></span>

<span data-ttu-id="65dda-112">Questa notifica viene ricevuta dal metodo [**IShellMenuCallback:: CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) .</span><span class="sxs-lookup"><span data-stu-id="65dda-112">This notification is received by the [**IShellMenuCallback::CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="65dda-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="65dda-113">Requirements</span></span>



| <span data-ttu-id="65dda-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="65dda-114">Requirement</span></span> | <span data-ttu-id="65dda-115">Valore</span><span class="sxs-lookup"><span data-stu-id="65dda-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="65dda-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="65dda-116">Minimum supported client</span></span><br/> | <span data-ttu-id="65dda-117">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="65dda-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="65dda-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="65dda-118">Minimum supported server</span></span><br/> | <span data-ttu-id="65dda-119">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="65dda-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="65dda-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="65dda-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="65dda-121"><dt>ShObjIdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="65dda-121"><dt>Shobjidl.h</dt></span></span> </dl>   |
| <span data-ttu-id="65dda-122">IDL</span><span class="sxs-lookup"><span data-stu-id="65dda-122">IDL</span></span><br/>                      | <dl> <span data-ttu-id="65dda-123"><dt>ShObjIdl. idl</dt></span><span class="sxs-lookup"><span data-stu-id="65dda-123"><dt>Shobjidl.idl</dt></span></span> </dl> |



 

 
