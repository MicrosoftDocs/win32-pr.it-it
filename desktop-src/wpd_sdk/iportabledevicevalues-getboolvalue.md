---
description: Il metodo GetBoolValue recupera un valore booleano (tipo VT \_ bool) specificato da una chiave.
ms.assetid: cb5fed7a-50b5-4af1-806a-c6582409d265
title: 'Metodo IPortableDeviceValues:: GetBoolValue (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetBoolValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 8554fc30a1b66226f6e4f8de4e5d8ac0e8abfabf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326959"
---
# <a name="iportabledevicevaluesgetboolvalue-method"></a><span data-ttu-id="a57a6-103">Metodo IPortableDeviceValues:: GetBoolValue</span><span class="sxs-lookup"><span data-stu-id="a57a6-103">IPortableDeviceValues::GetBoolValue method</span></span>

<span data-ttu-id="a57a6-104">Il metodo **GetBoolValue** recupera un valore **booleano** (tipo VT \_ bool) specificato da una chiave.</span><span class="sxs-lookup"><span data-stu-id="a57a6-104">The **GetBoolValue** method retrieves a **Boolean** value (type VT\_BOOL) specified by a key.</span></span>

## <a name="syntax"></a><span data-ttu-id="a57a6-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a57a6-105">Syntax</span></span>


```C++
HRESULT GetBoolValue(
  [in]  REFPROPERTYKEY key,
  [out] BOOL           *pValue
);
```



## <a name="parameters"></a><span data-ttu-id="a57a6-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a57a6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a57a6-107">*chiave* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="a57a6-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a57a6-108">Chiave **REFPROPERTYKEY** che specifica l'elemento da recuperare.</span><span class="sxs-lookup"><span data-stu-id="a57a6-108">A **REFPROPERTYKEY** key that specifies the item to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="a57a6-109">*pValue* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="a57a6-109">*pValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a57a6-110">Puntatore al valore **bool** recuperato.</span><span class="sxs-lookup"><span data-stu-id="a57a6-110">Pointer to the retrieved **BOOL** value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a57a6-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a57a6-111">Return value</span></span>

<span data-ttu-id="a57a6-112">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="a57a6-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="a57a6-113">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="a57a6-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="a57a6-114">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="a57a6-114">Return code</span></span>                                                                                                            | <span data-ttu-id="a57a6-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a57a6-115">Description</span></span>                                                          |
|------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <dl> <span data-ttu-id="a57a6-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="a57a6-116"><dt>**S\_OK**</dt></span></span> </dl>                                   | <span data-ttu-id="a57a6-117">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="a57a6-117">The method succeeded.</span></span><br/>                                     |
| <dl> <span data-ttu-id="a57a6-118"><dt>**DISP \_ E \_ TYPEMISMATCH**</dt></span><span class="sxs-lookup"><span data-stu-id="a57a6-118"><dt>**DISP\_E\_TYPEMISMATCH**</dt></span></span> </dl>                   | <span data-ttu-id="a57a6-119">La proprietà specificata da *Key* non è di tipo **bool** .</span><span class="sxs-lookup"><span data-stu-id="a57a6-119">The property specified by *key* is not a **BOOL** type.</span></span><br/>   |
| <dl> <span data-ttu-id="a57a6-120"><dt>**HRESULT \_ da \_ Win32 (errore \_ non \_ trovato)**</dt></span><span class="sxs-lookup"><span data-stu-id="a57a6-120"><dt>**HRESULT\_FROM\_WIN32(ERROR\_NOT\_FOUND)**</dt></span></span> </dl> | <span data-ttu-id="a57a6-121">La proprietà specificata dalla *chiave* non è presente nella raccolta.</span><span class="sxs-lookup"><span data-stu-id="a57a6-121">The property specified by *key* is not in the collection.</span></span><br/> |



 

## <a name="examples"></a><span data-ttu-id="a57a6-122">Esempio</span><span class="sxs-lookup"><span data-stu-id="a57a6-122">Examples</span></span>

<span data-ttu-id="a57a6-123">Per un esempio di come usare questo metodo, vedere [impostazione delle proprietà per un singolo oggetto](setting-properties-for-a-single-object.md).</span><span class="sxs-lookup"><span data-stu-id="a57a6-123">For an example of how to use this method, see [Setting Properties for a Single Object](setting-properties-for-a-single-object.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a57a6-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a57a6-124">Requirements</span></span>



| <span data-ttu-id="a57a6-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="a57a6-125">Requirement</span></span> | <span data-ttu-id="a57a6-126">Valore</span><span class="sxs-lookup"><span data-stu-id="a57a6-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a57a6-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a57a6-127">Header</span></span><br/>  | <dl> <span data-ttu-id="a57a6-128"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="a57a6-128"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="a57a6-129">Libreria</span><span class="sxs-lookup"><span data-stu-id="a57a6-129">Library</span></span><br/> | <dl> <span data-ttu-id="a57a6-130"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a57a6-130"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a57a6-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a57a6-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a57a6-132">**Interfaccia IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="a57a6-132">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="a57a6-133">**IPortableDeviceValues:: SetBoolValue**</span><span class="sxs-lookup"><span data-stu-id="a57a6-133">**IPortableDeviceValues::SetBoolValue**</span></span>](iportabledevicevalues-setboolvalue.md)
</dt> <dt>

[<span data-ttu-id="a57a6-134">Recupero degli eventi del servizio supportati</span><span class="sxs-lookup"><span data-stu-id="a57a6-134">Retrieving Supported Service Events</span></span>](retrieving-supported-events.md)
</dt> <dt>

[<span data-ttu-id="a57a6-135">Impostazione delle proprietà per un singolo oggetto</span><span class="sxs-lookup"><span data-stu-id="a57a6-135">Setting Properties for a Single Object</span></span>](setting-properties-for-a-single-object.md)
</dt> <dt>

[<span data-ttu-id="a57a6-136">Scrittura di proprietà di contenuto-oggetto</span><span class="sxs-lookup"><span data-stu-id="a57a6-136">Writing Content-Object Properties</span></span>](writing-content-object-properties.md)
</dt> </dl>

 

 




