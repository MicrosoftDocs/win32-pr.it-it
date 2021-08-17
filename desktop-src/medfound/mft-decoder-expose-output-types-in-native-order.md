---
description: Specifica se un decodificatore espone i tipi di output IYUV/I420 (adatti per la transcoding) prima di altri formati.
ms.assetid: 8505CFA1-210A-4DA8-B92A-FCE62F0310E5
title: MFT_DECODER_EXPOSE_OUTPUT_TYPES_IN_NATIVE_ORDER attributo (Mftransform.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46b91492054215aee5a63dbcf0adf300d74933a0859a2d71256e7e4352deba9e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117872340"
---
# <a name="mft_decoder_expose_output_types_in_native_order-attribute"></a>IL DECODIFICATORE MFT \_ ESPONE I TIPI DI OUTPUT \_ \_ \_ \_ \_ \_ NELL'attributo ORDER NATIVO

Specifica se un decodificatore espone i tipi di output IYUV/I420 (adatti per la transcoding) prima di altri formati.

## <a name="data-type"></a>Tipo di dati

**UINT32**

## <a name="remarks"></a>Commenti

Questo attributo è un suggerimento che consente al decodificatore di disporre l'elenco dei tipi di output in un ordine specifico, a seconda dell'uso previsto, riproduzione o transcodifica.

Per la maggior parte dei formati di codifica (H.264, MPEG-2, WMV), i decodificatori video in Microsoft Media Foundation supportano diversi output YUV comuni, tra cui NV12, YV12, YUY2, IYUV e I420. Il decodificatore offre un elenco ordinato di tipi di output tramite il relativo [**metodo IMFTransform::GetOutputAvailableType.**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype)

Per la riproduzione, NV12 è il formato più efficiente e ampiamente supportato. Pertanto, per impostazione predefinita, i decodificatori offrono in genere NV12 come primo tipo di output nell'elenco. In questo modo si riduce al minimo il tempo necessario per risolvere il tipo di contenuto multimediale durante la creazione di una topologia di riproduzione. Per la transcoding, tuttavia, IYUV o I420 sono più efficienti per la CPU e sono in genere preferiti dai codificatori.

Se un decodificatore supporta questo attributo, l'attributo presenta il comportamento seguente:

-   Se l'attributo ha un valore diverso da zero, IYUV e I420 vengono visualizzati per primi nell'elenco dei tipi di supporti di output. Questa impostazione è più efficiente per la transcoding.
-   Se l'attributo è zero, NV12 viene visualizzato per primo nell'elenco dei tipi di supporti di output. Questa impostazione è più efficiente per la riproduzione ed è l'impostazione predefinita.

Per impostare questo attributo:

1.  Chiamare [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) sul decodificatore per ottenere un [**puntatore IMFAttributes.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)
2.  Chiamare [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) per aggiungere l'attributo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 app desktop \| app UWP\]<br/>                                        |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                |
| Intestazione<br/>                   | <dl> <dt>Mftransform.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli Media Foundation personalizzati](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




