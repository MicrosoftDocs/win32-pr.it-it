---
title: Metodo IWMDRMLicense PersistLicense (wmdrmsdk. h)
description: Il metodo PersistLicense salva la licenza corrente dall'archivio temporaneo nell'archivio licenze locale permanente.
ms.assetid: 80a0f932-2800-416b-9dfe-97654a76c19b
keywords:
- Metodo PersistLicense Windows Media Format
- Metodo PersistLicense Windows Media Format, interfaccia IWMDRMLicense
- Interfaccia IWMDRMLicense-formato Windows Media, metodo PersistLicense
topic_type:
- apiref
api_name:
- IWMDRMLicense.PersistLicense
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f41b61cdf448d757d13917ca22af0c3d9d9d390
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327697"
---
# <a name="iwmdrmlicensepersistlicense-method"></a><span data-ttu-id="ba0d2-106">IWMDRMLicense::P metodo ersistLicense</span><span class="sxs-lookup"><span data-stu-id="ba0d2-106">IWMDRMLicense::PersistLicense method</span></span>

<span data-ttu-id="ba0d2-107">Il metodo **PersistLicense** salva la licenza corrente dall'archivio temporaneo nell'archivio licenze locale permanente.</span><span class="sxs-lookup"><span data-stu-id="ba0d2-107">The **PersistLicense** method saves the current license from the temporary store into the permanent local license store.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba0d2-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ba0d2-108">Syntax</span></span>


```C++
HRESULT PersistLicense();
```



## <a name="parameters"></a><span data-ttu-id="ba0d2-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="ba0d2-109">Parameters</span></span>

<span data-ttu-id="ba0d2-110">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="ba0d2-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ba0d2-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ba0d2-111">Return value</span></span>

<span data-ttu-id="ba0d2-112">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="ba0d2-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="ba0d2-113">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="ba0d2-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="ba0d2-114">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="ba0d2-114">Return code</span></span>                                                                          | <span data-ttu-id="ba0d2-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ba0d2-115">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="ba0d2-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="ba0d2-116"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="ba0d2-117">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="ba0d2-117">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ba0d2-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="ba0d2-118">Remarks</span></span>

<span data-ttu-id="ba0d2-119">Se la licenza corrente non è presente nell'archivio temporaneo, questo metodo avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="ba0d2-119">If the current license is not in the temporary store, this method will fail.</span></span>

<span data-ttu-id="ba0d2-120">È possibile chiamare [**CanPersist**](iwmdrmlicense-canpersist.md) per eseguire una query per verificare se la licenza è consentita per essere resa permanente.</span><span class="sxs-lookup"><span data-stu-id="ba0d2-120">You can call [**CanPersist**](iwmdrmlicense-canpersist.md) to query whether the license is allowed to be persisted.</span></span>

## <a name="requirements"></a><span data-ttu-id="ba0d2-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ba0d2-121">Requirements</span></span>



| <span data-ttu-id="ba0d2-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="ba0d2-122">Requirement</span></span> | <span data-ttu-id="ba0d2-123">Valore</span><span class="sxs-lookup"><span data-stu-id="ba0d2-123">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ba0d2-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ba0d2-124">Header</span></span><br/> | <dl> <span data-ttu-id="ba0d2-125"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="ba0d2-125"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ba0d2-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ba0d2-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba0d2-127">**Interfaccia IWMDRMLicense**</span><span class="sxs-lookup"><span data-stu-id="ba0d2-127">**IWMDRMLicense Interface**</span></span>](iwmdrmlicense.md)
</dt> </dl>

 

 





