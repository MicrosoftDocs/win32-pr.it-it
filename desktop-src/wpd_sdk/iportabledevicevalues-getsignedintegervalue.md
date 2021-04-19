---
description: Il metodo GetSignedIntegerValue recupera un valore LONG (tipo VT \_ I4) specificato da una chiave.
ms.assetid: d2291a64-d0b3-4a30-a37c-2b6cd9880a11
title: 'Metodo IPortableDeviceValues:: GetSignedIntegerValue (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetSignedIntegerValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: f2fe0c2f8714d3fa28f61624924eba169f9f1c5d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333219"
---
# <a name="iportabledevicevaluesgetsignedintegervalue-method"></a><span data-ttu-id="be6fe-103">Metodo IPortableDeviceValues:: GetSignedIntegerValue</span><span class="sxs-lookup"><span data-stu-id="be6fe-103">IPortableDeviceValues::GetSignedIntegerValue method</span></span>

<span data-ttu-id="be6fe-104">Il metodo **GetSignedIntegerValue** recupera un valore **Long** (tipo VT \_ I4) specificato da una chiave.</span><span class="sxs-lookup"><span data-stu-id="be6fe-104">The **GetSignedIntegerValue** method retrieves a **LONG** value (type VT\_I4) specified by a key.</span></span>

## <a name="syntax"></a><span data-ttu-id="be6fe-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="be6fe-105">Syntax</span></span>


```C++
HRESULT GetSignedIntegerValue(
  [in]  REFPROPERTYKEY key,
  [out] LONG           *pValue
);
```



## <a name="parameters"></a><span data-ttu-id="be6fe-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="be6fe-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be6fe-107">*chiave* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="be6fe-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be6fe-108">Chiave **REFPROPERTYKEY** che specifica l'elemento da recuperare.</span><span class="sxs-lookup"><span data-stu-id="be6fe-108">A **REFPROPERTYKEY** key that specifies the item to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="be6fe-109">*pValue* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="be6fe-109">*pValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="be6fe-110">Puntatore al valore **Long** recuperato.</span><span class="sxs-lookup"><span data-stu-id="be6fe-110">Pointer to the retrieved **LONG** value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="be6fe-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="be6fe-111">Return value</span></span>

<span data-ttu-id="be6fe-112">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="be6fe-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="be6fe-113">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="be6fe-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="be6fe-114">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="be6fe-114">Return code</span></span>                                                                                                            | <span data-ttu-id="be6fe-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="be6fe-115">Description</span></span>                                                          |
|------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <dl> <span data-ttu-id="be6fe-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="be6fe-116"><dt>**S\_OK**</dt></span></span> </dl>                                   | <span data-ttu-id="be6fe-117">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="be6fe-117">The method succeeded.</span></span><br/>                                     |
| <dl> <span data-ttu-id="be6fe-118"><dt>**DISP \_ E \_ TYPEMISMATCH**</dt></span><span class="sxs-lookup"><span data-stu-id="be6fe-118"><dt>**DISP\_E\_TYPEMISMATCH**</dt></span></span> </dl>                   | <span data-ttu-id="be6fe-119">La proprietà specificata da *Key* non è di tipo **Long** .</span><span class="sxs-lookup"><span data-stu-id="be6fe-119">The property specified by *key* is not a **LONG** type.</span></span><br/>   |
| <dl> <span data-ttu-id="be6fe-120"><dt>**HRESULT \_ da \_ Win32 (errore \_ non \_ trovato)**</dt></span><span class="sxs-lookup"><span data-stu-id="be6fe-120"><dt>**HRESULT\_FROM\_WIN32(ERROR\_NOT\_FOUND)**</dt></span></span> </dl> | <span data-ttu-id="be6fe-121">La proprietà specificata dalla *chiave* non è presente nella raccolta.</span><span class="sxs-lookup"><span data-stu-id="be6fe-121">The property specified by *key* is not in the collection.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="be6fe-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="be6fe-122">Requirements</span></span>



| <span data-ttu-id="be6fe-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="be6fe-123">Requirement</span></span> | <span data-ttu-id="be6fe-124">Valore</span><span class="sxs-lookup"><span data-stu-id="be6fe-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="be6fe-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="be6fe-125">Header</span></span><br/>  | <dl> <span data-ttu-id="be6fe-126"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="be6fe-126"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="be6fe-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="be6fe-127">Library</span></span><br/> | <dl> <span data-ttu-id="be6fe-128"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="be6fe-128"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="be6fe-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="be6fe-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be6fe-130">**Interfaccia IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="be6fe-130">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="be6fe-131">**IPortableDeviceValues::SetSignedIntegerValue**</span><span class="sxs-lookup"><span data-stu-id="be6fe-131">**IPortableDeviceValues::SetSignedIntegerValue**</span></span>](iportabledevicevalues-setsignedintegervalue.md)
</dt> </dl>

 

 




