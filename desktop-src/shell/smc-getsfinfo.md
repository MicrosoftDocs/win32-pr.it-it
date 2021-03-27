---
description: Richiede informazioni su una voce di menu della cartella della shell.
title: Messaggio SMC_GETSFINFO (ShObjIdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 4459670c-f0fd-4ae8-8a1f-810e1dcac713
api_name:
- SMC_GETSFINFO
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: f3a02b61565eb08f623978900d6ce47e30eea85e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104994837"
---
# <a name="smc_getsfinfo-message"></a><span data-ttu-id="0cee9-103">\_Messaggio GETSFINFO di SMC</span><span class="sxs-lookup"><span data-stu-id="0cee9-103">SMC\_GETSFINFO message</span></span>

<span data-ttu-id="0cee9-104">Richiede informazioni su una voce di menu della cartella della shell.</span><span class="sxs-lookup"><span data-stu-id="0cee9-104">Requests information about a Shell folder menu item.</span></span>


```C++
SMC_GETINFO 
    lParam = (LPARAM) (LPSMINFO) psminfo
            
```



## <a name="parameters"></a><span data-ttu-id="0cee9-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="0cee9-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0cee9-106">*psminfo*</span><span class="sxs-lookup"><span data-stu-id="0cee9-106">*psminfo*</span></span> 
</dt> <dd>

<span data-ttu-id="0cee9-107">Puntatore a una struttura [**SMINFO**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-sminfo) .</span><span class="sxs-lookup"><span data-stu-id="0cee9-107">Pointer to a [**SMINFO**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-sminfo) structure.</span></span> <span data-ttu-id="0cee9-108">Compilare la struttura con le informazioni appropriate e restituire S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="0cee9-108">Fill the structure with the appropriate information and return S\_OK.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0cee9-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0cee9-109">Return value</span></span>

<span data-ttu-id="0cee9-110">Restituisce \_ OK.</span><span class="sxs-lookup"><span data-stu-id="0cee9-110">Return S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="0cee9-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="0cee9-111">Remarks</span></span>

<span data-ttu-id="0cee9-112">Questa notifica viene ricevuta dal metodo [**IShellMenuCallback:: CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) .</span><span class="sxs-lookup"><span data-stu-id="0cee9-112">This notification is received by the [**IShellMenuCallback::CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="0cee9-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0cee9-113">Requirements</span></span>



| <span data-ttu-id="0cee9-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="0cee9-114">Requirement</span></span> | <span data-ttu-id="0cee9-115">Valore</span><span class="sxs-lookup"><span data-stu-id="0cee9-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0cee9-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0cee9-116">Minimum supported client</span></span><br/> | <span data-ttu-id="0cee9-117">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="0cee9-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="0cee9-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0cee9-118">Minimum supported server</span></span><br/> | <span data-ttu-id="0cee9-119">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="0cee9-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="0cee9-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0cee9-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="0cee9-121"><dt>ShObjIdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="0cee9-121"><dt>Shobjidl.h</dt></span></span> </dl>   |
| <span data-ttu-id="0cee9-122">IDL</span><span class="sxs-lookup"><span data-stu-id="0cee9-122">IDL</span></span><br/>                      | <dl> <span data-ttu-id="0cee9-123"><dt>ShObjIdl. idl</dt></span><span class="sxs-lookup"><span data-stu-id="0cee9-123"><dt>Shobjidl.idl</dt></span></span> </dl> |



 

 




