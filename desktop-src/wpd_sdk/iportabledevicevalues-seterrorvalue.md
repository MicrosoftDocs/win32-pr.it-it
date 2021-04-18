---
description: Il metodo SetErrorValue aggiunge un nuovo valore HRESULT (tipo \_ errore VT) o sovrascrive uno esistente.
ms.assetid: 87369791-42bd-4523-b15a-acf0ea1e5af8
title: 'Metodo IPortableDeviceValues:: SetErrorValue (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetErrorValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 19c7ca57d325e31fd9cd8e0bf5130dc594b0b8cd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330434"
---
# <a name="iportabledevicevaluesseterrorvalue-method"></a><span data-ttu-id="f6a12-103">Metodo IPortableDeviceValues:: SetErrorValue</span><span class="sxs-lookup"><span data-stu-id="f6a12-103">IPortableDeviceValues::SetErrorValue method</span></span>

<span data-ttu-id="f6a12-104">Il metodo **SetErrorValue** aggiunge un nuovo valore **HRESULT** (tipo \_ errore VT) o sovrascrive uno esistente.</span><span class="sxs-lookup"><span data-stu-id="f6a12-104">The **SetErrorValue** method adds a new **HRESULT** value (type VT\_ERROR) or overwrites an existing one.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6a12-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f6a12-105">Syntax</span></span>


```C++
HRESULT SetErrorValue(
  [in]       REFPROPERTYKEY key,
  [in] const HRESULT        Value
);
```



## <a name="parameters"></a><span data-ttu-id="f6a12-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="f6a12-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f6a12-107">*chiave* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="f6a12-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f6a12-108">Oggetto **REFPROPERTYKEY** che specifica l'elemento da creare o sovrascrivere.</span><span class="sxs-lookup"><span data-stu-id="f6a12-108">A **REFPROPERTYKEY** that specifies the item to create or overwrite.</span></span>

</dd> <dt>

<span data-ttu-id="f6a12-109">*Valore* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="f6a12-109">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f6a12-110">**HRESULT** che contiene il nuovo valore.</span><span class="sxs-lookup"><span data-stu-id="f6a12-110">An **HRESULT** that contains the new value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f6a12-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f6a12-111">Return value</span></span>

<span data-ttu-id="f6a12-112">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="f6a12-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="f6a12-113">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="f6a12-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="f6a12-114">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="f6a12-114">Return code</span></span>                                                                          | <span data-ttu-id="f6a12-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f6a12-115">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="f6a12-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="f6a12-116"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="f6a12-117">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="f6a12-117">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f6a12-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="f6a12-118">Remarks</span></span>

<span data-ttu-id="f6a12-119">Se un valore esistente ha la stessa chiave specificata dal parametro *Key* , sovrascrive il valore esistente senza alcun avviso.</span><span class="sxs-lookup"><span data-stu-id="f6a12-119">If an existing value has the same key specified by the *key* parameter, it overwrites the existing value without any warning.</span></span>

## <a name="requirements"></a><span data-ttu-id="f6a12-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f6a12-120">Requirements</span></span>



| <span data-ttu-id="f6a12-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="f6a12-121">Requirement</span></span> | <span data-ttu-id="f6a12-122">Valore</span><span class="sxs-lookup"><span data-stu-id="f6a12-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f6a12-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f6a12-123">Header</span></span><br/>  | <dl> <span data-ttu-id="f6a12-124"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="f6a12-124"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="f6a12-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="f6a12-125">Library</span></span><br/> | <dl> <span data-ttu-id="f6a12-126"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f6a12-126"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f6a12-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f6a12-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6a12-128">**Interfaccia IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="f6a12-128">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="f6a12-129">**IPortableDeviceValues::GetErrorValue**</span><span class="sxs-lookup"><span data-stu-id="f6a12-129">**IPortableDeviceValues::GetErrorValue**</span></span>](iportabledevicevalues-geterrorvalue.md)
</dt> </dl>

 

 




