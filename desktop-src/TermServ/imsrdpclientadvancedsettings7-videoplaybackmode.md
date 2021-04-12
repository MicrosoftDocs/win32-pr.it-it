---
title: Proprietà VideoPlaybackMode di IMsRdpClientAdvancedSettings7
description: Specifica o recupera un valore che indica la modalità di riproduzione video.
ms.assetid: 83f0baa3-3ac2-47ee-b106-5beaf60d73d2
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà VideoPlaybackMode
- Servizi Desktop remoto proprietà VideoPlaybackMode, interfaccia IMsRdpClientAdvancedSettings7
- Interfaccia IMsRdpClientAdvancedSettings7 Servizi Desktop remoto, proprietà VideoPlaybackMode
- Servizi Desktop remoto proprietà VideoPlaybackMode, interfaccia IMsRdpClientAdvancedSettings8
- Interfaccia IMsRdpClientAdvancedSettings8 Servizi Desktop remoto, proprietà VideoPlaybackMode
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings7.VideoPlaybackMode
- IMsRdpClientAdvancedSettings7.get_VideoPlaybackMode
- IMsRdpClientAdvancedSettings7.put_VideoPlaybackMode
- IMsRdpClientAdvancedSettings8.VideoPlaybackMode
- IMsRdpClientAdvancedSettings8.get_VideoPlaybackMode
- IMsRdpClientAdvancedSettings8.put_VideoPlaybackMode
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f864224f402814ada268b9b7cbc85ec115a1fa2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400938"
---
# <a name="imsrdpclientadvancedsettings7videoplaybackmode-property"></a><span data-ttu-id="37d6c-108">Proprietà IMsRdpClientAdvancedSettings7:: VideoPlaybackMode</span><span class="sxs-lookup"><span data-stu-id="37d6c-108">IMsRdpClientAdvancedSettings7::VideoPlaybackMode property</span></span>

<span data-ttu-id="37d6c-109">Specifica o recupera un valore che indica la modalità di riproduzione video.</span><span class="sxs-lookup"><span data-stu-id="37d6c-109">Specifies or retrieves a value that indicates the video playback mode.</span></span>

<span data-ttu-id="37d6c-110">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="37d6c-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="37d6c-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="37d6c-111">Syntax</span></span>


```C++
HRESULT put_VideoPlaybackMode(
  [in]          UINT videoPlaybackMode
);

HRESULT get_VideoPlaybackMode(
  [out, retval] UINT *pVideoPlaybackMode
);
```



## <a name="property-value"></a><span data-ttu-id="37d6c-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="37d6c-112">Property value</span></span>

<span data-ttu-id="37d6c-113">Valore che specifica la modalità di riproduzione video.</span><span class="sxs-lookup"><span data-stu-id="37d6c-113">A value that specifies the video playback mode.</span></span>

<span data-ttu-id="37d6c-114">I valori possibili sono:</span><span class="sxs-lookup"><span data-stu-id="37d6c-114">The possible values are:</span></span>

<dt>

<span data-ttu-id="37d6c-115">1</span><span class="sxs-lookup"><span data-stu-id="37d6c-115">1</span></span>
</dt> <dd>

<span data-ttu-id="37d6c-116">Modalità di riproduzione video predefinita.</span><span class="sxs-lookup"><span data-stu-id="37d6c-116">The default video playback mode.</span></span> <span data-ttu-id="37d6c-117">Quando la modalità di riproduzione video è impostata su questo valore, il reindirizzamento video è controllato dalla proprietà [**AudioRedirectionMode**](imsrdpclientsecuredsettings-autoredirectionmode.md) .</span><span class="sxs-lookup"><span data-stu-id="37d6c-117">When the video playback mode is set to this value, video redirection is controlled by the [**AudioRedirectionMode**](imsrdpclientsecuredsettings-autoredirectionmode.md) property.</span></span> <span data-ttu-id="37d6c-118">Quando la proprietà **AudioRedirectionMode** è impostata su **\_ \_ Reindirizzamento modalità audio**, il video viene decodificato e sottoposto a rendering nel client.</span><span class="sxs-lookup"><span data-stu-id="37d6c-118">When the **AudioRedirectionMode** property is set to **AUDIO\_MODE\_REDIRECT**, video is decoded and rendered on the client.</span></span>

</dd> <dt>

<span data-ttu-id="37d6c-119">0</span><span class="sxs-lookup"><span data-stu-id="37d6c-119">0</span></span>
</dt> <dd>

<span data-ttu-id="37d6c-120">Il reindirizzamento della riproduzione video è disabilitato, anche quando [**AudioRedirectionMode**](imsrdpclientsecuredsettings-autoredirectionmode.md) è impostato **su \_ \_ Reindirizzamento modalità audio**.</span><span class="sxs-lookup"><span data-stu-id="37d6c-120">Video playback redirection is disabled, even when [**AudioRedirectionMode**](imsrdpclientsecuredsettings-autoredirectionmode.md) is set to **AUDIO\_MODE\_REDIRECT**.</span></span> <span data-ttu-id="37d6c-121">In questa modalità, il video viene decodificato e sottoposto a rendering nel server Host sessione Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="37d6c-121">In this mode, video is decoded and rendered on the RD Session Host server.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="37d6c-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="37d6c-122">Requirements</span></span>



| <span data-ttu-id="37d6c-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="37d6c-123">Requirement</span></span> | <span data-ttu-id="37d6c-124">Valore</span><span class="sxs-lookup"><span data-stu-id="37d6c-124">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="37d6c-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="37d6c-125">Minimum supported client</span></span><br/> | <span data-ttu-id="37d6c-126">Windows 7</span><span class="sxs-lookup"><span data-stu-id="37d6c-126">Windows 7</span></span><br/>                                                                             |
| <span data-ttu-id="37d6c-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="37d6c-127">Minimum supported server</span></span><br/> | <span data-ttu-id="37d6c-128">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="37d6c-128">Windows Server 2008 R2</span></span><br/>                                                                |
| <span data-ttu-id="37d6c-129">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="37d6c-129">Type library</span></span><br/>             | <dl> <span data-ttu-id="37d6c-130"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="37d6c-130"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="37d6c-131">DLL</span><span class="sxs-lookup"><span data-stu-id="37d6c-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="37d6c-132"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="37d6c-132"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="37d6c-133">IID</span><span class="sxs-lookup"><span data-stu-id="37d6c-133">IID</span></span><br/>                      | <span data-ttu-id="37d6c-134">IID \_ IMsRdpClientAdvancedSettings7 è definito come 26036036-4010-4578-8091-0db9a1edf9c3</span><span class="sxs-lookup"><span data-stu-id="37d6c-134">IID\_IMsRdpClientAdvancedSettings7 is defined as 26036036-4010-4578-8091-0db9a1edf9c3</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="37d6c-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="37d6c-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37d6c-136">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="37d6c-136">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="37d6c-137">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="37d6c-137">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> </dl>

 

 





