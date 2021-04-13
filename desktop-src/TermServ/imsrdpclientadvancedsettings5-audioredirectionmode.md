---
title: Proprietà AudioRedirectionMode di IMsRdpClientAdvancedSettings5
description: Imposta e recupera la modalità di reindirizzamento audio e diverse opzioni di reindirizzamento audio.
ms.assetid: c0f5762b-00fd-40bb-ac97-3351b999f38d
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà AudioRedirectionMode
- Servizi Desktop remoto proprietà AudioRedirectionMode, interfaccia IMsRdpClientAdvancedSettings5
- Interfaccia IMsRdpClientAdvancedSettings5 Servizi Desktop remoto, proprietà AudioRedirectionMode
- Servizi Desktop remoto proprietà AudioRedirectionMode, interfaccia IMsRdpClientAdvancedSettings6
- Interfaccia IMsRdpClientAdvancedSettings6 Servizi Desktop remoto, proprietà AudioRedirectionMode
- Servizi Desktop remoto proprietà AudioRedirectionMode, interfaccia IMsRdpClientAdvancedSettings7
- Interfaccia IMsRdpClientAdvancedSettings7 Servizi Desktop remoto, proprietà AudioRedirectionMode
- Servizi Desktop remoto proprietà AudioRedirectionMode, interfaccia IMsRdpClientAdvancedSettings8
- Interfaccia IMsRdpClientAdvancedSettings8 Servizi Desktop remoto, proprietà AudioRedirectionMode
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings5.AudioRedirectionMode
- IMsRdpClientAdvancedSettings5.get_AudioRedirectionMode
- IMsRdpClientAdvancedSettings5.put_AudioRedirectionMode
- IMsRdpClientAdvancedSettings6.AudioRedirectionMode
- IMsRdpClientAdvancedSettings6.get_AudioRedirectionMode
- IMsRdpClientAdvancedSettings6.put_AudioRedirectionMode
- IMsRdpClientAdvancedSettings7.AudioRedirectionMode
- IMsRdpClientAdvancedSettings7.get_AudioRedirectionMode
- IMsRdpClientAdvancedSettings7.put_AudioRedirectionMode
- IMsRdpClientAdvancedSettings8.AudioRedirectionMode
- IMsRdpClientAdvancedSettings8.get_AudioRedirectionMode
- IMsRdpClientAdvancedSettings8.put_AudioRedirectionMode
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b40be8b8e63f210d060c0f585c9fe31328ac6ed6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340523"
---
# <a name="imsrdpclientadvancedsettings5audioredirectionmode-property"></a><span data-ttu-id="0a41b-112">Proprietà IMsRdpClientAdvancedSettings5:: AudioRedirectionMode</span><span class="sxs-lookup"><span data-stu-id="0a41b-112">IMsRdpClientAdvancedSettings5::AudioRedirectionMode property</span></span>

<span data-ttu-id="0a41b-113">Imposta e recupera la modalità di reindirizzamento audio e diverse opzioni di reindirizzamento audio.</span><span class="sxs-lookup"><span data-stu-id="0a41b-113">Sets and retrieves the audio redirection mode and different audio redirection options.</span></span>

<span data-ttu-id="0a41b-114">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="0a41b-114">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="0a41b-115">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0a41b-115">Syntax</span></span>


```C++
HRESULT put_AudioRedirectionMode(
  [in]  UINT uiAudioRedirectionMode
);

HRESULT get_AudioRedirectionMode(
  [out] UINT *puiAudioRedirectionMode
);
```



## <a name="property-value"></a><span data-ttu-id="0a41b-116">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="0a41b-116">Property value</span></span>

<span data-ttu-id="0a41b-117">Imposta valori diversi per la modalità di reindirizzamento audio.</span><span class="sxs-lookup"><span data-stu-id="0a41b-117">Sets different values for the audio redirection mode.</span></span> <span data-ttu-id="0a41b-118">Questo parametro presenta i valori possibili seguenti.</span><span class="sxs-lookup"><span data-stu-id="0a41b-118">This parameter has the following possible values.</span></span>

<dt>

