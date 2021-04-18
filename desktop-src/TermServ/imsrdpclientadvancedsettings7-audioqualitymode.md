---
title: Proprietà AudioQualityMode di IMsRdpClientAdvancedSettings7
description: Specifica o recupera un valore che indica l'impostazione della modalità di qualità audio per l'audio reindirizzato. Per impostazione predefinita, questo valore è impostato su 0.
ms.assetid: 9945c524-ca50-41ae-a7cf-1386cd758c0f
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà AudioQualityMode
- Servizi Desktop remoto proprietà AudioQualityMode, interfaccia IMsRdpClientAdvancedSettings7
- Interfaccia IMsRdpClientAdvancedSettings7 Servizi Desktop remoto, proprietà AudioQualityMode
- Servizi Desktop remoto proprietà AudioQualityMode, interfaccia IMsRdpClientAdvancedSettings8
- Interfaccia IMsRdpClientAdvancedSettings8 Servizi Desktop remoto, proprietà AudioQualityMode
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings7.AudioQualityMode
- IMsRdpClientAdvancedSettings7.get_AudioQualityMode
- IMsRdpClientAdvancedSettings7.put_AudioQualityMode
- IMsRdpClientAdvancedSettings8.AudioQualityMode
- IMsRdpClientAdvancedSettings8.get_AudioQualityMode
- IMsRdpClientAdvancedSettings8.put_AudioQualityMode
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5fdfc19176e03f8979e5adb25bf0c9eaf4ceed9f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301892"
---
# <a name="imsrdpclientadvancedsettings7audioqualitymode-property"></a><span data-ttu-id="ed3bb-109">Proprietà IMsRdpClientAdvancedSettings7:: AudioQualityMode</span><span class="sxs-lookup"><span data-stu-id="ed3bb-109">IMsRdpClientAdvancedSettings7::AudioQualityMode property</span></span>

<span data-ttu-id="ed3bb-110">Specifica o recupera un valore che indica l'impostazione della modalità di qualità audio per l'audio reindirizzato.</span><span class="sxs-lookup"><span data-stu-id="ed3bb-110">Specifies or retrieves a value that indicates the audio quality mode setting for redirected audio.</span></span> <span data-ttu-id="ed3bb-111">Per impostazione predefinita, questo valore è impostato su 0.</span><span class="sxs-lookup"><span data-stu-id="ed3bb-111">By default this is set to 0.</span></span>

<span data-ttu-id="ed3bb-112">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="ed3bb-112">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed3bb-113">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ed3bb-113">Syntax</span></span>


```C++
HRESULT put_AudioQualityMode(
  [in]          UINT audioQualityMode
);

HRESULT get_AudioQualityMode(
  [out, retval] UINT *pAudioQualityMode
);
```



## <a name="property-value"></a><span data-ttu-id="ed3bb-114">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="ed3bb-114">Property value</span></span>

<span data-ttu-id="ed3bb-115">Valore che specifica la modalità di qualità audio.</span><span class="sxs-lookup"><span data-stu-id="ed3bb-115">A value that specifies the audio quality mode.</span></span>

<span data-ttu-id="ed3bb-116">I valori possibili sono:</span><span class="sxs-lookup"><span data-stu-id="ed3bb-116">The possible values are:</span></span>

<dt>

<span data-ttu-id="ed3bb-117">0</span><span class="sxs-lookup"><span data-stu-id="ed3bb-117">0</span></span>
</dt> <dd>

<span data-ttu-id="ed3bb-118">Qualità audio dinamica.</span><span class="sxs-lookup"><span data-stu-id="ed3bb-118">Dynamic audio quality.</span></span> <span data-ttu-id="ed3bb-119">Questa è l'impostazione predefinita per la qualità audio.</span><span class="sxs-lookup"><span data-stu-id="ed3bb-119">This is the default audio quality setting.</span></span> <span data-ttu-id="ed3bb-120">Il server regola dinamicamente la qualità dell'output audio in risposta alle condizioni della rete e alle funzionalità client e server.</span><span class="sxs-lookup"><span data-stu-id="ed3bb-120">The server dynamically adjusts audio output quality in response to network conditions and the client and server capabilities.</span></span>

</dd> <dt>

<span data-ttu-id="ed3bb-121">1</span><span class="sxs-lookup"><span data-stu-id="ed3bb-121">1</span></span>
</dt> <dd>

<span data-ttu-id="ed3bb-122">Qualità audio media.</span><span class="sxs-lookup"><span data-stu-id="ed3bb-122">Medium audio quality.</span></span> <span data-ttu-id="ed3bb-123">Il server utilizza un formato fisso ma compresso per l'output audio.</span><span class="sxs-lookup"><span data-stu-id="ed3bb-123">The server uses a fixed but compressed format for audio output.</span></span>

</dd> <dt>

<span data-ttu-id="ed3bb-124">2</span><span class="sxs-lookup"><span data-stu-id="ed3bb-124">2</span></span>
</dt> <dd>

<span data-ttu-id="ed3bb-125">Qualità audio elevata.</span><span class="sxs-lookup"><span data-stu-id="ed3bb-125">High audio quality.</span></span> <span data-ttu-id="ed3bb-126">Il server fornisce l'output audio in formato PCM non compresso con un sovraccarico di elaborazione inferiore per la latenza.</span><span class="sxs-lookup"><span data-stu-id="ed3bb-126">The server provides audio output in uncompressed PCM format with lower processing overhead for latency.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ed3bb-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ed3bb-127">Requirements</span></span>



| <span data-ttu-id="ed3bb-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="ed3bb-128">Requirement</span></span> | <span data-ttu-id="ed3bb-129">Valore</span><span class="sxs-lookup"><span data-stu-id="ed3bb-129">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed3bb-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ed3bb-130">Minimum supported client</span></span><br/> | <span data-ttu-id="ed3bb-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="ed3bb-131">Windows 7</span></span><br/>                                                                             |
| <span data-ttu-id="ed3bb-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ed3bb-132">Minimum supported server</span></span><br/> | <span data-ttu-id="ed3bb-133">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ed3bb-133">Windows Server 2008 R2</span></span><br/>                                                                |
| <span data-ttu-id="ed3bb-134">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="ed3bb-134">Type library</span></span><br/>             | <dl> <span data-ttu-id="ed3bb-135"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ed3bb-135"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="ed3bb-136">DLL</span><span class="sxs-lookup"><span data-stu-id="ed3bb-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ed3bb-137"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ed3bb-137"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="ed3bb-138">IID</span><span class="sxs-lookup"><span data-stu-id="ed3bb-138">IID</span></span><br/>                      | <span data-ttu-id="ed3bb-139">IID \_ IMsRdpClientAdvancedSettings7 è definito come 26036036-4010-4578-8091-0db9a1edf9c3</span><span class="sxs-lookup"><span data-stu-id="ed3bb-139">IID\_IMsRdpClientAdvancedSettings7 is defined as 26036036-4010-4578-8091-0db9a1edf9c3</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ed3bb-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ed3bb-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed3bb-141">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="ed3bb-141">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="ed3bb-142">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="ed3bb-142">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> </dl>

 

 





