---
title: Interfaccia IMsRdpCameraRedirConfigCollection
description: Rappresenta la raccolta di fotocamere (e le configurazioni associate) disponibili per il reindirizzamento.
ms.tgt_platform: multiple
keywords:
- Interfaccia IMsRdpCameraRedirConfigCollection Servizi Desktop remoto
- Interfaccia IMsRdpCameraRedirConfigCollection Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfigCollection
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 3d97249a7485ec024ee3611809c87c5b6ed41143
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/19/2020
ms.locfileid: "104123282"
---
# <a name="imsrdpcameraredirconfigcollection-interface"></a><span data-ttu-id="a46a0-105">Interfaccia IMsRdpCameraRedirConfigCollection</span><span class="sxs-lookup"><span data-stu-id="a46a0-105">IMsRdpCameraRedirConfigCollection interface</span></span>

 <span data-ttu-id="a46a0-106">Rappresenta la raccolta di fotocamere (e le configurazioni associate) disponibili per il reindirizzamento.</span><span class="sxs-lookup"><span data-stu-id="a46a0-106">Represents the collection of cameras (and the associated configurations) that are available for redirection.</span></span>

## <a name="members"></a><span data-ttu-id="a46a0-107">Membri</span><span class="sxs-lookup"><span data-stu-id="a46a0-107">Members</span></span>

<span data-ttu-id="a46a0-108">L'interfaccia **IMsRdpCameraRedirConfigCollection** eredita da **IUnknown**.</span><span class="sxs-lookup"><span data-stu-id="a46a0-108">The **IMsRdpCameraRedirConfigCollection** interface inherits from **IUnknown**.</span></span> <span data-ttu-id="a46a0-109">**IMsRdpCameraRedirConfigCollection** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="a46a0-109">**IMsRdpCameraRedirConfigCollection** also has these types of members:</span></span>

