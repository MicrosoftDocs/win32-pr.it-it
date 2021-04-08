---
title: Metodo GetRemoteName IBackgroundCopyFile (Deliveryoptimization. h)
description: Recupera il nome remoto del file.
ms.assetid: 518857E0-C16A-400B-8F3D-5264B3CB43FF
keywords:
- GetRemoteName (metodo)
- Metodo GetRemoteName, interfaccia IBackgroundCopyFile
- Interfaccia IBackgroundCopyFile, Metodo GetRemoteName
topic_type:
- apiref
api_name:
- IBackgroundCopyFile.GetRemoteName
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9984ed9971fdfb91279dabc5810490b62804b7e3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048277"
---
# <a name="ibackgroundcopyfilegetremotename-method"></a><span data-ttu-id="1d4b8-106">Metodo IBackgroundCopyFile:: GetRemoteName</span><span class="sxs-lookup"><span data-stu-id="1d4b8-106">IBackgroundCopyFile::GetRemoteName method</span></span>

<span data-ttu-id="1d4b8-107">Recupera il nome remoto del file.</span><span class="sxs-lookup"><span data-stu-id="1d4b8-107">Retrieves the remote name of the file.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d4b8-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1d4b8-108">Syntax</span></span>


```C++
HRESULT GetRemoteName(
  [out] LPWSTR *ppName
);
```



## <a name="parameters"></a><span data-ttu-id="1d4b8-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="1d4b8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1d4b8-110">*ppName* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="1d4b8-110">*ppName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1d4b8-111">Stringa con terminazione null che contiene il nome remoto del file da trasferire.</span><span class="sxs-lookup"><span data-stu-id="1d4b8-111">Null-terminated string that contains the remote name of the file to transfer.</span></span> <span data-ttu-id="1d4b8-112">Il nome è completo.</span><span class="sxs-lookup"><span data-stu-id="1d4b8-112">The name is fully qualified.</span></span> <span data-ttu-id="1d4b8-113">Chiamare la funzione [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) per liberare *ppName* al termine.</span><span class="sxs-lookup"><span data-stu-id="1d4b8-113">Call the [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) function to free *ppName* when done.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1d4b8-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1d4b8-114">Return value</span></span>

<span data-ttu-id="1d4b8-115">Questo metodo restituisce **S_OK** in esito positivo o uno dei valori **HRESULT** com standard in errore.</span><span class="sxs-lookup"><span data-stu-id="1d4b8-115">This method returns **S_OK** on success or one of the standard COM **HRESULT** values on error.</span></span>

## <a name="remarks"></a><span data-ttu-id="1d4b8-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="1d4b8-116">Remarks</span></span>

<span data-ttu-id="1d4b8-117">Per modificare il nome del file remoto, chiamare il metodo [**IBackgroundCopyFile2:: Seremotename**](ibackgroundcopyfile2-setremotename-method.md) .</span><span class="sxs-lookup"><span data-stu-id="1d4b8-117">To change the remote file name, call the [**IBackgroundCopyFile2::SetRemoteName**](ibackgroundcopyfile2-setremotename-method.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="1d4b8-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1d4b8-118">Requirements</span></span>



| <span data-ttu-id="1d4b8-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="1d4b8-119">Requirement</span></span> | <span data-ttu-id="1d4b8-120">Valore</span><span class="sxs-lookup"><span data-stu-id="1d4b8-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1d4b8-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1d4b8-121">Minimum supported client</span></span><br/> | <span data-ttu-id="1d4b8-122">Solo app desktop Windows 10 versione 1709 \[\]</span><span class="sxs-lookup"><span data-stu-id="1d4b8-122">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="1d4b8-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1d4b8-123">Minimum supported server</span></span><br/> | <span data-ttu-id="1d4b8-124">Windows Server, versione 1709 \[ solo per le app desktop\]</span><span class="sxs-lookup"><span data-stu-id="1d4b8-124">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="1d4b8-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1d4b8-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="1d4b8-126"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="1d4b8-126"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="1d4b8-127">IDL</span><span class="sxs-lookup"><span data-stu-id="1d4b8-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="1d4b8-128"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="1d4b8-128"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="1d4b8-129">Libreria</span><span class="sxs-lookup"><span data-stu-id="1d4b8-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="1d4b8-130"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1d4b8-130"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="1d4b8-131">DLL</span><span class="sxs-lookup"><span data-stu-id="1d4b8-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1d4b8-132"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1d4b8-132"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="1d4b8-133">IID</span><span class="sxs-lookup"><span data-stu-id="1d4b8-133">IID</span></span><br/>                      | <span data-ttu-id="1d4b8-134">IID_IBackgroundCopyFile viene definito come 01B7BD23-FB88-4A77-8490-5891D3E4653A</span><span class="sxs-lookup"><span data-stu-id="1d4b8-134">IID_IBackgroundCopyFile is defined as 01B7BD23-FB88-4A77-8490-5891D3E4653A</span></span><br/>              |



## <a name="see-also"></a><span data-ttu-id="1d4b8-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1d4b8-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d4b8-136">**IBackgroundCopyFile**</span><span class="sxs-lookup"><span data-stu-id="1d4b8-136">**IBackgroundCopyFile**</span></span>](ibackgroundcopyfile.md)
</dt> <dt>

[<span data-ttu-id="1d4b8-137">**IBackgroundCopyFile:: GetLocalName**</span><span class="sxs-lookup"><span data-stu-id="1d4b8-137">**IBackgroundCopyFile::GetLocalName**</span></span>](ibackgroundcopyfile-getlocalname-method.md)
</dt> </dl>

 

