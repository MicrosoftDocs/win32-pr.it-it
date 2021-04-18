---
title: Costanti HTTP_RESPONSE_FLAG_ (http. h)
description: Definire le opzioni per configurare le risposte nell'API del server HTTP.
ms.assetid: bcb59457-fd22-4166-8a72-ba85209ec8c7
topic_type:
- apiref
api_name:
- HTTP_RESPONSE_FLAG_MULTIPLE_ENCODINGS_AVAILABLE
api_location:
- http.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 96b7c34d453c1b9bbe45cf2c85ad268b414f3439
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301378"
---
# <a name="http_response_flag_-constants"></a>\_Costanti del \_ flag di risposta http \_

Le costanti del **\_ \_ flag \_ di risposta http** definiscono le opzioni per la configurazione delle risposte nell'API del server http.

Queste costanti vengono usate nel membro dei **flag** della struttura della [**\_ risposta http \_ V1**](/windows/desktop/api/Http/ns-http-http_response_v1) .

<dl> <dt>

<span id="HTTP_RESPONSE_FLAG_MULTIPLE_ENCODINGS_AVAILABLE"></span><span id="http_response_flag_multiple_encodings_available"></span>**\_flag di risposta http \_ \_ più \_ codifiche \_ disponibili**
</dt> <dd> <dl> <dt>



Per questa risorsa sono disponibili codifiche diverse dal formato Identity. Questo flag viene ignorato se all'applicazione non è stata richiesta la memorizzazione della risposta nella cache. Viene usato come suggerimento per l'API del server HTTP per la negoziazione del contenuto quando serve dalla cache di risposta del kernel.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                        |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2008 R2 \[\]<br/>                           |
| Intestazione<br/>                   | <dl> <dt>Http. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Costanti API server HTTP versione 2,0](http-server-api-version-2-0-constants.md)
</dt> <dt>

[**\_Risposta http \_ V1**](/windows/desktop/api/Http/ns-http-http_response_v1)
</dt> </dl>

 

 





