---
title: Metodo ISoftKbd GetSoftKeyboardColors (Softkbdc. h)
description: Il metodo ISoftKbd GetSoftKeyboardColors Recupera il colore della tastiera flessibile corrispondente al tipo di colore fornito.
ms.assetid: d59d249c-a1c4-4d6a-add6-632be55a7549
keywords:
- Framework servizi di testo Metodo GetSoftKeyboardColors
- Framework dei servizi di testo del metodo GetSoftKeyboardColors, interfaccia ISoftKbd
- ISoftKbd Interface Text Services Framework, metodo GetSoftKeyboardColors
topic_type:
- apiref
api_name:
- ISoftKbd.GetSoftKeyboardColors
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f8f184dc04ddcbef18a9279000b1a68acd35bd3
ms.sourcegitcommit: d6bf2018c588c9782e1eed21b3cdea3523ec6955
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2021
ms.locfileid: "106320171"
---
# <a name="isoftkbdgetsoftkeyboardcolors-method"></a><span data-ttu-id="ea3f1-106">Metodo ISoftKbd:: GetSoftKeyboardColors</span><span class="sxs-lookup"><span data-stu-id="ea3f1-106">ISoftKbd::GetSoftKeyboardColors method</span></span>

<span data-ttu-id="ea3f1-107">Il metodo **ISoftKbd:: GetSoftKeyboardColors** Recupera il colore della tastiera flessibile corrispondente al tipo di colore fornito.</span><span class="sxs-lookup"><span data-stu-id="ea3f1-107">The **ISoftKbd::GetSoftKeyboardColors** method retrieves the soft keyboard color corresponding to the supplied color type.</span></span>

## <a name="syntax"></a><span data-ttu-id="ea3f1-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ea3f1-108">Syntax</span></span>


```C++
HRESULT GetSoftKeyboardColors(
  [in]  COLORTYPE colorType,
  [out] COLORREF  *lpColor
);
```



## <a name="parameters"></a><span data-ttu-id="ea3f1-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="ea3f1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ea3f1-110">*ColorType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ea3f1-110">*colorType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ea3f1-111">Valore che specifica il tipo di colore da recuperare per la tastiera soft.</span><span class="sxs-lookup"><span data-stu-id="ea3f1-111">A value specifying the color type to retrieve for the soft keyboard.</span></span> <span data-ttu-id="ea3f1-112">I valori possibili sono definiti per l'enumerazione [**ColorType**](/windows/win32/api/icm/ne-icm-colortype) .</span><span class="sxs-lookup"><span data-stu-id="ea3f1-112">Possible values are defined for the [**COLORTYPE**](/windows/win32/api/icm/ne-icm-colortype) enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="ea3f1-113">*lpColor* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="ea3f1-113">*lpColor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ea3f1-114">Puntatore a un buffer in cui questo metodo recupera un valore [**COLORREF**](/windows/desktop/gdi/colorref) a 32 bit specificando un colore RGB.</span><span class="sxs-lookup"><span data-stu-id="ea3f1-114">Pointer to a buffer in which this method retrieves a 32-bit [**COLORREF**](/windows/desktop/gdi/colorref) value specifying an RGB color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ea3f1-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ea3f1-115">Return value</span></span>

<span data-ttu-id="ea3f1-116">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="ea3f1-116">This method can return one of these values.</span></span>



| <span data-ttu-id="ea3f1-117">Valore</span><span class="sxs-lookup"><span data-stu-id="ea3f1-117">Value</span></span>                                                                                        | <span data-ttu-id="ea3f1-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ea3f1-118">Description</span></span>                                  |
|----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="ea3f1-119"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="ea3f1-119"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="ea3f1-120">Il metodo è stato eseguito correttamente.</span><span class="sxs-lookup"><span data-stu-id="ea3f1-120">The method was successful.</span></span><br/>        |
| <dl> <span data-ttu-id="ea3f1-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="ea3f1-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="ea3f1-122">Uno dei parametri non è valido.</span><span class="sxs-lookup"><span data-stu-id="ea3f1-122">One of the parameters is invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="ea3f1-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ea3f1-123">Requirements</span></span>



| <span data-ttu-id="ea3f1-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="ea3f1-124">Requirement</span></span> | <span data-ttu-id="ea3f1-125">Valore</span><span class="sxs-lookup"><span data-stu-id="ea3f1-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ea3f1-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ea3f1-126">Minimum supported client</span></span><br/> | <span data-ttu-id="ea3f1-127">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="ea3f1-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="ea3f1-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ea3f1-128">Minimum supported server</span></span><br/> | <span data-ttu-id="ea3f1-129">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="ea3f1-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="ea3f1-130">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="ea3f1-130">Redistributable</span></span><br/>          | <span data-ttu-id="ea3f1-131">TSF 1,0 su Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="ea3f1-131">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="ea3f1-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ea3f1-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="ea3f1-133"><dt>Softkbdc. h</dt></span><span class="sxs-lookup"><span data-stu-id="ea3f1-133"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="ea3f1-134">IDL</span><span class="sxs-lookup"><span data-stu-id="ea3f1-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ea3f1-135"><dt>Softkbd. idl</dt></span><span class="sxs-lookup"><span data-stu-id="ea3f1-135"><dt>Softkbd.idl</dt></span></span> </dl> |
| <span data-ttu-id="ea3f1-136">DLL</span><span class="sxs-lookup"><span data-stu-id="ea3f1-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ea3f1-137"><dt>Softkbd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ea3f1-137"><dt>Softkbd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ea3f1-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ea3f1-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea3f1-139">**ISoftKbd**</span><span class="sxs-lookup"><span data-stu-id="ea3f1-139">**ISoftKbd**</span></span>](isoftkbd.md)
</dt> <dt>

[<span data-ttu-id="ea3f1-140">**ISoftKbd::SetSoftKeyboardColors**</span><span class="sxs-lookup"><span data-stu-id="ea3f1-140">**ISoftKbd::SetSoftKeyboardColors**</span></span>](/windows/desktop/TSF/isoftkbd-setsoftkeyboardcolors)
</dt> <dt>

[<span data-ttu-id="ea3f1-141">**COLORTYPE**</span><span class="sxs-lookup"><span data-stu-id="ea3f1-141">**COLORTYPE**</span></span>](/windows/win32/api/icm/ne-icm-colortype)
</dt> <dt>

[<span data-ttu-id="ea3f1-142">**COLORREF**</span><span class="sxs-lookup"><span data-stu-id="ea3f1-142">**COLORREF**</span></span>](/windows/desktop/gdi/colorref)
</dt> </dl>

 

