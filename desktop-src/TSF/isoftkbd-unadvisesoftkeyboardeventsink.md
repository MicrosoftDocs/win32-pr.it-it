---
title: Metodo ISoftKbd UnadviseSoftKeyboardEventSink (Softkbdc. h)
description: Il metodo ISoftKbd UnadviseSoftKeyboardEventSink rimuove un sink di evento della tastiera soft.
ms.assetid: 785340bd-c4f6-4c80-a492-6e60d1c1d552
keywords:
- Framework servizi di testo Metodo UnadviseSoftKeyboardEventSink
- Framework dei servizi di testo del metodo UnadviseSoftKeyboardEventSink, interfaccia ISoftKbd
- ISoftKbd Interface Text Services Framework, metodo UnadviseSoftKeyboardEventSink
topic_type:
- apiref
api_name:
- ISoftKbd.UnadviseSoftKeyboardEventSink
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a77129d1b5df024964af4ab19318963708d4b3d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742786"
---
# <a name="isoftkbdunadvisesoftkeyboardeventsink-method"></a><span data-ttu-id="c9e6d-106">Metodo ISoftKbd:: UnadviseSoftKeyboardEventSink</span><span class="sxs-lookup"><span data-stu-id="c9e6d-106">ISoftKbd::UnadviseSoftKeyboardEventSink method</span></span>

<span data-ttu-id="c9e6d-107">Il metodo **ISoftKbd:: UnadviseSoftKeyboardEventSink** rimuove un sink di evento della tastiera soft.</span><span class="sxs-lookup"><span data-stu-id="c9e6d-107">The **ISoftKbd::UnadviseSoftKeyboardEventSink** method removes a soft keyboard event sink.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9e6d-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c9e6d-108">Syntax</span></span>


```C++
HRESULT UnadviseSoftKeyboardEventSink(
  [in] TfClientId tid
);
```



## <a name="parameters"></a><span data-ttu-id="c9e6d-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="c9e6d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9e6d-110">*TID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c9e6d-110">*tid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9e6d-111">Identificatore del client proprietario del sink di evento della tastiera soft.</span><span class="sxs-lookup"><span data-stu-id="c9e6d-111">Identifier of the client that owns the soft keyboard event sink.</span></span> <span data-ttu-id="c9e6d-112">Questo valore è stato passato quando è stato installato il sink di evento utilizzando [ISoftKbd:: AdviseSoftKeyboardEventSink](isoftkbd-advisesoftkeyboardeventsink.md).</span><span class="sxs-lookup"><span data-stu-id="c9e6d-112">This value was passed when the event sink was installed using [ISoftKbd::AdviseSoftKeyboardEventSink](isoftkbd-advisesoftkeyboardeventsink.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c9e6d-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c9e6d-113">Return value</span></span>

<span data-ttu-id="c9e6d-114">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="c9e6d-114">This method can return one of these values.</span></span>



| <span data-ttu-id="c9e6d-115">Valore</span><span class="sxs-lookup"><span data-stu-id="c9e6d-115">Value</span></span>                                                                                                   | <span data-ttu-id="c9e6d-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c9e6d-116">Description</span></span>                                                   |
|---------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <dl> <span data-ttu-id="c9e6d-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="c9e6d-117"><dt>**S\_OK**</dt></span></span> </dl>                    | <span data-ttu-id="c9e6d-118">Il metodo è stato eseguito correttamente.</span><span class="sxs-lookup"><span data-stu-id="c9e6d-118">The method was successful.</span></span><br/>                         |
| <dl> <span data-ttu-id="c9e6d-119"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="c9e6d-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl>            | <span data-ttu-id="c9e6d-120">Il parametro *TID* non è valido.</span><span class="sxs-lookup"><span data-stu-id="c9e6d-120">The *tid* parameter is invalid.</span></span><br/>                    |
| <dl> <span data-ttu-id="c9e6d-121"><dt>**Connetti \_ E \_ NOCONNECTION**</dt></span><span class="sxs-lookup"><span data-stu-id="c9e6d-121"><dt>**CONNECT\_E\_NOCONNECTION**</dt></span></span> </dl> | <span data-ttu-id="c9e6d-122">Il sink di notifica identificato da *TID* non è stato trovato.</span><span class="sxs-lookup"><span data-stu-id="c9e6d-122">The advise sink identified by *tid* was not found.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="c9e6d-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c9e6d-123">Requirements</span></span>



| <span data-ttu-id="c9e6d-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="c9e6d-124">Requirement</span></span> | <span data-ttu-id="c9e6d-125">Valore</span><span class="sxs-lookup"><span data-stu-id="c9e6d-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c9e6d-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c9e6d-126">Minimum supported client</span></span><br/> | <span data-ttu-id="c9e6d-127">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="c9e6d-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="c9e6d-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c9e6d-128">Minimum supported server</span></span><br/> | <span data-ttu-id="c9e6d-129">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="c9e6d-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="c9e6d-130">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="c9e6d-130">Redistributable</span></span><br/>          | <span data-ttu-id="c9e6d-131">TSF 1,0 su Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="c9e6d-131">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="c9e6d-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c9e6d-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="c9e6d-133"><dt>Softkbdc. h</dt></span><span class="sxs-lookup"><span data-stu-id="c9e6d-133"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="c9e6d-134">IDL</span><span class="sxs-lookup"><span data-stu-id="c9e6d-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c9e6d-135"><dt>Softkbd. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c9e6d-135"><dt>Softkbd.idl</dt></span></span> </dl> |
| <span data-ttu-id="c9e6d-136">DLL</span><span class="sxs-lookup"><span data-stu-id="c9e6d-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c9e6d-137"><dt>Softkbd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c9e6d-137"><dt>Softkbd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c9e6d-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c9e6d-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9e6d-139">**ISoftKbd**</span><span class="sxs-lookup"><span data-stu-id="c9e6d-139">**ISoftKbd**</span></span>](isoftkbd.md)
</dt> <dt>

[<span data-ttu-id="c9e6d-140">ISoftKbd::AdviseSoftKeyboardEventSink</span><span class="sxs-lookup"><span data-stu-id="c9e6d-140">ISoftKbd::AdviseSoftKeyboardEventSink</span></span>](isoftkbd-advisesoftkeyboardeventsink.md)
</dt> </dl>

 

 





