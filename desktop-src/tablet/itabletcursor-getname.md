---
description: Recupera il nome dello stilo del tablet.
ms.assetid: 94955c04-f699-428b-b4bf-53919b61b1ab
title: 'Metodo ITabletCursor:: GetName'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletCursor.GetName
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: b9d984d5eb711c2344ba0f9fb2dbf410a7d49bde
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968418"
---
# <a name="itabletcursorgetname-method"></a><span data-ttu-id="10b72-103">Metodo ITabletCursor:: GetName</span><span class="sxs-lookup"><span data-stu-id="10b72-103">ITabletCursor::GetName method</span></span>

<span data-ttu-id="10b72-104">Recupera il nome dello stilo del tablet.</span><span class="sxs-lookup"><span data-stu-id="10b72-104">Retrieves the name of the tablet stylus.</span></span>

## <a name="syntax"></a><span data-ttu-id="10b72-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="10b72-105">Syntax</span></span>


```C++
HRESULT GetName(
  [out] LPWSTR *ppwszName
);
```



## <a name="parameters"></a><span data-ttu-id="10b72-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="10b72-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="10b72-107">*ppwszName* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="10b72-107">*ppwszName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="10b72-108">Nome dello stilo del tablet.</span><span class="sxs-lookup"><span data-stu-id="10b72-108">The name of the tablet stylus.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="10b72-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="10b72-109">Return value</span></span>

<span data-ttu-id="10b72-110">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="10b72-110">This method can return one of these values.</span></span>



| <span data-ttu-id="10b72-111">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="10b72-111">Return code</span></span>                                                                            | <span data-ttu-id="10b72-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="10b72-112">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="10b72-113"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="10b72-113"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="10b72-114">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="10b72-114">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="10b72-115"><dt>**E \_ non riescono**</dt></span><span class="sxs-lookup"><span data-stu-id="10b72-115"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="10b72-116">Si è verificato un errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="10b72-116">An unspecified error occurred.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="10b72-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="10b72-117">Remarks</span></span>

<span data-ttu-id="10b72-118">È responsabilità del chiamante liberare la memoria restituita da questo metodo usando [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).</span><span class="sxs-lookup"><span data-stu-id="10b72-118">It is the caller's responsibility to free the memory returned from this method by using [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).</span></span>

## <a name="requirements"></a><span data-ttu-id="10b72-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="10b72-119">Requirements</span></span>



| <span data-ttu-id="10b72-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="10b72-120">Requirement</span></span> | <span data-ttu-id="10b72-121">Valore</span><span class="sxs-lookup"><span data-stu-id="10b72-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="10b72-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="10b72-122">Minimum supported client</span></span><br/> | <span data-ttu-id="10b72-123">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="10b72-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="10b72-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="10b72-124">Minimum supported server</span></span><br/> | <span data-ttu-id="10b72-125">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="10b72-125">None supported</span></span><br/>                                                              |
| <span data-ttu-id="10b72-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="10b72-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="10b72-127"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="10b72-127"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="10b72-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="10b72-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10b72-129">**ITabletCursor**</span><span class="sxs-lookup"><span data-stu-id="10b72-129">**ITabletCursor**</span></span>](itabletcursor.md)
</dt> <dt>

[<span data-ttu-id="10b72-130">**Interfaccia ITabletCursorButton**</span><span class="sxs-lookup"><span data-stu-id="10b72-130">**ITabletCursorButton Interface**</span></span>](itabletcursorbutton.md)
</dt> </dl>

 

