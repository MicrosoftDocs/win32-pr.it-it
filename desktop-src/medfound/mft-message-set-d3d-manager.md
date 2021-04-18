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
# <a name="mft_message_set_d3d_manager"></a>\_ \_ Gestione D3D del set di messaggi MFT \_ \_

Imposta o cancella il [Gestione dispositivi Direct3D](direct3d-device-manager.md) per DirectX video ACCERERATION (DXVA).

## <a name="message-parameter"></a>Parametro del messaggio

Quando inizia il flusso, il parametro *ulParam* contiene un puntatore **IUnknown** . Il MFT eseguirà una query su questo puntatore per l'interfaccia [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) per Direct3D 9 e l'interfaccia [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) per Direct3D 11. Quando il flusso si interrompe, *ulParameter* contiene il valore **null**.

## <a name="remarks"></a>Commenti

Per inviare questo messaggio, chiamare [**IMFTransform::P rocessmessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).

Questo messaggio si applica solo alle trasformazioni video. Il client non deve inviare questo messaggio, a meno che il MFT non restituisca **true** per l'attributo di compatibilità con la compatibilità [**MF \_ sa \_ \_**](mf-sa-d3d-aware-attribute.md) ([MF \_ sa \_ d3d11 \_ Aware](mf-sa-d3d11-aware.md) for Direct3D 11).

Non inviare questo messaggio a un MFT con più output.

### <a name="implementation"></a>Implementazione

Un MFT deve supportare questo messaggio solo se il MFT usa l'accelerazione video DirectX per l'elaborazione o la decodifica dei video.

Se un MFT supporta questo messaggio, deve implementare anche il metodo [**IMFTransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) e restituire il valore **true** per l'attributo di compatibilità con l'applicazione [**MF \_ sa \_ D3D \_**](mf-sa-d3d-aware-attribute.md) (([MF \_ sa \_ d3d11 \_ Aware](mf-sa-d3d11-aware.md) per Direct3D 11). Questo attributo informa il client che il client deve inviare il messaggio **MFT \_ message set \_ di \_ \_ gestione D3D** a MFT prima che venga avviato il flusso.

Se un MFT non supporta questo messaggio, deve restituire **e \_ NOTIMPL** da [**ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage). Si tratta di un'eccezione alla regola generale che un MFT **può restituire da \_** qualsiasi messaggio ignorato.

Per altre informazioni, vedere [MFTS compatibile con Direct3D](direct3d-aware-mfts.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                     |
| Intestazione<br/>                   | <dl> <dt>Mftransform. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[MFTs compatibili con Direct3D](direct3d-aware-mfts.md)
</dt> <dt>

[Supporto di DXVA 2,0 in Media Foundation](supporting-dxva-2-0-in-media-foundation.md)
</dt> <dt>

[Supporto della decodifica video Direct3D 11 in Media Foundation](supporting-direct3d-11-video-decoding-in-media-foundation.md)
</dt> <dt>

[**\_tipo di messaggio MFT \_**](/windows/desktop/api/mftransform/ne-mftransform-mft_message_type)
</dt> </dl>

 

 




