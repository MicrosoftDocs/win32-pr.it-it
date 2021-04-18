---
description: Specifica se una trasformazione Media Foundation (MFT) supporta l'accelerazione video DirectX (DXVA). Questo attributo si applica solo ai video MFTs.
ms.assetid: db6a8b20-fda0-4ffe-b1b5-a77b7604d290
title: Attributo MF_SA_D3D_AWARE (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2eb0de8c5a66eaa89f66becf6770f69e6449c1c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314539"
---
# <a name="mf_sa_d3d_aware-attribute"></a>\_Attributo in \_ grado di \_ riconoscere D3D per MF SA

Specifica se una trasformazione Media Foundation (MFT) supporta l'accelerazione video DirectX (DXVA). Questo attributo si applica solo ai video MFTs.

## <a name="data-type"></a>Tipo di dati

**Bool** archiviato come **UInt32**

## <a name="remarks"></a>Commenti

Per eseguire una query su questo attributo, chiamare [**IMFTransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) per ottenere l'archivio di attributi globale di MFT. Se **GetAttributes** ha esito positivo, chiamare [**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Questo attributo indica al client se MFT può usare il video Direct3D 9:

-   Se l'attributo è diverso da zero, il client può assegnare a MFT un puntatore all'interfaccia [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) prima dell'avvio del flusso. A tale scopo, il client invia il messaggio di [**\_ \_ \_ \_ gestione D3D message set D3D**](mft-message-set-d3d-manager.md) al MFT. Il client non è necessario per l'invio di questo messaggio.
-   Se questo attributo è zero (**false**), MFT non supporta il video Direct3D 9 e il client non deve inviare il messaggio [**MFT \_ message set \_ di \_ \_ gestione D3D**](mft-message-set-d3d-manager.md) al MFT.

Il valore predefinito di questo attributo è **false**. Considerare questo attributo come di sola lettura. Non modificare il valore. il MFT ignorerà tutte le modifiche apportate al valore.

Per altre informazioni sull'implementazione di questo attributo in un MFT personalizzato, vedere [MFTS compatibile con Direct3D](direct3d-aware-mfts.md).

La costante GUID per questo attributo viene esportata da mfuuid. lib.

## <a name="examples"></a>Esempio

Il codice seguente verifica se un MFT supporta DXVA.


```C++
// Returns TRUE is an MFT supports DirectX Video Acceleration.

BOOL IsTransformD3DAware(IMFTransform *pMFT)
{
    BOOL bD3DAware = FALSE;
    
    IMFAttributes *pAttributes = NULL;

    HRESULT hr = pMFT->GetAttributes(&pAttributes);
    if (SUCCEEDED(hr))
    {
        bD3DAware = MFGetAttributeUINT32(pAttributes, MF_SA_D3D_AWARE, FALSE);
        pAttributes->Release();
    }
    return bD3DAware;
}
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | App desktop di Windows Vista app \[ \| UWP\]<br/>                                    |
| Server minimo supportato<br/> | App UWP per \[ app desktop di Windows Server 2008 \|\]<br/>                              |
| Intestazione<br/>                   | <dl> <dt>Mftransform. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli attributi di Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[MFTs compatibili con Direct3D](direct3d-aware-mfts.md)
</dt> <dt>

[Supporto di DXVA 2,0 in Media Foundation](supporting-dxva-2-0-in-media-foundation.md)
</dt> <dt>

[Trasformazioni Media Foundation](media-foundation-transforms.md)
</dt> <dt>

[Attributi di trasformazione](transform-attributes.md)
</dt> <dt>

[**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes:: seuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[\_Modalità DXVA topologia MF \_ \_](mf-topology-dxva-mode.md)
</dt> </dl>

 

 




