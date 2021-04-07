---
title: Metodo IMsRdpClientNonScriptable6 SendLocation2D
description: Invia un valore di latitudine e longitudine al server in modo che la posizione geografica del client possa essere riflessa nella sessione remota.
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo SendLocation2D
- Metodo SendLocation2D Servizi Desktop remoto, interfaccia IMsRdpClientNonScriptable6
- Interfaccia IMsRdpClientNonScriptable6 Servizi Desktop remoto, metodo SendLocation2D
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable6.SendLocation2D
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: b706fdb35ba8360b294d25021c0c1a18bbe90188
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/19/2020
ms.locfileid: "103745343"
---
# <a name="imsrdpclientnonscriptable6sendlocation2d-method"></a><span data-ttu-id="71e64-106">Metodo IMsRdpClientNonScriptable6:: SendLocation2D</span><span class="sxs-lookup"><span data-stu-id="71e64-106">IMsRdpClientNonScriptable6::SendLocation2D method</span></span>

<span data-ttu-id="71e64-107">Invia un valore di latitudine e longitudine al server in modo che la posizione geografica del client possa essere riflessa nella sessione remota.</span><span class="sxs-lookup"><span data-stu-id="71e64-107">Sends a latitude and longitude value to the server so the client’s geographic location can be reflected in the remote session.</span></span>

## <a name="syntax"></a><span data-ttu-id="71e64-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="71e64-108">Syntax</span></span>

```C++
HRESULT SendLocation2D(
  [in] DOUBLE latitude,
  [in] DOUBLE longitude
);
```

## <a name="parameters"></a><span data-ttu-id="71e64-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="71e64-109">Parameters</span></span>

<span data-ttu-id="71e64-110">*Latitudine* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="71e64-110">*latitude* \[in\]</span></span>

<span data-ttu-id="71e64-111">Latitudine di una posizione geografica.</span><span class="sxs-lookup"><span data-stu-id="71e64-111">The latitude of a geographic location.</span></span> <span data-ttu-id="71e64-112">L'intervallo valido di valori di latitudine è compreso tra-90,0 e 90,0 gradi.</span><span class="sxs-lookup"><span data-stu-id="71e64-112">The valid range of latitude values is from -90.0 to 90.0 degrees.</span></span>

<span data-ttu-id="71e64-113">*Longitudine* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="71e64-113">*longitude* \[in\]</span></span>

<span data-ttu-id="71e64-114">Longitudine di una posizione geografica.</span><span class="sxs-lookup"><span data-stu-id="71e64-114">The longitude of a geographic location.</span></span> <span data-ttu-id="71e64-115">L'intervallo valido di valori di latitudine è compreso tra-180,0 e 180,0 gradi.</span><span class="sxs-lookup"><span data-stu-id="71e64-115">The valid range of latitude values is from -180.0 to 180.0 degrees.</span></span>

## <a name="return-value"></a><span data-ttu-id="71e64-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="71e64-116">Return value</span></span>

<span data-ttu-id="71e64-117">Se l'operazione ha esito positivo, restituire **S \_ OK** .</span><span class="sxs-lookup"><span data-stu-id="71e64-117">Return **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="71e64-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="71e64-118">Requirements</span></span>

| <span data-ttu-id="71e64-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="71e64-119">Requirement</span></span> | <span data-ttu-id="71e64-120">Valore</span><span class="sxs-lookup"><span data-stu-id="71e64-120">Value</span></span> |
|-------------------------------------|---------------------------------------|
| <span data-ttu-id="71e64-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="71e64-121">Minimum supported client</span></span>| <span data-ttu-id="71e64-122">Windows 10, versione 1709 (build 16299)</span><span class="sxs-lookup"><span data-stu-id="71e64-122">Windows 10, version 1709 (build 16299)</span></span>      |
| <span data-ttu-id="71e64-123">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="71e64-123">Type library</span></span>            | <span data-ttu-id="71e64-124">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="71e64-124">MsTscAx.dll</span></span>                        |
| <span data-ttu-id="71e64-125">DLL</span><span class="sxs-lookup"><span data-stu-id="71e64-125">DLL</span></span>                  | <span data-ttu-id="71e64-126">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="71e64-126">MsTscAx.dll</span></span>     |
| <span data-ttu-id="71e64-127">IID</span><span class="sxs-lookup"><span data-stu-id="71e64-127">IID</span></span>                      | <span data-ttu-id="71e64-128">IID \_ IMsRdpClientNonScriptable6 è definito come 05293249-B28B-4DB8-BE64-1B2F496B910E</span><span class="sxs-lookup"><span data-stu-id="71e64-128">IID\_IMsRdpClientNonScriptable6 is defined as 05293249-B28B-4DB8-BE64-1B2F496B910E</span></span>            |

## <a name="see-also"></a><span data-ttu-id="71e64-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="71e64-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71e64-130">**IMsRdpClientNonScriptable6**</span><span class="sxs-lookup"><span data-stu-id="71e64-130">**IMsRdpClientNonScriptable6**</span></span>](imsrdpclientnonscriptable6.md)
</dt> </dl>
