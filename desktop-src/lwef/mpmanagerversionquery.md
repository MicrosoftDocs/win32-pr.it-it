---
title: Funzione MpManagerVersionQuery (MpClient. h)
description: Restituisce le informazioni sulla versione dei vari componenti di malware Protection Manager.
ms.assetid: 47DE12BF-D7A4-468B-B0E7-79B5C27E56F5
keywords:
- Funzionalità dell'ambiente Windows legacy della funzione MpManagerVersionQuery
topic_type:
- apiref
api_name:
- MpManagerVersionQuery
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a841a83d8ceb828de0a5a9cd80f5f5bdc7f5c914
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302068"
---
# <a name="mpmanagerversionquery-function"></a><span data-ttu-id="1ef73-104">MpManagerVersionQuery (funzione)</span><span class="sxs-lookup"><span data-stu-id="1ef73-104">MpManagerVersionQuery function</span></span>

<span data-ttu-id="1ef73-105">Restituisce le informazioni sulla versione dei vari componenti di malware Protection Manager.</span><span class="sxs-lookup"><span data-stu-id="1ef73-105">Returns version information about various components of the malware protection manager.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ef73-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1ef73-106">Syntax</span></span>


```C++
HRESULT WINAPI MpManagerVersionQuery(
  _In_  MPHANDLE        hMpHandle,
  _Out_ PMPVERSION_INFO pVersionInfo
);
```



## <a name="parameters"></a><span data-ttu-id="1ef73-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="1ef73-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1ef73-108">*hMpHandle* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1ef73-108">*hMpHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ef73-109">Tipo: **MPHANDLE**</span><span class="sxs-lookup"><span data-stu-id="1ef73-109">Type: **MPHANDLE**</span></span>

<span data-ttu-id="1ef73-110">Handle per l'interfaccia di malware Protection Manager.</span><span class="sxs-lookup"><span data-stu-id="1ef73-110">Handle to the malware protection manager interface.</span></span> <span data-ttu-id="1ef73-111">Questo handle viene restituito dalla funzione [**MpManagerOpen**](mpmanageropen.md) .</span><span class="sxs-lookup"><span data-stu-id="1ef73-111">This handle is returned by the [**MpManagerOpen**](mpmanageropen.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="1ef73-112">*pVersionInfo* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="1ef73-112">*pVersionInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1ef73-113">Tipo: **PMPVERSION \_ info**</span><span class="sxs-lookup"><span data-stu-id="1ef73-113">Type: **PMPVERSION\_INFO**</span></span>

<span data-ttu-id="1ef73-114">Puntatore a una struttura che contiene informazioni sulla versione dei vari componenti di malware Protection Manager.</span><span class="sxs-lookup"><span data-stu-id="1ef73-114">Pointer to a structure that contains version information about various components of the malware protection manager.</span></span> <span data-ttu-id="1ef73-115">Vedere [**MPVERSION \_ info**](mpversion-info.md).</span><span class="sxs-lookup"><span data-stu-id="1ef73-115">See [**MPVERSION\_INFO**](mpversion-info.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1ef73-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1ef73-116">Return value</span></span>

<span data-ttu-id="1ef73-117">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="1ef73-117">Type: **HRESULT**</span></span>

<span data-ttu-id="1ef73-118">Se la funzione ha esito positivo, il valore restituito è **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="1ef73-118">If the function succeeds the return value is **S\_OK**.</span></span>

<span data-ttu-id="1ef73-119">Se la funzione ha esito negativo, il valore restituito è un codice **HRESULT** non riuscito.</span><span class="sxs-lookup"><span data-stu-id="1ef73-119">If the function fails then the return value is a failed **HRESULT** code.</span></span> <span data-ttu-id="1ef73-120">Il chiamante può utilizzare la funzione [**MpErrorMessageFormat**](mperrormessageformat.md) per ottenere una descrizione generica del messaggio di errore.</span><span class="sxs-lookup"><span data-stu-id="1ef73-120">The caller can use the [**MpErrorMessageFormat**](mperrormessageformat.md) function to get a generic description of the error message.</span></span>

## <a name="requirements"></a><span data-ttu-id="1ef73-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1ef73-121">Requirements</span></span>



| <span data-ttu-id="1ef73-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="1ef73-122">Requirement</span></span> | <span data-ttu-id="1ef73-123">Valore</span><span class="sxs-lookup"><span data-stu-id="1ef73-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1ef73-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1ef73-124">Minimum supported client</span></span><br/> | <span data-ttu-id="1ef73-125">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="1ef73-125">Windows 8 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="1ef73-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1ef73-126">Minimum supported server</span></span><br/> | <span data-ttu-id="1ef73-127">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="1ef73-127">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="1ef73-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1ef73-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="1ef73-129"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="1ef73-129"><dt>MpClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="1ef73-130">DLL</span><span class="sxs-lookup"><span data-stu-id="1ef73-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1ef73-131"><dt>MpClient.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1ef73-131"><dt>MpClient.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1ef73-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1ef73-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ef73-133">**MpErrorMessageFormat**</span><span class="sxs-lookup"><span data-stu-id="1ef73-133">**MpErrorMessageFormat**</span></span>](mperrormessageformat.md)
</dt> <dt>

[<span data-ttu-id="1ef73-134">**MpManagerOpen**</span><span class="sxs-lookup"><span data-stu-id="1ef73-134">**MpManagerOpen**</span></span>](mpmanageropen.md)
</dt> <dt>

[<span data-ttu-id="1ef73-135">**\_informazioni MPVERSION**</span><span class="sxs-lookup"><span data-stu-id="1ef73-135">**MPVERSION\_INFO**</span></span>](mpversion-info.md)
</dt> </dl>

 

 





