---
description: Specifica se il lettore di origine Abilita l'accelerazione video DirectX (DXVA) nel decodificatore video.
ms.assetid: ec539038-3fd3-41b7-a0e6-e75e3f2828a7
title: Attributo MF_SOURCE_READER_DISABLE_DXVA (Mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9362f067d1d6ceae426e9ee6530e08b95837595f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348736"
---
# <a name="mf_source_reader_disable_dxva-attribute"></a>MF \_ source \_ Reader \_ disabilitare l' \_ attributo DXVA

Specifica se il [lettore di origine](source-reader.md) Abilita l'accelerazione video DirectX (DXVA) nel decodificatore video.

## <a name="data-type"></a>Tipo di dati

**UINT32**

## <a name="getset"></a>Ottenere/impostare

Per ottenere questo attributo, chiamare [**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Per impostare questo attributo, chiamare [**IMFAttributes::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)SetAttribute.

## <a name="remarks"></a>Commenti

Questo attributo si applica se vengono soddisfatte le condizioni seguenti:

-   Il lettore di origine decodifica un flusso video.
-   Il decodificatore video supporta la decodifica DXVA.
-   L'applicazione usa l'attributo di [ \_ \_ \_ \_ gestione D3D del lettore di origine MF](mf-source-reader-d3d-manager.md) per impostare il [Gestione dispositivi Direct3D](direct3d-device-manager.md) nel lettore di origine.

Questo attributo consente all'applicazione di disabilitare DXVA, pur continuando a eseguire la decodifica nelle superfici Direct3D.

Per impostazione predefinita, il lettore di origine usa il [Gestione dispositivi Direct3D](direct3d-device-manager.md) per due scopi:

-   Per abilitare la decodifica DXVA nel decodificatore video.
-   Per allocare le superfici Direct3D per gli esempi video.

Se il valore dell'attributo MF \_ source \_ Reader \_ Disable \_ DXVA è **true**, il lettore di origine Disabilita la decodifica DXVA, anche se usa ancora il [Gestione dispositivi Direct3D](direct3d-device-manager.md) per allocare le superfici Direct3D.

Se l'attributo di [ \_ \_ \_ \_ gestione D3D di Reader Source Reader](mf-source-reader-d3d-manager.md) non è impostato, l'attributo MF \_ source \_ Reader \_ Disable \_ DXVA viene ignorato.

Il valore predefinito di questo attributo è **false**, vale a dire che la decodifica DXVA è abilitata quando disponibile.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | App desktop di Windows 7 \[ \| UWP\]<br/>                                        |
| Server minimo supportato<br/> | App desktop di Windows Server 2008 R2 \[ \| UWP\]<br/>                           |
| Intestazione<br/>                   | <dl> <dt>Mfreadwrite. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli attributi di Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Lettore di origine](source-reader.md)
</dt> <dt>

[Attributi lettore di origine](source-reader-attributes.md)
</dt> </dl>

 

 




