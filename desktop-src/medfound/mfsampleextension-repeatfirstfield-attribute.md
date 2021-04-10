---
description: Specifica se ripetere il primo campo in un frame interlacciato. Questo attributo si applica agli esempi di supporti.
ms.assetid: c469f418-fa23-443f-8012-0d548ee98c17
title: Attributo MFSampleExtension_RepeatFirstField (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0af10157c280a3e48ed8f415529534fc97fd5cc2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130519"
---
# <a name="mfsampleextension_repeatfirstfield-attribute"></a>\_Attributo RepeatFirstField di MFSampleExtension

Specifica se ripetere il primo campo in un frame interlacciato. Questo attributo si applica agli esempi di supporti.

## <a name="data-type"></a>Tipo di dati

**Bool** archiviato come **UInt32**

## <a name="getset"></a>Ottenere/impostare

Per ottenere questo attributo, chiamare [**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Per impostare questo attributo, chiamare [**IMFAttributes::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)SetAttribute.

## <a name="applies-to"></a>Si applica a

[**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a>Commenti

Se il valore è **false** o l'attributo non è impostato, il primo campo non viene ripetuto. Se il valore è **true**, il primo campo viene ripetuto. Il valore **true** è valido solo quando sono soddisfatte le condizioni seguenti:

-   Il tipo di supporto è misto interlacciato e progressivo. L'attributo dell'attributo della [**\_ \_ \_ modalità di interpolazione MF mt**](mf-mt-interlace-mode-attribute.md) sul tipo di supporto è **MFVideoInterlace \_ MixedInterlaceOrProgressive**.
-   Il frame è progressivo e l'attributo [**\_ interlacciato MFSampleExtension**](mfsampleextension-interlaced-attribute.md) nell'esempio è **true**.
-   L' [**attributo \_ BottomFieldFirst di MFSampleExtension**](mfsampleextension-bottomfieldfirst-attribute.md) è impostato nell'esempio. Il valore può essere **true** o **false**. L'ordinamento dei campi è determinato da questo attributo.

Questo attributo viene usato per la discesa 3:2. La tabella seguente mostra l'ordine in cui vengono visualizzati i campi.



| \_RepeatFirstField MFSampleExtension | \_BottomFieldFirst MFSampleExtension | Ordine campi         |
|-------------------------------------|-------------------------------------|---------------------|
| **TRUE**                            | **TRUE**                            | Inferiore, superiore, inferiore |
| **TRUE**                            | **FALSE**                           | Superiore, inferiore, superiore |
| **FALSE**                           | **TRUE**                            | Inferiore, superiore        |
| **FALSE**                           | **FALSE**                           | Superiore, inferiore        |



 

La costante GUID per questo attributo viene esportata da mfuuid. lib.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | App desktop di Windows Vista app \[ \| UWP\]<br/>                              |
| Server minimo supportato<br/> | App UWP per \[ app desktop di Windows Server 2008 \|\]<br/>                        |
| Intestazione<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli attributi di Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributi di esempio](sample-attributes.md)
</dt> <dt>

[Esempi di supporti](media-samples.md)
</dt> <dt>

[Interlacciamento video](video-interlacing.md)
</dt> </dl>

 

 




