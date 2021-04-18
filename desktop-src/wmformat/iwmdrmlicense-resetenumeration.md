---
title: Metodo IWMDRMLicense ResetEnumeration (wmdrmsdk. h)
description: Il metodo ResetEnumeration Reimposta l'elenco di licenze sullo stato originale. La licenza attiva diventa la prima licenza dell'elenco.
ms.assetid: cb5a31a8-ee25-44d6-81ca-746c379cb99e
keywords:
- Metodo ResetEnumeration Windows Media Format
- Metodo ResetEnumeration Windows Media Format, interfaccia IWMDRMLicense
- Interfaccia IWMDRMLicense-formato Windows Media, metodo ResetEnumeration
topic_type:
- apiref
api_name:
- IWMDRMLicense.ResetEnumeration
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6510c05b4c974051d9902ed2d30d9cdf99956af
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326992"
---
# <a name="iwmdrmlicenseresetenumeration-method"></a><span data-ttu-id="5a693-107">Metodo IWMDRMLicense:: ResetEnumeration</span><span class="sxs-lookup"><span data-stu-id="5a693-107">IWMDRMLicense::ResetEnumeration method</span></span>

<span data-ttu-id="5a693-108">Il metodo **ResetEnumeration** Reimposta l'elenco di licenze sullo stato originale.</span><span class="sxs-lookup"><span data-stu-id="5a693-108">The **ResetEnumeration** method resets the license list to its original state.</span></span> <span data-ttu-id="5a693-109">La licenza attiva diventa la prima licenza dell'elenco.</span><span class="sxs-lookup"><span data-stu-id="5a693-109">The active license becomes the first license in the list.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a693-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5a693-110">Syntax</span></span>


```C++
HRESULT ResetEnumeration();
```



## <a name="parameters"></a><span data-ttu-id="5a693-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="5a693-111">Parameters</span></span>

<span data-ttu-id="5a693-112">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="5a693-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5a693-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5a693-113">Return value</span></span>

<span data-ttu-id="5a693-114">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="5a693-114">The method returns an **HRESULT**.</span></span> <span data-ttu-id="5a693-115">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="5a693-115">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="5a693-116">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="5a693-116">Return code</span></span>                                                                                                | <span data-ttu-id="5a693-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5a693-117">Description</span></span>                                              |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="5a693-118"><dt>**NS \_ E \_ DRM di DRM \_ \_ troppo \_ piccoli**</dt></span><span class="sxs-lookup"><span data-stu-id="5a693-118"><dt>**NS\_E\_DRM\_RIV\_TOO\_SMALL**</dt></span></span> </dl> | <span data-ttu-id="5a693-119">È necessario un elenco di revoche di contenuti aggiornato.</span><span class="sxs-lookup"><span data-stu-id="5a693-119">An updated content revocation list is needed.</span></span><br/> |
| <dl> <span data-ttu-id="5a693-120"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="5a693-120"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="5a693-121">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="5a693-121">The method succeeded.</span></span><br/>                         |



 

## <a name="remarks"></a><span data-ttu-id="5a693-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="5a693-122">Remarks</span></span>

<span data-ttu-id="5a693-123">Nessuna.</span><span class="sxs-lookup"><span data-stu-id="5a693-123">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="5a693-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5a693-124">Requirements</span></span>



| <span data-ttu-id="5a693-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="5a693-125">Requirement</span></span> | <span data-ttu-id="5a693-126">Valore</span><span class="sxs-lookup"><span data-stu-id="5a693-126">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5a693-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5a693-127">Header</span></span><br/>  | <dl> <span data-ttu-id="5a693-128"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="5a693-128"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="5a693-129">Libreria</span><span class="sxs-lookup"><span data-stu-id="5a693-129">Library</span></span><br/> | <dl> <span data-ttu-id="5a693-130"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5a693-130"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5a693-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5a693-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a693-132">**Interfaccia IWMDRMLicense**</span><span class="sxs-lookup"><span data-stu-id="5a693-132">**IWMDRMLicense Interface**</span></span>](iwmdrmlicense.md)
</dt> </dl>

 

 





