---
description: Specifica il CLSID di un plug-in di post-elaborazione per un dispositivo di acquisizione video.
ms.assetid: 8F626FAA-C7B8-4DBA-BD65-7CE97CBF3A86
title: Attributo MF_DEVICESTREAM_EXTENSION_PLUGIN_CLSID (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25c7ea9973b73cf6f1157eb19609293f2766d38f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307976"
---
# <a name="mf_devicestream_extension_plugin_clsid-attribute"></a>\_ \_ \_ Attributo CLSID del plug \_ -in dell'estensione MF DEVICESTREAM

Specifica il CLSID di un plug-in di post-elaborazione per un dispositivo di acquisizione video.

## <a name="data-type"></a>Tipo di dati

**GUID**

## <a name="remarks"></a>Commenti

Un plug-in di post-elaborazione è un MFT che elabora l'immagine video dopo che è stata acquisita. Il fornitore dell'hardware può includere un plug-in di post-elaborazione come parte del pacchetto di installazione. In tal caso, l'origine di acquisizione video imposta \_ l' \_ \_ attributo CLSID del plug-in dell'estensione MF DEVICESTREAM sul \_ CLSID del plug-in.

Per ottenere questo attributo, procedere come segue:

1.  Eseguire una query sull'origine multimediale per l'interfaccia [**IMFMediaSourceEx**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourceex) .
2.  Chiamare [**IMFMediaSourceEx:: GetStreamAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getstreamattributes) per ottenere un puntatore [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) per il flusso.
3.  Chiamare [**IMFAttributes:: GetGuid**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid) per ottenere l'attributo.

Per creare il plug-in, chiamare [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                         |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli attributi di Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
