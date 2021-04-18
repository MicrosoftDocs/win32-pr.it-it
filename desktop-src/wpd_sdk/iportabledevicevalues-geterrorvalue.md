---
description: Il metodo GetErrorValue recupera un valore HRESULT (tipo \_ errore VT) specificato da una chiave.
ms.assetid: af57ddbd-5503-4b9b-bd75-ba9c9c202b73
title: 'Metodo IPortableDeviceValues:: GetErrorValue (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetErrorValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 86e5dacfa398cfe2bb57bfd289e4c8e792f14a66
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328187"
---
# <a name="iportabledevicevaluesgeterrorvalue-method"></a><span data-ttu-id="61cba-103">Metodo IPortableDeviceValues:: GetErrorValue</span><span class="sxs-lookup"><span data-stu-id="61cba-103">IPortableDeviceValues::GetErrorValue method</span></span>

<span data-ttu-id="61cba-104">Il metodo **GetErrorValue** recupera un valore **HRESULT** (tipo \_ errore VT) specificato da una chiave.</span><span class="sxs-lookup"><span data-stu-id="61cba-104">The **GetErrorValue** method retrieves an **HRESULT** value (type VT\_ERROR) specified by a key.</span></span>

## <a name="syntax"></a><span data-ttu-id="61cba-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="61cba-105">Syntax</span></span>


```C++
HRESULT GetErrorValue(
  [in]  REFPROPERTYKEY key,
  [out] HRESULT        *pValue
);
```



## <a name="parameters"></a><span data-ttu-id="61cba-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="61cba-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="61cba-107">*chiave* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="61cba-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="61cba-108">Chiave **REFPROPERTYKEY** che specifica l'elemento da recuperare.</span><span class="sxs-lookup"><span data-stu-id="61cba-108">A **REFPROPERTYKEY** key that specifies the item to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="61cba-109">*pValue* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="61cba-109">*pValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="61cba-110">Puntatore al valore **HRESULT** recuperato.</span><span class="sxs-lookup"><span data-stu-id="61cba-110">Pointer to the retrieved **HRESULT** value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="61cba-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="61cba-111">Return value</span></span>

<span data-ttu-id="61cba-112">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="61cba-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="61cba-113">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="61cba-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="61cba-114">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="61cba-114">Return code</span></span>                                                                                                            | <span data-ttu-id="61cba-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="61cba-115">Description</span></span>                                                            |
|------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <span data-ttu-id="61cba-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="61cba-116"><dt>**S\_OK**</dt></span></span> </dl>                                   | <span data-ttu-id="61cba-117">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="61cba-117">The method succeeded.</span></span><br/>                                       |
| <dl> <span data-ttu-id="61cba-118"><dt>**DISP \_ E \_ TYPEMISMATCH**</dt></span><span class="sxs-lookup"><span data-stu-id="61cba-118"><dt>**DISP\_E\_TYPEMISMATCH**</dt></span></span> </dl>                   | <span data-ttu-id="61cba-119">La proprietà specificata da *Key* non è un tipo **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="61cba-119">The property specified by *key* is not an **HRESULT** type.</span></span><br/> |
| <dl> <span data-ttu-id="61cba-120"><dt>**HRESULT \_ da \_ Win32 (errore \_ non \_ trovato)**</dt></span><span class="sxs-lookup"><span data-stu-id="61cba-120"><dt>**HRESULT\_FROM\_WIN32(ERROR\_NOT\_FOUND)**</dt></span></span> </dl> | <span data-ttu-id="61cba-121">La proprietà specificata dalla *chiave* non è presente nella raccolta.</span><span class="sxs-lookup"><span data-stu-id="61cba-121">The property specified by *key* is not in the collection.</span></span><br/>   |



 

## <a name="requirements"></a><span data-ttu-id="61cba-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="61cba-122">Requirements</span></span>



| <span data-ttu-id="61cba-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="61cba-123">Requirement</span></span> | <span data-ttu-id="61cba-124">Valore</span><span class="sxs-lookup"><span data-stu-id="61cba-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="61cba-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="61cba-125">Header</span></span><br/>  | <dl> <span data-ttu-id="61cba-126"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="61cba-126"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="61cba-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="61cba-127">Library</span></span><br/> | <dl> <span data-ttu-id="61cba-128"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="61cba-128"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="61cba-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="61cba-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61cba-130">**Interfaccia IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="61cba-130">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="61cba-131">**IPortableDeviceValues::SetErrorValue**</span><span class="sxs-lookup"><span data-stu-id="61cba-131">**IPortableDeviceValues::SetErrorValue**</span></span>](iportabledevicevalues-seterrorvalue.md)
</dt> </dl>

 

 




