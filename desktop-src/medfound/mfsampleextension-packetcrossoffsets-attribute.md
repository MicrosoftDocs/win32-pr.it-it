---
description: Specifica gli offset ai limiti del payload in un frame per i campioni protetti.
ms.assetid: 8aa25afd-efa8-4fe0-92d4-8432f9d633c9
title: MFSampleExtension_PacketCrossOffsets attributo (Wmcontainer.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b39abdcaf0dfb5888c1705a0a76a19c3a55be522b82405f5a77345efe0d8f13e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119102307"
---
# <a name="mfsampleextension_packetcrossoffsets-attribute"></a>Attributo MFSampleExtension \_ PacketCrossOffsets

Specifica gli offset ai limiti del payload in un frame per i campioni protetti.

## <a name="data-type"></a>Tipo di dati

Matrice di byte

## <a name="getset"></a>Ottenere/impostare

Per ottenere questo attributo, chiamare [**IMFAttributes::GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).

Per impostare questo attributo, chiamare [**IMFAttributes::SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob).

## <a name="applies-to"></a>Si applica a

[**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a>Commenti

Questo attributo si applica agli esempi di supporti protetti da Windows Media Digital Rights Management (DRM). Il valore dell'attributo è una matrice **di valori DWORD.** Ogni voce nella matrice è l'offset di un limite di payload, relativo all'inizio del frame. Un'applicazione può usare questi valori durante la decrittografia e la ricostruzione dei fotogrammi.

La costante GUID per questo attributo viene esportata da mfuuid.lib.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows App desktop vista \[ \| app UWP\]<br/>                                    |
| Server minimo supportato<br/> | Windows App desktop di Server 2008 \[ \| app UWP\]<br/>                              |
| Intestazione<br/>                   | <dl> <dt>Wmcontainer.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli Media Foundation personalizzati](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Barra di divisione ASF](asf-splitter.md)
</dt> <dt>

[Attributi di esempio](sample-attributes.md)
</dt> <dt>

[Esempi di supporti](media-samples.md)
</dt> </dl>

 

 