- [<span data-ttu-id="a46a0-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="a46a0-110">Methods</span></span>](#methods)
- [<span data-ttu-id="a46a0-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="a46a0-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="a46a0-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="a46a0-112">Methods</span></span>

<span data-ttu-id="a46a0-113">L'interfaccia **IMsRdpCameraRedirConfigCollection** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="a46a0-113">The **IMsRdpCameraRedirConfigCollection** interface has these methods.</span></span>

| <span data-ttu-id="a46a0-114">Metodo</span><span class="sxs-lookup"><span data-stu-id="a46a0-114">Method</span></span>            | <span data-ttu-id="a46a0-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a46a0-115">Description</span></span>              |
|:------------------|:-------------------------|
| [<span data-ttu-id="a46a0-116">**AddConfig**</span><span class="sxs-lookup"><span data-stu-id="a46a0-116">**AddConfig**</span></span>](imsrdpcameraredirconfigcollection-addconfig.md)       |  <span data-ttu-id="a46a0-117">Aggiunge un oggetto [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) alla raccolta (la fotocamera corrispondente non deve essere connessa).</span><span class="sxs-lookup"><span data-stu-id="a46a0-117">Adds an [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) object to the collection (the corresponding camera does not have to be connected).</span></span>                   |
| [<span data-ttu-id="a46a0-118">**Ripeti analisi**</span><span class="sxs-lookup"><span data-stu-id="a46a0-118">**Rescan**</span></span>](imsrdpcameraredirconfigcollection-rescan.md)       |  <span data-ttu-id="a46a0-119">Enumera i dispositivi della fotocamera connessa.</span><span class="sxs-lookup"><span data-stu-id="a46a0-119">Enumerates connected camera devices.</span></span>                   |

### <a name="properties"></a><span data-ttu-id="a46a0-120">Proprietà</span><span class="sxs-lookup"><span data-stu-id="a46a0-120">Properties</span></span>

<span data-ttu-id="a46a0-121">L'interfaccia **IMsRdpCameraRedirConfigCollection** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="a46a0-121">The **IMsRdpCameraRedirConfigCollection** interface has these properties.</span></span>

| <span data-ttu-id="a46a0-122">Proprietà</span><span class="sxs-lookup"><span data-stu-id="a46a0-122">Property</span></span>         | <span data-ttu-id="a46a0-123">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="a46a0-123">Access type</span></span>           | <span data-ttu-id="a46a0-124">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a46a0-124">Description</span></span>            |
|:-----------------|:----------------------|:-----------------------|
| [<span data-ttu-id="a46a0-125">**ByIndex**</span><span class="sxs-lookup"><span data-stu-id="a46a0-125">**ByIndex**</span></span>](imsrdpcameraredirconfigcollection-byindex.md)      | <span data-ttu-id="a46a0-126">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="a46a0-126">Read-only</span></span> |  <span data-ttu-id="a46a0-127">Restituisce un oggetto [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) in base al relativo indice nella raccolta.</span><span class="sxs-lookup"><span data-stu-id="a46a0-127">Returns an [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) object by its index in the collection.</span></span>   |
| [<span data-ttu-id="a46a0-128">**ByInstanceId**</span><span class="sxs-lookup"><span data-stu-id="a46a0-128">**ByInstanceId**</span></span>](imsrdpcameraredirconfigcollection-byinstanceid.md)                       | <span data-ttu-id="a46a0-129">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="a46a0-129">Read-only</span></span> |    <span data-ttu-id="a46a0-130">Restituisce un oggetto [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) dalla raccolta che corrisponde all'ID istanza specificato.</span><span class="sxs-lookup"><span data-stu-id="a46a0-130">Returns an [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) object from the collection that corresponds to the specified instance ID.</span></span>    |
| [<span data-ttu-id="a46a0-131">**BySymbolicLink**</span><span class="sxs-lookup"><span data-stu-id="a46a0-131">**BySymbolicLink**</span></span>](imsrdpcameraredirconfigcollection-bysymboliclink.md)      | <span data-ttu-id="a46a0-132">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="a46a0-132">Read-only</span></span> |  <span data-ttu-id="a46a0-133">Restituisce un oggetto [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) dalla raccolta che corrisponde al collegamento simbolico specificato dell'interfaccia **KSCATEGORY_VIDEO_CAMERA** per la fotocamera.</span><span class="sxs-lookup"><span data-stu-id="a46a0-133">Returns an [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) object from the collection that corresponds to the given symbolic link of the **KSCATEGORY_VIDEO_CAMERA** interface for the camera.</span></span>  |
| [<span data-ttu-id="a46a0-134">**Conteggio**</span><span class="sxs-lookup"><span data-stu-id="a46a0-134">**Count**</span></span>](imsrdpcameraredirconfigcollection-count.md)                       | <span data-ttu-id="a46a0-135">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="a46a0-135">Read-only</span></span> |    <span data-ttu-id="a46a0-136">Restituisce il numero di oggetti [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) nell'insieme.</span><span class="sxs-lookup"><span data-stu-id="a46a0-136">Returns the number of [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) objects in the collection.</span></span>   |
| [<span data-ttu-id="a46a0-137">**EncodeVideo**</span><span class="sxs-lookup"><span data-stu-id="a46a0-137">**EncodeVideo**</span></span>](imsrdpcameraredirconfigcollection-encodevideo.md)      | <span data-ttu-id="a46a0-138">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="a46a0-138">Read/Write</span></span> |  <span data-ttu-id="a46a0-139">Specifica se il flusso video è codificato con H. 264.</span><span class="sxs-lookup"><span data-stu-id="a46a0-139">Specifies whether or not the video stream is H.264 encoded.</span></span>  |
| [<span data-ttu-id="a46a0-140">**EncodingQuality**</span><span class="sxs-lookup"><span data-stu-id="a46a0-140">**EncodingQuality**</span></span>](imsrdpcameraredirconfigcollection-encodingquality.md)                       | <span data-ttu-id="a46a0-141">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="a46a0-141">Read/Write</span></span> |    <span data-ttu-id="a46a0-142">Specifica la qualità della codifica (velocità in bit).</span><span class="sxs-lookup"><span data-stu-id="a46a0-142">Specifies the encoding quality (bit rate).</span></span>   |
| [<span data-ttu-id="a46a0-143">**RedirectByDefault**</span><span class="sxs-lookup"><span data-stu-id="a46a0-143">**RedirectByDefault**</span></span>](imsrdpcameraredirconfigcollection-redirectbydefault.md)                       | <span data-ttu-id="a46a0-144">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="a46a0-144">Read/Write</span></span> |   <span data-ttu-id="a46a0-145">Specifica se una nuova fotocamera viene reindirizzata per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="a46a0-145">Specifies whether or not any new camera gets redirected by default.</span></span>    |

## <a name="requirements"></a><span data-ttu-id="a46a0-146">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a46a0-146">Requirements</span></span>

| <span data-ttu-id="a46a0-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="a46a0-147">Requirement</span></span> | <span data-ttu-id="a46a0-148">Valore</span><span class="sxs-lookup"><span data-stu-id="a46a0-148">Value</span></span> |
|-------------------------------------|---------------------------------------|
| <span data-ttu-id="a46a0-149">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a46a0-149">Minimum supported client</span></span>| <span data-ttu-id="a46a0-150">Windows 10, versione 1803 (build 17134)</span><span class="sxs-lookup"><span data-stu-id="a46a0-150">Windows 10, version 1803 (build 17134)</span></span>      |
| <span data-ttu-id="a46a0-151">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="a46a0-151">Type library</span></span>            | <span data-ttu-id="a46a0-152">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="a46a0-152">MsTscAx.dll</span></span>                        |
| <span data-ttu-id="a46a0-153">DLL</span><span class="sxs-lookup"><span data-stu-id="a46a0-153">DLL</span></span>                  | <span data-ttu-id="a46a0-154">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="a46a0-154">MsTscAx.dll</span></span>     |
| <span data-ttu-id="a46a0-155">IID</span><span class="sxs-lookup"><span data-stu-id="a46a0-155">IID</span></span>                      | <span data-ttu-id="a46a0-156">IID \_ IMsRdpCameraRedirConfigCollection è definito come AE45252B-aaab-4504-B681-649D6073A37A</span><span class="sxs-lookup"><span data-stu-id="a46a0-156">IID\_IMsRdpCameraRedirConfigCollection is defined as AE45252B-AAAB-4504-B681-649D6073A37A</span></span>            |

## <a name="see-also"></a><span data-ttu-id="a46a0-157">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a46a0-157">See also</span></span>

- [<span data-ttu-id="a46a0-158">**IMsRdpCameraRedirConfig**</span><span class="sxs-lookup"><span data-stu-id="a46a0-158">**IMsRdpCameraRedirConfig**</span></span>](imsrdpcameraredirconfig.md)
- [<span data-ttu-id="a46a0-159">**IMsRdpClientNonScriptable7::CameraRedirConfigCollection**</span><span class="sxs-lookup"><span data-stu-id="a46a0-159">**IMsRdpClientNonScriptable7::CameraRedirConfigCollection**</span></span>](imsrdpclientnonscriptable7-cameraredirconfigcollection.md)
