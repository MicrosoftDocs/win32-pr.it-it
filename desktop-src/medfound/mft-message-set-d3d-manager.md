---
description: Imposta o cancella Gestione dispositivi Direct3D per DirectX Video Accereration (DXVA).
ms.assetid: fd346d56-1f80-488a-94c8-4e4e36d72890
title: MFT_MESSAGE_SET_D3D_MANAGER (Mftransform.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a0e7ccbf9f28615b17e6acded6ecc932334b4fb0fa4a607d6fd6213ba2cd214
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119848067"
---
# <a name="mft_message_set_d3d_manager"></a>MFT \_ MESSAGE \_ SET \_ D3D \_ MANAGER

Imposta o cancella [Gestione dispositivi Direct3D per](direct3d-device-manager.md) DirectX Video Accereration (DXVA).

## <a name="message-parameter"></a>Parametro del messaggio

Quando inizia il flusso, il *parametro ulParam* contiene un **puntatore IUnknown.** MFT esegue una query su questo puntatore per [**l'interfaccia IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) per Direct3D 9 e l'interfaccia [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) per Direct3D 11. Quando il flusso si arresta, *ulParameter* contiene il valore **NULL.**

## <a name="remarks"></a>Commenti

Per inviare questo messaggio, chiamare [**IMFTransform::P rocessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).

Questo messaggio si applica solo alle trasformazioni video. Il client non deve inviare questo messaggio a meno che MFT non restituisca **TRUE** per l'attributo [**MF \_ SA \_ D3D \_ AWARE**](mf-sa-d3d-aware-attribute.md) [(MF \_ SA \_ D3D11 \_ AWARE](mf-sa-d3d11-aware.md) per Direct3D 11).

Non inviare questo messaggio a un MFT con più output.

### <a name="implementation"></a>Implementazione

Un MFT deve supportare questo messaggio solo se il MFT usa l'accelerazione video DirectX per l'elaborazione o la decodifica video.

Se un MFT supporta questo messaggio, deve implementare anche il metodo [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) e restituire il valore **TRUE** per l'attributo [**MF \_ SA \_ D3D \_ AWARE**](mf-sa-d3d-aware-attribute.md) (([MF \_ SA \_ D3D11 \_ AWARE](mf-sa-d3d11-aware.md) per Direct3D 11). Questo attributo informa il client che il client deve inviare il messaggio **MFT \_ MESSAGE SET \_ \_ D3D \_ MANAGER** a MFT prima dell'inizio del flusso.

Se un MFT non supporta questo messaggio, deve restituire **E \_ NOTIMPL** da [**ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage). Si tratta di un'eccezione alla regola generale che un MFT può restituire **S \_ OK** da qualsiasi messaggio ignorato.

Per altre informazioni, vedere [MFT con supporto direct3D.](direct3d-aware-mfts.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                           |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                     |
| Intestazione<br/>                   | <dl> <dt>Mftransform.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[MFT con riconoscere Direct3D](direct3d-aware-mfts.md)
</dt> <dt>

[Supporto di DXVA 2.0 in Media Foundation](supporting-dxva-2-0-in-media-foundation.md)
</dt> <dt>

[Supporto della decodifica video Direct3D 11 in Media Foundation](supporting-direct3d-11-video-decoding-in-media-foundation.md)
</dt> <dt>

[**TIPO DI \_ MESSAGGIO \_ MFT**](/windows/desktop/api/mftransform/ne-mftransform-mft_message_type)
</dt> </dl>

 

 




