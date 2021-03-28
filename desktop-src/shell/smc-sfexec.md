---
description: Eseguire l'elemento della cartella della shell specificato nella struttura SMDATA associata.
title: Messaggio SMC_SFEXEC (ShObjIdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: bb8f6434-0936-460f-b7dc-39be58bb70ce
api_name:
- SMC_SFEXEC
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: b4e414cd7dab9968882272b19b9b21b95da0f1d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980143"
---
# <a name="smc_sfexec-message"></a><span data-ttu-id="6ceca-103">\_Messaggio SFEXEC di SMC</span><span class="sxs-lookup"><span data-stu-id="6ceca-103">SMC\_SFEXEC message</span></span>

<span data-ttu-id="6ceca-104">Eseguire l'elemento della cartella della shell specificato nella struttura [**SMDATA**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) associata.</span><span class="sxs-lookup"><span data-stu-id="6ceca-104">Execute the Shell folder item specified in the accompanying [**SMDATA**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) structure.</span></span>


```C++
SMC_SFEXEC
            
```



## <a name="parameters"></a><span data-ttu-id="6ceca-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="6ceca-105">Parameters</span></span>

<span data-ttu-id="6ceca-106">Questo messaggio non contiene parametri.</span><span class="sxs-lookup"><span data-stu-id="6ceca-106">This message has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6ceca-107">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6ceca-107">Return value</span></span>

<span data-ttu-id="6ceca-108">Restituisce \_ OK.</span><span class="sxs-lookup"><span data-stu-id="6ceca-108">Return S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="6ceca-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="6ceca-109">Remarks</span></span>

<span data-ttu-id="6ceca-110">Questa notifica viene ricevuta dal metodo [**IShellMenuCallback:: CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) .</span><span class="sxs-lookup"><span data-stu-id="6ceca-110">This notification is received by the [**IShellMenuCallback::CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="6ceca-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6ceca-111">Requirements</span></span>



| <span data-ttu-id="6ceca-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="6ceca-112">Requirement</span></span> | <span data-ttu-id="6ceca-113">Valore</span><span class="sxs-lookup"><span data-stu-id="6ceca-113">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6ceca-114">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6ceca-114">Minimum supported client</span></span><br/> | <span data-ttu-id="6ceca-115">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="6ceca-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="6ceca-116">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6ceca-116">Minimum supported server</span></span><br/> | <span data-ttu-id="6ceca-117">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="6ceca-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="6ceca-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6ceca-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="6ceca-119"><dt>ShObjIdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="6ceca-119"><dt>Shobjidl.h</dt></span></span> </dl>   |
| <span data-ttu-id="6ceca-120">IDL</span><span class="sxs-lookup"><span data-stu-id="6ceca-120">IDL</span></span><br/>                      | <dl> <span data-ttu-id="6ceca-121"><dt>ShObjIdl. idl</dt></span><span class="sxs-lookup"><span data-stu-id="6ceca-121"><dt>Shobjidl.idl</dt></span></span> </dl> |



 

 




