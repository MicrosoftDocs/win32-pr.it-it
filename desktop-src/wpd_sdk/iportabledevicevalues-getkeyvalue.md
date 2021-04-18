---
description: Il metodo GetKeyValue recupera un valore PROPERTYKEY specificato da una chiave.
ms.assetid: 2c92b1c0-3ea6-4a14-8b63-d57752b649b8
title: 'Metodo IPortableDeviceValues:: GetKeyValue (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetKeyValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 3d5080a35faa5555d2813c6e419a1965def05bdd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327262"
---
# <a name="iportabledevicevaluesgetkeyvalue-method"></a><span data-ttu-id="b7082-103">Metodo IPortableDeviceValues:: GetKeyValue</span><span class="sxs-lookup"><span data-stu-id="b7082-103">IPortableDeviceValues::GetKeyValue method</span></span>

<span data-ttu-id="b7082-104">Il metodo **GetKeyValue** recupera un valore **PropertyKey** specificato da una chiave.</span><span class="sxs-lookup"><span data-stu-id="b7082-104">The **GetKeyValue** method retrieves a **PROPERTYKEY** value specified by a key.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7082-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b7082-105">Syntax</span></span>


```C++
HRESULT GetKeyValue(
  [in]  REFPROPERTYKEY key,
  [out] PROPERTYKEY    *pValue
);
```



## <a name="parameters"></a><span data-ttu-id="b7082-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b7082-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b7082-107">*chiave* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="b7082-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7082-108">Chiave **REFPROPERTYKEY** che specifica l'elemento da recuperare.</span><span class="sxs-lookup"><span data-stu-id="b7082-108">A **REFPROPERTYKEY** key that specifies the item to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="b7082-109">*pValue* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="b7082-109">*pValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b7082-110">Puntatore al valore **PropertyKey** recuperato.</span><span class="sxs-lookup"><span data-stu-id="b7082-110">Pointer to the retrieved **PROPERTYKEY** value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b7082-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b7082-111">Return value</span></span>

<span data-ttu-id="b7082-112">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="b7082-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="b7082-113">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="b7082-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="b7082-114">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="b7082-114">Return code</span></span>                                                                                                            | <span data-ttu-id="b7082-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b7082-115">Description</span></span>                                                               |
|------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b7082-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="b7082-116"><dt>**S\_OK**</dt></span></span> </dl>                                   | <span data-ttu-id="b7082-117">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="b7082-117">The method succeeded.</span></span><br/>                                          |
| <dl> <span data-ttu-id="b7082-118"><dt>**DISP \_ E \_ TYPEMISMATCH**</dt></span><span class="sxs-lookup"><span data-stu-id="b7082-118"><dt>**DISP\_E\_TYPEMISMATCH**</dt></span></span> </dl>                   | <span data-ttu-id="b7082-119">La proprietà specificata da *Key* non è di tipo **PropertyKey** .</span><span class="sxs-lookup"><span data-stu-id="b7082-119">The property specified by *key* is not a **PROPERTYKEY** type.</span></span><br/> |
| <dl> <span data-ttu-id="b7082-120"><dt>**HRESULT \_ da \_ Win32 (errore \_ non \_ trovato)**</dt></span><span class="sxs-lookup"><span data-stu-id="b7082-120"><dt>**HRESULT\_FROM\_WIN32(ERROR\_NOT\_FOUND)**</dt></span></span> </dl> | <span data-ttu-id="b7082-121">La proprietà specificata dalla *chiave* non è presente nella raccolta.</span><span class="sxs-lookup"><span data-stu-id="b7082-121">The property specified by *key* is not in the collection.</span></span><br/>      |



 

## <a name="requirements"></a><span data-ttu-id="b7082-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b7082-122">Requirements</span></span>



| <span data-ttu-id="b7082-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="b7082-123">Requirement</span></span> | <span data-ttu-id="b7082-124">Valore</span><span class="sxs-lookup"><span data-stu-id="b7082-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b7082-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b7082-125">Header</span></span><br/>  | <dl> <span data-ttu-id="b7082-126"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="b7082-126"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="b7082-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="b7082-127">Library</span></span><br/> | <dl> <span data-ttu-id="b7082-128"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b7082-128"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b7082-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b7082-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7082-130">**Interfaccia IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="b7082-130">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="b7082-131">**IPortableDeviceValues::SetKeyValue**</span><span class="sxs-lookup"><span data-stu-id="b7082-131">**IPortableDeviceValues::SetKeyValue**</span></span>](iportabledevicevalues-setkeyvalue.md)
</dt> </dl>

 

 




