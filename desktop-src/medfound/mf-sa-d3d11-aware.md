---
description: Specifica se una trasformazione Media Foundation (MFT) supporta Microsoft Direct3D 11.
ms.assetid: 23482B8A-58F3-4B39-9C6D-54EC27D36C01
title: MF_SA_D3D11_AWARE attributo (Mftransform.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59a996493ace387d1c6e93c734110772274986c6e5490b9e0e08567024d47c0a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119955401"
---
# <a name="mf_sa_d3d11_aware-attribute"></a>Attributo MF \_ SA \_ D3D11 \_ AWARE

Specifica se una trasformazione Media Foundation (MFT) supporta Microsoft Direct3D 11.

## <a name="data-type"></a>Tipo di dati

**BOOL** archiviato come **UINT32**

## <a name="remarks"></a>Commenti

Questo attributo si applica solo ai MFT video. Per eseguire una query su questo attributo, chiamare [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) per ottenere l'archivio attributi MFT. Se **GetAttributes ha** esito positivo, chiamare [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

-   Se l'attributo è diverso da zero, il client può assegnare al MFT un puntatore [**all'interfaccia IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) prima dell'avvio del flusso. A tale scopo, il client invia il [**messaggio MFT \_ MESSAGE SET \_ \_ D3D \_ MANAGER**](mft-message-set-d3d-manager.md) a MFT. Il client non deve inviare questo messaggio.
-   Se questo attributo è zero **(FALSE),** MFT non supporta Direct3D 11 e il client non deve inviare il messaggio [**MFT \_ MESSAGE SET \_ \_ D3D \_ MANAGER**](mft-message-set-d3d-manager.md) a MFT.

Il valore predefinito di questo attributo è **FALSE.** Considerare questo attributo come di sola lettura. Non modificare il valore. MFT ignorerà tutte le modifiche apportate al valore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 app desktop \| app UWP\]<br/>                                        |
| Server minimo supportato<br/> | \[Windows Server 2012 app desktop \| app UWP\]<br/>                              |
| Intestazione<br/>                   | <dl> <dt>Mftransform.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli Media Foundation personalizzati](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Supporto della decodifica video Direct3D 11 in Media Foundation](supporting-direct3d-11-video-decoding-in-media-foundation.md)
</dt> </dl>

 

 




