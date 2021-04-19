---
title: Metodo ISoftKbd SetSoftKeyboardTextFont (Softkbdc. h)
description: Il metodo ISoftKbd SetSoftKeyboardTextFont imposta il tipo di carattere del testo utilizzato da una tastiera soft.
ms.assetid: 14705723-4592-40ef-9ebb-1c44c10c3cda
keywords:
- Framework servizi di testo Metodo SetSoftKeyboardTextFont
- Framework dei servizi di testo del metodo SetSoftKeyboardTextFont, interfaccia ISoftKbd
- ISoftKbd Interface Text Services Framework, metodo SetSoftKeyboardTextFont
topic_type:
- apiref
api_name:
- ISoftKbd.SetSoftKeyboardTextFont
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ff0a9adce61bc1a671d28c6e5d6ac5b6d329b42
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302180"
---
# <a name="isoftkbdsetsoftkeyboardtextfont-method"></a><span data-ttu-id="aa0c0-106">Metodo ISoftKbd:: SetSoftKeyboardTextFont</span><span class="sxs-lookup"><span data-stu-id="aa0c0-106">ISoftKbd::SetSoftKeyboardTextFont method</span></span>

<span data-ttu-id="aa0c0-107">Il metodo **ISoftKbd:: SetSoftKeyboardTextFont** imposta il tipo di carattere del testo utilizzato da una tastiera soft.</span><span class="sxs-lookup"><span data-stu-id="aa0c0-107">The **ISoftKbd::SetSoftKeyboardTextFont** method sets the text font used by a soft keyboard.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa0c0-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="aa0c0-108">Syntax</span></span>


```C++
HRESULT SetSoftKeyboardTextFont(
  [in] LOGFONTW *pLogFont
);
```



## <a name="parameters"></a><span data-ttu-id="aa0c0-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="aa0c0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aa0c0-110">*pLogFont* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="aa0c0-110">*pLogFont* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aa0c0-111">Puntatore a una struttura [**Campo LOGFONTW**](/windows/win32/api/wingdi/ns-wingdi-logfonta) che definisce il tipo di carattere del testo per la tastiera soft.</span><span class="sxs-lookup"><span data-stu-id="aa0c0-111">Pointer to a [**LOGFONTW**](/windows/win32/api/wingdi/ns-wingdi-logfonta) structure defining the text font for the soft keyboard.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aa0c0-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="aa0c0-112">Return value</span></span>

<span data-ttu-id="aa0c0-113">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="aa0c0-113">This method can return one of these values.</span></span>



| <span data-ttu-id="aa0c0-114">Valore</span><span class="sxs-lookup"><span data-stu-id="aa0c0-114">Value</span></span>                                                                                        | <span data-ttu-id="aa0c0-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="aa0c0-115">Description</span></span>                                     |
|----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="aa0c0-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="aa0c0-116"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="aa0c0-117">Il metodo è stato eseguito correttamente.</span><span class="sxs-lookup"><span data-stu-id="aa0c0-117">The method was successful.</span></span><br/>           |
| <dl> <span data-ttu-id="aa0c0-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="aa0c0-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="aa0c0-119">Il parametro *pLogFont* non è valido.</span><span class="sxs-lookup"><span data-stu-id="aa0c0-119">The *pLogFont* parameter is invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="aa0c0-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="aa0c0-120">Requirements</span></span>



| <span data-ttu-id="aa0c0-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="aa0c0-121">Requirement</span></span> | <span data-ttu-id="aa0c0-122">Valore</span><span class="sxs-lookup"><span data-stu-id="aa0c0-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="aa0c0-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="aa0c0-123">Minimum supported client</span></span><br/> | <span data-ttu-id="aa0c0-124">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="aa0c0-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="aa0c0-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="aa0c0-125">Minimum supported server</span></span><br/> | <span data-ttu-id="aa0c0-126">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="aa0c0-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="aa0c0-127">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="aa0c0-127">Redistributable</span></span><br/>          | <span data-ttu-id="aa0c0-128">TSF 1,0 su Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="aa0c0-128">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="aa0c0-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="aa0c0-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="aa0c0-130"><dt>Softkbdc. h</dt></span><span class="sxs-lookup"><span data-stu-id="aa0c0-130"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="aa0c0-131">IDL</span><span class="sxs-lookup"><span data-stu-id="aa0c0-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="aa0c0-132"><dt>Softkbd. idl</dt></span><span class="sxs-lookup"><span data-stu-id="aa0c0-132"><dt>Softkbd.idl</dt></span></span> </dl> |
| <span data-ttu-id="aa0c0-133">DLL</span><span class="sxs-lookup"><span data-stu-id="aa0c0-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aa0c0-134"><dt>Softkbd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aa0c0-134"><dt>Softkbd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aa0c0-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="aa0c0-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa0c0-136">**ISoftKbd**</span><span class="sxs-lookup"><span data-stu-id="aa0c0-136">**ISoftKbd**</span></span>](isoftkbd.md)
</dt> <dt>

[<span data-ttu-id="aa0c0-137">**ISoftKbd::GetSoftKeyboardTextFont**</span><span class="sxs-lookup"><span data-stu-id="aa0c0-137">**ISoftKbd::GetSoftKeyboardTextFont**</span></span>](isoftkbd-getsoftkeyboardtextfont.md)
</dt> </dl>

 

