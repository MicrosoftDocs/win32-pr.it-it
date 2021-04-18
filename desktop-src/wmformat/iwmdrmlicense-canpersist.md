---
title: Metodo IWMDRMLicense CanPersist (wmdrmsdk. h)
description: Il metodo CanPersist esegue una query per determinare se la licenza può essere mantenute in un archivio licenze locale.
ms.assetid: 040b30d8-4e47-44a3-8b09-e81cc30e8a53
keywords:
- Metodo CanPersist Windows Media Format
- Metodo CanPersist Windows Media Format, interfaccia IWMDRMLicense
- Interfaccia IWMDRMLicense-formato Windows Media, metodo CanPersist
topic_type:
- apiref
api_name:
- IWMDRMLicense.CanPersist
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a7772dac73b99443626b1eeec6f5e90851f92c4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328532"
---
# <a name="iwmdrmlicensecanpersist-method"></a><span data-ttu-id="53f2c-106">Metodo IWMDRMLicense:: CanPersist</span><span class="sxs-lookup"><span data-stu-id="53f2c-106">IWMDRMLicense::CanPersist method</span></span>

<span data-ttu-id="53f2c-107">Il metodo **CanPersist** esegue una query per determinare se la licenza può essere mantenute in un archivio licenze locale.</span><span class="sxs-lookup"><span data-stu-id="53f2c-107">The **CanPersist** method queries whether the license can be persisted on in a local license store.</span></span>

## <a name="syntax"></a><span data-ttu-id="53f2c-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="53f2c-108">Syntax</span></span>


```C++
HRESULT CanPersist(
  [out] BOOL *pfCanPersist
);
```



## <a name="parameters"></a><span data-ttu-id="53f2c-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="53f2c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="53f2c-110">*pfCanPersist* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="53f2c-110">*pfCanPersist* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="53f2c-111">TRUE indica che la licenza può essere mantenute.</span><span class="sxs-lookup"><span data-stu-id="53f2c-111">TRUE indicates that the license can be persisted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="53f2c-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="53f2c-112">Return value</span></span>

<span data-ttu-id="53f2c-113">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="53f2c-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="53f2c-114">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="53f2c-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="53f2c-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="53f2c-115">Return code</span></span>                                                                          | <span data-ttu-id="53f2c-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="53f2c-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="53f2c-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="53f2c-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="53f2c-118">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="53f2c-118">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="53f2c-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="53f2c-119">Remarks</span></span>

<span data-ttu-id="53f2c-120">Nessuna.</span><span class="sxs-lookup"><span data-stu-id="53f2c-120">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="53f2c-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="53f2c-121">Requirements</span></span>



| <span data-ttu-id="53f2c-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="53f2c-122">Requirement</span></span> | <span data-ttu-id="53f2c-123">Valore</span><span class="sxs-lookup"><span data-stu-id="53f2c-123">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="53f2c-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="53f2c-124">Header</span></span><br/> | <dl> <span data-ttu-id="53f2c-125"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="53f2c-125"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="53f2c-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="53f2c-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53f2c-127">**Interfaccia IWMDRMLicense**</span><span class="sxs-lookup"><span data-stu-id="53f2c-127">**IWMDRMLicense Interface**</span></span>](iwmdrmlicense.md)
</dt> </dl>

 

 





