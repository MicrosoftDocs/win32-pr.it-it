---
description: Specifica se un fotogramma video deinterlacciato è stato derivato dal campo superiore o dal campo inferiore.
ms.assetid: 3710ab94-afb3-44d3-a680-b4a716810ec1
title: Attributo MFSampleExtension_DerivedFromTopField (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f90a67edf0b08337748bc118b0aa4ff024ec0ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310243"
---
# <a name="mfsampleextension_derivedfromtopfield-attribute"></a>\_Attributo DerivedFromTopField di MFSampleExtension

Specifica se un fotogramma video deinterlacciato è stato derivato dal campo superiore o dal campo inferiore. Questo attributo si applica agli esempi di supporti.

## <a name="data-type"></a>Tipo di dati

**Bool** archiviato come **UInt32**

## <a name="getset"></a>Ottenere/impostare

Per ottenere questo attributo, chiamare [**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Per impostare questo attributo, chiamare [**IMFAttributes::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)SetAttribute.

## <a name="applies-to"></a>Si applica a

[**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a>Commenti

Questo attributo è valido solo per gli esempi deinterlacciati. Impostare questo attributo se il frame è stato deinterlacciato interpolando uno dei campi.

Se il valore è **true**, il campo inferiore è stato interpolato dal campo superiore. Se il valore è **false**, il campo superiore è stato interpolato dal campo inferiore.

Se l'attributo non è impostato, il frame non è stato deinterlacciato. Il frame è un frame progressivo reale oppure è un frame interlacciato.

Questo attributo è informativo. Un deinterlacciatore software può impostare questo attributo. Se questo attributo è impostato, fornisce un suggerimento che è possibile ripristinare il campo originale eliminando le righe di analisi interpolate. Se, ad esempio, l'attributo è **true**, è possibile ripristinare il campo superiore originale rimuovendo il campo inferiore interpolato.

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

 

 




