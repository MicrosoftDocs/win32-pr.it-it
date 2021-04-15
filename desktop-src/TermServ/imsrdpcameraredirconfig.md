---
title: Interfaccia IMsRdpCameraRedirConfig
description: Rappresenta le configurazioni per una fotocamera disponibile per il reindirizzamento.
ms.tgt_platform: multiple
keywords:
- Interfaccia IMsRdpCameraRedirConfig Servizi Desktop remoto
- Interfaccia IMsRdpCameraRedirConfig Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfig
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: fbb0f3344e0653ea4a87c876bb8ca7b8a67e7d21
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/19/2020
ms.locfileid: "104520306"
---
# <a name="imsrdpcameraredirconfig-interface"></a><span data-ttu-id="33ca1-105">Interfaccia IMsRdpCameraRedirConfig</span><span class="sxs-lookup"><span data-stu-id="33ca1-105">IMsRdpCameraRedirConfig interface</span></span>

<span data-ttu-id="33ca1-106">Rappresenta le configurazioni per una fotocamera disponibile per il reindirizzamento.</span><span class="sxs-lookup"><span data-stu-id="33ca1-106">Represents the configurations for a camera that is available for redirection.</span></span>

## <a name="members"></a><span data-ttu-id="33ca1-107">Membri</span><span class="sxs-lookup"><span data-stu-id="33ca1-107">Members</span></span>

<span data-ttu-id="33ca1-108">L'interfaccia **IMsRdpCameraRedirConfig** eredita da **IUnknown**.</span><span class="sxs-lookup"><span data-stu-id="33ca1-108">The **IMsRdpCameraRedirConfig** interface inherits from **IUnknown**.</span></span> <span data-ttu-id="33ca1-109">**IMsRdpCameraRedirConfig** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="33ca1-109">**IMsRdpCameraRedirConfig** also has these types of members:</span></span>

