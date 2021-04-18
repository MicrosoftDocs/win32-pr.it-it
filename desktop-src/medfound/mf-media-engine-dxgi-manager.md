---
description: Imposta Microsoft DirectX Graphics Infrastructure (DXGI) Gestione dispositivi nel motore multimediale.
ms.assetid: CB952492-0ACF-4501-BD8B-133E26FCE8F7
title: Attributo MF_MEDIA_ENGINE_DXGI_MANAGER (Mfmediaengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98e731b5aa2449ae772427c6743ec4f97b5d7601
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320484"
---
# <a name="mf_media_engine_dxgi_manager-attribute"></a>\_Attributo MF media \_ Engine \_ DXGI \_ Manager

Imposta Microsoft DirectX Graphics Infrastructure (DXGI) Gestione dispositivi nel motore multimediale.

## <a name="data-type"></a>Tipo di dati

**IMFDXGIDeviceManager \* *_ archiviato come _* IUnknown\***

## <a name="getset"></a>Ottenere/impostare

Per ottenere questo attributo, chiamare [**IMFAttributes:: getunknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).

Per impostare questo attributo, chiamare [**IMFAttributes:: seunknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).

## <a name="remarks"></a>Commenti

Il valore di questo attributo è un puntatore all'interfaccia [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) .

In modalità frame-server questo attributo consente al motore multimediale di usare l'accelerazione hardware per la decodifica video e l'elaborazione video. Se l'attributo non è impostato, il motore multimediale usa la decodifica software e l'elaborazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | App desktop di Windows 8 app \[ \| UWP\]<br/>                                          |
| Server minimo supportato<br/> | App UWP per \[ app desktop di Windows Server 2012 \|\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Mfmediaengine. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli attributi di Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFMediaEngineClassFactory:: CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance)
</dt> </dl>

 

 