<span id="AUDIO_MODE_REDIRECT___0"></span><span id="audio_mode_redirect___0"></span>

<span data-ttu-id="0a41b-119">**Audio \_ \_Reindirizzamento modalità 0** (il reindirizzamento audio è abilitato e l'opzione per il reindirizzamento è "porta a questo computer".</span><span class="sxs-lookup"><span data-stu-id="0a41b-119">**AUDIO\_MODE\_REDIRECT 0** (Audio redirection is enabled and the option for redirection is "Bring to this computer".</span></span> <span data-ttu-id="0a41b-120">Questa è la modalità predefinita.</span><span class="sxs-lookup"><span data-stu-id="0a41b-120">This is the default mode.)</span></span>


</dt> <dd></dd> <dt>

<span id="AUDIO_MODE_PLAY_ON_SERVER_1"></span><span id="audio_mode_play_on_server_1"></span>

<span data-ttu-id="0a41b-121">**Audio \_ MODALITÀ \_ Play \_ sul \_ Server 1** (il reindirizzamento audio è abilitato e l'opzione è "leave at remote computer".</span><span class="sxs-lookup"><span data-stu-id="0a41b-121">**AUDIO\_MODE\_PLAY\_ON\_SERVER 1** (Audio redirection is enabled and the option is "Leave at remote computer".</span></span> <span data-ttu-id="0a41b-122">L'opzione "lascia nel computer remoto" è supportata solo quando ci si connette in remoto a un computer host che esegue Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="0a41b-122">The "Leave at remote computer" option is supported only when connecting remotely to a host computer that is running Windows Vista.</span></span> <span data-ttu-id="0a41b-123">Se la connessione è a un computer host che esegue Windows Server 2008, l'opzione "lascia in remoto computer" viene modificata in "non riprodurre".</span><span class="sxs-lookup"><span data-stu-id="0a41b-123">If the connection is to a host computer that is running Windows Server 2008, the option "Leave at remote computer" is changed to "Do not play".)</span></span>


</dt> <dd></dd> <dt>

<span id="AUDIO_MODE_NONE_2"></span><span id="audio_mode_none_2"></span>

<span data-ttu-id="0a41b-124">**Audio \_ MODALITÀ \_ nessuno 2** (il reindirizzamento audio è abilitato e la modalità è "non riprodurre").</span><span class="sxs-lookup"><span data-stu-id="0a41b-124">**AUDIO\_MODE\_NONE 2** (Audio redirection is enabled and the mode is "Do not play".)</span></span>


<span data-ttu-id="0a41b-125"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="0a41b-125"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="0a41b-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0a41b-126">Requirements</span></span>



| <span data-ttu-id="0a41b-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="0a41b-127">Requirement</span></span> | <span data-ttu-id="0a41b-128">Valore</span><span class="sxs-lookup"><span data-stu-id="0a41b-128">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0a41b-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0a41b-129">Minimum supported client</span></span><br/> | <span data-ttu-id="0a41b-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0a41b-130">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="0a41b-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0a41b-131">Minimum supported server</span></span><br/> | <span data-ttu-id="0a41b-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0a41b-132">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="0a41b-133">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="0a41b-133">Type library</span></span><br/>             | <dl> <span data-ttu-id="0a41b-134"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0a41b-134"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="0a41b-135">DLL</span><span class="sxs-lookup"><span data-stu-id="0a41b-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0a41b-136"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0a41b-136"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="0a41b-137">IID</span><span class="sxs-lookup"><span data-stu-id="0a41b-137">IID</span></span><br/>                      | <span data-ttu-id="0a41b-138">IID \_ IMsRdpClientAdvancedSettings5 è definito come FBA7F64E-6783-4405-DA45-FA4A763DABD0</span><span class="sxs-lookup"><span data-stu-id="0a41b-138">IID\_IMsRdpClientAdvancedSettings5 is defined as FBA7F64E-6783-4405-DA45-FA4A763DABD0</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0a41b-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0a41b-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a41b-140">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="0a41b-140">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="0a41b-141">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="0a41b-141">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="0a41b-142">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="0a41b-142">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="0a41b-143">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="0a41b-143">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> </dl>

 

 





