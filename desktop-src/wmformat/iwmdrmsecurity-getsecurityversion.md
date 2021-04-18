---
title: Metodo IWMDRMSecurity GetSecurityVersion (wmdrmsdk. h)
description: Il metodo GetSecurityVersion recupera la versione del sottosistema DRM nel computer client.
ms.assetid: ec97dec8-61ba-4424-b5eb-2e6885cc1f48
keywords:
- Metodo GetSecurityVersion Windows Media Format
- Metodo GetSecurityVersion Windows Media Format, interfaccia IWMDRMSecurity
- Interfaccia IWMDRMSecurity-formato Windows Media, metodo GetSecurityVersion
topic_type:
- apiref
api_name:
- IWMDRMSecurity.GetSecurityVersion
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33be994383a7e16d136aac340a77deef8256d62f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327264"
---
# <a name="iwmdrmsecuritygetsecurityversion-method"></a><span data-ttu-id="fff5c-106">Metodo IWMDRMSecurity:: GetSecurityVersion</span><span class="sxs-lookup"><span data-stu-id="fff5c-106">IWMDRMSecurity::GetSecurityVersion method</span></span>

<span data-ttu-id="fff5c-107">Il metodo **GetSecurityVersion** recupera la versione del sottosistema DRM nel computer client.</span><span class="sxs-lookup"><span data-stu-id="fff5c-107">The **GetSecurityVersion** method retrieves the version of the DRM subsystem on the client computer.</span></span>

## <a name="syntax"></a><span data-ttu-id="fff5c-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fff5c-108">Syntax</span></span>


```C++
HRESULT GetSecurityVersion(
  [out] BSTR *pbstrVersion
);
```



## <a name="parameters"></a><span data-ttu-id="fff5c-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="fff5c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fff5c-110">*pbstrVersion* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="fff5c-110">*pbstrVersion* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fff5c-111">Indirizzo di una variabile che riceve il numero di versione del sottosistema DRM.</span><span class="sxs-lookup"><span data-stu-id="fff5c-111">Address of a variable that receives the DRM subsystem version number.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fff5c-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fff5c-112">Return value</span></span>

<span data-ttu-id="fff5c-113">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="fff5c-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="fff5c-114">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="fff5c-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="fff5c-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="fff5c-115">Return code</span></span>                                                                          | <span data-ttu-id="fff5c-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fff5c-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="fff5c-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="fff5c-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="fff5c-118">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="fff5c-118">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="fff5c-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="fff5c-119">Remarks</span></span>

<span data-ttu-id="fff5c-120">Il numero di versione è espresso come stringa costituita da quattro numeri separati da punti.</span><span class="sxs-lookup"><span data-stu-id="fff5c-120">The version number is expressed as a string consisting of four numbers separated by periods.</span></span> <span data-ttu-id="fff5c-121">Il primo numero è il numero di versione principale, che in genere è impostato su 2.</span><span class="sxs-lookup"><span data-stu-id="fff5c-121">The first number is the major version number, which is usually set to 2.</span></span> <span data-ttu-id="fff5c-122">Il secondo numero è il numero di versione secondario, compreso tra 2 e 10.</span><span class="sxs-lookup"><span data-stu-id="fff5c-122">The second number is the minor version number, ranging from 2 to 10.</span></span> <span data-ttu-id="fff5c-123">Il terzo numero è sempre impostato su 0.</span><span class="sxs-lookup"><span data-stu-id="fff5c-123">The third number is always set to 0.</span></span> <span data-ttu-id="fff5c-124">Il quarto numero è impostato su 0 o 1 e è un valore booleano che indica se il sottosistema è stato personalizzato.</span><span class="sxs-lookup"><span data-stu-id="fff5c-124">The fourth number is set to 0 or 1, and is a Boolean value indicating whether the subsystem has been individualized.</span></span> <span data-ttu-id="fff5c-125">Ad esempio, un numero di versione di "2.4.0.1" indica la quarta versione secondaria della seconda versione principale.</span><span class="sxs-lookup"><span data-stu-id="fff5c-125">For example, a version number of "2.4.0.1" indicates the individualized fourth minor version of the second major version.</span></span>

## <a name="requirements"></a><span data-ttu-id="fff5c-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fff5c-126">Requirements</span></span>



| <span data-ttu-id="fff5c-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="fff5c-127">Requirement</span></span> | <span data-ttu-id="fff5c-128">Valore</span><span class="sxs-lookup"><span data-stu-id="fff5c-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fff5c-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fff5c-129">Header</span></span><br/>  | <dl> <span data-ttu-id="fff5c-130"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="fff5c-130"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="fff5c-131">Libreria</span><span class="sxs-lookup"><span data-stu-id="fff5c-131">Library</span></span><br/> | <dl> <span data-ttu-id="fff5c-132"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fff5c-132"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fff5c-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fff5c-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fff5c-134">**Interfaccia IWMDRMSecurity**</span><span class="sxs-lookup"><span data-stu-id="fff5c-134">**IWMDRMSecurity Interface**</span></span>](iwmdrmsecurity.md)
</dt> </dl>

 

 





