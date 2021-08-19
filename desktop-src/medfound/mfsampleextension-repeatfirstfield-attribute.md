---
description: Specifica se ripetere il primo campo in un frame interlacciato. Questo attributo si applica agli esempi di supporti.
ms.assetid: c469f418-fa23-443f-8012-0d548ee98c17
title: MFSampleExtension_RepeatFirstField attributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f0668e37e6a6958615c83f98c4b6b87eb170b115cf0549f3944a43b21c5b65d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117872421"
---
# <a name="mfsampleextension_repeatfirstfield-attribute"></a>Attributo MFSampleExtension \_ RepeatFirstField

Specifica se ripetere il primo campo in un frame interlacciato. Questo attributo si applica agli esempi di supporti.

## <a name="data-type"></a>Tipo di dati

**BOOL** archiviato come **UINT32**

## <a name="getset"></a>Ottenere/impostare

Per ottenere questo attributo, chiamare [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Per impostare questo attributo, chiamare [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>Si applica a

[**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a>Commenti

Se il valore è **FALSE** o l'attributo non è impostato, il primo campo non viene ripetuto. Se il valore è **TRUE,** il primo campo viene ripetuto. Il valore **TRUE** è valido solo quando si verificano le condizioni seguenti:

-   Il tipo di supporto è misto interlacciato e progressivo. [**L'attributo \_ MF MT \_ INTERLACE \_ MODE**](mf-mt-interlace-mode-attribute.md) nel tipo di supporto è **MFVideoInterlace \_ MixedInterlaceOrProgressive.**
-   Il frame è progressivo e [**l'attributo \_ interlacciato MFSampleExtension**](mfsampleextension-interlaced-attribute.md) nell'esempio è **TRUE.**
-   [**L'attributo MFSampleExtension \_ BottomFieldFirst**](mfsampleextension-bottomfieldfirst-attribute.md) è impostato nell'esempio. Il valore può essere **TRUE** o **FALSE.** L'ordinamento dei campi è determinato da questo attributo.

Questo attributo viene usato per il pulldown 3:2. La tabella seguente illustra l'ordine in cui vengono visualizzati i campi.



| MFSampleExtension \_ RepeatFirstField | MFSampleExtension \_ BottomFieldFirst | Ordine dei campi         |
|-------------------------------------|-------------------------------------|---------------------|
| **TRUE**                            | **TRUE**                            | Inferiore, Superiore, Inferiore |
| **TRUE**                            | **FALSE**                           | Superiore, inferiore, superiore |
| **FALSE**                           | **TRUE**                            | Inferiore, superiore        |
| **FALSE**                           | **FALSE**                           | Superiore, inferiore        |



 

La costante GUID per questo attributo viene esportata da mfuuid.lib.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows App desktop vista \[ \| app UWP\]<br/>                              |
| Server minimo supportato<br/> | Windows App desktop di Server 2008 \[ \| app UWP\]<br/>                        |
| Intestazione<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli Media Foundation personalizzati](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributi di esempio](sample-attributes.md)
</dt> <dt>

[Esempi di supporti](media-samples.md)
</dt> <dt>

[Video Interlacing](video-interlacing.md)
</dt> </dl>

 

 




