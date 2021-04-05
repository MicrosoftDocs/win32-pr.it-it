---
title: Metodo GetLocalName IBackgroundCopyFile (Deliveryoptimization. h)
description: Recupera il nome locale del file.
ms.assetid: 9AA57EB7-5C29-4E5E-972B-DD34B130E6E4
keywords:
- GetLocalName (metodo)
- Metodo GetLocalName, interfaccia IBackgroundCopyFile
- Interfaccia IBackgroundCopyFile, metodo GetLocalName
topic_type:
- apiref
api_name:
- IBackgroundCopyFile.GetLocalName
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e1c3a957e64701242d9c698a014ec2ab4028cd85
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048279"
---
# <a name="ibackgroundcopyfilegetlocalname-method"></a><span data-ttu-id="55ecf-106">Metodo IBackgroundCopyFile:: GetLocalName</span><span class="sxs-lookup"><span data-stu-id="55ecf-106">IBackgroundCopyFile::GetLocalName method</span></span>

<span data-ttu-id="55ecf-107">Recupera il nome locale del file.</span><span class="sxs-lookup"><span data-stu-id="55ecf-107">Retrieves the local name of the file.</span></span>

## <a name="syntax"></a><span data-ttu-id="55ecf-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="55ecf-108">Syntax</span></span>


```C++
HRESULT GetLocalName(
  [out] LPWSTR *ppName
);
```



## <a name="parameters"></a><span data-ttu-id="55ecf-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="55ecf-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="55ecf-110">*ppName* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="55ecf-110">*ppName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="55ecf-111">Stringa con terminazione null che contiene il nome del file nel client.</span><span class="sxs-lookup"><span data-stu-id="55ecf-111">Null-terminated string that contains the name of the file on the client.</span></span> <span data-ttu-id="55ecf-112">Il nome è completo.</span><span class="sxs-lookup"><span data-stu-id="55ecf-112">The name is fully qualified.</span></span> <span data-ttu-id="55ecf-113">Chiamare la funzione [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) per liberare *ppName* al termine.</span><span class="sxs-lookup"><span data-stu-id="55ecf-113">Call the [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) function to free *ppName* when done.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="55ecf-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="55ecf-114">Return value</span></span>

<span data-ttu-id="55ecf-115">Questo metodo restituisce **S_OK** in esito positivo o uno dei valori **HRESULT** com standard in errore.</span><span class="sxs-lookup"><span data-stu-id="55ecf-115">This method returns **S_OK** on success or one of the standard COM **HRESULT** values on error.</span></span>

## <a name="requirements"></a><span data-ttu-id="55ecf-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="55ecf-116">Requirements</span></span>



| <span data-ttu-id="55ecf-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="55ecf-117">Requirement</span></span> | <span data-ttu-id="55ecf-118">Valore</span><span class="sxs-lookup"><span data-stu-id="55ecf-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="55ecf-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="55ecf-119">Minimum supported client</span></span><br/> | <span data-ttu-id="55ecf-120">Solo app desktop Windows 10 versione 1709 \[\]</span><span class="sxs-lookup"><span data-stu-id="55ecf-120">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="55ecf-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="55ecf-121">Minimum supported server</span></span><br/> | <span data-ttu-id="55ecf-122">Windows Server, versione 1709 \[ solo per le app desktop\]</span><span class="sxs-lookup"><span data-stu-id="55ecf-122">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="55ecf-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="55ecf-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="55ecf-124"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="55ecf-124"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="55ecf-125">IDL</span><span class="sxs-lookup"><span data-stu-id="55ecf-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="55ecf-126"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="55ecf-126"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="55ecf-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="55ecf-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="55ecf-128"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="55ecf-128"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="55ecf-129">DLL</span><span class="sxs-lookup"><span data-stu-id="55ecf-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="55ecf-130"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="55ecf-130"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="55ecf-131">IID</span><span class="sxs-lookup"><span data-stu-id="55ecf-131">IID</span></span><br/>                      | <span data-ttu-id="55ecf-132">IID_IBackgroundCopyFile viene definito come 01B7BD23-FB88-4A77-8490-5891D3E4653A</span><span class="sxs-lookup"><span data-stu-id="55ecf-132">IID_IBackgroundCopyFile is defined as 01B7BD23-FB88-4A77-8490-5891D3E4653A</span></span><br/>              |



## <a name="see-also"></a><span data-ttu-id="55ecf-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="55ecf-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55ecf-134">**IBackgroundCopyFile**</span><span class="sxs-lookup"><span data-stu-id="55ecf-134">**IBackgroundCopyFile**</span></span>](ibackgroundcopyfile.md)
</dt> <dt>

[<span data-ttu-id="55ecf-135">**IBackgroundCopyFile:: GetRemoteName**</span><span class="sxs-lookup"><span data-stu-id="55ecf-135">**IBackgroundCopyFile::GetRemoteName**</span></span>](ibackgroundcopyfile-getremotename-method.md)
</dt> </dl>

 

