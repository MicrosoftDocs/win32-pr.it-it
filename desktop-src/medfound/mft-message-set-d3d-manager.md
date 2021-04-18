---
description: Imposta o cancella il Gestione dispositivi Direct3D per DirectX video Accereration (DXVA).
ms.assetid: fd346d56-1f80-488a-94c8-4e4e36d72890
title: MFT_MESSAGE_SET_D3D_MANAGER (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef8ecb5db474935bb25138a960b6df1c2109c16c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310214"
---
# <a name="mft_message_set_d3d_manager"></a><span data-ttu-id="2bd6e-103">\_ \_ Gestione D3D del set di messaggi MFT \_ \_</span><span class="sxs-lookup"><span data-stu-id="2bd6e-103">MFT\_MESSAGE\_SET\_D3D\_MANAGER</span></span>

<span data-ttu-id="2bd6e-104">Imposta o cancella il [Gestione dispositivi Direct3D](direct3d-device-manager.md) per DirectX video ACCERERATION (DXVA).</span><span class="sxs-lookup"><span data-stu-id="2bd6e-104">Sets or clears the [Direct3D Device Manager](direct3d-device-manager.md) for DirectX Video Accereration (DXVA).</span></span>

## <a name="message-parameter"></a><span data-ttu-id="2bd6e-105">Parametro del messaggio</span><span class="sxs-lookup"><span data-stu-id="2bd6e-105">Message Parameter</span></span>

<span data-ttu-id="2bd6e-106">Quando inizia il flusso, il parametro *ulParam* contiene un puntatore **IUnknown** .</span><span class="sxs-lookup"><span data-stu-id="2bd6e-106">When streaming begins, the *ulParam* parameter contains an **IUnknown** pointer.</span></span> <span data-ttu-id="2bd6e-107">Il MFT eseguirà una query su questo puntatore per l'interfaccia [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) per Direct3D 9 e l'interfaccia [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) per Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="2bd6e-107">The MFT will query this pointer for the [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) interface for Direct3D 9 and the [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) interface for Direct3D 11.</span></span> <span data-ttu-id="2bd6e-108">Quando il flusso si interrompe, *ulParameter* contiene il valore **null**.</span><span class="sxs-lookup"><span data-stu-id="2bd6e-108">When streaming stops, the *ulParameter* contains the value **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="2bd6e-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="2bd6e-109">Remarks</span></span>

<span data-ttu-id="2bd6e-110">Per inviare questo messaggio, chiamare [**IMFTransform::P rocessmessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).</span><span class="sxs-lookup"><span data-stu-id="2bd6e-110">To send this message, call [**IMFTransform::ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).</span></span>

<span data-ttu-id="2bd6e-111">Questo messaggio si applica solo alle trasformazioni video.</span><span class="sxs-lookup"><span data-stu-id="2bd6e-111">This message applies only to video transforms.</span></span> <span data-ttu-id="2bd6e-112">Il client non deve inviare questo messaggio, a meno che il MFT non restituisca **true** per l'attributo di compatibilità con la compatibilità [**MF \_ sa \_ \_**](mf-sa-d3d-aware-attribute.md) ([MF \_ sa \_ d3d11 \_ Aware](mf-sa-d3d11-aware.md) for Direct3D 11).</span><span class="sxs-lookup"><span data-stu-id="2bd6e-112">The client should not send this message unless the MFT returns **TRUE** for the [**MF\_SA\_D3D\_AWARE**](mf-sa-d3d-aware-attribute.md) attribute ([MF\_SA\_D3D11\_AWARE](mf-sa-d3d11-aware.md) for Direct3D 11).</span></span>

<span data-ttu-id="2bd6e-113">Non inviare questo messaggio a un MFT con più output.</span><span class="sxs-lookup"><span data-stu-id="2bd6e-113">Do not send this message to an MFT with multiple ouputs.</span></span>

### <a name="implementation"></a><span data-ttu-id="2bd6e-114">Implementazione</span><span class="sxs-lookup"><span data-stu-id="2bd6e-114">Implementation</span></span>

<span data-ttu-id="2bd6e-115">Un MFT deve supportare questo messaggio solo se il MFT usa l'accelerazione video DirectX per l'elaborazione o la decodifica dei video.</span><span class="sxs-lookup"><span data-stu-id="2bd6e-115">An MFT should support this message only if the MFT uses DirectX Video Acceleration for video processing or decoding.</span></span>

<span data-ttu-id="2bd6e-116">Se un MFT supporta questo messaggio, deve implementare anche il metodo [**IMFTransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) e restituire il valore **true** per l'attributo di compatibilità con l'applicazione [**MF \_ sa \_ D3D \_**](mf-sa-d3d-aware-attribute.md) (([MF \_ sa \_ d3d11 \_ Aware](mf-sa-d3d11-aware.md) per Direct3D 11).</span><span class="sxs-lookup"><span data-stu-id="2bd6e-116">If an MFT supports this message, it should also implement the [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) method and return the value **TRUE** for the [**MF\_SA\_D3D\_AWARE**](mf-sa-d3d-aware-attribute.md) attribute (([MF\_SA\_D3D11\_AWARE](mf-sa-d3d11-aware.md) for Direct3D 11).</span></span> <span data-ttu-id="2bd6e-117">Questo attributo informa il client che il client deve inviare il messaggio **MFT \_ message set \_ di \_ \_ gestione D3D** a MFT prima che venga avviato il flusso.</span><span class="sxs-lookup"><span data-stu-id="2bd6e-117">This attribute informs the client that the client should send the **MFT\_MESSAGE\_SET\_D3D\_MANAGER** message to the MFT before streaming begins.</span></span>

<span data-ttu-id="2bd6e-118">Se un MFT non supporta questo messaggio, deve restituire **e \_ NOTIMPL** da [**ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).</span><span class="sxs-lookup"><span data-stu-id="2bd6e-118">If an MFT does not support this message, it should return **E\_NOTIMPL** from [**ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).</span></span> <span data-ttu-id="2bd6e-119">Si tratta di un'eccezione alla regola generale che un MFT **può restituire da \_** qualsiasi messaggio ignorato.</span><span class="sxs-lookup"><span data-stu-id="2bd6e-119">This is an exception to the general rule that an MFT can return **S\_OK** from any message it ignores.</span></span>

<span data-ttu-id="2bd6e-120">Per altre informazioni, vedere [MFTS compatibile con Direct3D](direct3d-aware-mfts.md).</span><span class="sxs-lookup"><span data-stu-id="2bd6e-120">For more information, see [Direct3D-Aware MFTs](direct3d-aware-mfts.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2bd6e-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2bd6e-121">Requirements</span></span>



| <span data-ttu-id="2bd6e-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="2bd6e-122">Requirement</span></span> | <span data-ttu-id="2bd6e-123">Valore</span><span class="sxs-lookup"><span data-stu-id="2bd6e-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="2bd6e-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2bd6e-124">Minimum supported client</span></span><br/> | <span data-ttu-id="2bd6e-125">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2bd6e-125">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="2bd6e-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2bd6e-126">Minimum supported server</span></span><br/> | <span data-ttu-id="2bd6e-127">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="2bd6e-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="2bd6e-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2bd6e-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="2bd6e-129"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="2bd6e-129"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2bd6e-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2bd6e-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2bd6e-131">MFTs compatibili con Direct3D</span><span class="sxs-lookup"><span data-stu-id="2bd6e-131">Direct3D-Aware MFTs</span></span>](direct3d-aware-mfts.md)
</dt> <dt>

[<span data-ttu-id="2bd6e-132">Supporto di DXVA 2,0 in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="2bd6e-132">Supporting DXVA 2.0 in Media Foundation</span></span>](supporting-dxva-2-0-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="2bd6e-133">Supporto della decodifica video Direct3D 11 in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="2bd6e-133">Supporting Direct3D 11 Video Decoding in Media Foundation</span></span>](supporting-direct3d-11-video-decoding-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="2bd6e-134">**\_tipo di messaggio MFT \_**</span><span class="sxs-lookup"><span data-stu-id="2bd6e-134">**MFT\_MESSAGE\_TYPE**</span></span>](/windows/desktop/api/mftransform/ne-mftransform-mft_message_type)
</dt> </dl>

 

 




