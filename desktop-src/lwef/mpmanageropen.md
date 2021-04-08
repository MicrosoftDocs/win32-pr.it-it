---
title: Funzione MpManagerOpen (MpClient. h)
description: Stabilisce una connessione a malware Protection Manager nel computer locale.
ms.assetid: 40513A74-AFCC-4E22-9B78-D46FEB575A00
keywords:
- Funzionalità dell'ambiente Windows legacy della funzione MpManagerOpen
topic_type:
- apiref
api_name:
- MpManagerOpen
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af432cc7d91530fd3d37176592f7f457b31b6314
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743183"
---
# <a name="mpmanageropen-function"></a><span data-ttu-id="79167-104">MpManagerOpen (funzione)</span><span class="sxs-lookup"><span data-stu-id="79167-104">MpManagerOpen function</span></span>

<span data-ttu-id="79167-105">Stabilisce una connessione a malware Protection Manager nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="79167-105">Establishes a connection to the malware protection manager on the local computer.</span></span>

## <a name="syntax"></a><span data-ttu-id="79167-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="79167-106">Syntax</span></span>


```C++
HRESULT WINAPI MpManagerOpen(
  _In_  DWORD     dwReserved,
  _Out_ PMPHANDLE phMpHandle
);
```



## <a name="parameters"></a><span data-ttu-id="79167-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="79167-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="79167-108">*dwReserved* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="79167-108">*dwReserved* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="79167-109">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="79167-109">Type: **DWORD**</span></span>

<span data-ttu-id="79167-110">Riservato per utilizzi futuri.</span><span class="sxs-lookup"><span data-stu-id="79167-110">Reserved for future use.</span></span> <span data-ttu-id="79167-111">Deve essere 0.</span><span class="sxs-lookup"><span data-stu-id="79167-111">Must be set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="79167-112">*phMpHandle* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="79167-112">*phMpHandle* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="79167-113">Tipo: **PMPHANDLE**</span><span class="sxs-lookup"><span data-stu-id="79167-113">Type: **PMPHANDLE**</span></span>

<span data-ttu-id="79167-114">Handle per l'interfaccia di malware Protection Manager.</span><span class="sxs-lookup"><span data-stu-id="79167-114">Handle to the malware protection manager interface.</span></span> <span data-ttu-id="79167-115">Questo handle deve essere chiuso con la funzione [**MpHandleClose**](mphandleclose.md) .</span><span class="sxs-lookup"><span data-stu-id="79167-115">This handle must be closed with the [**MpHandleClose**](mphandleclose.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="79167-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="79167-116">Return value</span></span>

<span data-ttu-id="79167-117">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="79167-117">Type: **HRESULT**</span></span>

<span data-ttu-id="79167-118">Se la funzione ha esito positivo, il valore restituito è **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="79167-118">If the function succeeds the return value is **S\_OK**.</span></span> <span data-ttu-id="79167-119">Questa chiamata di funzione ha esito positivo anche se un servizio antimalware non è in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="79167-119">This function call is guaranteed to succeed even if an AntiMalware service is not running.</span></span>

<span data-ttu-id="79167-120">Se la funzione ha esito negativo, il valore restituito è un codice **HRESULT** non riuscito.</span><span class="sxs-lookup"><span data-stu-id="79167-120">If the function fails then the return value is a failed **HRESULT** code.</span></span> <span data-ttu-id="79167-121">Il chiamante può utilizzare la funzione [**MpErrorMessageFormat**](mperrormessageformat.md) per ottenere una descrizione generica del messaggio di errore.</span><span class="sxs-lookup"><span data-stu-id="79167-121">The caller can use the [**MpErrorMessageFormat**](mperrormessageformat.md) function to get a generic description of the error message.</span></span>

## <a name="requirements"></a><span data-ttu-id="79167-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="79167-122">Requirements</span></span>



| <span data-ttu-id="79167-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="79167-123">Requirement</span></span> | <span data-ttu-id="79167-124">Valore</span><span class="sxs-lookup"><span data-stu-id="79167-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="79167-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="79167-125">Minimum supported client</span></span><br/> | <span data-ttu-id="79167-126">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="79167-126">Windows 8 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="79167-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="79167-127">Minimum supported server</span></span><br/> | <span data-ttu-id="79167-128">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="79167-128">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="79167-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="79167-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="79167-130"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="79167-130"><dt>MpClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="79167-131">DLL</span><span class="sxs-lookup"><span data-stu-id="79167-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="79167-132"><dt>MpClient.dll</dt></span><span class="sxs-lookup"><span data-stu-id="79167-132"><dt>MpClient.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="79167-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="79167-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79167-134">**MpErrorMessageFormat**</span><span class="sxs-lookup"><span data-stu-id="79167-134">**MpErrorMessageFormat**</span></span>](mperrormessageformat.md)
</dt> <dt>

[<span data-ttu-id="79167-135">**MpHandleClose**</span><span class="sxs-lookup"><span data-stu-id="79167-135">**MpHandleClose**</span></span>](mphandleclose.md)
</dt> </dl>

 

 





