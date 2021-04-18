---
title: Metodo CreateObject IWMDRMProvider (wmdrmsdk. h)
description: Il metodo CreateObject recupera un puntatore a un'interfaccia specificata e, se necessario, crea l'oggetto di implementazione.
ms.assetid: d408f7f3-9e49-4747-ac8f-d39db31d1240
keywords:
- Metodo CreateObject formato Windows Media
- Metodo CreateObject formato Windows Media, interfaccia IWMDRMProvider
- Interfaccia IWMDRMProvider-formato Windows Media, metodo CreateObject
topic_type:
- apiref
api_name:
- IWMDRMProvider.CreateObject
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c0422138391b0d6f5e38fbc81fd5141bd3d8535
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325545"
---
# <a name="iwmdrmprovidercreateobject-method"></a><span data-ttu-id="fcce4-106">Metodo IWMDRMProvider:: CreateObject</span><span class="sxs-lookup"><span data-stu-id="fcce4-106">IWMDRMProvider::CreateObject method</span></span>

<span data-ttu-id="fcce4-107">Il metodo **CreateObject** recupera un puntatore a un'interfaccia specificata e, se necessario, crea l'oggetto di implementazione.</span><span class="sxs-lookup"><span data-stu-id="fcce4-107">The **CreateObject** method retrieves a pointer to a specified interface, creating the implementing object if needed.</span></span>

## <a name="syntax"></a><span data-ttu-id="fcce4-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fcce4-108">Syntax</span></span>


```C++
HRESULT CreateObject(
  [in]  REFIID riid,
  [out] void   **ppvObject
);
```



## <a name="parameters"></a><span data-ttu-id="fcce4-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="fcce4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fcce4-110">*riid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fcce4-110">*riid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fcce4-111">Identificatore dell'interfaccia da creare.</span><span class="sxs-lookup"><span data-stu-id="fcce4-111">Identifier of the interface to be created.</span></span> <span data-ttu-id="fcce4-112">Impostare su uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="fcce4-112">Set to one of the following values.</span></span>

-   <span data-ttu-id="fcce4-113">\_IWMDRMLICENSEMANAGEMENT IID</span><span class="sxs-lookup"><span data-stu-id="fcce4-113">IID\_IWMDRMLicenseManagement</span></span>
-   <span data-ttu-id="fcce4-114">\_IWMDRMLICENSEQUERY IID</span><span class="sxs-lookup"><span data-stu-id="fcce4-114">IID\_IWMDRMLicenseQuery</span></span>
-   <span data-ttu-id="fcce4-115">\_IWMDRMNETRECEIVER IID</span><span class="sxs-lookup"><span data-stu-id="fcce4-115">IID\_IWMDRMNetReceiver</span></span>
-   <span data-ttu-id="fcce4-116">\_IWMDRMNETTRANSMITTER IID</span><span class="sxs-lookup"><span data-stu-id="fcce4-116">IID\_IWMDRMNetTransmitter</span></span>
-   <span data-ttu-id="fcce4-117">\_IWMDRMSECURITY IID</span><span class="sxs-lookup"><span data-stu-id="fcce4-117">IID\_IWMDRMSecurity</span></span>

</dd> <dt>

<span data-ttu-id="fcce4-118">*ppvObject* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="fcce4-118">*ppvObject* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fcce4-119">Indirizzo di un puntatore che riceve l'indirizzo dell'interfaccia richiesta.</span><span class="sxs-lookup"><span data-stu-id="fcce4-119">Address of a pointer that receives the address of the requested interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fcce4-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fcce4-120">Return value</span></span>

<span data-ttu-id="fcce4-121">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="fcce4-121">The method returns an **HRESULT**.</span></span> <span data-ttu-id="fcce4-122">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="fcce4-122">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="fcce4-123">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="fcce4-123">Return code</span></span>                                                                          | <span data-ttu-id="fcce4-124">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fcce4-124">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="fcce4-125"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="fcce4-125"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="fcce4-126">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="fcce4-126">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="fcce4-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="fcce4-127">Remarks</span></span>

<span data-ttu-id="fcce4-128">Nessuna.</span><span class="sxs-lookup"><span data-stu-id="fcce4-128">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="fcce4-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fcce4-129">Requirements</span></span>



| <span data-ttu-id="fcce4-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="fcce4-130">Requirement</span></span> | <span data-ttu-id="fcce4-131">Valore</span><span class="sxs-lookup"><span data-stu-id="fcce4-131">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fcce4-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fcce4-132">Header</span></span><br/>  | <dl> <span data-ttu-id="fcce4-133"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="fcce4-133"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="fcce4-134">Libreria</span><span class="sxs-lookup"><span data-stu-id="fcce4-134">Library</span></span><br/> | <dl> <span data-ttu-id="fcce4-135"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fcce4-135"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fcce4-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fcce4-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fcce4-137">**Interfaccia IWMDRMProvider**</span><span class="sxs-lookup"><span data-stu-id="fcce4-137">**IWMDRMProvider Interface**</span></span>](iwmdrmprovider.md)
</dt> <dt>

[<span data-ttu-id="fcce4-138">**Interfaccia IWMDRMLicenseManagement**</span><span class="sxs-lookup"><span data-stu-id="fcce4-138">**IWMDRMLicenseManagement Interface**</span></span>](iwmdrmlicensemanagement.md)
</dt> <dt>

[<span data-ttu-id="fcce4-139">**Interfaccia IWMDRMLicenseQuery**</span><span class="sxs-lookup"><span data-stu-id="fcce4-139">**IWMDRMLicenseQuery Interface**</span></span>](iwmdrmlicensequery.md)
</dt> <dt>

[<span data-ttu-id="fcce4-140">**Interfaccia IWMDRMNetReceiver**</span><span class="sxs-lookup"><span data-stu-id="fcce4-140">**IWMDRMNetReceiver Interface**</span></span>](iwmdrmnetreceiver.md)
</dt> <dt>

[<span data-ttu-id="fcce4-141">**Interfaccia IWMDRMNetTransmitter**</span><span class="sxs-lookup"><span data-stu-id="fcce4-141">**IWMDRMNetTransmitter Interface**</span></span>](iwmdrmnettransmitter.md)
</dt> <dt>

[<span data-ttu-id="fcce4-142">**Interfaccia IWMDRMSecurity**</span><span class="sxs-lookup"><span data-stu-id="fcce4-142">**IWMDRMSecurity Interface**</span></span>](iwmdrmsecurity.md)
</dt> </dl>

 

 





