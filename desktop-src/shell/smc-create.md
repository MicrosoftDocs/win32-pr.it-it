---
description: Notifica all'utente che è stata creata una banda di menu.
title: Messaggio SMC_CREATE (ShObjIdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 8eeca6f6-1718-4ff6-b4a7-4b68b9527468
api_name:
- SMC_CREATE
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 59219f376288431fa20e198d8c427ff40c7fba62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104994864"
---
# <a name="smc_create-message"></a><span data-ttu-id="eceac-103">\_Creazione messaggio SMC</span><span class="sxs-lookup"><span data-stu-id="eceac-103">SMC\_CREATE message</span></span>

<span data-ttu-id="eceac-104">Notifica all'utente che è stata creata una banda di menu.</span><span class="sxs-lookup"><span data-stu-id="eceac-104">Notifies you that a menu band has been created.</span></span>


```C++
SMC_CREATE 
    lParam = (LPARAM) (LPSMDATA) psmd
            
```



## <a name="parameters"></a><span data-ttu-id="eceac-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="eceac-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eceac-106">*psmd*</span><span class="sxs-lookup"><span data-stu-id="eceac-106">*psmd*</span></span> 
</dt> <dd>

<span data-ttu-id="eceac-107">Puntatore al membro **pvUserData** di una struttura [**SMDATA**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) .</span><span class="sxs-lookup"><span data-stu-id="eceac-107">A pointer to the **pvUserData** member of an [**SMDATA**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eceac-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="eceac-108">Return value</span></span>

<span data-ttu-id="eceac-109">Restituisce \_ OK.</span><span class="sxs-lookup"><span data-stu-id="eceac-109">Return S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="eceac-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="eceac-110">Remarks</span></span>

<span data-ttu-id="eceac-111">Questa notifica viene ricevuta dal metodo [**IShellMenuCallback:: CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) .</span><span class="sxs-lookup"><span data-stu-id="eceac-111">This notification is received by the [**IShellMenuCallback::CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="eceac-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="eceac-112">Requirements</span></span>



| <span data-ttu-id="eceac-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="eceac-113">Requirement</span></span> | <span data-ttu-id="eceac-114">Valore</span><span class="sxs-lookup"><span data-stu-id="eceac-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="eceac-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="eceac-115">Minimum supported client</span></span><br/> | <span data-ttu-id="eceac-116">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="eceac-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="eceac-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="eceac-117">Minimum supported server</span></span><br/> | <span data-ttu-id="eceac-118">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="eceac-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="eceac-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="eceac-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="eceac-120"><dt>ShObjIdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="eceac-120"><dt>Shobjidl.h</dt></span></span> </dl>   |
| <span data-ttu-id="eceac-121">IDL</span><span class="sxs-lookup"><span data-stu-id="eceac-121">IDL</span></span><br/>                      | <dl> <span data-ttu-id="eceac-122"><dt>ShObjIdl. idl</dt></span><span class="sxs-lookup"><span data-stu-id="eceac-122"><dt>Shobjidl.idl</dt></span></span> </dl> |



 

 




