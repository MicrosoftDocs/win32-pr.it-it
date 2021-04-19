---
title: Metodo ISoftKbd SetSoftKeyboardColors (Softkbdc. h)
description: Il metodo ISoftKbd SetSoftKeyboardColors imposta il colore della tastiera soft per il tipo di colore specificato.
ms.assetid: 1abbff35-a5ef-4119-9367-60b6e0961c59
keywords:
- Framework servizi di testo Metodo SetSoftKeyboardColors
- Framework dei servizi di testo del metodo SetSoftKeyboardColors, interfaccia ISoftKbd
- ISoftKbd Interface Text Services Framework, metodo SetSoftKeyboardColors
topic_type:
- apiref
api_name:
- ISoftKbd.SetSoftKeyboardColors
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38357331db2440c35ca7557d08c97729fde9c9f0
ms.sourcegitcommit: d6bf2018c588c9782e1eed21b3cdea3523ec6955
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2021
ms.locfileid: "106320173"
---
# <a name="isoftkbdsetsoftkeyboardcolors-method"></a><span data-ttu-id="d6a09-106">Metodo ISoftKbd:: SetSoftKeyboardColors</span><span class="sxs-lookup"><span data-stu-id="d6a09-106">ISoftKbd::SetSoftKeyboardColors method</span></span>

<span data-ttu-id="d6a09-107">Il metodo **ISoftKbd:: SetSoftKeyboardColors** imposta il colore della tastiera soft per il tipo di colore specificato.</span><span class="sxs-lookup"><span data-stu-id="d6a09-107">The **ISoftKbd::SetSoftKeyboardColors** method sets the soft keyboard color for the specified color type.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6a09-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d6a09-108">Syntax</span></span>


```C++
HRESULT SetSoftKeyboardColors(
  [in] COLORTYPE colorType,
  [in] COLORREF  Color
);
```



## <a name="parameters"></a><span data-ttu-id="d6a09-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="d6a09-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d6a09-110">*ColorType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d6a09-110">*colorType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6a09-111">Valore che specifica il tipo di colore per la tastiera soft.</span><span class="sxs-lookup"><span data-stu-id="d6a09-111">A value specifying the color type for the soft keyboard.</span></span> <span data-ttu-id="d6a09-112">I valori possibili sono definiti per l'enumerazione [**ColorType**](/windows/win32/api/icm/ne-icm-colortype) .</span><span class="sxs-lookup"><span data-stu-id="d6a09-112">Possible values are defined for the [**COLORTYPE**](/windows/win32/api/icm/ne-icm-colortype) enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="d6a09-113">*Colore* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d6a09-113">*Color* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6a09-114">Valore [**COLORREF**](/windows/desktop/gdi/colorref) a 32 bit che specifica un colore RGB.</span><span class="sxs-lookup"><span data-stu-id="d6a09-114">A 32-bit [**COLORREF**](/windows/desktop/gdi/colorref) value specifying an RGB color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d6a09-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d6a09-115">Return value</span></span>

<span data-ttu-id="d6a09-116">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="d6a09-116">This method can return one of these values.</span></span>



| <span data-ttu-id="d6a09-117">Valore</span><span class="sxs-lookup"><span data-stu-id="d6a09-117">Value</span></span>                                                                                        | <span data-ttu-id="d6a09-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d6a09-118">Description</span></span>                                  |
|----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="d6a09-119"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="d6a09-119"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="d6a09-120">Il metodo è stato eseguito correttamente.</span><span class="sxs-lookup"><span data-stu-id="d6a09-120">The method was successful.</span></span><br/>        |
| <dl> <span data-ttu-id="d6a09-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="d6a09-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="d6a09-122">Uno dei parametri non è valido.</span><span class="sxs-lookup"><span data-stu-id="d6a09-122">One of the parameters is invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="d6a09-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d6a09-123">Requirements</span></span>



| <span data-ttu-id="d6a09-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="d6a09-124">Requirement</span></span> | <span data-ttu-id="d6a09-125">Valore</span><span class="sxs-lookup"><span data-stu-id="d6a09-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d6a09-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d6a09-126">Minimum supported client</span></span><br/> | <span data-ttu-id="d6a09-127">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d6a09-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="d6a09-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d6a09-128">Minimum supported server</span></span><br/> | <span data-ttu-id="d6a09-129">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d6a09-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="d6a09-130">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="d6a09-130">Redistributable</span></span><br/>          | <span data-ttu-id="d6a09-131">TSF 1,0 su Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="d6a09-131">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="d6a09-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d6a09-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="d6a09-133"><dt>Softkbdc. h</dt></span><span class="sxs-lookup"><span data-stu-id="d6a09-133"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="d6a09-134">IDL</span><span class="sxs-lookup"><span data-stu-id="d6a09-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d6a09-135"><dt>Softkbd. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d6a09-135"><dt>Softkbd.idl</dt></span></span> </dl> |
| <span data-ttu-id="d6a09-136">DLL</span><span class="sxs-lookup"><span data-stu-id="d6a09-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d6a09-137"><dt>Softkbd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d6a09-137"><dt>Softkbd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d6a09-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d6a09-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6a09-139">**ISoftKbd**</span><span class="sxs-lookup"><span data-stu-id="d6a09-139">**ISoftKbd**</span></span>](isoftkbd.md)
</dt> <dt>

[<span data-ttu-id="d6a09-140">**ISoftKbd::GetSoftKeyboardColors**</span><span class="sxs-lookup"><span data-stu-id="d6a09-140">**ISoftKbd::GetSoftKeyboardColors**</span></span>](isoftkbd-getsoftkeyboardcolors.md)
</dt> <dt>

[<span data-ttu-id="d6a09-141">**COLORTYPE**</span><span class="sxs-lookup"><span data-stu-id="d6a09-141">**COLORTYPE**</span></span>](/windows/win32/api/icm/ne-icm-colortype)
</dt> <dt>

[<span data-ttu-id="d6a09-142">**COLORREF**</span><span class="sxs-lookup"><span data-stu-id="d6a09-142">**COLORREF**</span></span>](/windows/desktop/gdi/colorref)
</dt> </dl>

 

