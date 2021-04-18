---
title: Attributo DTCPIPPort
description: L'attributo DTCPIPPort è il numero di porta Transmission Control Protocol (TCP) del computer o del dispositivo che deve essere contattato per lo scambio di chiave autenticato di trasmissione digitale protezione del contenuto over Internet Protocol (DTCP-IP) per l'elemento multimediale.
ms.assetid: 63767ec1-dd01-40c2-bf9a-6e9b8a7db7f8
keywords:
- Attributo DTCPIPPort Windows Media Player
topic_type:
- apiref
api_name:
- DTCPIPPort Attribute
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16c1c6117425211c0015d218412c8a9ac0971d7b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333930"
---
# <a name="dtcpipport-attribute"></a>Attributo DTCPIPPort

L'attributo **DTCPIPPort** è il numero di porta Transmission Control Protocol (TCP) del computer o del dispositivo che deve essere contattato per lo scambio di chiave autenticato di trasmissione digitale protezione del contenuto over Internet Protocol (DTCP-IP) per l'elemento multimediale.

## <a name="applies-to"></a>Si applica a

-   [**Elementi audio**](audio-item-attributes.md)
-   [**Elementi foto**](photo-item-attributes.md)
-   [**Elementi della playlist**](playlist-attributes-ref.md)
-   [**Elementi video**](video-item-attributes.md)

## <a name="remarks"></a>Commenti

Se questo attributo è disponibile, l'elemento multimediale viene protetto tramite DTCP-IP.

Questo attributo non è disponibile per gli elementi multimediali nella libreria locale dell'utente corrente. È disponibile solo per gli elementi multimediali che appartengono a una libreria remota; ovvero una libreria che è stata resa disponibile da un altro utente nella rete domestica. Per determinare se un catalogo multimediale è remoto, chiamare [**IWMPLibrary:: Get \_ Type**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibrary-get_type).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------|
| Versione<br/> | Windows Media Player 12<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Riferimento agli attributi**](attribute-reference.md)
</dt> </dl>

 

 





