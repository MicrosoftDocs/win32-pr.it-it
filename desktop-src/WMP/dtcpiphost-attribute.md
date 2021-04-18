---
title: Attributo DTCPIPHost
description: L'attributo DTCPIPHost è il nome o l'indirizzo IP del computer o del dispositivo che deve essere contattato per lo scambio di chiave autenticato di trasmissione digitale protezione del contenuto over Internet Protocol (DTCP-IP) per l'elemento multimediale.
ms.assetid: 61b7d6fb-c216-49ae-811a-8ce42fdb71e4
keywords:
- Attributo DTCPIPHost Windows Media Player
topic_type:
- apiref
api_name:
- DTCPIPHost Attribute
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9983cac920f2d11b9040e03af30e10b9c0c3fbcb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331240"
---
# <a name="dtcpiphost-attribute"></a>Attributo DTCPIPHost

L'attributo **DTCPIPHost** è il nome o l'indirizzo IP del computer o del dispositivo che deve essere contattato per lo scambio di chiave autenticato di trasmissione digitale protezione del contenuto over Internet Protocol (DTCP-IP) per l'elemento multimediale.

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

 

 





