---
description: Per un tipo di supporto che descrive un flusso di trasporto MPEG-2 (TS), specifica se i pacchetti di trasporto contengono intestazioni dei pacchetti di contenuto.
ms.assetid: 527B965D-4330-4DCB-B6DA-32D6BCDF5515
title: Attributo MF_MT_MPEG2_CONTENT_PACKET (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: acb297081a150ab3aa5b842be9b5792d849e2457
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883217"
---
# <a name="mf_mt_mpeg2_content_packet-attribute"></a>\_ \_ \_ Attributo pacchetto di contenuto \_ MPEG2 MF mt

Per un tipo di supporto che descrive un flusso di trasporto MPEG-2 (TS), specifica se i pacchetti di trasporto contengono intestazioni dei pacchetti di contenuto.

## <a name="data-type"></a>Tipo di dati

**UINT32**



| Valore                                                                                                | Significato                                                                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="0"></span><dl> <dt>**0**</dt> </dl> | Non sono state aggiunte intestazioni di pacchetti di contenuto.<br/>                                                                                                                                                                    |
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | A intervalli di 200 – 1000 millisecondi, l'intestazione di un pacchetto di contenuto a 14 byte viene aggiunta all'inizio del pacchetto di trasporto, come definito dall'associazione dello standard radio Industries and business (ARIB).<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | App desktop di Windows 8 app \[ \| UWP\]<br/>                                  |
| Server minimo supportato<br/> | App UWP per \[ app desktop di Windows Server 2012 \|\]<br/>                        |
| Intestazione<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli attributi di Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




