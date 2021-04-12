---
title: Metodo IDeviceBroker OpenDeviceFromInterfacePath
description: Tenta di aprire un'istanza dell'interfaccia del dispositivo per conto di un client. IID 8604b268-34A6-4b1A-A59F-CDBD8379FD98.
ms.assetid: 5ADDB994-3AAB-49B2-8B83-F71883AFD854
keywords:
- API broker Access Device Method OpenDeviceFromInterfacePath
- API gestore di accesso ai dispositivi del metodo OpenDeviceFromInterfacePath, interfaccia IDeviceBroker
- API del broker di accesso ai dispositivi dell'interfaccia IDeviceBroker, metodo OpenDeviceFromInterfacePath
topic_type:
- apiref
api_name:
- IDeviceBroker.OpenDeviceFromInterfacePath
api_type:
- COM
ms.topic: article
ms.date: 02/11/2020
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5363600455ee1ba5c1c86cb12690afd242f68118
ms.sourcegitcommit: 01a4383738056cf3de4f45f36d98ef73d4dc694d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/11/2020
ms.locfileid: "104398522"
---
# <a name="idevicebrokeropendevicefrominterfacepath-method"></a><span data-ttu-id="74c21-107">Metodo IDeviceBroker:: OpenDeviceFromInterfacePath</span><span class="sxs-lookup"><span data-stu-id="74c21-107">IDeviceBroker::OpenDeviceFromInterfacePath method</span></span>

> [!Important]  
> <span data-ttu-id="74c21-108">Queste interfacce non sono supportate e non devono essere usate.</span><span class="sxs-lookup"><span data-stu-id="74c21-108">These interfaces are not supported and should not be used.</span></span> <span data-ttu-id="74c21-109">Usare invece le API nella Guida di riferimento per la [programmazione di API di accesso ai dispositivi](device-access-api-c---programming-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="74c21-109">Use the APIs in the [Device Access API C++ Programming Reference](device-access-api-c---programming-reference.md) instead.</span></span>

<span data-ttu-id="74c21-110">Tenta di aprire un'istanza dell'interfaccia del dispositivo per conto di un client.</span><span class="sxs-lookup"><span data-stu-id="74c21-110">Attempts to open a device interface instance on behalf of a client.</span></span> <span data-ttu-id="74c21-111">IID = 8604b268-34A6-4b1A-A59F-CDBD8379FD98.</span><span class="sxs-lookup"><span data-stu-id="74c21-111">IID = 8604b268-34A6-4b1A-A59F-CDBD8379FD98.</span></span>

## <a name="syntax"></a><span data-ttu-id="74c21-112">Sintassi</span><span class="sxs-lookup"><span data-stu-id="74c21-112">Syntax</span></span>

```C++
HRESULT OpenDeviceFromInterfacePath(
  [in]  PCWSTR pszDeviceInterfacePath,
  [in]  DWORD  desiredAccess,
  [in]  DWORD  shareMode,
  [in]  DWORD  flagsAndAttributes,
  [out] Handle *phDevice
);
```

## <a name="parameters"></a><span data-ttu-id="74c21-113">Parametri</span><span class="sxs-lookup"><span data-stu-id="74c21-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="74c21-114">*pszDeviceInterfacePath* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="74c21-114">*pszDeviceInterfacePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74c21-115">Istanza dell'interfaccia del dispositivo da aprire.</span><span class="sxs-lookup"><span data-stu-id="74c21-115">Device interface instance to open.</span></span>

</dd> <dt>

<span data-ttu-id="74c21-116">*desiredAccess* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="74c21-116">*desiredAccess* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74c21-117">Accesso desiderato da passare a Open.</span><span class="sxs-lookup"><span data-stu-id="74c21-117">Desired access to be passed to open.</span></span>

</dd> <dt>

<span data-ttu-id="74c21-118">*shareMode* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="74c21-118">*shareMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74c21-119">Modalità di condivisione da passare a Open.</span><span class="sxs-lookup"><span data-stu-id="74c21-119">Share mode to be passed to open.</span></span>

</dd> <dt>

<span data-ttu-id="74c21-120">*flagsAndAttributes* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="74c21-120">*flagsAndAttributes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74c21-121">Flag e attributi da passare a Open.</span><span class="sxs-lookup"><span data-stu-id="74c21-121">Flags and attributes to be passed to open.</span></span>

</dd> <dt>

<span data-ttu-id="74c21-122">*\* phDevice* \[\]</span><span class="sxs-lookup"><span data-stu-id="74c21-122">*\*phDevice* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="74c21-123">Handle risultante se l'apertura è stata completata.</span><span class="sxs-lookup"><span data-stu-id="74c21-123">Resulting handle if open was successful.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="74c21-124">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="74c21-124">Return value</span></span>

<span data-ttu-id="74c21-125">Se questa funzione ha esito positivo, restituisce S_OK.</span><span class="sxs-lookup"><span data-stu-id="74c21-125">If this function succeeds, it returns S_OK.</span></span> <span data-ttu-id="74c21-126">In caso contrario, restituisce un codice di errore HRESULT.</span><span class="sxs-lookup"><span data-stu-id="74c21-126">Otherwise, it returns an HRESULT error code.</span></span>
