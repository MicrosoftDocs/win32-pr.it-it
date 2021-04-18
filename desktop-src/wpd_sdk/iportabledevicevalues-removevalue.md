---
description: Il Metodo RemoveValue rimuove un elemento dalla raccolta.
ms.assetid: 864c23ee-5a4e-4e06-add0-f6aef5562430
title: 'Metodo IPortableDeviceValues:: RemoveValue (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.RemoveValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: f65160cc2798524d88471382c855f65dea2e6033
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325810"
---
# <a name="iportabledevicevaluesremovevalue-method"></a><span data-ttu-id="b9ece-103">Metodo IPortableDeviceValues:: RemoveValue</span><span class="sxs-lookup"><span data-stu-id="b9ece-103">IPortableDeviceValues::RemoveValue method</span></span>

<span data-ttu-id="b9ece-104">Il metodo **RemoveValue** rimuove un elemento dalla raccolta.</span><span class="sxs-lookup"><span data-stu-id="b9ece-104">The **RemoveValue** method removes an item from the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="b9ece-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b9ece-105">Syntax</span></span>


```C++
HRESULT RemoveValue(
  [in] REFPROPERTYKEY key
);
```



## <a name="parameters"></a><span data-ttu-id="b9ece-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b9ece-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b9ece-107">*chiave* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="b9ece-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b9ece-108">Oggetto **REFPROPERTYKEY** che specifica l'elemento da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="b9ece-108">A **REFPROPERTYKEY** that specifies the item to remove.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b9ece-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b9ece-109">Return value</span></span>

<span data-ttu-id="b9ece-110">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="b9ece-110">The method returns an **HRESULT**.</span></span> <span data-ttu-id="b9ece-111">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="b9ece-111">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="b9ece-112">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="b9ece-112">Return code</span></span>                                                                          | <span data-ttu-id="b9ece-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b9ece-113">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="b9ece-114"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="b9ece-114"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="b9ece-115">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="b9ece-115">The method succeeded.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="b9ece-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b9ece-116">Requirements</span></span>



| <span data-ttu-id="b9ece-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="b9ece-117">Requirement</span></span> | <span data-ttu-id="b9ece-118">Valore</span><span class="sxs-lookup"><span data-stu-id="b9ece-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b9ece-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b9ece-119">Header</span></span><br/>  | <dl> <span data-ttu-id="b9ece-120"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="b9ece-120"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="b9ece-121">Libreria</span><span class="sxs-lookup"><span data-stu-id="b9ece-121">Library</span></span><br/> | <dl> <span data-ttu-id="b9ece-122"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b9ece-122"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b9ece-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b9ece-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9ece-124">**Interfaccia IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="b9ece-124">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="b9ece-125">**IPortableDeviceValues:: GetValue**</span><span class="sxs-lookup"><span data-stu-id="b9ece-125">**IPortableDeviceValues::GetValue**</span></span>](iportabledevicevalues-getvalue.md)
</dt> <dt>

[<span data-ttu-id="b9ece-126">**IPortableDeviceValues:: SetValue**</span><span class="sxs-lookup"><span data-stu-id="b9ece-126">**IPortableDeviceValues::SetValue**</span></span>](iportabledevicevalues-setvalue.md)
</dt> </dl>

 

 




