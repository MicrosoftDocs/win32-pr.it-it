---
description: Specifica se un decodificatore espone i tipi di output IYUV/I420 (adatti per la transcodifica) prima di altri formati.
ms.assetid: 8505CFA1-210A-4DA8-B92A-FCE62F0310E5
title: Attributo MFT_DECODER_EXPOSE_OUTPUT_TYPES_IN_NATIVE_ORDER (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01ecf074fa0767552a48e3238374dbd02f077404
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755279"
---
# <a name="mft_decoder_expose_output_types_in_native_order-attribute"></a>Il \_ decodificatore MFT \_ espone i \_ \_ tipi \_ di output nell' \_ \_ attributo Order nativo

Specifica se un decodificatore espone i tipi di output IYUV/I420 (adatti per la transcodifica) prima di altri formati.

## <a name="data-type"></a>Tipo di dati

**UINT32**

## <a name="remarks"></a>Commenti

Questo attributo è un suggerimento per il decodificatore per disporre l'elenco di tipi di output in un ordine particolare, a seconda dell'utilizzo previsto, ovvero la riproduzione o la transcodifica.

Per la maggior parte dei formati di codifica (H. 264, MPEG-2, WMV), i decodificatori video in Microsoft Media Foundation supportano diversi output YUV comuni, tra cui NV12, YV12, YUY2, IYUV e I420. Il decodificatore offre un elenco ordinato di tipi di output tramite il metodo [**IMFTransform:: GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) .

Per la riproduzione, NV12 è il formato più efficiente e ampiamente supportato. Pertanto, per impostazione predefinita, i decodificatori offrono in genere NV12 come primo tipo di output nell'elenco. In questo modo è possibile ridurre al minimo il tempo necessario per risolvere il tipo di supporto quando si compila una topologia di riproduzione. Per la transcodifica, tuttavia, IYUV o I420 sono più efficienti per la CPU e sono in genere preferiti dai codificatori.

Se un decodificatore supporta questo attributo, l'attributo presenta il comportamento seguente:

-   Se l'attributo ha un valore diverso da zero, IYUV e I420 vengono visualizzati per primi nell'elenco dei tipi di supporto di output. Questa impostazione è più efficiente per la transcodifica.
-   Se l'attributo è zero, NV12 viene visualizzato per primo nell'elenco dei tipi di supporto di output. Questa impostazione è più efficiente per la riproduzione ed è il valore predefinito.

Per impostare l'attributo:

1.  Chiamare [**IMFTransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) nel decodificatore per ottenere un puntatore [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .
2.  Chiamare [**IMFAttributes::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) SetAttribute per aggiungere l'attributo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | App desktop di Windows 8 app \[ \| UWP\]<br/>                                        |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                |
| Intestazione<br/>                   | <dl> <dt>Mftransform. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli attributi di Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




