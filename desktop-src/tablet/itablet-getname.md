---
description: Restituisce una stringa contenente il nome del dispositivo tablet.
ms.assetid: 025620b5-ab68-4e36-ae26-2226a2fdeb61
title: 'Metodo ITablet:: GetName'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet.GetName
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: c2d6bd20a011b1bf5cfbe7582445de45728bbd7a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104231914"
---
# <a name="itabletgetname-method"></a><span data-ttu-id="4a76f-103">Metodo ITablet:: GetName</span><span class="sxs-lookup"><span data-stu-id="4a76f-103">ITablet::GetName method</span></span>

<span data-ttu-id="4a76f-104">Restituisce una stringa contenente il nome del dispositivo tablet.</span><span class="sxs-lookup"><span data-stu-id="4a76f-104">Returns a string containing the name of the tablet device.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a76f-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4a76f-105">Syntax</span></span>


```C++
HRESULT GetName(
  [out] LPWSTR *ppwszName
);
```



## <a name="parameters"></a><span data-ttu-id="4a76f-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="4a76f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4a76f-107">*ppwszName* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="4a76f-107">*ppwszName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4a76f-108">Puntatore a una stringa che contiene il nome del dispositivo tablet.</span><span class="sxs-lookup"><span data-stu-id="4a76f-108">Pointer to a string containing the name of the tablet device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4a76f-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4a76f-109">Return value</span></span>

<span data-ttu-id="4a76f-110">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="4a76f-110">This method can return one of these values.</span></span>



| <span data-ttu-id="4a76f-111">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="4a76f-111">Return code</span></span>                                                                            | <span data-ttu-id="4a76f-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4a76f-112">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="4a76f-113"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="4a76f-113"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="4a76f-114">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="4a76f-114">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="4a76f-115"><dt>**E \_ non riescono**</dt></span><span class="sxs-lookup"><span data-stu-id="4a76f-115"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="4a76f-116">Si è verificato un errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="4a76f-116">An unspecified error occurred.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="4a76f-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="4a76f-117">Remarks</span></span>

<span data-ttu-id="4a76f-118">È responsabilità del chiamante liberare la memoria restituita da questo metodo usando [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).</span><span class="sxs-lookup"><span data-stu-id="4a76f-118">It is the caller's responsibility to free the memory returned from this method by using [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).</span></span>

## <a name="requirements"></a><span data-ttu-id="4a76f-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4a76f-119">Requirements</span></span>



| <span data-ttu-id="4a76f-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="4a76f-120">Requirement</span></span> | <span data-ttu-id="4a76f-121">Valore</span><span class="sxs-lookup"><span data-stu-id="4a76f-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4a76f-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4a76f-122">Minimum supported client</span></span><br/> | <span data-ttu-id="4a76f-123">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="4a76f-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="4a76f-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4a76f-124">Minimum supported server</span></span><br/> | <span data-ttu-id="4a76f-125">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="4a76f-125">None supported</span></span><br/>                                                              |
| <span data-ttu-id="4a76f-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="4a76f-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="4a76f-127"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="4a76f-127"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4a76f-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4a76f-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a76f-129">**Interfaccia ITablet**</span><span class="sxs-lookup"><span data-stu-id="4a76f-129">**ITablet Interface**</span></span>](itablet.md)
</dt> </dl>

 

