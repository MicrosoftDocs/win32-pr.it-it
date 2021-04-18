---
description: Il metodo SetSignedIntegerValue aggiunge un nuovo valore LONG (tipo VT \_ I4) o sovrascrive uno esistente.
ms.assetid: b0bb2992-2906-446c-be9a-20bff13f8e1d
title: 'Metodo IPortableDeviceValues:: SetSignedIntegerValue (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetSignedIntegerValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 26a5d01ec69203c39008de394e3693acc833d262
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326857"
---
# <a name="iportabledevicevaluessetsignedintegervalue-method"></a><span data-ttu-id="3951a-103">Metodo IPortableDeviceValues:: SetSignedIntegerValue</span><span class="sxs-lookup"><span data-stu-id="3951a-103">IPortableDeviceValues::SetSignedIntegerValue method</span></span>

<span data-ttu-id="3951a-104">Il metodo **SetSignedIntegerValue** aggiunge un nuovo valore **Long** (tipo VT \_ I4) o sovrascrive uno esistente.</span><span class="sxs-lookup"><span data-stu-id="3951a-104">The **SetSignedIntegerValue** method adds a new **LONG** value (type VT\_I4) or overwrites an existing one.</span></span>

## <a name="syntax"></a><span data-ttu-id="3951a-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3951a-105">Syntax</span></span>


```C++
HRESULT SetSignedIntegerValue(
  [in]       REFPROPERTYKEY key,
  [in] const LONG           Value
);
```



## <a name="parameters"></a><span data-ttu-id="3951a-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="3951a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3951a-107">*chiave* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="3951a-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3951a-108">Oggetto **REFPROPERTYKEY** che specifica l'elemento da creare o sovrascrivere.</span><span class="sxs-lookup"><span data-stu-id="3951a-108">A **REFPROPERTYKEY** that specifies the item to create or overwrite.</span></span>

</dd> <dt>

<span data-ttu-id="3951a-109">*Valore* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="3951a-109">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3951a-110">Oggetto **Long** che specifica il nuovo valore.</span><span class="sxs-lookup"><span data-stu-id="3951a-110">A **LONG** that specifies the new value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3951a-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3951a-111">Return value</span></span>

<span data-ttu-id="3951a-112">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="3951a-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="3951a-113">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="3951a-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="3951a-114">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="3951a-114">Return code</span></span>                                                                          | <span data-ttu-id="3951a-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3951a-115">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="3951a-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="3951a-116"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="3951a-117">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="3951a-117">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="3951a-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="3951a-118">Remarks</span></span>

<span data-ttu-id="3951a-119">Se un valore esistente ha la stessa chiave specificata dal parametro *Key* , sovrascrive il valore esistente senza alcun avviso.</span><span class="sxs-lookup"><span data-stu-id="3951a-119">If an existing value has the same key that is specified by the *key* parameter, it overwrites the existing value without any warning.</span></span>

## <a name="requirements"></a><span data-ttu-id="3951a-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3951a-120">Requirements</span></span>



| <span data-ttu-id="3951a-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="3951a-121">Requirement</span></span> | <span data-ttu-id="3951a-122">Valore</span><span class="sxs-lookup"><span data-stu-id="3951a-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3951a-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3951a-123">Header</span></span><br/>  | <dl> <span data-ttu-id="3951a-124"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="3951a-124"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="3951a-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="3951a-125">Library</span></span><br/> | <dl> <span data-ttu-id="3951a-126"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3951a-126"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3951a-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3951a-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3951a-128">**Interfaccia IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="3951a-128">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="3951a-129">**IPortableDeviceValues::GetSignedIntegerValue**</span><span class="sxs-lookup"><span data-stu-id="3951a-129">**IPortableDeviceValues::GetSignedIntegerValue**</span></span>](iportabledevicevalues-getsignedintegervalue.md)
</dt> </dl>

 

 




