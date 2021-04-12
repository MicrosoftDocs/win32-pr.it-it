---
title: Metodo ISoftKbd SetSoftKeyboardTypeMode (Softkbdc. h)
description: Il metodo ISoftKbd SetSoftKeyboardTypeMode imposta la modalità del tipo per una tastiera soft.
ms.assetid: 0b5b5056-59b3-41c7-bc43-70b5c3cd51c2
keywords:
- Framework servizi di testo Metodo SetSoftKeyboardTypeMode
- Framework dei servizi di testo del metodo SetSoftKeyboardTypeMode, interfaccia ISoftKbd
- ISoftKbd Interface Text Services Framework, metodo SetSoftKeyboardTypeMode
topic_type:
- apiref
api_name:
- ISoftKbd.SetSoftKeyboardTypeMode
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55c01465debc42926888e2cb12a3a5b9d884498b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478209"
---
# <a name="isoftkbdsetsoftkeyboardtypemode-method"></a><span data-ttu-id="f09f6-106">Metodo ISoftKbd:: SetSoftKeyboardTypeMode</span><span class="sxs-lookup"><span data-stu-id="f09f6-106">ISoftKbd::SetSoftKeyboardTypeMode method</span></span>

<span data-ttu-id="f09f6-107">Il metodo **ISoftKbd:: SetSoftKeyboardTypeMode** imposta la modalità del tipo per una tastiera soft.</span><span class="sxs-lookup"><span data-stu-id="f09f6-107">The **ISoftKbd::SetSoftKeyboardTypeMode** method sets the type mode for a soft keyboard.</span></span>

## <a name="syntax"></a><span data-ttu-id="f09f6-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f09f6-108">Syntax</span></span>


```C++
HRESULT SetSoftKeyboardTypeMode(
  [in] TYPEMODE TypeMode
);
```



## <a name="parameters"></a><span data-ttu-id="f09f6-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="f09f6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f09f6-110">*TypeMode* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f09f6-110">*TypeMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f09f6-111">Modalità del tipo.</span><span class="sxs-lookup"><span data-stu-id="f09f6-111">The type mode.</span></span> <span data-ttu-id="f09f6-112">I valori possibili sono definiti per l'enumerazione [**TYPEMODE**](typemode.md) .</span><span class="sxs-lookup"><span data-stu-id="f09f6-112">Possible values are defined for the [**TYPEMODE**](typemode.md) enumeration.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f09f6-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f09f6-113">Return value</span></span>

<span data-ttu-id="f09f6-114">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="f09f6-114">This method can return one of these values.</span></span>



| <span data-ttu-id="f09f6-115">Valore</span><span class="sxs-lookup"><span data-stu-id="f09f6-115">Value</span></span>                                                                                        | <span data-ttu-id="f09f6-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f09f6-116">Description</span></span>                                     |
|----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="f09f6-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="f09f6-117"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="f09f6-118">Il metodo è stato eseguito correttamente.</span><span class="sxs-lookup"><span data-stu-id="f09f6-118">The method was successful.</span></span><br/>           |
| <dl> <span data-ttu-id="f09f6-119"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="f09f6-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="f09f6-120">Il parametro *TypeMode* non è valido.</span><span class="sxs-lookup"><span data-stu-id="f09f6-120">The *TypeMode* parameter is invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="f09f6-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f09f6-121">Requirements</span></span>



| <span data-ttu-id="f09f6-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="f09f6-122">Requirement</span></span> | <span data-ttu-id="f09f6-123">Valore</span><span class="sxs-lookup"><span data-stu-id="f09f6-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f09f6-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f09f6-124">Minimum supported client</span></span><br/> | <span data-ttu-id="f09f6-125">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="f09f6-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="f09f6-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f09f6-126">Minimum supported server</span></span><br/> | <span data-ttu-id="f09f6-127">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="f09f6-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="f09f6-128">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="f09f6-128">Redistributable</span></span><br/>          | <span data-ttu-id="f09f6-129">TSF 1,0 su Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="f09f6-129">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="f09f6-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f09f6-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="f09f6-131"><dt>Softkbdc. h</dt></span><span class="sxs-lookup"><span data-stu-id="f09f6-131"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="f09f6-132">IDL</span><span class="sxs-lookup"><span data-stu-id="f09f6-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f09f6-133"><dt>Softkbd. idl</dt></span><span class="sxs-lookup"><span data-stu-id="f09f6-133"><dt>Softkbd.idl</dt></span></span> </dl> |
| <span data-ttu-id="f09f6-134">DLL</span><span class="sxs-lookup"><span data-stu-id="f09f6-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f09f6-135"><dt>Softkbd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f09f6-135"><dt>Softkbd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f09f6-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f09f6-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f09f6-137">**ISoftKbd**</span><span class="sxs-lookup"><span data-stu-id="f09f6-137">**ISoftKbd**</span></span>](isoftkbd.md)
</dt> <dt>

[<span data-ttu-id="f09f6-138">**ISoftKbd::GetSoftKeyboardTypeMode**</span><span class="sxs-lookup"><span data-stu-id="f09f6-138">**ISoftKbd::GetSoftKeyboardTypeMode**</span></span>](isoftkbd-getsoftkeyboardtypemode.md)
</dt> <dt>

[<span data-ttu-id="f09f6-139">**TYPEMODE**</span><span class="sxs-lookup"><span data-stu-id="f09f6-139">**TYPEMODE**</span></span>](typemode.md)
</dt> </dl>

 

 





