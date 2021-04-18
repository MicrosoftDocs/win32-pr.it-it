---
title: Metodo ISoftKbd CreateSoftKeyboardLayoutFromXMLFile (Softkbdc. h)
description: Il metodo ISoftKbd CreateSoftKeyboardLayoutFromXMLFile crea un layout di tastiera soft dal file XML specificato.
ms.assetid: e665adab-1d75-4e41-87bf-c8ce0f7a0399
keywords:
- Framework servizi di testo Metodo CreateSoftKeyboardLayoutFromXMLFile
- Framework dei servizi di testo del metodo CreateSoftKeyboardLayoutFromXMLFile, interfaccia ISoftKbd
- ISoftKbd Interface Text Services Framework, metodo CreateSoftKeyboardLayoutFromXMLFile
topic_type:
- apiref
api_name:
- ISoftKbd.CreateSoftKeyboardLayoutFromXMLFile
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9252db845c5e1cc732adc295e1989fee83d4ac6e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302102"
---
# <a name="isoftkbdcreatesoftkeyboardlayoutfromxmlfile-method"></a><span data-ttu-id="843a2-106">Metodo ISoftKbd:: CreateSoftKeyboardLayoutFromXMLFile</span><span class="sxs-lookup"><span data-stu-id="843a2-106">ISoftKbd::CreateSoftKeyboardLayoutFromXMLFile method</span></span>

<span data-ttu-id="843a2-107">Il metodo **ISoftKbd:: CreateSoftKeyboardLayoutFromXMLFile** crea un layout di tastiera soft dal file XML specificato.</span><span class="sxs-lookup"><span data-stu-id="843a2-107">The **ISoftKbd::CreateSoftKeyboardLayoutFromXMLFile** method creates a soft keyboard layout from the specified XML file.</span></span>

## <a name="syntax"></a><span data-ttu-id="843a2-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="843a2-108">Syntax</span></span>


```C++
HRESULT CreateSoftKeyboardLayoutFromXMLFile(
  [in]  WCHAR *lpszKeyboardDesFile,
  [in]  INT   szFileStrLen,
  [out] DWORD *pdwLayoutCookie
);
```



## <a name="parameters"></a><span data-ttu-id="843a2-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="843a2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="843a2-110">*lpszKeyboardDesFile* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="843a2-110">*lpszKeyboardDesFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="843a2-111">Puntatore a una stringa con terminazione zero che indica il nome del file XML.</span><span class="sxs-lookup"><span data-stu-id="843a2-111">Pointer to a zero-terminated string indicating the name of the XML file.</span></span>

</dd> <dt>

<span data-ttu-id="843a2-112">*szFileStrLen* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="843a2-112">*szFileStrLen* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="843a2-113">Stringa con terminazione zero che indica la lunghezza del file XML.</span><span class="sxs-lookup"><span data-stu-id="843a2-113">Zero-terminated string indicating the length of the XML file.</span></span>

</dd> <dt>

<span data-ttu-id="843a2-114">*pdwLayoutCookie* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="843a2-114">*pdwLayoutCookie* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="843a2-115">Puntatore al buffer in cui questo metodo recupera un cookie di layout di tastiera soft.</span><span class="sxs-lookup"><span data-stu-id="843a2-115">Pointer to the buffer in which this method retrieves a soft keyboard layout cookie.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="843a2-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="843a2-116">Return value</span></span>

<span data-ttu-id="843a2-117">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="843a2-117">This method can return one of these values.</span></span>



| <span data-ttu-id="843a2-118">Valore</span><span class="sxs-lookup"><span data-stu-id="843a2-118">Value</span></span>                                                                                        | <span data-ttu-id="843a2-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="843a2-119">Description</span></span>                                    |
|----------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="843a2-120"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="843a2-120"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="843a2-121">Il metodo è stato eseguito correttamente.</span><span class="sxs-lookup"><span data-stu-id="843a2-121">The method was successful.</span></span><br/>          |
| <dl> <span data-ttu-id="843a2-122"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="843a2-122"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="843a2-123">Uno o più parametri non sono validi.</span><span class="sxs-lookup"><span data-stu-id="843a2-123">One or more parameters are invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="843a2-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="843a2-124">Requirements</span></span>



| <span data-ttu-id="843a2-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="843a2-125">Requirement</span></span> | <span data-ttu-id="843a2-126">Valore</span><span class="sxs-lookup"><span data-stu-id="843a2-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="843a2-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="843a2-127">Minimum supported client</span></span><br/> | <span data-ttu-id="843a2-128">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="843a2-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="843a2-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="843a2-129">Minimum supported server</span></span><br/> | <span data-ttu-id="843a2-130">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="843a2-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="843a2-131">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="843a2-131">Redistributable</span></span><br/>          | <span data-ttu-id="843a2-132">TSF 1,0 su Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="843a2-132">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="843a2-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="843a2-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="843a2-134"><dt>Softkbdc. h</dt></span><span class="sxs-lookup"><span data-stu-id="843a2-134"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="843a2-135">IDL</span><span class="sxs-lookup"><span data-stu-id="843a2-135">IDL</span></span><br/>                      | <dl> <span data-ttu-id="843a2-136"><dt>Softkbd. idl</dt></span><span class="sxs-lookup"><span data-stu-id="843a2-136"><dt>Softkbd.idl</dt></span></span> </dl> |
| <span data-ttu-id="843a2-137">DLL</span><span class="sxs-lookup"><span data-stu-id="843a2-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="843a2-138"><dt>Softkbd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="843a2-138"><dt>Softkbd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="843a2-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="843a2-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="843a2-140">**ISoftKbd**</span><span class="sxs-lookup"><span data-stu-id="843a2-140">**ISoftKbd**</span></span>](isoftkbd.md)
</dt> <dt>

[<span data-ttu-id="843a2-141">**ISoftKbd::CreateSoftKeyboardLayoutFromResource**</span><span class="sxs-lookup"><span data-stu-id="843a2-141">**ISoftKbd::CreateSoftKeyboardLayoutFromResource**</span></span>](isoftkbd-createsoftkeyboardlayoutfromresource.md)
</dt> </dl>

 

 





