---
title: Metodo ISoftKbd CreateSoftKeyboardLayoutFromResource (Softkbdc. h)
description: Il metodo ISoftKbd CreateSoftKeybboardLayoutFromResource crea un layout di tastiera soft dalla risorsa specificata.
ms.assetid: c1b2f8bd-8065-426d-9c23-67fa46a33dc8
keywords:
- Framework servizi di testo Metodo CreateSoftKeyboardLayoutFromResource
- Framework dei servizi di testo del metodo CreateSoftKeyboardLayoutFromResource, interfaccia ISoftKbd
- ISoftKbd Interface Text Services Framework, metodo CreateSoftKeyboardLayoutFromResource
topic_type:
- apiref
api_name:
- ISoftKbd.CreateSoftKeyboardLayoutFromResource
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f454b5d8f3366517d91170d6a92d6a9dbed5764
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302103"
---
# <a name="isoftkbdcreatesoftkeyboardlayoutfromresource-method"></a><span data-ttu-id="66c10-106">Metodo ISoftKbd:: CreateSoftKeyboardLayoutFromResource</span><span class="sxs-lookup"><span data-stu-id="66c10-106">ISoftKbd::CreateSoftKeyboardLayoutFromResource method</span></span>

<span data-ttu-id="66c10-107">Il metodo **ISoftKbd:: CreateSoftKeybboardLayoutFromResource** crea un layout di tastiera soft dalla risorsa specificata.</span><span class="sxs-lookup"><span data-stu-id="66c10-107">The **ISoftKbd::CreateSoftKeybboardLayoutFromResource** method creates a soft keyboard layout from the specified resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="66c10-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="66c10-108">Syntax</span></span>


```C++
HRESULT CreateSoftKeyboardLayoutFromResource(
  [in]  WCHAR *lpszResFile,
  [in]  WCHAR *lpszResType,
  [in]  WCHAR *lpszXMLResString,
  [out] DWORD *lpdwLayoutCookie
);
```



## <a name="parameters"></a><span data-ttu-id="66c10-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="66c10-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="66c10-110">*lpszResFile* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="66c10-110">*lpszResFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="66c10-111">Puntatore a una stringa con terminazione zero che indica il nome del file di risorse.</span><span class="sxs-lookup"><span data-stu-id="66c10-111">Pointer to a zero-terminated string indicating the name of the resource file.</span></span>

</dd> <dt>

<span data-ttu-id="66c10-112">*lpszResType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="66c10-112">*lpszResType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="66c10-113">Puntatore a una stringa con terminazione zero che indica il tipo di risorsa.</span><span class="sxs-lookup"><span data-stu-id="66c10-113">Pointer to a zero-terminated string indicating the type of resource.</span></span>

</dd> <dt>

<span data-ttu-id="66c10-114">*lpszXMLResString* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="66c10-114">*lpszXMLResString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="66c10-115">Puntatore a una stringa con terminazione zero che identifica la risorsa.</span><span class="sxs-lookup"><span data-stu-id="66c10-115">Pointer to a zero-terminated string identifying the resource.</span></span>

</dd> <dt>

<span data-ttu-id="66c10-116">*lpdwLayoutCookie* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="66c10-116">*lpdwLayoutCookie* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="66c10-117">Puntatore al buffer in cui questo metodo recupera un cookie di layout di tastiera soft.</span><span class="sxs-lookup"><span data-stu-id="66c10-117">Pointer to the buffer in which this method retrieves a soft keyboard layout cookie.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="66c10-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="66c10-118">Return value</span></span>

<span data-ttu-id="66c10-119">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="66c10-119">This method can return one of these values.</span></span>



| <span data-ttu-id="66c10-120">Valore</span><span class="sxs-lookup"><span data-stu-id="66c10-120">Value</span></span>                                                                                        | <span data-ttu-id="66c10-121">Descrizione</span><span class="sxs-lookup"><span data-stu-id="66c10-121">Description</span></span>                                    |
|----------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="66c10-122"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="66c10-122"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="66c10-123">Il metodo è stato eseguito correttamente.</span><span class="sxs-lookup"><span data-stu-id="66c10-123">The method was successful.</span></span><br/>          |
| <dl> <span data-ttu-id="66c10-124"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="66c10-124"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="66c10-125">Uno o più parametri non sono validi.</span><span class="sxs-lookup"><span data-stu-id="66c10-125">One or more parameters are invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="66c10-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="66c10-126">Requirements</span></span>



| <span data-ttu-id="66c10-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="66c10-127">Requirement</span></span> | <span data-ttu-id="66c10-128">Valore</span><span class="sxs-lookup"><span data-stu-id="66c10-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="66c10-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="66c10-129">Minimum supported client</span></span><br/> | <span data-ttu-id="66c10-130">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="66c10-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="66c10-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="66c10-131">Minimum supported server</span></span><br/> | <span data-ttu-id="66c10-132">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="66c10-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="66c10-133">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="66c10-133">Redistributable</span></span><br/>          | <span data-ttu-id="66c10-134">TSF 1,0 su Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="66c10-134">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="66c10-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="66c10-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="66c10-136"><dt>Softkbdc. h</dt></span><span class="sxs-lookup"><span data-stu-id="66c10-136"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="66c10-137">IDL</span><span class="sxs-lookup"><span data-stu-id="66c10-137">IDL</span></span><br/>                      | <dl> <span data-ttu-id="66c10-138"><dt>Softkbd. idl</dt></span><span class="sxs-lookup"><span data-stu-id="66c10-138"><dt>Softkbd.idl</dt></span></span> </dl> |
| <span data-ttu-id="66c10-139">DLL</span><span class="sxs-lookup"><span data-stu-id="66c10-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="66c10-140"><dt>Softkbd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="66c10-140"><dt>Softkbd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="66c10-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="66c10-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66c10-142">**ISoftKbd**</span><span class="sxs-lookup"><span data-stu-id="66c10-142">**ISoftKbd**</span></span>](isoftkbd.md)
</dt> <dt>

[<span data-ttu-id="66c10-143">**ISoftKbd::CreateSoftKeyboardLayoutFromXMLFile**</span><span class="sxs-lookup"><span data-stu-id="66c10-143">**ISoftKbd::CreateSoftKeyboardLayoutFromXMLFile**</span></span>](isoftkbd-createsoftkeyboardlayoutfromxmlfile.md)
</dt> <dt>

[<span data-ttu-id="66c10-144">**ISoftKbd::ShowSoftKeyboard**</span><span class="sxs-lookup"><span data-stu-id="66c10-144">**ISoftKbd::ShowSoftKeyboard**</span></span>](isoftkbd-showsoftkeyboard.md)
</dt> </dl>

 

 





