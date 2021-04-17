---
title: Metodo ISoftKbd AdviseSoftKeyboardEventSink (Softkbdc. h)
description: Il metodo ISoftKbd AdviseSoftKeyboardEventSink installa un sink di evento della tastiera soft per gestire le notifiche OnKeySelection dalla tastiera soft.
ms.assetid: f7a441dc-7bef-4fc0-bc62-c153a55a844c
keywords:
- Framework servizi di testo Metodo AdviseSoftKeyboardEventSink
- Framework dei servizi di testo del metodo AdviseSoftKeyboardEventSink, interfaccia ISoftKbd
- ISoftKbd Interface Text Services Framework, metodo AdviseSoftKeyboardEventSink
topic_type:
- apiref
api_name:
- ISoftKbd.AdviseSoftKeyboardEventSink
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ab17de2104c6104b044f027152cfc45cca968b6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400819"
---
# <a name="isoftkbdadvisesoftkeyboardeventsink-method"></a><span data-ttu-id="c64f5-106">Metodo ISoftKbd:: AdviseSoftKeyboardEventSink</span><span class="sxs-lookup"><span data-stu-id="c64f5-106">ISoftKbd::AdviseSoftKeyboardEventSink method</span></span>

<span data-ttu-id="c64f5-107">Il metodo **ISoftKbd:: AdviseSoftKeyboardEventSink** installa un sink di evento della tastiera soft per gestire le notifiche OnKeySelection dalla tastiera soft.</span><span class="sxs-lookup"><span data-stu-id="c64f5-107">The **ISoftKbd::AdviseSoftKeyboardEventSink** method installs a soft keyboard event sink to handle OnKeySelection notifications from the soft keyboard.</span></span>

## <a name="syntax"></a><span data-ttu-id="c64f5-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c64f5-108">Syntax</span></span>


```C++
HRESULT AdviseSoftKeyboardEventSink(
  [in]  DWORD    dwKeyboardId,
  [in]  REFIID   riid,
  [in]  IUnknown *punk,
  [out] DWORD    *pdwCookie
);
```



## <a name="parameters"></a><span data-ttu-id="c64f5-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="c64f5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c64f5-110">*dwKeyboardId* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c64f5-110">*dwKeyboardId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c64f5-111">Identificatore della tastiera soft.</span><span class="sxs-lookup"><span data-stu-id="c64f5-111">Identifier of the soft keyboard.</span></span>

</dd> <dt>

<span data-ttu-id="c64f5-112">*riid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c64f5-112">*riid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c64f5-113">Identificatore di interfaccia per l'interfaccia sink.</span><span class="sxs-lookup"><span data-stu-id="c64f5-113">Interface identifier for the sink interface.</span></span>

</dd> <dt>

<span data-ttu-id="c64f5-114">*punk* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c64f5-114">*punk* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c64f5-115">Puntatore a [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) per l'interfaccia sink specificata da *riid*.</span><span class="sxs-lookup"><span data-stu-id="c64f5-115">Pointer to [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) for the sink interface specified by *riid*.</span></span> <span data-ttu-id="c64f5-116">Questo parametro non può essere impostato su **null**.</span><span class="sxs-lookup"><span data-stu-id="c64f5-116">This parameter cannot be set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="c64f5-117">*pdwCookie* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="c64f5-117">*pdwCookie* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c64f5-118">Puntatore al buffer in cui questo metodo recupera il "cookie" della tastiera soft usato per la connessione al client.</span><span class="sxs-lookup"><span data-stu-id="c64f5-118">Pointer to the buffer in which this method retrieves the soft keyboard "cookie" used for connection to the client.</span></span> <span data-ttu-id="c64f5-119">Il cookie deve essere univoco per ogni connessione.</span><span class="sxs-lookup"><span data-stu-id="c64f5-119">The cookie must be unique for each connection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c64f5-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c64f5-120">Return value</span></span>

<span data-ttu-id="c64f5-121">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="c64f5-121">This method can return one of these values.</span></span>



| <span data-ttu-id="c64f5-122">Valore</span><span class="sxs-lookup"><span data-stu-id="c64f5-122">Value</span></span>                                                                                        | <span data-ttu-id="c64f5-123">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c64f5-123">Description</span></span>                                    |
|----------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="c64f5-124"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="c64f5-124"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="c64f5-125">Il metodo è stato eseguito correttamente.</span><span class="sxs-lookup"><span data-stu-id="c64f5-125">The method was successful.</span></span><br/>          |
| <dl> <span data-ttu-id="c64f5-126"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="c64f5-126"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="c64f5-127">Uno o più parametri non sono validi.</span><span class="sxs-lookup"><span data-stu-id="c64f5-127">One or more parameters are invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="c64f5-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c64f5-128">Requirements</span></span>



| <span data-ttu-id="c64f5-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="c64f5-129">Requirement</span></span> | <span data-ttu-id="c64f5-130">Valore</span><span class="sxs-lookup"><span data-stu-id="c64f5-130">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c64f5-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c64f5-131">Minimum supported client</span></span><br/> | <span data-ttu-id="c64f5-132">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="c64f5-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="c64f5-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c64f5-133">Minimum supported server</span></span><br/> | <span data-ttu-id="c64f5-134">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="c64f5-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="c64f5-135">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="c64f5-135">Redistributable</span></span><br/>          | <span data-ttu-id="c64f5-136">TSF 1,0 su Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="c64f5-136">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="c64f5-137">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c64f5-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="c64f5-138"><dt>Softkbdc. h</dt></span><span class="sxs-lookup"><span data-stu-id="c64f5-138"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="c64f5-139">IDL</span><span class="sxs-lookup"><span data-stu-id="c64f5-139">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c64f5-140"><dt>Softkbd. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c64f5-140"><dt>Softkbd.idl</dt></span></span> </dl> |
| <span data-ttu-id="c64f5-141">DLL</span><span class="sxs-lookup"><span data-stu-id="c64f5-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c64f5-142"><dt>Softkbd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c64f5-142"><dt>Softkbd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c64f5-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c64f5-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c64f5-144">**ISoftKbd**</span><span class="sxs-lookup"><span data-stu-id="c64f5-144">**ISoftKbd**</span></span>](isoftkbd.md)
</dt> <dt>

[<span data-ttu-id="c64f5-145">**ISoftKbd::UnadviseSoftKeyboardEventSink**</span><span class="sxs-lookup"><span data-stu-id="c64f5-145">**ISoftKbd::UnadviseSoftKeyboardEventSink**</span></span>](isoftkbd-unadvisesoftkeyboardeventsink.md)
</dt> </dl>

 

