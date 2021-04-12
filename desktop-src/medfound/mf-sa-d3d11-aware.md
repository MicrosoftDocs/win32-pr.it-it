---
description: Specifica se una trasformazione Media Foundation (MFT) supporta Microsoft Direct3D 11.
ms.assetid: 23482B8A-58F3-4B39-9C6D-54EC27D36C01
title: Attributo MF_SA_D3D11_AWARE (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d90f560e3d31b80c1b3fbcbb5c25c4e20815f51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344176"
---
# <a name="mf_sa_d3d11_aware-attribute"></a>\_ \_ \_ Attributo Aware SA d3d11

Specifica se una trasformazione Media Foundation (MFT) supporta Microsoft Direct3D 11.

## <a name="data-type"></a>Tipo di dati

**Bool** archiviato come **UInt32**

## <a name="remarks"></a>Commenti

Questo attributo si applica solo ai video MFTs. Per eseguire una query su questo attributo, chiamare [**IMFTransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) per ottenere l'archivio di attributi MFT. Se **GetAttributes** ha esito positivo, chiamare [**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

-   Se l'attributo è diverso da zero, il client può assegnare a MFT un puntatore all'interfaccia [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) prima dell'avvio del flusso. A tale scopo, il client invia il messaggio di [**\_ \_ \_ \_ gestione D3D message set D3D**](mft-message-set-d3d-manager.md) al MFT. Il client non è necessario per l'invio di questo messaggio.
-   Se questo attributo è zero (**false**), MFT non supporta Direct3D 11 e il client non deve inviare il messaggio [**MFT \_ message \_ set \_ D3D \_ Manager**](mft-message-set-d3d-manager.md) al MFT.

Il valore predefinito di questo attributo è **false**. Considerare questo attributo come di sola lettura. Non modificare il valore. il MFT ignorerà tutte le modifiche apportate al valore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | App desktop di Windows 8 app \[ \| UWP\]<br/>                                        |
| Server minimo supportato<br/> | App UWP per \[ app desktop di Windows Server 2012 \|\]<br/>                              |
| Intestazione<br/>                   | <dl> <dt>Mftransform. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli attributi di Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Supporto della decodifica video Direct3D 11 in Media Foundation](supporting-direct3d-11-video-decoding-in-media-foundation.md)
</dt> </dl>

 

 