- [<span data-ttu-id="33ca1-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="33ca1-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="33ca1-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="33ca1-111">Properties</span></span>

<span data-ttu-id="33ca1-112">L'interfaccia **IMsRdpCameraRedirConfig** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="33ca1-112">The **IMsRdpCameraRedirConfig** interface has these properties.</span></span>

| <span data-ttu-id="33ca1-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="33ca1-113">Property</span></span>         | <span data-ttu-id="33ca1-114">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="33ca1-114">Access type</span></span>           | <span data-ttu-id="33ca1-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="33ca1-115">Description</span></span>            |
|:-----------------|:----------------------|:-----------------------|
| [<span data-ttu-id="33ca1-116">**DeviceExists**</span><span class="sxs-lookup"><span data-stu-id="33ca1-116">**DeviceExists**</span></span>](imsrdpcameraredirconfig-deviceexists.md)      | <span data-ttu-id="33ca1-117">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="33ca1-117">Read-only</span></span> | <span data-ttu-id="33ca1-118">Specifica se il dispositivo della fotocamera è attualmente esistente (ovvero la fotocamera è connessa).</span><span class="sxs-lookup"><span data-stu-id="33ca1-118">Specifies whether or not the camera device currently exists (that is, the camera is connected).</span></span>   |
| [<span data-ttu-id="33ca1-119">**FriendlyName**</span><span class="sxs-lookup"><span data-stu-id="33ca1-119">**FriendlyName**</span></span>](imsrdpcameraredirconfig-friendlyname.md)                       | <span data-ttu-id="33ca1-120">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="33ca1-120">Read-only</span></span> |    <span data-ttu-id="33ca1-121">Ottiene il nome descrittivo della fotocamera.</span><span class="sxs-lookup"><span data-stu-id="33ca1-121">Gets the camera’s friendly name.</span></span>    |
| [<span data-ttu-id="33ca1-122">**InstanceId**</span><span class="sxs-lookup"><span data-stu-id="33ca1-122">**InstanceId**</span></span>](imsrdpcameraredirconfig-instanceid.md)      | <span data-ttu-id="33ca1-123">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="33ca1-123">Read-only</span></span> |  <span data-ttu-id="33ca1-124">Ottiene l'ID dell'istanza della fotocamera.</span><span class="sxs-lookup"><span data-stu-id="33ca1-124">Gets the instance ID of the camera.</span></span>  |
| [<span data-ttu-id="33ca1-125">**ParentInstanceId**</span><span class="sxs-lookup"><span data-stu-id="33ca1-125">**ParentInstanceId**</span></span>](imsrdpcameraredirconfig-parentinstanceid.md)                       | <span data-ttu-id="33ca1-126">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="33ca1-126">Read-only</span></span> |    <span data-ttu-id="33ca1-127">Ottiene l'ID dell'istanza del dispositivo padre della fotocamera.</span><span class="sxs-lookup"><span data-stu-id="33ca1-127">Gets the parent device instance ID of the camera.</span></span>   |
| [<span data-ttu-id="33ca1-128">**Redirected**</span><span class="sxs-lookup"><span data-stu-id="33ca1-128">**Redirected**</span></span>](imsrdpcameraredirconfig-redirected.md)      | <span data-ttu-id="33ca1-129">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="33ca1-129">Read/Write</span></span> |  <span data-ttu-id="33ca1-130">Specifica se la fotocamera viene reindirizzata o meno.</span><span class="sxs-lookup"><span data-stu-id="33ca1-130">Specifies whether or not the camera is redirected.</span></span>  |
| [<span data-ttu-id="33ca1-131">**SymbolicLink**</span><span class="sxs-lookup"><span data-stu-id="33ca1-131">**SymbolicLink**</span></span>](imsrdpcameraredirconfig-symboliclink.md)                       | <span data-ttu-id="33ca1-132">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="33ca1-132">Read-only</span></span> |   <span data-ttu-id="33ca1-133">Ottiene il collegamento simbolico dell'interfaccia **KSCATEGORY_VIDEO_CAMERA** per la fotocamera.</span><span class="sxs-lookup"><span data-stu-id="33ca1-133">Gets the symbolic link of the **KSCATEGORY_VIDEO_CAMERA** interface for the camera.</span></span>   |

## <a name="requirements"></a><span data-ttu-id="33ca1-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="33ca1-134">Requirements</span></span>

| <span data-ttu-id="33ca1-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="33ca1-135">Requirement</span></span> | <span data-ttu-id="33ca1-136">Valore</span><span class="sxs-lookup"><span data-stu-id="33ca1-136">Value</span></span> |
|-------------------------------------|---------------------------------------|
| <span data-ttu-id="33ca1-137">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="33ca1-137">Minimum supported client</span></span>| <span data-ttu-id="33ca1-138">Windows 10, versione 1803 (build 17134)</span><span class="sxs-lookup"><span data-stu-id="33ca1-138">Windows 10, version 1803 (build 17134)</span></span>      |
| <span data-ttu-id="33ca1-139">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="33ca1-139">Type library</span></span>            | <span data-ttu-id="33ca1-140">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="33ca1-140">MsTscAx.dll</span></span>                        |
| <span data-ttu-id="33ca1-141">DLL</span><span class="sxs-lookup"><span data-stu-id="33ca1-141">DLL</span></span>                  | <span data-ttu-id="33ca1-142">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="33ca1-142">MsTscAx.dll</span></span>     |
| <span data-ttu-id="33ca1-143">IID</span><span class="sxs-lookup"><span data-stu-id="33ca1-143">IID</span></span>                      | <span data-ttu-id="33ca1-144">IID \_ IMsRdpCameraRedirConfig è definito come 09750604-D625-47C1-9FCD-F09F735705D7</span><span class="sxs-lookup"><span data-stu-id="33ca1-144">IID\_IMsRdpCameraRedirConfig is defined as 09750604-D625-47C1-9FCD-F09F735705D7</span></span>            |

## <a name="see-also"></a><span data-ttu-id="33ca1-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="33ca1-145">See also</span></span>

- [<span data-ttu-id="33ca1-146">**IMsRdpCameraRedirConfigCollection**</span><span class="sxs-lookup"><span data-stu-id="33ca1-146">**IMsRdpCameraRedirConfigCollection**</span></span>](imsrdpcameraredirconfigcollection.md)
- [<span data-ttu-id="33ca1-147">**IMsRdpClientNonScriptable7::CameraRedirConfigCollection**</span><span class="sxs-lookup"><span data-stu-id="33ca1-147">**IMsRdpClientNonScriptable7::CameraRedirConfigCollection**</span></span>](imsrdpclientnonscriptable7-cameraredirconfigcollection.md)