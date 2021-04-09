---
title: Proprietà AudioCaptureRedirectionMode di IMsRdpClientAdvancedSettings7
description: Specifica o recupera un valore booleano che indica se il dispositivo di input audio predefinito viene reindirizzato dal client alla sessione remota.
ms.assetid: e75add5e-4652-41a7-b2cb-2c60793cd079
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà AudioCaptureRedirectionMode
- Servizi Desktop remoto proprietà AudioCaptureRedirectionMode, interfaccia IMsRdpClientAdvancedSettings7
- Interfaccia IMsRdpClientAdvancedSettings7 Servizi Desktop remoto, proprietà AudioCaptureRedirectionMode
- Servizi Desktop remoto proprietà AudioCaptureRedirectionMode, interfaccia IMsRdpClientAdvancedSettings8
- Interfaccia IMsRdpClientAdvancedSettings8 Servizi Desktop remoto, proprietà AudioCaptureRedirectionMode
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings7.AudioCaptureRedirectionMode
- IMsRdpClientAdvancedSettings7.get_AudioCaptureRedirectionMode
- IMsRdpClientAdvancedSettings7.put_AudioCaptureRedirectionMode
- IMsRdpClientAdvancedSettings8.AudioCaptureRedirectionMode
- IMsRdpClientAdvancedSettings8.get_AudioCaptureRedirectionMode
- IMsRdpClientAdvancedSettings8.put_AudioCaptureRedirectionMode
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c752315067ed70103da2e048e9e8f613665ae919
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964426"
---
# <a name="imsrdpclientadvancedsettings7audiocaptureredirectionmode-property"></a><span data-ttu-id="4b8e2-108">Proprietà IMsRdpClientAdvancedSettings7:: AudioCaptureRedirectionMode</span><span class="sxs-lookup"><span data-stu-id="4b8e2-108">IMsRdpClientAdvancedSettings7::AudioCaptureRedirectionMode property</span></span>

<span data-ttu-id="4b8e2-109">Specifica o recupera un valore booleano che indica se il dispositivo di input audio predefinito viene reindirizzato dal client alla sessione remota.</span><span class="sxs-lookup"><span data-stu-id="4b8e2-109">Specifies or retrieves a Boolean value that indicates whether the default audio input device is redirected from the client to the remote session.</span></span>

<span data-ttu-id="4b8e2-110">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="4b8e2-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b8e2-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4b8e2-111">Syntax</span></span>


```C++
HRESULT put_AudioCaptureRedirectionMode(
  [in]          VARIANT_BOOL fRedir
);

HRESULT get_AudioCaptureRedirectionMode(
  [out, retval] VARIANT_BOOL *pfRedir
);
```



## <a name="property-value"></a><span data-ttu-id="4b8e2-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="4b8e2-112">Property value</span></span>

<span data-ttu-id="4b8e2-113">Valore **\_ bool Variant** che specifica se l'acquisizione audio viene reindirizzata.</span><span class="sxs-lookup"><span data-stu-id="4b8e2-113">A **VARIANT\_BOOL** value that specifies whether audio capture is redirected.</span></span> <span data-ttu-id="4b8e2-114">Specificare **Variant \_ true** se si vuole che l'acquisizione audio venga reindirizzata.</span><span class="sxs-lookup"><span data-stu-id="4b8e2-114">Specify **VARIANT\_TRUE** if you want audio capture to be redirected.</span></span>

## <a name="requirements"></a><span data-ttu-id="4b8e2-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4b8e2-115">Requirements</span></span>



| <span data-ttu-id="4b8e2-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="4b8e2-116">Requirement</span></span> | <span data-ttu-id="4b8e2-117">Valore</span><span class="sxs-lookup"><span data-stu-id="4b8e2-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4b8e2-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4b8e2-118">Minimum supported client</span></span><br/> | <span data-ttu-id="4b8e2-119">Windows 7</span><span class="sxs-lookup"><span data-stu-id="4b8e2-119">Windows 7</span></span><br/>                                                                             |
| <span data-ttu-id="4b8e2-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4b8e2-120">Minimum supported server</span></span><br/> | <span data-ttu-id="4b8e2-121">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="4b8e2-121">Windows Server 2008 R2</span></span><br/>                                                                |
| <span data-ttu-id="4b8e2-122">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="4b8e2-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="4b8e2-123"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4b8e2-123"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="4b8e2-124">DLL</span><span class="sxs-lookup"><span data-stu-id="4b8e2-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4b8e2-125"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4b8e2-125"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="4b8e2-126">IID</span><span class="sxs-lookup"><span data-stu-id="4b8e2-126">IID</span></span><br/>                      | <span data-ttu-id="4b8e2-127">IID \_ IMsRdpClientAdvancedSettings7 è definito come 26036036-4010-4578-8091-0db9a1edf9c3</span><span class="sxs-lookup"><span data-stu-id="4b8e2-127">IID\_IMsRdpClientAdvancedSettings7 is defined as 26036036-4010-4578-8091-0db9a1edf9c3</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4b8e2-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4b8e2-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b8e2-129">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="4b8e2-129">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="4b8e2-130">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="4b8e2-130">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> </dl>

 

 





