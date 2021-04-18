---
description: Il metodo SetBufferValue aggiunge un nuovo \* valore byte (Type VT \_ vector \| VT \_ Ui1) o ne sovrascrive uno esistente.
ms.assetid: 6c421240-2ff8-4862-bd90-1feee5d15a8d
title: 'Metodo IPortableDeviceValues:: SetBufferValue (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetBufferValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: e04b41fdd397d8d03e7e0576d2ba8fb3b6ad1401
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330435"
---
# <a name="iportabledevicevaluessetbuffervalue-method"></a><span data-ttu-id="ca945-103">Metodo IPortableDeviceValues:: SetBufferValue</span><span class="sxs-lookup"><span data-stu-id="ca945-103">IPortableDeviceValues::SetBufferValue method</span></span>

<span data-ttu-id="ca945-104">Il metodo **SetBufferValue** aggiunge un nuovo valore **byte** \* (Type VT \_ vector \| VT \_ Ui1) o ne sovrascrive uno esistente.</span><span class="sxs-lookup"><span data-stu-id="ca945-104">The **SetBufferValue** method adds a new **BYTE**\* value (type VT\_VECTOR \| VT\_UI1) or overwrites an existing one.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca945-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ca945-105">Syntax</span></span>


```C++
HRESULT SetBufferValue(
  [in] REFPROPERTYKEY key,
  [in] BYTE           *pValue,
  [in] DWORD          cbValue
);
```



## <a name="parameters"></a><span data-ttu-id="ca945-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="ca945-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ca945-107">*chiave* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="ca945-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ca945-108">Oggetto **REFPROPERTYKEY** che specifica l'elemento da creare o sovrascrivere.</span><span class="sxs-lookup"><span data-stu-id="ca945-108">A **REFPROPERTYKEY** that specifies the item to create or overwrite.</span></span>

</dd> <dt>

<span data-ttu-id="ca945-109">*pValue* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ca945-109">*pValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ca945-110">**Byte \*** che contiene i dati da scrivere nell'elemento.</span><span class="sxs-lookup"><span data-stu-id="ca945-110">A **BYTE\*** that contains the data to write to the item.</span></span> <span data-ttu-id="ca945-111">I dati del buffer inviati vengono copiati nell'interfaccia, quindi il chiamante può liberare il buffer dopo aver effettuato la chiamata.</span><span class="sxs-lookup"><span data-stu-id="ca945-111">The submitted buffer data is copied to the interface, so the caller can free this buffer after making this call.</span></span>

</dd> <dt>

<span data-ttu-id="ca945-112">*cbValue* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ca945-112">*cbValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ca945-113">Dimensioni del valore a cui punta *pValue* in byte.</span><span class="sxs-lookup"><span data-stu-id="ca945-113">The size of the value pointed to by *pValue*, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ca945-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ca945-114">Return value</span></span>

<span data-ttu-id="ca945-115">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="ca945-115">The method returns an **HRESULT**.</span></span> <span data-ttu-id="ca945-116">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="ca945-116">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="ca945-117">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="ca945-117">Return code</span></span>                                                                          | <span data-ttu-id="ca945-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ca945-118">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="ca945-119"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="ca945-119"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="ca945-120">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="ca945-120">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ca945-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="ca945-121">Remarks</span></span>

<span data-ttu-id="ca945-122">Se un valore esistente ha la stessa chiave specificata dal parametro *Key* , sovrascrive il valore esistente senza alcun avviso.</span><span class="sxs-lookup"><span data-stu-id="ca945-122">If an existing value has the same key that is specified by the *key* parameter, it overwrites the existing value without any warning.</span></span> <span data-ttu-id="ca945-123">La memoria della chiave esistente viene rilasciata in modo appropriato.</span><span class="sxs-lookup"><span data-stu-id="ca945-123">The existing key memory is released appropriately.</span></span>

<span data-ttu-id="ca945-124">L'impostazione di un buffer di dimensioni **null** o zero non è supportata.</span><span class="sxs-lookup"><span data-stu-id="ca945-124">Setting a **NULL** or a zero-sized buffer is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="ca945-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ca945-125">Requirements</span></span>



| <span data-ttu-id="ca945-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="ca945-126">Requirement</span></span> | <span data-ttu-id="ca945-127">Valore</span><span class="sxs-lookup"><span data-stu-id="ca945-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca945-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ca945-128">Header</span></span><br/>  | <dl> <span data-ttu-id="ca945-129"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="ca945-129"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="ca945-130">Libreria</span><span class="sxs-lookup"><span data-stu-id="ca945-130">Library</span></span><br/> | <dl> <span data-ttu-id="ca945-131"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ca945-131"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ca945-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ca945-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca945-133">**Interfaccia IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="ca945-133">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="ca945-134">**IPortableDeviceValues::GetBufferValue**</span><span class="sxs-lookup"><span data-stu-id="ca945-134">**IPortableDeviceValues::GetBufferValue**</span></span>](iportabledevicevalues-getbuffervalue.md)
</dt> </dl>

 

 




