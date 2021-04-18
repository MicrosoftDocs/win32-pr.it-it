---
title: Metodo ISoftKbd DestroySoftKeyboardWindow (Softkbdc. h)
description: Il metodo ISoftKbd DestroySoftKeyboardWindow Elimina una finestra della tastiera soft.
ms.assetid: 44030934-7b4a-46c1-95ea-709fc9004e43
keywords:
- Framework servizi di testo Metodo DestroySoftKeyboardWindow
- Framework dei servizi di testo del metodo DestroySoftKeyboardWindow, interfaccia ISoftKbd
- ISoftKbd Interface Text Services Framework, metodo DestroySoftKeyboardWindow
topic_type:
- apiref
api_name:
- ISoftKbd.DestroySoftKeyboardWindow
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb0c460912e8b891503771425fc72484fcc471ff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301686"
---
# <a name="isoftkbddestroysoftkeyboardwindow-method"></a><span data-ttu-id="50510-106">ISoftKbd::D Metodo estroySoftKeyboardWindow</span><span class="sxs-lookup"><span data-stu-id="50510-106">ISoftKbd::DestroySoftKeyboardWindow method</span></span>

<span data-ttu-id="50510-107">Il metodo **ISoftKbd::D estroysoftkeyboardwindow** Elimina una finestra della tastiera soft.</span><span class="sxs-lookup"><span data-stu-id="50510-107">The **ISoftKbd::DestroySoftKeyboardWindow** method destroys a soft keyboard window.</span></span>

## <a name="syntax"></a><span data-ttu-id="50510-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="50510-108">Syntax</span></span>


```C++
HRESULT DestroySoftKeyboardWindow();
```



## <a name="parameters"></a><span data-ttu-id="50510-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="50510-109">Parameters</span></span>

<span data-ttu-id="50510-110">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="50510-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="50510-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="50510-111">Return value</span></span>

<span data-ttu-id="50510-112">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="50510-112">This method can return one of these values.</span></span>



| <span data-ttu-id="50510-113">Valore</span><span class="sxs-lookup"><span data-stu-id="50510-113">Value</span></span>                                                                                | <span data-ttu-id="50510-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="50510-114">Description</span></span>                           |
|--------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="50510-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="50510-115"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="50510-116">Il metodo è stato eseguito correttamente.</span><span class="sxs-lookup"><span data-stu-id="50510-116">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="50510-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="50510-117">Remarks</span></span>

<span data-ttu-id="50510-118">Questo metodo rimuove una finestra di tastiera soft creata in precedenza con una chiamata a [**ISoftKbd:: CreateSoftKeyboardWindow**](isoftkbd-createsoftkeyboardwindow.md).</span><span class="sxs-lookup"><span data-stu-id="50510-118">This method removes a soft keyboard window previously created with a call to [**ISoftKbd::CreateSoftKeyboardWindow**](isoftkbd-createsoftkeyboardwindow.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="50510-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="50510-119">Requirements</span></span>



| <span data-ttu-id="50510-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="50510-120">Requirement</span></span> | <span data-ttu-id="50510-121">Valore</span><span class="sxs-lookup"><span data-stu-id="50510-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="50510-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="50510-122">Minimum supported client</span></span><br/> | <span data-ttu-id="50510-123">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="50510-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="50510-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="50510-124">Minimum supported server</span></span><br/> | <span data-ttu-id="50510-125">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="50510-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="50510-126">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="50510-126">Redistributable</span></span><br/>          | <span data-ttu-id="50510-127">TSF 1,0 su Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="50510-127">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="50510-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="50510-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="50510-129"><dt>Softkbdc. h</dt></span><span class="sxs-lookup"><span data-stu-id="50510-129"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="50510-130">IDL</span><span class="sxs-lookup"><span data-stu-id="50510-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="50510-131"><dt>Softkbd. idl</dt></span><span class="sxs-lookup"><span data-stu-id="50510-131"><dt>Softkbd.idl</dt></span></span> </dl> |
| <span data-ttu-id="50510-132">DLL</span><span class="sxs-lookup"><span data-stu-id="50510-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="50510-133"><dt>Softkbd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="50510-133"><dt>Softkbd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="50510-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="50510-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50510-135">**ISoftKbd**</span><span class="sxs-lookup"><span data-stu-id="50510-135">**ISoftKbd**</span></span>](isoftkbd.md)
</dt> <dt>

[<span data-ttu-id="50510-136">**ISoftKbd::CreateSoftKeyboardWindow**</span><span class="sxs-lookup"><span data-stu-id="50510-136">**ISoftKbd::CreateSoftKeyboardWindow**</span></span>](isoftkbd-createsoftkeyboardwindow.md)
</dt> </dl>

 

 





