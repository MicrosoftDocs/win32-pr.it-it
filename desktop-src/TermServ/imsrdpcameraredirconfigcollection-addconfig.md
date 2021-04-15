---
title: Metodo IMsRdpCameraRedirConfigCollection AddConfig
description: Aggiunge un oggetto IMsRdpCameraRedirConfig alla raccolta (la fotocamera corrispondente non deve essere connessa).
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo AddConfig
- Metodo AddConfig Servizi Desktop remoto, interfaccia IMsRdpCameraRedirConfigCollection
- Interfaccia IMsRdpCameraRedirConfigCollection Servizi Desktop remoto, metodo AddConfig
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfigCollection.AddConfig
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: e8c954b710c3f35bca9685d461e478104dac9039
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/19/2020
ms.locfileid: "104520305"
---
# <a name="imsrdpcameraredirconfigcollectionaddconfig-method"></a><span data-ttu-id="2a85f-106">Metodo IMsRdpCameraRedirConfigCollection:: AddConfig</span><span class="sxs-lookup"><span data-stu-id="2a85f-106">IMsRdpCameraRedirConfigCollection::AddConfig method</span></span>

<span data-ttu-id="2a85f-107">Aggiunge un oggetto [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) alla raccolta (la fotocamera corrispondente non deve essere connessa).</span><span class="sxs-lookup"><span data-stu-id="2a85f-107">Adds an [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) object to the collection (the corresponding camera does not have to be connected).</span></span>

## <a name="syntax"></a><span data-ttu-id="2a85f-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2a85f-108">Syntax</span></span>

```C++
HRESULT AddConfig(
    [in] BSTR symbolicLink,
    [in] VARIANT_BOOL fRedirected
);
```

## <a name="parameters"></a><span data-ttu-id="2a85f-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="2a85f-109">Parameters</span></span>

<span data-ttu-id="2a85f-110">*symbolicLink* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2a85f-110">*symbolicLink* \[in\]</span></span>

<span data-ttu-id="2a85f-111">Collegamento simbolico per il nuovo oggetto [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) .</span><span class="sxs-lookup"><span data-stu-id="2a85f-111">The symbolic link for the new [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) object.</span></span>

<span data-ttu-id="2a85f-112">*fRedirected* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2a85f-112">*fRedirected* \[in\]</span></span>

<span data-ttu-id="2a85f-113">Specifica se la nuova fotocamera viene reindirizzata per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="2a85f-113">Specifies whether or not the new camera gets redirected by default.</span></span>

## <a name="return-value"></a><span data-ttu-id="2a85f-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2a85f-114">Return value</span></span>

<span data-ttu-id="2a85f-115">Se l'operazione ha esito positivo, restituire **S \_ OK** .</span><span class="sxs-lookup"><span data-stu-id="2a85f-115">Return **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="2a85f-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2a85f-116">Requirements</span></span>

| <span data-ttu-id="2a85f-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="2a85f-117">Requirement</span></span> | <span data-ttu-id="2a85f-118">Valore</span><span class="sxs-lookup"><span data-stu-id="2a85f-118">Value</span></span> |
|-------------------------------------|---------------------------------------|
| <span data-ttu-id="2a85f-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2a85f-119">Minimum supported client</span></span>| <span data-ttu-id="2a85f-120">Windows 10, versione 1803 (build 17134)</span><span class="sxs-lookup"><span data-stu-id="2a85f-120">Windows 10, version 1803 (build 17134)</span></span>      |
| <span data-ttu-id="2a85f-121">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="2a85f-121">Type library</span></span>            | <span data-ttu-id="2a85f-122">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="2a85f-122">MsTscAx.dll</span></span>                        |
| <span data-ttu-id="2a85f-123">DLL</span><span class="sxs-lookup"><span data-stu-id="2a85f-123">DLL</span></span>                  | <span data-ttu-id="2a85f-124">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="2a85f-124">MsTscAx.dll</span></span>     |
| <span data-ttu-id="2a85f-125">IID</span><span class="sxs-lookup"><span data-stu-id="2a85f-125">IID</span></span>                      | <span data-ttu-id="2a85f-126">IID \_ IMsRdpCameraRedirConfigCollection è definito come AE45252B-aaab-4504-B681-649D6073A37A</span><span class="sxs-lookup"><span data-stu-id="2a85f-126">IID\_IMsRdpCameraRedirConfigCollection is defined as AE45252B-AAAB-4504-B681-649D6073A37A</span></span>          |

## <a name="see-also"></a><span data-ttu-id="2a85f-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2a85f-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a85f-128">**IMsRdpCameraRedirConfigCollection**</span><span class="sxs-lookup"><span data-stu-id="2a85f-128">**IMsRdpCameraRedirConfigCollection**</span></span>](imsrdpcameraredirconfigcollection.md)
</dt> </dl>