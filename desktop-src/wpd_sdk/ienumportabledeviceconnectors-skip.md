---
description: Ignora il numero specificato di dispositivi nella sequenza di enumerazione.
ms.assetid: 38b72b80-93f5-433e-977c-e3ee503daae5
title: 'Metodo IEnumPortableDeviceConnectors:: Skip (Devpkey. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPortableDeviceConnectors.Skip
api_type:
- COM
api_location:
- PortableDeviceGuids.lib
- PortableDeviceGuids.dll
ms.openlocfilehash: c00daecccd12beee8e9e741c2906e47484fa6da3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104057890"
---
# <a name="ienumportabledeviceconnectorsskip-method"></a><span data-ttu-id="b6236-103">Metodo IEnumPortableDeviceConnectors:: Skip</span><span class="sxs-lookup"><span data-stu-id="b6236-103">IEnumPortableDeviceConnectors::Skip method</span></span>

<span data-ttu-id="b6236-104">Il metodo **Skip** ignora il numero specificato di dispositivi nella sequenza di enumerazione.</span><span class="sxs-lookup"><span data-stu-id="b6236-104">The **Skip** method skips the specified number of devices in the enumeration sequence.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6236-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b6236-105">Syntax</span></span>


```C++
HRESULT Skip(
  [in] UINT32 cConnectors
);
```



## <a name="parameters"></a><span data-ttu-id="b6236-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b6236-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b6236-107">*cConnectors* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b6236-107">*cConnectors* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6236-108">Numero di dispositivi da ignorare.</span><span class="sxs-lookup"><span data-stu-id="b6236-108">The number of devices to skip.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b6236-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b6236-109">Return value</span></span>

<span data-ttu-id="b6236-110">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="b6236-110">The method returns an **HRESULT**.</span></span> <span data-ttu-id="b6236-111">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="b6236-111">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="b6236-112">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="b6236-112">Return code</span></span>                                                                             | <span data-ttu-id="b6236-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b6236-113">Description</span></span>                                                                                                                                                                               |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b6236-114"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="b6236-114"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="b6236-115">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="b6236-115">The method succeeded.</span></span><br/>                                                                                                                                                          |
| <dl> <span data-ttu-id="b6236-116"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="b6236-116"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="b6236-117">Non è stato possibile ignorare il numero specificato di dispositivi.</span><span class="sxs-lookup"><span data-stu-id="b6236-117">The specified number of devices could not be skipped.</span></span> <span data-ttu-id="b6236-118">Una delle possibili cause: il parametro *cConnectors* specifica più dispositivi che rimangono effettivamente nella sequenza di enumerazione.</span><span class="sxs-lookup"><span data-stu-id="b6236-118">One possible cause: The *cConnectors* parameter specifies more devices than actually remain in the enumeration sequence.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="b6236-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b6236-119">Requirements</span></span>



| <span data-ttu-id="b6236-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="b6236-120">Requirement</span></span> | <span data-ttu-id="b6236-121">Valore</span><span class="sxs-lookup"><span data-stu-id="b6236-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6236-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b6236-122">Minimum supported client</span></span><br/> | <span data-ttu-id="b6236-123">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="b6236-123">Windows 7 \[desktop apps only\]</span></span><br/>                                                                                                                             |
| <span data-ttu-id="b6236-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b6236-124">Minimum supported server</span></span><br/> | <span data-ttu-id="b6236-125">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="b6236-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                                   |
| <span data-ttu-id="b6236-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b6236-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="b6236-127"><dt>Devpkey. h; </dt> <dt>PortableDeviceConnectApi. h</dt></span><span class="sxs-lookup"><span data-stu-id="b6236-127"><dt>Devpkey.h; </dt> <dt>Portabledeviceconnectapi.h</dt></span></span> </dl> |
| <span data-ttu-id="b6236-128">IDL</span><span class="sxs-lookup"><span data-stu-id="b6236-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b6236-129"><dt>PortableDeviceConnectApi. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b6236-129"><dt>Portabledeviceconnectapi.idl</dt></span></span> </dl>                                                                |
| <span data-ttu-id="b6236-130">Libreria</span><span class="sxs-lookup"><span data-stu-id="b6236-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="b6236-131"><dt>PortableDeviceGuids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b6236-131"><dt>PortableDeviceGuids.lib</dt></span></span> </dl>                                                                     |



## <a name="see-also"></a><span data-ttu-id="b6236-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b6236-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6236-133">**IEnumPortableDeviceConnectors**</span><span class="sxs-lookup"><span data-stu-id="b6236-133">**IEnumPortableDeviceConnectors**</span></span>](ienumportabledeviceconnectors.md)
</dt> </dl>

 

 




