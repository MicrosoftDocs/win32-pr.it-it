---
description: Il metodo SetGuidValue aggiunge un nuovo valore GUID (tipo VT \_ CLSID) o sovrascrive uno esistente.
ms.assetid: 429a83c0-59b6-4e2f-a657-cbec1dfb9070
title: 'Metodo IPortableDeviceValues:: SetGuidValue (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetGuidValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 9d9f85def6ba487163f7c4c7d7441a89e0747ed6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328527"
---
# <a name="iportabledevicevaluessetguidvalue-method"></a><span data-ttu-id="f3841-103">Metodo IPortableDeviceValues:: SetGuidValue</span><span class="sxs-lookup"><span data-stu-id="f3841-103">IPortableDeviceValues::SetGuidValue method</span></span>

<span data-ttu-id="f3841-104">Il metodo **SetGuidValue** aggiunge un nuovo valore **GUID** (tipo VT \_ CLSID) o sovrascrive uno esistente.</span><span class="sxs-lookup"><span data-stu-id="f3841-104">The **SetGuidValue** method adds a new **GUID** value (type VT\_CLSID) or overwrites an existing one.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3841-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f3841-105">Syntax</span></span>


```C++
HRESULT SetGuidValue(
  [in] REFPROPERTYKEY key,
  [in] REFGUID        Value
);
```



## <a name="parameters"></a><span data-ttu-id="f3841-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="f3841-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f3841-107">*chiave* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="f3841-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3841-108">Oggetto **REFPROPERTYKEY** che specifica l'elemento da creare o sovrascrivere.</span><span class="sxs-lookup"><span data-stu-id="f3841-108">A **REFPROPERTYKEY** that specifies the item to create or overwrite.</span></span>

</dd> <dt>

<span data-ttu-id="f3841-109">*Valore* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="f3841-109">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3841-110">Oggetto **REFGUID** che contiene il nuovo valore.</span><span class="sxs-lookup"><span data-stu-id="f3841-110">A **REFGUID** that contains the new value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f3841-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f3841-111">Return value</span></span>

<span data-ttu-id="f3841-112">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="f3841-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="f3841-113">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="f3841-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="f3841-114">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="f3841-114">Return code</span></span>                                                                          | <span data-ttu-id="f3841-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f3841-115">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="f3841-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="f3841-116"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="f3841-117">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="f3841-117">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f3841-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="f3841-118">Remarks</span></span>

<span data-ttu-id="f3841-119">Se un valore esistente ha la stessa chiave specificata dal parametro *Key* , sovrascrive il valore esistente senza alcun avviso.</span><span class="sxs-lookup"><span data-stu-id="f3841-119">If an existing value has the same key that is specified by the *key* parameter, it overwrites the existing value without any warning.</span></span>

## <a name="requirements"></a><span data-ttu-id="f3841-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f3841-120">Requirements</span></span>



| <span data-ttu-id="f3841-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="f3841-121">Requirement</span></span> | <span data-ttu-id="f3841-122">Valore</span><span class="sxs-lookup"><span data-stu-id="f3841-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3841-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f3841-123">Header</span></span><br/>  | <dl> <span data-ttu-id="f3841-124"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="f3841-124"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="f3841-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="f3841-125">Library</span></span><br/> | <dl> <span data-ttu-id="f3841-126"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f3841-126"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f3841-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f3841-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3841-128">Aggiunta di una risorsa a un oggetto</span><span class="sxs-lookup"><span data-stu-id="f3841-128">Adding a Resource to an Object</span></span>](adding-a-resource-to-an-object.md)
</dt> <dt>

[<span data-ttu-id="f3841-129">**Interfaccia IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="f3841-129">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="f3841-130">**IPortableDeviceValues::GetGuidValue**</span><span class="sxs-lookup"><span data-stu-id="f3841-130">**IPortableDeviceValues::GetGuidValue**</span></span>](iportabledevicevalues-getguidvalue.md)
</dt> </dl>

 

 




