---
description: Specifica la qualità di codifica per il sink multimediale Digital Living Network Alliance (DLNA).
ms.assetid: 4cf745ab-66ae-40f2-b5c4-3f72f1b9badb
title: Attributo MF_MP2DLNA_ENCODE_QUALITY (Mfmp2dlna. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81c785ff12524d45d096d566014a5c0a5e24eea8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050098"
---
# <a name="mf_mp2dlna_encode_quality-attribute"></a>\_Attributo MP2DLNA di \_ codifica \_ MF

Specifica la qualità di codifica per il sink multimediale Digital Living Network Alliance (DLNA).

## <a name="data-type"></a>Tipo di dati

**UINT32**

Intervallo: 0 – 18

## <a name="getset"></a>Ottenere/impostare

Per ottenere questo attributo, chiamare [**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Per impostare questo attributo, chiamare [**IMFAttributes::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)SetAttribute.

## <a name="remarks"></a>Commenti

I numeri più alti indicano una migliore qualità della codifica. I numeri più bassi indicano una codifica più veloce, ma la qualità della codifica è inferiore. Il valore predefinito è 9.

Per impostare questo attributo sul sink multimediale DLNA, eseguire una query sul sink multimediale per l'interfaccia [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) . Impostare l'attributo prima dell'inizio del flusso.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                             |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2008 R2 \[\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Mfmp2dlna. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli attributi di Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




