---
description: Il metodo SetIUnknownValue aggiunge un nuovo valore IUnknown (Type VT \_ Unknown) o ne sovrascrive uno esistente.
ms.assetid: 292adf45-439c-4aae-9b17-e4d9ed701eda
title: 'Metodo IPortableDeviceValues:: SetIUnknownValue (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetIUnknownValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 2c3a27fe5ea89359884d70162000b5164b7c1aec
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326861"
---
# <a name="iportabledevicevaluessetiunknownvalue-method"></a><span data-ttu-id="8a3bc-103">Metodo IPortableDeviceValues:: SetIUnknownValue</span><span class="sxs-lookup"><span data-stu-id="8a3bc-103">IPortableDeviceValues::SetIUnknownValue method</span></span>

<span data-ttu-id="8a3bc-104">Il metodo **SetIUnknownValue** aggiunge un nuovo valore **IUnknown** (Type VT \_ Unknown) o ne sovrascrive uno esistente.</span><span class="sxs-lookup"><span data-stu-id="8a3bc-104">The **SetIUnknownValue** method adds a new **IUnknown** value (type VT\_UNKNOWN) or overwrites an existing one.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a3bc-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8a3bc-105">Syntax</span></span>


```C++
HRESULT SetIUnknownValue(
  [in] REFPROPERTYKEY key,
  [in] IUnknown       *pValue
);
```



## <a name="parameters"></a><span data-ttu-id="8a3bc-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="8a3bc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8a3bc-107">*chiave* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="8a3bc-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a3bc-108">Oggetto **REFPROPERTYKEY** che specifica l'elemento da creare o sovrascrivere.</span><span class="sxs-lookup"><span data-stu-id="8a3bc-108">A **REFPROPERTYKEY** that specifies the item to create or overwrite.</span></span>

</dd> <dt>

<span data-ttu-id="8a3bc-109">*pValue* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8a3bc-109">*pValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a3bc-110">Puntatore a un'interfaccia **IUnknown** che specifica il nuovo valore.</span><span class="sxs-lookup"><span data-stu-id="8a3bc-110">A pointer to an **IUnknown** interface that specifies the new value.</span></span> <span data-ttu-id="8a3bc-111">L'SDK copia un riferimento all'interfaccia inviata e chiama **AddRef** .</span><span class="sxs-lookup"><span data-stu-id="8a3bc-111">The SDK copies a reference to the submitted interface and calls **AddRef** on it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8a3bc-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8a3bc-112">Return value</span></span>

<span data-ttu-id="8a3bc-113">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="8a3bc-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="8a3bc-114">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="8a3bc-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="8a3bc-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="8a3bc-115">Return code</span></span>                                                                          | <span data-ttu-id="8a3bc-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8a3bc-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="8a3bc-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="8a3bc-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="8a3bc-118">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="8a3bc-118">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="8a3bc-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="8a3bc-119">Remarks</span></span>

<span data-ttu-id="8a3bc-120">Se un valore esistente ha la stessa chiave specificata dal parametro *Key* , sovrascrive il valore esistente senza alcun avviso.</span><span class="sxs-lookup"><span data-stu-id="8a3bc-120">If an existing value has the same key that is specified by the *key* parameter, it overwrites the existing value without any warning.</span></span> <span data-ttu-id="8a3bc-121">La memoria della chiave esistente viene rilasciata in modo appropriato.</span><span class="sxs-lookup"><span data-stu-id="8a3bc-121">The existing key memory is released appropriately.</span></span>

## <a name="requirements"></a><span data-ttu-id="8a3bc-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8a3bc-122">Requirements</span></span>



| <span data-ttu-id="8a3bc-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="8a3bc-123">Requirement</span></span> | <span data-ttu-id="8a3bc-124">Valore</span><span class="sxs-lookup"><span data-stu-id="8a3bc-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8a3bc-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8a3bc-125">Header</span></span><br/>  | <dl> <span data-ttu-id="8a3bc-126"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="8a3bc-126"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="8a3bc-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="8a3bc-127">Library</span></span><br/> | <dl> <span data-ttu-id="8a3bc-128"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8a3bc-128"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8a3bc-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8a3bc-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a3bc-130">**Interfaccia IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="8a3bc-130">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="8a3bc-131">**IPortableDeviceValues::GetIUnknownValue**</span><span class="sxs-lookup"><span data-stu-id="8a3bc-131">**IPortableDeviceValues::GetIUnknownValue**</span></span>](iportabledevicevalues-getiunknownvalue.md)
</dt> </dl>

 

 




