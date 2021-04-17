---
title: Metodo ISoftKbd GetSoftKeyboardTypeMode (Softkbdc. h)
description: Il metodo ISoftKbd GetSoftKeyboardTypeMode recupera la modalità del tipo per una tastiera soft.
ms.assetid: 77294652-b82e-4b69-bb55-5ebebc3c97c7
keywords:
- Framework servizi di testo Metodo GetSoftKeyboardTypeMode
- Framework dei servizi di testo del metodo GetSoftKeyboardTypeMode, interfaccia ISoftKbd
- ISoftKbd Interface Text Services Framework, metodo GetSoftKeyboardTypeMode
topic_type:
- apiref
api_name:
- ISoftKbd.GetSoftKeyboardTypeMode
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6aad6d60c50ee0050cf418018dd6db1c7a33efc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400207"
---
# <a name="isoftkbdgetsoftkeyboardtypemode-method"></a><span data-ttu-id="646a4-106">Metodo ISoftKbd:: GetSoftKeyboardTypeMode</span><span class="sxs-lookup"><span data-stu-id="646a4-106">ISoftKbd::GetSoftKeyboardTypeMode method</span></span>

<span data-ttu-id="646a4-107">Il metodo **ISoftKbd:: GetSoftKeyboardTypeMode** recupera la modalità del tipo per una tastiera soft.</span><span class="sxs-lookup"><span data-stu-id="646a4-107">The **ISoftKbd::GetSoftKeyboardTypeMode** method retrieves the type mode for a soft keyboard.</span></span>

## <a name="syntax"></a><span data-ttu-id="646a4-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="646a4-108">Syntax</span></span>


```C++
HRESULT GetSoftKeyboardTypeMode(
  [out] TYPEMODE *lpTypeMode
);
```



## <a name="parameters"></a><span data-ttu-id="646a4-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="646a4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="646a4-110">*lpTypeMode* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="646a4-110">*lpTypeMode* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="646a4-111">Puntatore a un buffer in cui questo metodo recupera la modalità del tipo.</span><span class="sxs-lookup"><span data-stu-id="646a4-111">Pointer to a buffer in which this method retrieves the type mode.</span></span> <span data-ttu-id="646a4-112">I valori possibili sono definiti per l'enumerazione [**TYPEMODE**](typemode.md) .</span><span class="sxs-lookup"><span data-stu-id="646a4-112">Possible values are defined for the [**TYPEMODE**](typemode.md) enumeration.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="646a4-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="646a4-113">Return value</span></span>

<span data-ttu-id="646a4-114">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="646a4-114">This method can return one of these values.</span></span>



| <span data-ttu-id="646a4-115">Valore</span><span class="sxs-lookup"><span data-stu-id="646a4-115">Value</span></span>                                                                                        | <span data-ttu-id="646a4-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="646a4-116">Description</span></span>                                       |
|----------------------------------------------------------------------------------------------|---------------------------------------------------|
| <dl> <span data-ttu-id="646a4-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="646a4-117"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="646a4-118">Il metodo è stato eseguito correttamente.</span><span class="sxs-lookup"><span data-stu-id="646a4-118">The method was successful.</span></span><br/>             |
| <dl> <span data-ttu-id="646a4-119"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="646a4-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="646a4-120">Il parametro *lpTypeMode* non è valido.</span><span class="sxs-lookup"><span data-stu-id="646a4-120">The *lpTypeMode* parameter is invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="646a4-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="646a4-121">Requirements</span></span>



| <span data-ttu-id="646a4-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="646a4-122">Requirement</span></span> | <span data-ttu-id="646a4-123">Valore</span><span class="sxs-lookup"><span data-stu-id="646a4-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="646a4-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="646a4-124">Minimum supported client</span></span><br/> | <span data-ttu-id="646a4-125">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="646a4-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="646a4-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="646a4-126">Minimum supported server</span></span><br/> | <span data-ttu-id="646a4-127">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="646a4-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="646a4-128">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="646a4-128">Redistributable</span></span><br/>          | <span data-ttu-id="646a4-129">TSF 1,0 su Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="646a4-129">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="646a4-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="646a4-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="646a4-131"><dt>Softkbdc. h</dt></span><span class="sxs-lookup"><span data-stu-id="646a4-131"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="646a4-132">IDL</span><span class="sxs-lookup"><span data-stu-id="646a4-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="646a4-133"><dt>Softkbd. idl</dt></span><span class="sxs-lookup"><span data-stu-id="646a4-133"><dt>Softkbd.idl</dt></span></span> </dl> |
| <span data-ttu-id="646a4-134">DLL</span><span class="sxs-lookup"><span data-stu-id="646a4-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="646a4-135"><dt>Softkbd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="646a4-135"><dt>Softkbd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="646a4-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="646a4-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="646a4-137">**ISoftKbd**</span><span class="sxs-lookup"><span data-stu-id="646a4-137">**ISoftKbd**</span></span>](isoftkbd.md)
</dt> <dt>

[<span data-ttu-id="646a4-138">**ISoftKbd::SetSoftKeyboardTypeMode**</span><span class="sxs-lookup"><span data-stu-id="646a4-138">**ISoftKbd::SetSoftKeyboardTypeMode**</span></span>](isoftkbd-setsoftkeyboardtypemode.md)
</dt> <dt>

[<span data-ttu-id="646a4-139">**TYPEMODE**</span><span class="sxs-lookup"><span data-stu-id="646a4-139">**TYPEMODE**</span></span>](typemode.md)
</dt> </dl>

 

 





