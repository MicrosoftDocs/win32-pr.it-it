---
description: Il metodo CopyValuesFromPropertyStore copia il contenuto di un oggetto IPropertyStore nella raccolta.
ms.assetid: 887c9569-ff76-41cf-8782-62c59c04e831
title: 'Metodo IPortableDeviceValues:: CopyValuesFromPropertyStore (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.CopyValuesFromPropertyStore
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: fbc2508d300fe4d0680d539153fde5f86603e04d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330710"
---
# <a name="iportabledevicevaluescopyvaluesfrompropertystore-method"></a><span data-ttu-id="38b84-103">Metodo IPortableDeviceValues:: CopyValuesFromPropertyStore</span><span class="sxs-lookup"><span data-stu-id="38b84-103">IPortableDeviceValues::CopyValuesFromPropertyStore method</span></span>

<span data-ttu-id="38b84-104">Il metodo **CopyValuesFromPropertyStore** copia il contenuto di un oggetto **IPropertyStore** nella raccolta.</span><span class="sxs-lookup"><span data-stu-id="38b84-104">The **CopyValuesFromPropertyStore** method copies the contents of an **IPropertyStore** into the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="38b84-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="38b84-105">Syntax</span></span>


```C++
HRESULT CopyValuesFromPropertyStore(
  [in] IPropertyStore *pStore
);
```



## <a name="parameters"></a><span data-ttu-id="38b84-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="38b84-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="38b84-107">*pStore* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="38b84-107">*pStore* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="38b84-108">Puntatore a un oggetto **IPropertyStore** da copiare nella raccolta.</span><span class="sxs-lookup"><span data-stu-id="38b84-108">Pointer to an **IPropertyStore** to copy into the collection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="38b84-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="38b84-109">Return value</span></span>

<span data-ttu-id="38b84-110">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="38b84-110">The method returns an **HRESULT**.</span></span> <span data-ttu-id="38b84-111">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="38b84-111">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="38b84-112">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="38b84-112">Return code</span></span>                                                                          | <span data-ttu-id="38b84-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="38b84-113">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="38b84-114"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="38b84-114"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="38b84-115">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="38b84-115">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="38b84-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="38b84-116">Remarks</span></span>

<span data-ttu-id="38b84-117">Questo metodo converte automaticamente tutti i valori **\_ BSTR di VT** in valori **\_ LPWSTR VT** .</span><span class="sxs-lookup"><span data-stu-id="38b84-117">This method automatically converts all **VT\_BSTR** values to **VT\_LPWSTR** values.</span></span>

<span data-ttu-id="38b84-118">Molte applicazioni o componenti esterni che comunicano con l'applicazione, ad esempio alcune applicazioni shell, usano l'interfaccia **IPropertyStore** .</span><span class="sxs-lookup"><span data-stu-id="38b84-118">Many external applications or components that communicate with your application, such as some shell applications, use the **IPropertyStore** interface.</span></span> <span data-ttu-id="38b84-119">Questo metodo consente di scambiare dati in modo semplice e rapido con questi programmi.</span><span class="sxs-lookup"><span data-stu-id="38b84-119">This method provides a quick and easy way to exchange data with these programs.</span></span>

<span data-ttu-id="38b84-120">Questo metodo è supportato in Windows Vista e nelle versioni successive di Windows.</span><span class="sxs-lookup"><span data-stu-id="38b84-120">This method is supported in Windows Vista and later versions of Windows.</span></span>

## <a name="requirements"></a><span data-ttu-id="38b84-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="38b84-121">Requirements</span></span>



| <span data-ttu-id="38b84-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="38b84-122">Requirement</span></span> | <span data-ttu-id="38b84-123">Valore</span><span class="sxs-lookup"><span data-stu-id="38b84-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="38b84-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="38b84-124">Header</span></span><br/>  | <dl> <span data-ttu-id="38b84-125"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="38b84-125"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="38b84-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="38b84-126">Library</span></span><br/> | <dl> <span data-ttu-id="38b84-127"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="38b84-127"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="38b84-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="38b84-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38b84-129">**Interfaccia IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="38b84-129">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="38b84-130">**IPortableDeviceValues::CopyValuesToPropertyStore**</span><span class="sxs-lookup"><span data-stu-id="38b84-130">**IPortableDeviceValues::CopyValuesToPropertyStore**</span></span>](iportabledevicevalues-copyvaluestopropertystore.md)
</dt> </dl>

 

 




