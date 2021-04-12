---
title: Metodo IMsRdpClientNonScriptable6 SendLocation3D
description: Invia un valore di latitudine, Longitudine e altitudine al server in modo che la posizione geografica del client possa essere riflessa nella sessione remota.
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo SendLocation3D
- Metodo SendLocation3D Servizi Desktop remoto, interfaccia IMsRdpClientNonScriptable6
- Interfaccia IMsRdpClientNonScriptable6 Servizi Desktop remoto, metodo SendLocation3D
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable6.SendLocation3D
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: c63e779b6d6d090544af40a7ee6d9c05f8c49494
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/19/2020
ms.locfileid: "104480524"
---
# <a name="imsrdpclientnonscriptable6sendlocation3d-method"></a><span data-ttu-id="7b14d-106">Metodo IMsRdpClientNonScriptable6:: SendLocation3D</span><span class="sxs-lookup"><span data-stu-id="7b14d-106">IMsRdpClientNonScriptable6::SendLocation3D method</span></span>

<span data-ttu-id="7b14d-107">Invia un valore di latitudine, Longitudine e altitudine al server in modo che la posizione geografica del client possa essere riflessa nella sessione remota.</span><span class="sxs-lookup"><span data-stu-id="7b14d-107">Sends a latitude, longitude and altitude value to the server so the client’s geographic location can be reflected in the remote session.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b14d-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7b14d-108">Syntax</span></span>

```C++
HRESULT SendLocation3D(
  [in] DOUBLE latitude,
  [in] DOUBLE longitude,
  [in] INT32 altitude
);
```

## <a name="parameters"></a><span data-ttu-id="7b14d-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="7b14d-109">Parameters</span></span>

<span data-ttu-id="7b14d-110">*Latitudine* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7b14d-110">*latitude* \[in\]</span></span>

<span data-ttu-id="7b14d-111">Latitudine di una posizione geografica.</span><span class="sxs-lookup"><span data-stu-id="7b14d-111">The latitude of a geographic location.</span></span> <span data-ttu-id="7b14d-112">L'intervallo valido di valori di latitudine è compreso tra-90,0 e 90,0 gradi.</span><span class="sxs-lookup"><span data-stu-id="7b14d-112">The valid range of latitude values is from -90.0 to 90.0 degrees.</span></span>

<span data-ttu-id="7b14d-113">*Longitudine* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7b14d-113">*longitude* \[in\]</span></span>

<span data-ttu-id="7b14d-114">Longitudine di una posizione geografica.</span><span class="sxs-lookup"><span data-stu-id="7b14d-114">The longitude of a geographic location.</span></span> <span data-ttu-id="7b14d-115">L'intervallo valido di valori di latitudine è compreso tra-180,0 e 180,0 gradi.</span><span class="sxs-lookup"><span data-stu-id="7b14d-115">The valid range of latitude values is from -180.0 to 180.0 degrees.</span></span>

<span data-ttu-id="7b14d-116">*altitudine* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7b14d-116">*altitude* \[in\]</span></span>

<span data-ttu-id="7b14d-117">L'altitudine di una posizione geografica in metri.</span><span class="sxs-lookup"><span data-stu-id="7b14d-117">The altitude of a geographic location in meters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7b14d-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7b14d-118">Return value</span></span>

<span data-ttu-id="7b14d-119">Se l'operazione ha esito positivo, restituire **S \_ OK** .</span><span class="sxs-lookup"><span data-stu-id="7b14d-119">Return **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="7b14d-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7b14d-120">Requirements</span></span>

| <span data-ttu-id="7b14d-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="7b14d-121">Requirement</span></span> | <span data-ttu-id="7b14d-122">Valore</span><span class="sxs-lookup"><span data-stu-id="7b14d-122">Value</span></span> |
|-------------------------------------|---------------------------------------|
| <span data-ttu-id="7b14d-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7b14d-123">Minimum supported client</span></span>| <span data-ttu-id="7b14d-124">Windows 10, versione 1709 (build 16299)</span><span class="sxs-lookup"><span data-stu-id="7b14d-124">Windows 10, version 1709 (build 16299)</span></span>      |
| <span data-ttu-id="7b14d-125">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="7b14d-125">Type library</span></span>            | <span data-ttu-id="7b14d-126">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="7b14d-126">MsTscAx.dll</span></span>                        |
| <span data-ttu-id="7b14d-127">DLL</span><span class="sxs-lookup"><span data-stu-id="7b14d-127">DLL</span></span>                  | <span data-ttu-id="7b14d-128">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="7b14d-128">MsTscAx.dll</span></span>     |
| <span data-ttu-id="7b14d-129">IID</span><span class="sxs-lookup"><span data-stu-id="7b14d-129">IID</span></span>                      | <span data-ttu-id="7b14d-130">IID \_ IMsRdpClientNonScriptable6 è definito come 05293249-B28B-4DB8-BE64-1B2F496B910E</span><span class="sxs-lookup"><span data-stu-id="7b14d-130">IID\_IMsRdpClientNonScriptable6 is defined as 05293249-B28B-4DB8-BE64-1B2F496B910E</span></span>            |

## <a name="see-also"></a><span data-ttu-id="7b14d-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7b14d-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b14d-132">**IMsRdpClientNonScriptable6**</span><span class="sxs-lookup"><span data-stu-id="7b14d-132">**IMsRdpClientNonScriptable6**</span></span>](imsrdpclientnonscriptable6.md)
</dt> </dl>
