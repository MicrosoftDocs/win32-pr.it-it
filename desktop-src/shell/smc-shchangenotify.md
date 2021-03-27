---
description: Notifica all'utente che è stata apportata una modifica.
title: Messaggio SMC_SHCHANGENOTIFY (ShObjIdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 8232f170-0dab-475a-ace0-67c04f01c777
api_name:
- SMC_SHCHANGENOTIFY
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 258a885ddaf61b45df1cfff9f9c77ce37a233dd0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104979802"
---
# <a name="smc_shchangenotify-message"></a><span data-ttu-id="90146-103">\_Messaggio SHCHANGENOTIFY di SMC</span><span class="sxs-lookup"><span data-stu-id="90146-103">SMC\_SHCHANGENOTIFY message</span></span>

<span data-ttu-id="90146-104">Notifica all'utente che è stata apportata una modifica.</span><span class="sxs-lookup"><span data-stu-id="90146-104">Notifies you that a change has taken place.</span></span>


```C++
SMC_SHCHANGENOTIFY
    lParam = (LPARAM) (PSMCSCHANGENOTIFYSTRUCT) psmc
            
```



## <a name="parameters"></a><span data-ttu-id="90146-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="90146-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="90146-106">*PSMC*</span><span class="sxs-lookup"><span data-stu-id="90146-106">*psmc*</span></span> 
</dt> <dd>

<span data-ttu-id="90146-107">Puntatore a una struttura [**SMCSHCHANGENOTIFYSTRUCT**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smcshchangenotifystruct) con informazioni sulla modifica.</span><span class="sxs-lookup"><span data-stu-id="90146-107">A pointer to an [**SMCSHCHANGENOTIFYSTRUCT**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smcshchangenotifystruct) structure with information on the change.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="90146-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="90146-108">Return value</span></span>

<span data-ttu-id="90146-109">Restituisce \_ OK.</span><span class="sxs-lookup"><span data-stu-id="90146-109">Return S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="90146-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="90146-110">Remarks</span></span>

<span data-ttu-id="90146-111">Questa notifica viene ricevuta dal metodo [**IShellMenuCallback:: CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) .</span><span class="sxs-lookup"><span data-stu-id="90146-111">This notification is received by the [**IShellMenuCallback::CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="90146-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="90146-112">Requirements</span></span>



| <span data-ttu-id="90146-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="90146-113">Requirement</span></span> | <span data-ttu-id="90146-114">Valore</span><span class="sxs-lookup"><span data-stu-id="90146-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="90146-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="90146-115">Minimum supported client</span></span><br/> | <span data-ttu-id="90146-116">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="90146-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="90146-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="90146-117">Minimum supported server</span></span><br/> | <span data-ttu-id="90146-118">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="90146-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="90146-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="90146-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="90146-120"><dt>ShObjIdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="90146-120"><dt>Shobjidl.h</dt></span></span> </dl>   |
| <span data-ttu-id="90146-121">IDL</span><span class="sxs-lookup"><span data-stu-id="90146-121">IDL</span></span><br/>                      | <dl> <span data-ttu-id="90146-122"><dt>ShObjIdl. idl</dt></span><span class="sxs-lookup"><span data-stu-id="90146-122"><dt>Shobjidl.idl</dt></span></span> </dl> |



 

 




