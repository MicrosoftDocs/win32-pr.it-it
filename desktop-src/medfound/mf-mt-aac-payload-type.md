---
description: Specifica il tipo di payload di un flusso AAC (Advanced Audio Coding).
ms.assetid: a032fcf4-2584-4047-adbd-d94d4fc4e841
title: Attributo MF_MT_AAC_PAYLOAD_TYPE (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd3edba98bdac54b12fb6e3e44fb67373f7fce6a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324708"
---
# <a name="mf_mt_aac_payload_type-attribute"></a>\_Attributo del \_ \_ tipo di payload MF mt AAC \_

Specifica il tipo di payload di un flusso AAC (Advanced Audio Coding).

## <a name="data-type"></a>Tipo di dati

**UINT32**

Sono possibili i valori seguenti.



| Valore                                                                        | Significato                                                                                                                           |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | Il flusso contiene solo elementi di blocco di dati non elaborati \_ \_ .<br/>                                                                    |
| <dl> <dt>1</dt> </dl> | Flusso di trasporto dati audio (ADTS). Il flusso contiene una \_ sequenza ADTS, come definito da MPEG-2.<br/>                       |
| <dl> <dt>2</dt> </dl> | Formato di interscambio dati audio (ADIF). Il flusso contiene una \_ sequenza ADIF, come definito da MPEG-2.<br/>                     |
| <dl> <dt>3</dt> </dl> | Il flusso contiene un flusso di trasporto audio MPEG-4 con un livello di sincronizzazione (LOAS) e un livello multiplex (LATM).<br/> |



 

## <a name="getset"></a>Ottenere/impostare

Per ottenere questo attributo, chiamare [**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Per impostare questo attributo, chiamare [**IMFAttributes::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)SetAttribute.

## <a name="applies-to"></a>Si applica a

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a>Commenti

Il \_ tipo di payload MF mt \_ AAC \_ \_ è facoltativo. Se questo attributo non viene specificato, viene usato il valore predefinito 0, che specifica che il flusso contiene \_ solo elementi di blocco di dati non elaborati \_ .

Si applica solo a **MFAudioFormat \_ AAC**.

La costante GUID per questo attributo viene esportata da mfuuid. lib.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli attributi di Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributi del tipo di supporto](media-type-attributes.md)
</dt> </dl>

 

 




