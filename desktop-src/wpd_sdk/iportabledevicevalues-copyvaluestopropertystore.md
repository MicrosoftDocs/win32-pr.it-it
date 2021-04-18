---
description: Il metodo CopyValuesToPropertyStore copia tutti i valori da una raccolta in un'interfaccia IPropertyStore.
ms.assetid: 417a8723-fa46-44c8-9bdc-412c0f20969a
title: 'Metodo IPortableDeviceValues:: CopyValuesToPropertyStore (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.CopyValuesToPropertyStore
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: d6ab6b4614c336d3e0da50c0291b2e69a260ae1f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330707"
---
# <a name="iportabledevicevaluescopyvaluestopropertystore-method"></a><span data-ttu-id="c4ba5-103">Metodo IPortableDeviceValues:: CopyValuesToPropertyStore</span><span class="sxs-lookup"><span data-stu-id="c4ba5-103">IPortableDeviceValues::CopyValuesToPropertyStore method</span></span>

<span data-ttu-id="c4ba5-104">Il metodo **CopyValuesToPropertyStore** copia tutti i valori da una raccolta in un'interfaccia **IPropertyStore** .</span><span class="sxs-lookup"><span data-stu-id="c4ba5-104">The **CopyValuesToPropertyStore** method copies all the values from a collection into an **IPropertyStore** interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4ba5-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c4ba5-105">Syntax</span></span>


```C++
HRESULT CopyValuesToPropertyStore(
  [in] IPropertyStore *pStore
);
```



## <a name="parameters"></a><span data-ttu-id="c4ba5-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="c4ba5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c4ba5-107">*pStore* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c4ba5-107">*pStore* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4ba5-108">Puntatore a un oggetto Store.</span><span class="sxs-lookup"><span data-stu-id="c4ba5-108">Pointer to a store object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c4ba5-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c4ba5-109">Return value</span></span>

<span data-ttu-id="c4ba5-110">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="c4ba5-110">The method returns an **HRESULT**.</span></span> <span data-ttu-id="c4ba5-111">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="c4ba5-111">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="c4ba5-112">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="c4ba5-112">Return code</span></span>                                                                          | <span data-ttu-id="c4ba5-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c4ba5-113">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="c4ba5-114"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="c4ba5-114"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="c4ba5-115">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="c4ba5-115">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="c4ba5-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="c4ba5-116">Remarks</span></span>

<span data-ttu-id="c4ba5-117">Questo metodo non converte i valori dei \_ LPWSTR VT in VT \_ BSTR.</span><span class="sxs-lookup"><span data-stu-id="c4ba5-117">This method does not convert values of VT\_LPWSTR into VT\_BSTR.</span></span> <span data-ttu-id="c4ba5-118">Molte applicazioni o componenti esterni che comunicano con l'applicazione, ad esempio alcune applicazioni shell, usano l'interfaccia **IPropertyStore** .</span><span class="sxs-lookup"><span data-stu-id="c4ba5-118">Many external applications or components that communicate with your application, such as some shell applications, use the **IPropertyStore** interface.</span></span> <span data-ttu-id="c4ba5-119">Questo metodo consente di scambiare dati in modo semplice e rapido con questi programmi.</span><span class="sxs-lookup"><span data-stu-id="c4ba5-119">This method provides a quick and easy way to exchange data with these programs.</span></span>

<span data-ttu-id="c4ba5-120">Questo metodo è supportato in Windows Vista e nelle versioni successive di Windows.</span><span class="sxs-lookup"><span data-stu-id="c4ba5-120">This method is supported in Windows Vista and later versions of Windows.</span></span>

## <a name="requirements"></a><span data-ttu-id="c4ba5-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c4ba5-121">Requirements</span></span>



| <span data-ttu-id="c4ba5-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="c4ba5-122">Requirement</span></span> | <span data-ttu-id="c4ba5-123">Valore</span><span class="sxs-lookup"><span data-stu-id="c4ba5-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4ba5-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c4ba5-124">Header</span></span><br/>  | <dl> <span data-ttu-id="c4ba5-125"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="c4ba5-125"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="c4ba5-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="c4ba5-126">Library</span></span><br/> | <dl> <span data-ttu-id="c4ba5-127"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c4ba5-127"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c4ba5-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c4ba5-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4ba5-129">**Interfaccia IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="c4ba5-129">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="c4ba5-130">**IPortableDeviceValues::CopyValuesFromPropertyStore**</span><span class="sxs-lookup"><span data-stu-id="c4ba5-130">**IPortableDeviceValues::CopyValuesFromPropertyStore**</span></span>](iportabledevicevalues-copyvaluesfrompropertystore.md)
</dt> </dl>

 

 




