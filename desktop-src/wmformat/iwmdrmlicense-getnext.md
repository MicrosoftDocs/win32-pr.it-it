---
title: Metodo GetNext IWMDRMLicense (wmdrmsdk. h)
description: Il metodo GetNext carica le informazioni relative all'elemento successivo nell'elenco.
ms.assetid: 5ef91751-2883-4a8e-9908-7a6dfe6d2af3
keywords:
- Formato Windows Media metodo GetNext
- Metodo GetNext, formato Windows Media, interfaccia IWMDRMLicense
- Interfaccia IWMDRMLicense-formato Windows Media, metodo GetNext
topic_type:
- apiref
api_name:
- IWMDRMLicense.GetNext
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da1dd1f8ce41648c7a67730d909058d10d616e7a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326293"
---
# <a name="iwmdrmlicensegetnext-method"></a><span data-ttu-id="55ff7-106">Metodo IWMDRMLicense:: GetNext</span><span class="sxs-lookup"><span data-stu-id="55ff7-106">IWMDRMLicense::GetNext method</span></span>

<span data-ttu-id="55ff7-107">Il metodo **GetNext** carica le informazioni relative all'elemento successivo nell'elenco.</span><span class="sxs-lookup"><span data-stu-id="55ff7-107">The **GetNext** method loads the information about the next item in the list.</span></span>

## <a name="syntax"></a><span data-ttu-id="55ff7-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="55ff7-108">Syntax</span></span>


```C++
HRESULT GetNext();
```



## <a name="parameters"></a><span data-ttu-id="55ff7-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="55ff7-109">Parameters</span></span>

<span data-ttu-id="55ff7-110">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="55ff7-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="55ff7-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="55ff7-111">Return value</span></span>

<span data-ttu-id="55ff7-112">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="55ff7-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="55ff7-113">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="55ff7-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="55ff7-114">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="55ff7-114">Return code</span></span>                                                                                                | <span data-ttu-id="55ff7-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="55ff7-115">Description</span></span>                                              |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="55ff7-116"><dt>**NS \_ E \_ DRM di DRM \_ \_ troppo \_ piccoli**</dt></span><span class="sxs-lookup"><span data-stu-id="55ff7-116"><dt>**NS\_E\_DRM\_RIV\_TOO\_SMALL**</dt></span></span> </dl> | <span data-ttu-id="55ff7-117">È necessario un elenco di revoche di contenuti aggiornato.</span><span class="sxs-lookup"><span data-stu-id="55ff7-117">An updated content revocation list is needed.</span></span><br/> |
| <dl> <span data-ttu-id="55ff7-118"><dt>**ERRORE \_ nessun \_ altro \_ elemento**</dt></span><span class="sxs-lookup"><span data-stu-id="55ff7-118"><dt>**ERROR\_NO\_MORE\_ITEMS**</dt></span></span> </dl>      | <span data-ttu-id="55ff7-119">Non sono presenti altri elementi nell'elenco.</span><span class="sxs-lookup"><span data-stu-id="55ff7-119">There are no more items in the list.</span></span><br/>          |
| <dl> <span data-ttu-id="55ff7-120"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="55ff7-120"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="55ff7-121">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="55ff7-121">The method succeeded.</span></span><br/>                         |



 

## <a name="remarks"></a><span data-ttu-id="55ff7-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="55ff7-122">Remarks</span></span>

<span data-ttu-id="55ff7-123">I metodi dell'interfaccia [**IWMDRMLicense**](iwmdrmlicense.md) forniscono dati relativi a una singola licenza alla volta.</span><span class="sxs-lookup"><span data-stu-id="55ff7-123">The methods of the [**IWMDRMLicense**](iwmdrmlicense.md) interface provide data about a single license at a time.</span></span> <span data-ttu-id="55ff7-124">L'oggetto sottostante contiene un elenco di una o più licenze.</span><span class="sxs-lookup"><span data-stu-id="55ff7-124">The underlying object contains a list of one or more licenses.</span></span> <span data-ttu-id="55ff7-125">Quando si chiama questo metodo, l'interfaccia sposta i relativi riferimenti interni alla licenza successiva nell'elenco.</span><span class="sxs-lookup"><span data-stu-id="55ff7-125">When you call this method, the interface moves its internal references to the next license in the list.</span></span>

## <a name="requirements"></a><span data-ttu-id="55ff7-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="55ff7-126">Requirements</span></span>



| <span data-ttu-id="55ff7-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="55ff7-127">Requirement</span></span> | <span data-ttu-id="55ff7-128">Valore</span><span class="sxs-lookup"><span data-stu-id="55ff7-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="55ff7-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="55ff7-129">Header</span></span><br/>  | <dl> <span data-ttu-id="55ff7-130"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="55ff7-130"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="55ff7-131">Libreria</span><span class="sxs-lookup"><span data-stu-id="55ff7-131">Library</span></span><br/> | <dl> <span data-ttu-id="55ff7-132"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="55ff7-132"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="55ff7-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="55ff7-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55ff7-134">**Interfaccia IWMDRMLicense**</span><span class="sxs-lookup"><span data-stu-id="55ff7-134">**IWMDRMLicense Interface**</span></span>](iwmdrmlicense.md)
</dt> </dl>

 

 





