---
description: Specifica la dominanza del campo per un fotogramma video interlacciato.
ms.assetid: 680c42e4-2808-46ed-98a8-c77b14a55def
title: Attributo MFSampleExtension_BottomFieldFirst (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e608160c92fa53e8cde6adee1831d6c3e8789bc4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344866"
---
# <a name="mfsampleextension_bottomfieldfirst-attribute"></a>\_Attributo BottomFieldFirst di MFSampleExtension

Specifica la dominanza del campo per un fotogramma video interlacciato. Questo attributo si applica agli esempi di supporti.

## <a name="data-type"></a>Tipo di dati

**Bool** archiviato come **UInt32**

## <a name="getset"></a>Ottenere/impostare

Per ottenere questo attributo, chiamare [**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Per impostare questo attributo, chiamare [**IMFAttributes::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)SetAttribute.

## <a name="applies-to"></a>Si applica a

[**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a>Commenti

Se il fotogramma video è interlacciato e l'esempio contiene due campi con interfoliazione, questo attributo indica il campo che viene visualizzato per primo. Se **true**, il campo inferiore è il primo nel tempo. Se **false**, il campo superiore è primo.

Se il frame è interlacciato e l'esempio contiene un solo campo, questo attributo indica il campo contenuto nell'esempio. Se **true**, l'esempio contiene il campo in basso. Se **false**, l'esempio contiene il campo superiore.

Se il frame è progressivo, questo attributo descrive il modo in cui i campi devono essere ordinati quando l'output è interlacciato. Se **true**, il campo inferiore dovrebbe essere l'output per primo. Se **false**, il campo superiore deve essere restituito per primo.

Se questo attributo non è impostato, il tipo di supporto descrive la dominanza dei campi.

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

 

 




