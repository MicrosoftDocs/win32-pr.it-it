---
description: Crea una copia dell'interfaccia IEnumPortableDeviceConnectors corrente.
ms.assetid: 64274cb0-1f57-481d-914f-41238cbe2f1b
title: 'Metodo IEnumPortableDeviceConnectors:: Clone (Devpkey. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPortableDeviceConnectors.Clone
api_type:
- COM
api_location:
- PortableDeviceGuids.lib
- PortableDeviceGuids.dll
ms.openlocfilehash: 0e5273f1c400732c94c7c63918787f5e130a854d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348566"
---
# <a name="ienumportabledeviceconnectorsclone-method"></a><span data-ttu-id="73f16-103">Metodo IEnumPortableDeviceConnectors:: Clone</span><span class="sxs-lookup"><span data-stu-id="73f16-103">IEnumPortableDeviceConnectors::Clone method</span></span>

<span data-ttu-id="73f16-104">Il metodo **Clone** crea una copia dell'interfaccia [**IEnumPortableDeviceConnectors**](ienumportabledeviceconnectors.md) corrente.</span><span class="sxs-lookup"><span data-stu-id="73f16-104">The **Clone** method creates a copy of the current [**IEnumPortableDeviceConnectors**](ienumportabledeviceconnectors.md) interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="73f16-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="73f16-105">Syntax</span></span>


```C++
HRESULT Clone(
  [out] IEnumPortableDeviceConnectors **ppEnum
);
```



## <a name="parameters"></a><span data-ttu-id="73f16-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="73f16-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="73f16-107">*ppEnum* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="73f16-107">*ppEnum* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="73f16-108">Indirizzo di un puntatore a un'interfaccia [**IEnumPortableDeviceConnectors**](ienumportabledeviceconnectors.md) .</span><span class="sxs-lookup"><span data-stu-id="73f16-108">The address of a pointer to an [**IEnumPortableDeviceConnectors**](ienumportabledeviceconnectors.md) interface.</span></span> <span data-ttu-id="73f16-109">L'applicazione chiamante deve rilasciare questa interfaccia quando viene eseguita.</span><span class="sxs-lookup"><span data-stu-id="73f16-109">The calling application must release this interface when it is done with it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="73f16-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="73f16-110">Return value</span></span>

<span data-ttu-id="73f16-111">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="73f16-111">The method returns an **HRESULT**.</span></span> <span data-ttu-id="73f16-112">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="73f16-112">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="73f16-113">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="73f16-113">Return code</span></span>                                                                          | <span data-ttu-id="73f16-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="73f16-114">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="73f16-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="73f16-115"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="73f16-116">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="73f16-116">The method succeeded.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="73f16-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="73f16-117">Requirements</span></span>



| <span data-ttu-id="73f16-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="73f16-118">Requirement</span></span> | <span data-ttu-id="73f16-119">Valore</span><span class="sxs-lookup"><span data-stu-id="73f16-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="73f16-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="73f16-120">Minimum supported client</span></span><br/> | <span data-ttu-id="73f16-121">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="73f16-121">Windows 7 \[desktop apps only\]</span></span><br/>                                                                                                                             |
| <span data-ttu-id="73f16-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="73f16-122">Minimum supported server</span></span><br/> | <span data-ttu-id="73f16-123">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="73f16-123">None supported</span></span><br/>                                                                                                                                              |
| <span data-ttu-id="73f16-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="73f16-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="73f16-125"><dt>Devpkey. h; </dt> <dt>PortableDeviceConnectApi. h</dt></span><span class="sxs-lookup"><span data-stu-id="73f16-125"><dt>Devpkey.h; </dt> <dt>Portabledeviceconnectapi.h</dt></span></span> </dl> |
| <span data-ttu-id="73f16-126">IDL</span><span class="sxs-lookup"><span data-stu-id="73f16-126">IDL</span></span><br/>                      | <dl> <span data-ttu-id="73f16-127"><dt>PortableDeviceConnectApi. idl</dt></span><span class="sxs-lookup"><span data-stu-id="73f16-127"><dt>Portabledeviceconnectapi.idl</dt></span></span> </dl>                                                                |
| <span data-ttu-id="73f16-128">Libreria</span><span class="sxs-lookup"><span data-stu-id="73f16-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="73f16-129"><dt>PortableDeviceGuids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="73f16-129"><dt>PortableDeviceGuids.lib</dt></span></span> </dl>                                                                     |



## <a name="see-also"></a><span data-ttu-id="73f16-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="73f16-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73f16-131">**IEnumPortableDeviceConnectors**</span><span class="sxs-lookup"><span data-stu-id="73f16-131">**IEnumPortableDeviceConnectors**</span></span>](ienumportabledeviceconnectors.md)
</dt> </dl>

 

 




