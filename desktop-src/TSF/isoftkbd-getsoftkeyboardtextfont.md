---
title: Metodo ISoftKbd GetSoftKeyboardTextFont (Softkbdc. h)
description: Il metodo ISoftKbd GetSoftKeyboardTextFont Recupera il tipo di carattere del testo utilizzato da una tastiera soft.
ms.assetid: 73239359-70b4-47d6-abc5-9fee279ed3a6
keywords:
- Framework servizi di testo Metodo GetSoftKeyboardTextFont
- Framework dei servizi di testo del metodo GetSoftKeyboardTextFont, interfaccia ISoftKbd
- ISoftKbd Interface Text Services Framework, metodo GetSoftKeyboardTextFont
topic_type:
- apiref
api_name:
- ISoftKbd.GetSoftKeyboardTextFont
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce939347042415a9060459102cd8a56665ac2de0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120818"
---
# <a name="isoftkbdgetsoftkeyboardtextfont-method"></a><span data-ttu-id="9e1d1-106">Metodo ISoftKbd:: GetSoftKeyboardTextFont</span><span class="sxs-lookup"><span data-stu-id="9e1d1-106">ISoftKbd::GetSoftKeyboardTextFont method</span></span>

<span data-ttu-id="9e1d1-107">Il metodo **ISoftKbd:: GetSoftKeyboardTextFont** Recupera il tipo di carattere del testo utilizzato da una tastiera soft.</span><span class="sxs-lookup"><span data-stu-id="9e1d1-107">The **ISoftKbd::GetSoftKeyboardTextFont** method retrieves the text font used by a soft keyboard.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e1d1-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9e1d1-108">Syntax</span></span>


```C++
HRESULT GetSoftKeyboardTextFont(
  [out] LOGFONTW *pLogFont
);
```



## <a name="parameters"></a><span data-ttu-id="9e1d1-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="9e1d1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9e1d1-110">*pLogFont* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="9e1d1-110">*pLogFont* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9e1d1-111">Puntatore a un buffer in cui questo metodo recupera una struttura [**Campo LOGFONTW**](/windows/win32/api/wingdi/ns-wingdi-logfonta) che definisce il tipo di carattere del testo per la tastiera soft.</span><span class="sxs-lookup"><span data-stu-id="9e1d1-111">Pointer to a buffer in which this method retrieves a [**LOGFONTW**](/windows/win32/api/wingdi/ns-wingdi-logfonta) structure defining the text font for the soft keyboard.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9e1d1-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9e1d1-112">Return value</span></span>

<span data-ttu-id="9e1d1-113">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="9e1d1-113">This method can return one of these values.</span></span>



| <span data-ttu-id="9e1d1-114">Valore</span><span class="sxs-lookup"><span data-stu-id="9e1d1-114">Value</span></span>                                                                                        | <span data-ttu-id="9e1d1-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9e1d1-115">Description</span></span>                                     |
|----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="9e1d1-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="9e1d1-116"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="9e1d1-117">Il metodo è stato eseguito correttamente.</span><span class="sxs-lookup"><span data-stu-id="9e1d1-117">The method was successful.</span></span><br/>           |
| <dl> <span data-ttu-id="9e1d1-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="9e1d1-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="9e1d1-119">Il parametro *pLogFont* non è valido.</span><span class="sxs-lookup"><span data-stu-id="9e1d1-119">The *pLogFont* parameter is invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="9e1d1-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9e1d1-120">Requirements</span></span>



| <span data-ttu-id="9e1d1-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="9e1d1-121">Requirement</span></span> | <span data-ttu-id="9e1d1-122">Valore</span><span class="sxs-lookup"><span data-stu-id="9e1d1-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9e1d1-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9e1d1-123">Minimum supported client</span></span><br/> | <span data-ttu-id="9e1d1-124">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="9e1d1-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="9e1d1-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9e1d1-125">Minimum supported server</span></span><br/> | <span data-ttu-id="9e1d1-126">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="9e1d1-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="9e1d1-127">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="9e1d1-127">Redistributable</span></span><br/>          | <span data-ttu-id="9e1d1-128">TSF 1,0 su Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="9e1d1-128">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="9e1d1-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9e1d1-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="9e1d1-130"><dt>Softkbdc. h</dt></span><span class="sxs-lookup"><span data-stu-id="9e1d1-130"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="9e1d1-131">IDL</span><span class="sxs-lookup"><span data-stu-id="9e1d1-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="9e1d1-132"><dt>Softkbd. idl</dt></span><span class="sxs-lookup"><span data-stu-id="9e1d1-132"><dt>Softkbd.idl</dt></span></span> </dl> |
| <span data-ttu-id="9e1d1-133">DLL</span><span class="sxs-lookup"><span data-stu-id="9e1d1-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9e1d1-134"><dt>Softkbd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9e1d1-134"><dt>Softkbd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9e1d1-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9e1d1-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e1d1-136">**ISoftKbd**</span><span class="sxs-lookup"><span data-stu-id="9e1d1-136">**ISoftKbd**</span></span>](isoftkbd.md)
</dt> <dt>

[<span data-ttu-id="9e1d1-137">**ISoftKbd::SetSoftKeyboardTextFont**</span><span class="sxs-lookup"><span data-stu-id="9e1d1-137">**ISoftKbd::SetSoftKeyboardTextFont**</span></span>](isoftkbd-setsoftkeyboardtextfont.md)
</dt> </dl>

 

