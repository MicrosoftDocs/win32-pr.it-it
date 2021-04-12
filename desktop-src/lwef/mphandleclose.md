---
title: Funzione MpHandleClose (MpClient. h)
description: Chiude l'handle restituito da MpManagerOpen, MpScanStart, MpThreatOpen o MpUpdateStart.
ms.assetid: 335776E2-7598-4DC1-92AB-B49B35222EF6
keywords:
- Funzionalità dell'ambiente Windows legacy della funzione MpHandleClose
topic_type:
- apiref
api_name:
- MpHandleClose
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43c937548c8e1d3b98aa2e3d10d7577f8c69c1c5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518754"
---
# <a name="mphandleclose-function"></a><span data-ttu-id="03290-104">MpHandleClose (funzione)</span><span class="sxs-lookup"><span data-stu-id="03290-104">MpHandleClose function</span></span>

<span data-ttu-id="03290-105">Chiude l'handle restituito da [**MpManagerOpen**](mpmanageropen.md), [**MpScanStart**](mpscanstart.md), [**MpThreatOpen**](mpthreatopen.md)o [**MpUpdateStart**](mpupdatestart.md).</span><span class="sxs-lookup"><span data-stu-id="03290-105">Closes the handle returned by [**MpManagerOpen**](mpmanageropen.md), [**MpScanStart**](mpscanstart.md), [**MpThreatOpen**](mpthreatopen.md), or [**MpUpdateStart**](mpupdatestart.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="03290-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="03290-106">Syntax</span></span>


```C++
HRESULT WINAPI MpHandleClose(
  _In_ MPHANDLE hMpHandle
);
```



## <a name="parameters"></a><span data-ttu-id="03290-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="03290-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="03290-108">*hMpHandle* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="03290-108">*hMpHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="03290-109">Tipo: **MPHANDLE**</span><span class="sxs-lookup"><span data-stu-id="03290-109">Type: **MPHANDLE**</span></span>

<span data-ttu-id="03290-110">Handle da chiudere.</span><span class="sxs-lookup"><span data-stu-id="03290-110">Handle to close.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="03290-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="03290-111">Return value</span></span>

<span data-ttu-id="03290-112">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="03290-112">Type: **HRESULT**</span></span>

<span data-ttu-id="03290-113">Se la funzione ha esito positivo, il valore restituito è **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="03290-113">If the function succeeds the return value is **S\_OK**.</span></span>

<span data-ttu-id="03290-114">Se la funzione ha esito negativo, il valore restituito è un codice **HRESULT** non riuscito.</span><span class="sxs-lookup"><span data-stu-id="03290-114">If the function fails then the return value is a failed **HRESULT** code.</span></span> <span data-ttu-id="03290-115">Il chiamante può utilizzare la funzione [**MpErrorMessageFormat**](mperrormessageformat.md) per ottenere una descrizione generica del messaggio di errore.</span><span class="sxs-lookup"><span data-stu-id="03290-115">The caller can use the [**MpErrorMessageFormat**](mperrormessageformat.md) function to get a generic description of the error message.</span></span>

<span data-ttu-id="03290-116">La funzione può restituire l'errore specifico seguente:</span><span class="sxs-lookup"><span data-stu-id="03290-116">The following specific error can be returned by the function:</span></span>

| <span data-ttu-id="03290-117">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="03290-117">Return Code</span></span>             | <span data-ttu-id="03290-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="03290-118">Description</span></span>                      |
|-------------------------|----------------------------------|
| <span data-ttu-id="03290-119">E \_ vincere \_ un \_ handle non valido</span><span class="sxs-lookup"><span data-stu-id="03290-119">E\_WIN\_INVALID\_HANDLE</span></span> | <span data-ttu-id="03290-120">L'handle specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="03290-120">The specified handle is invalid.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="03290-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="03290-121">Requirements</span></span>



| <span data-ttu-id="03290-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="03290-122">Requirement</span></span> | <span data-ttu-id="03290-123">Valore</span><span class="sxs-lookup"><span data-stu-id="03290-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="03290-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="03290-124">Minimum supported client</span></span><br/> | <span data-ttu-id="03290-125">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="03290-125">Windows 8 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="03290-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="03290-126">Minimum supported server</span></span><br/> | <span data-ttu-id="03290-127">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="03290-127">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="03290-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="03290-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="03290-129"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="03290-129"><dt>MpClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="03290-130">DLL</span><span class="sxs-lookup"><span data-stu-id="03290-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="03290-131"><dt>MpClient.dll</dt></span><span class="sxs-lookup"><span data-stu-id="03290-131"><dt>MpClient.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="03290-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="03290-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03290-133">**MpErrorMessageFormat**</span><span class="sxs-lookup"><span data-stu-id="03290-133">**MpErrorMessageFormat**</span></span>](mperrormessageformat.md)
</dt> <dt>

[<span data-ttu-id="03290-134">**MpManagerOpen**</span><span class="sxs-lookup"><span data-stu-id="03290-134">**MpManagerOpen**</span></span>](mpmanageropen.md)
</dt> <dt>

[<span data-ttu-id="03290-135">**MpScanStart**</span><span class="sxs-lookup"><span data-stu-id="03290-135">**MpScanStart**</span></span>](mpscanstart.md)
</dt> <dt>

[<span data-ttu-id="03290-136">**MpThreatOpen**</span><span class="sxs-lookup"><span data-stu-id="03290-136">**MpThreatOpen**</span></span>](mpthreatopen.md)
</dt> </dl>

 

 





