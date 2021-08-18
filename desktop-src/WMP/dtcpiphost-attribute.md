---
title: Attributo DTCPIPHost
description: L'attributo DTCPIPHost è il nome o l'indirizzo IP del computer o del dispositivo che deve essere contattato per digital transmission protezione del contenuto over Internet Protocol (DTCP-IP) Authenticated Key Exchange (AKE) per l'elemento multimediale.
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
ms.openlocfilehash: 88eaa85b756a46b1333db2e5eabda9cbaf86a702f5ae9c8225d6f6d8928e2d2d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118996951"
---
# <a name="dtcpiphost-attribute"></a>Attributo DTCPIPHost

**L'attributo DTCPIPHost** è il nome o l'indirizzo IP del computer o del dispositivo che deve essere contattato per l'elemento multimediale Digital Transmission protezione del contenuto over Internet Protocol (DTCP-IP) Authenticated Key Exchange (AKE).

## <a name="applies-to"></a>Si applica a

-   [**Elementi audio**](audio-item-attributes.md)
-   [**Elementi foto**](photo-item-attributes.md)
-   [**Elementi della playlist**](playlist-attributes-ref.md)
-   [**Elementi video**](video-item-attributes.md)

## <a name="remarks"></a>Commenti

Se questo attributo è disponibile, l'elemento multimediale è protetto tramite DTCP-IP.

Questo attributo non è disponibile per gli elementi multimediali nella libreria locale dell'utente corrente. È disponibile solo per gli elementi multimediali che appartengono a una libreria remota. una libreria resa disponibile da un altro utente nella rete domestica. Per determinare se una libreria multimediale è remota, chiamare [**IWMPLibrary::get \_ di tipo**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibrary-get_type).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------|
| Versione<br/> | Windows Media Player 12<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Informazioni di riferimento su attributi**](attribute-reference.md)
</dt> </dl>

 

 





