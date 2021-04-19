---
description: Restituisce una stringa contenente l'ID Plug and Play per la tavoletta.
ms.assetid: a0b6619b-f80c-470b-aa3f-f0b30a9dbda8
title: 'Metodo ITablet:: GetPlugAndPlayId'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet.GetPlugAndPlayId
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 3fb6ce7d59cb29aac4b06b7245bc6246b0688a7b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313921"
---
# <a name="itabletgetplugandplayid-method"></a><span data-ttu-id="e34bc-103">Metodo ITablet:: GetPlugAndPlayId</span><span class="sxs-lookup"><span data-stu-id="e34bc-103">ITablet::GetPlugAndPlayId method</span></span>

<span data-ttu-id="e34bc-104">Restituisce una stringa contenente l'ID Plug and Play per la tavoletta.</span><span class="sxs-lookup"><span data-stu-id="e34bc-104">Returns a string containing the Plug and Play ID for the tablet device.</span></span>

## <a name="syntax"></a><span data-ttu-id="e34bc-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e34bc-105">Syntax</span></span>


```C++
HRESULT GetPlugAndPlayId(
  [out] LPWSTR *ppwszPPId
);
```



## <a name="parameters"></a><span data-ttu-id="e34bc-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e34bc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e34bc-107">*ppwszPPId* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="e34bc-107">*ppwszPPId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e34bc-108">Puntatore a una stringa contenente l'ID Plug and Play per la tavoletta.</span><span class="sxs-lookup"><span data-stu-id="e34bc-108">Pointer to a string containing the Plug and Play ID for the tablet device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e34bc-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e34bc-109">Return value</span></span>

<span data-ttu-id="e34bc-110">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="e34bc-110">This method can return one of these values.</span></span>



| <span data-ttu-id="e34bc-111">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="e34bc-111">Return code</span></span>                                                                            | <span data-ttu-id="e34bc-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e34bc-112">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="e34bc-113"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="e34bc-113"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="e34bc-114">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="e34bc-114">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="e34bc-115"><dt>**E \_ non riescono**</dt></span><span class="sxs-lookup"><span data-stu-id="e34bc-115"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="e34bc-116">Si è verificato un errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="e34bc-116">An unspecified error occurred.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="e34bc-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="e34bc-117">Remarks</span></span>

<span data-ttu-id="e34bc-118">È responsabilità del chiamante liberare la memoria restituita da questo metodo usando [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).</span><span class="sxs-lookup"><span data-stu-id="e34bc-118">It is the caller's responsibility to free the memory returned from this method by using [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).</span></span>

## <a name="requirements"></a><span data-ttu-id="e34bc-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e34bc-119">Requirements</span></span>



| <span data-ttu-id="e34bc-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="e34bc-120">Requirement</span></span> | <span data-ttu-id="e34bc-121">Valore</span><span class="sxs-lookup"><span data-stu-id="e34bc-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e34bc-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e34bc-122">Minimum supported client</span></span><br/> | <span data-ttu-id="e34bc-123">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="e34bc-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="e34bc-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e34bc-124">Minimum supported server</span></span><br/> | <span data-ttu-id="e34bc-125">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="e34bc-125">None supported</span></span><br/>                                                              |
| <span data-ttu-id="e34bc-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="e34bc-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="e34bc-127"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e34bc-127"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e34bc-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e34bc-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e34bc-129">**Interfaccia ITablet**</span><span class="sxs-lookup"><span data-stu-id="e34bc-129">**ITablet Interface**</span></span>](itablet.md)
</dt> </dl>

 

