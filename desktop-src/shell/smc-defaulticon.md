---
description: Restituisce l'icona predefinita per l'elemento specificato dalla struttura SMDATA associata.
title: Messaggio SMC_DEFAULTICON (ShObjIdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: d5f6789a-f160-4fba-ba64-b1a0c491fdaa
api_name:
- SMC_DEFAULTICON
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 10edab26c87dae4b1c9d2d5f06390fc608ba1edd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104994853"
---
# <a name="smc_defaulticon-message"></a><span data-ttu-id="caac9-103">\_Messaggio DEFAULTICON di SMC</span><span class="sxs-lookup"><span data-stu-id="caac9-103">SMC\_DEFAULTICON message</span></span>

<span data-ttu-id="caac9-104">Restituisce l'icona predefinita per l'elemento specificato dalla struttura [**SMDATA**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) associata.</span><span class="sxs-lookup"><span data-stu-id="caac9-104">Return the default icon for the item specified by the accompanying [**SMDATA**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) structure.</span></span>


```C++
SMC_DEFAULTICON 
    wParam = (WPARAM) (LPWSTR) pwszIcon;
    lParam = (LPARAM) (int) iIcon
            
```



## <a name="parameters"></a><span data-ttu-id="caac9-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="caac9-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="caac9-106">*pwszIcon*</span><span class="sxs-lookup"><span data-stu-id="caac9-106">*pwszIcon*</span></span> 
</dt> <dd>

<span data-ttu-id="caac9-107">Puntatore a una stringa che riceve il percorso completo del file che contiene l'icona predefinita.</span><span class="sxs-lookup"><span data-stu-id="caac9-107">A pointer to a string that receives the fully qualified path of the file that contains the default icon.</span></span>

</dd> <dt>

<span data-ttu-id="caac9-108">*iIcon*</span><span class="sxs-lookup"><span data-stu-id="caac9-108">*iIcon*</span></span> 
</dt> <dd>

<span data-ttu-id="caac9-109">Puntatore a un intero che riceve l'indice dell'icona nel file specificato da *pwszIcon*.</span><span class="sxs-lookup"><span data-stu-id="caac9-109">A pointer to an integer that receives the index of the icon in the file specified by *pwszIcon*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="caac9-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="caac9-110">Return value</span></span>

<span data-ttu-id="caac9-111">Restituisce \_ OK.</span><span class="sxs-lookup"><span data-stu-id="caac9-111">Return S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="caac9-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="caac9-112">Remarks</span></span>

<span data-ttu-id="caac9-113">Questa notifica viene ricevuta dal metodo [**IShellMenuCallback:: CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) .</span><span class="sxs-lookup"><span data-stu-id="caac9-113">This notification is received by the [**IShellMenuCallback::CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="caac9-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="caac9-114">Requirements</span></span>



| <span data-ttu-id="caac9-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="caac9-115">Requirement</span></span> | <span data-ttu-id="caac9-116">Valore</span><span class="sxs-lookup"><span data-stu-id="caac9-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="caac9-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="caac9-117">Minimum supported client</span></span><br/> | <span data-ttu-id="caac9-118">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="caac9-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="caac9-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="caac9-119">Minimum supported server</span></span><br/> | <span data-ttu-id="caac9-120">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="caac9-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="caac9-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="caac9-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="caac9-122"><dt>ShObjIdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="caac9-122"><dt>Shobjidl.h</dt></span></span> </dl>   |
| <span data-ttu-id="caac9-123">IDL</span><span class="sxs-lookup"><span data-stu-id="caac9-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="caac9-124"><dt>ShObjIdl. idl</dt></span><span class="sxs-lookup"><span data-stu-id="caac9-124"><dt>Shobjidl.idl</dt></span></span> </dl> |



 

 




