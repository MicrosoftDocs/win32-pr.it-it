---
description: Imposta Gestione dispositivi microsoft DirectX Graphic Infrastructure (DXGI) nel motore multimediale.
ms.assetid: CB952492-0ACF-4501-BD8B-133E26FCE8F7
title: MF_MEDIA_ENGINE_DXGI_MANAGER attributo (Mfmediaengine.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c454041f83a58cdb5b3c1e340d63908386546090eb52811e0c876e5d8bed0bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119723054"
---
# <a name="mf_media_engine_dxgi_manager-attribute"></a>Attributo MF \_ MEDIA \_ ENGINE \_ DXGI \_ MANAGER

Imposta Gestione dispositivi microsoft DirectX Graphic Infrastructure (DXGI) nel motore multimediale.

## <a name="data-type"></a>Tipo di dati

**IMFDXGIDeviceManager \* *_ archiviato come _* IUnknown\***

## <a name="getset"></a>Ottenere/impostare

Per ottenere questo attributo, chiamare [**IMFAttributes::GetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).

Per impostare questo attributo, chiamare [**IMFAttributes::SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).

## <a name="remarks"></a>Commenti

Il valore di questo attributo è un puntatore [**all'interfaccia IMFDXGIDeviceManager.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager)

In modalità server frame, questo attributo consente al motore multimediale di usare l'accelerazione hardware per la decodifica video e l'elaborazione video. Se l'attributo non è impostato, il motore multimediale usa la decodifica e l'elaborazione software.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 app desktop \| app UWP\]<br/>                                          |
| Server minimo supportato<br/> | \[Windows Server 2012 app desktop \| app UWP\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Mfmediaengine.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico di Media Foundation attributi](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFMediaEngineClassFactory::CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance)
</dt> </dl>

 

 




