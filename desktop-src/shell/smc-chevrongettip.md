---
description: Richiede il titolo e il testo per un infotip della freccia di espansione per l'elemento specificato dalla struttura SMDATA associata.
ms.assetid: 7bce4079-994c-4eb0-ab86-9044701d85a1
title: Messaggio SMC_CHEVRONGETTIP (ShObjIdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 118056627d19990648e81b69aa355f3df99ec286
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980175"
---
# <a name="smc_chevrongettip-message"></a><span data-ttu-id="46b31-103">\_Messaggio CHEVRONGETTIP di SMC</span><span class="sxs-lookup"><span data-stu-id="46b31-103">SMC\_CHEVRONGETTIP message</span></span>

<span data-ttu-id="46b31-104">Richiede il titolo e il testo per un infotip della freccia di espansione per l'elemento specificato dalla struttura [**SMDATA**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) associata.</span><span class="sxs-lookup"><span data-stu-id="46b31-104">Requests the title and text for a chevron infotip for the item specified by the accompanying [**SMDATA**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) structure.</span></span>


```C++
SMC_CHEVRONGETTIP 
    wParam = (WPARAM) (LPWSTR) pwszTipTitle;
    lParam = (LPARAM) (LPWSTR) pwszTipText
            
```



## <a name="parameters"></a><span data-ttu-id="46b31-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="46b31-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="46b31-106">*pwszTipTitle*</span><span class="sxs-lookup"><span data-stu-id="46b31-106">*pwszTipTitle*</span></span> 
</dt> <dd>

<span data-ttu-id="46b31-107">Puntatore a un buffer che riceve una stringa Unicode con terminazione **null** che contiene il titolo di infotip.</span><span class="sxs-lookup"><span data-stu-id="46b31-107">A pointer to a buffer that receives a **NULL**-terminated Unicode string that contains the infotip's title.</span></span> <span data-ttu-id="46b31-108">Questa stringa non deve essere più lunga di un massimo di \_ caratteri di percorso, incluso il carattere di terminazione **null** .</span><span class="sxs-lookup"><span data-stu-id="46b31-108">This string must be no longer than MAX\_PATH characters long, including the terminating **NULL** character.</span></span>

</dd> <dt>

<span data-ttu-id="46b31-109">*pwszTipText*</span><span class="sxs-lookup"><span data-stu-id="46b31-109">*pwszTipText*</span></span> 
</dt> <dd>

<span data-ttu-id="46b31-110">Puntatore a un buffer che riceve una stringa Unicode con terminazione **null** che contiene il testo del infotip.</span><span class="sxs-lookup"><span data-stu-id="46b31-110">A pointer to a buffer that receives a **NULL**-terminated Unicode string that contains the infotip's text.</span></span> <span data-ttu-id="46b31-111">Questa stringa non deve essere più lunga di un massimo di \_ caratteri di percorso, incluso il carattere di terminazione **null** .</span><span class="sxs-lookup"><span data-stu-id="46b31-111">This string must be no longer than MAX\_PATH characters long, including the terminating **NULL** character.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="46b31-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="46b31-112">Return value</span></span>

<span data-ttu-id="46b31-113">Restituisce \_ OK.</span><span class="sxs-lookup"><span data-stu-id="46b31-113">Return S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="46b31-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="46b31-114">Remarks</span></span>

<span data-ttu-id="46b31-115">Questa notifica viene ricevuta dal metodo [**IShellMenuCallback:: CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) .</span><span class="sxs-lookup"><span data-stu-id="46b31-115">This notification is received by the [**IShellMenuCallback::CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="46b31-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="46b31-116">Requirements</span></span>



| <span data-ttu-id="46b31-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="46b31-117">Requirement</span></span> | <span data-ttu-id="46b31-118">Valore</span><span class="sxs-lookup"><span data-stu-id="46b31-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="46b31-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="46b31-119">Minimum supported client</span></span><br/> | <span data-ttu-id="46b31-120">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="46b31-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="46b31-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="46b31-121">Minimum supported server</span></span><br/> | <span data-ttu-id="46b31-122">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="46b31-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="46b31-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="46b31-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="46b31-124"><dt>ShObjIdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="46b31-124"><dt>Shobjidl.h</dt></span></span> </dl>   |
| <span data-ttu-id="46b31-125">IDL</span><span class="sxs-lookup"><span data-stu-id="46b31-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="46b31-126"><dt>ShObjIdl. idl</dt></span><span class="sxs-lookup"><span data-stu-id="46b31-126"><dt>Shobjidl.idl</dt></span></span> </dl> |



 

 




