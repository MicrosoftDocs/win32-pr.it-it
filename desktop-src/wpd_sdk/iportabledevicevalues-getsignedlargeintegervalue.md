---
description: Il metodo GetSignedLargeIntegerValue recupera un valore LONGLONG (di tipo VT \_ I8) specificato da una chiave.
ms.assetid: b8d2a0b6-7ca3-4a56-a502-cc18b08df22a
title: 'Metodo IPortableDeviceValues:: GetSignedLargeIntegerValue (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetSignedLargeIntegerValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 5fc41c263ffdef540300a08f88665a6489fa9d41
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330583"
---
# <a name="iportabledevicevaluesgetsignedlargeintegervalue-method"></a><span data-ttu-id="9e062-103">Metodo IPortableDeviceValues:: GetSignedLargeIntegerValue</span><span class="sxs-lookup"><span data-stu-id="9e062-103">IPortableDeviceValues::GetSignedLargeIntegerValue method</span></span>

<span data-ttu-id="9e062-104">Il metodo **GetSignedLargeIntegerValue** recupera un valore **LONGLONG** (di tipo VT \_ I8) specificato da una chiave.</span><span class="sxs-lookup"><span data-stu-id="9e062-104">The **GetSignedLargeIntegerValue** method retrieves a **LONGLONG** value (type VT\_I8) specified by a key.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e062-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9e062-105">Syntax</span></span>


```C++
HRESULT GetSignedLargeIntegerValue(
  [in]  REFPROPERTYKEY key,
  [out] LONGLONG       *pValue
);
```



## <a name="parameters"></a><span data-ttu-id="9e062-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="9e062-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9e062-107">*chiave* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="9e062-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9e062-108">Chiave **REFPROPERTYKEY** che specifica l'elemento da recuperare.</span><span class="sxs-lookup"><span data-stu-id="9e062-108">A **REFPROPERTYKEY** key that specifies the item to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="9e062-109">*pValue* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="9e062-109">*pValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9e062-110">Puntatore al valore **ULONG** recuperato.</span><span class="sxs-lookup"><span data-stu-id="9e062-110">Pointer to the retrieved **ULONG** value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9e062-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9e062-111">Return value</span></span>

<span data-ttu-id="9e062-112">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="9e062-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="9e062-113">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="9e062-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="9e062-114">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="9e062-114">Return code</span></span>                                                                                                            | <span data-ttu-id="9e062-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9e062-115">Description</span></span>                                                            |
|------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <span data-ttu-id="9e062-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="9e062-116"><dt>**S\_OK**</dt></span></span> </dl>                                   | <span data-ttu-id="9e062-117">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="9e062-117">The method succeeded.</span></span><br/>                                       |
| <dl> <span data-ttu-id="9e062-118"><dt>**DISP \_ E \_ TYPEMISMATCH**</dt></span><span class="sxs-lookup"><span data-stu-id="9e062-118"><dt>**DISP\_E\_TYPEMISMATCH**</dt></span></span> </dl>                   | <span data-ttu-id="9e062-119">La proprietà specificata da *Key* non è di tipo **LONGLONG** .</span><span class="sxs-lookup"><span data-stu-id="9e062-119">The property specified by *key* is not a **LONGLONG** type.</span></span><br/> |
| <dl> <span data-ttu-id="9e062-120"><dt>**HRESULT \_ da \_ Win32 (errore \_ non \_ trovato)**</dt></span><span class="sxs-lookup"><span data-stu-id="9e062-120"><dt>**HRESULT\_FROM\_WIN32(ERROR\_NOT\_FOUND)**</dt></span></span> </dl> | <span data-ttu-id="9e062-121">La proprietà specificata dalla *chiave* non è presente nella raccolta.</span><span class="sxs-lookup"><span data-stu-id="9e062-121">The property specified by *key* is not in the collection.</span></span><br/>   |



 

## <a name="requirements"></a><span data-ttu-id="9e062-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9e062-122">Requirements</span></span>



| <span data-ttu-id="9e062-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="9e062-123">Requirement</span></span> | <span data-ttu-id="9e062-124">Valore</span><span class="sxs-lookup"><span data-stu-id="9e062-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9e062-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9e062-125">Header</span></span><br/>  | <dl> <span data-ttu-id="9e062-126"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="9e062-126"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="9e062-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="9e062-127">Library</span></span><br/> | <dl> <span data-ttu-id="9e062-128"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9e062-128"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9e062-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9e062-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e062-130">**Interfaccia IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="9e062-130">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="9e062-131">**IPortableDeviceValues::SetSignedLargeIntegerValue**</span><span class="sxs-lookup"><span data-stu-id="9e062-131">**IPortableDeviceValues::SetSignedLargeIntegerValue**</span></span>](iportabledevicevalues-setsignedlargeintegervalue.md)
</dt> </dl>

 

 




