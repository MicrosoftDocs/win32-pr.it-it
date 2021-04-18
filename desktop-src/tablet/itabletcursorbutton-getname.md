---
description: Recupera il nome del pulsante dello stilo.
ms.assetid: 26fad9bc-43c2-4b00-b76b-bf9f1242da77
title: 'Metodo ITabletCursorButton:: GetName'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletCursorButton.GetName
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: b21fd92823fb0f60c0936f662982d176a938b4dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313455"
---
# <a name="itabletcursorbuttongetname-method"></a><span data-ttu-id="3b458-103">Metodo ITabletCursorButton:: GetName</span><span class="sxs-lookup"><span data-stu-id="3b458-103">ITabletCursorButton::GetName method</span></span>

<span data-ttu-id="3b458-104">Recupera il nome del pulsante dello stilo.</span><span class="sxs-lookup"><span data-stu-id="3b458-104">Retrieves the name of the stylus button.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b458-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3b458-105">Syntax</span></span>


```C++
HRESULT GetName(
  [out] LPWSTR *ppwszName
);
```



## <a name="parameters"></a><span data-ttu-id="3b458-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="3b458-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3b458-107">*ppwszName* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="3b458-107">*ppwszName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3b458-108">Nome del pulsante dello stilo.</span><span class="sxs-lookup"><span data-stu-id="3b458-108">The name of the stylus button.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3b458-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3b458-109">Return value</span></span>

<span data-ttu-id="3b458-110">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="3b458-110">This method can return one of these values.</span></span>



| <span data-ttu-id="3b458-111">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="3b458-111">Return code</span></span>                                                                            | <span data-ttu-id="3b458-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3b458-112">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="3b458-113"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="3b458-113"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="3b458-114">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="3b458-114">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="3b458-115"><dt>**E \_ non riescono**</dt></span><span class="sxs-lookup"><span data-stu-id="3b458-115"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="3b458-116">Si è verificato un errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="3b458-116">An unspecified error occurred.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="3b458-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="3b458-117">Remarks</span></span>

<span data-ttu-id="3b458-118">È responsabilità del chiamante liberare la memoria restituita da questo metodo usando [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).</span><span class="sxs-lookup"><span data-stu-id="3b458-118">It is the caller's responsibility to free the memory returned from this method by using [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).</span></span>

## <a name="requirements"></a><span data-ttu-id="3b458-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3b458-119">Requirements</span></span>



| <span data-ttu-id="3b458-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="3b458-120">Requirement</span></span> | <span data-ttu-id="3b458-121">Valore</span><span class="sxs-lookup"><span data-stu-id="3b458-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3b458-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3b458-122">Minimum supported client</span></span><br/> | <span data-ttu-id="3b458-123">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="3b458-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="3b458-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3b458-124">Minimum supported server</span></span><br/> | <span data-ttu-id="3b458-125">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="3b458-125">None supported</span></span><br/>                                                              |
| <span data-ttu-id="3b458-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="3b458-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="3b458-127"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3b458-127"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3b458-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3b458-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b458-129">**Interfaccia ITabletCursorButton**</span><span class="sxs-lookup"><span data-stu-id="3b458-129">**ITabletCursorButton Interface**</span></span>](itabletcursorbutton.md)
</dt> </dl>

 

