---
title: HTTP_RESPONSE_FLAG_ costanti (Http.h)
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
ms.openlocfilehash: 3099012df5be9ed4a53d3072319be6dc47ede32b71567749c4668cd7870fee29
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118394409"
---
# <a name="http_response_flag_-constants"></a>Costanti \_ HTTP RESPONSE \_ FLAG \_

Le **costanti HTTP RESPONSE \_ \_ FLAG \_** definiscono le opzioni per configurare le risposte nell'API del server HTTP.

Queste costanti vengono usate nel **membro Flags** della struttura HTTP [**RESPONSE \_ \_ V1.**](/windows/desktop/api/Http/ns-http-http_response_v1)

<dl> <dt>

<span id="HTTP_RESPONSE_FLAG_MULTIPLE_ENCODINGS_AVAILABLE"></span><span id="http_response_flag_multiple_encodings_available"></span>**FLAG DI RISPOSTA HTTP \_ \_ SONO DISPONIBILI PIÙ \_ \_ \_ CODIFICHE**
</dt> <dd> <dl> <dt>



Per questa risorsa sono disponibili codifiche diverse dal modulo di identità. Questo flag viene ignorato se l'applicazione non ha richiesto la memorizzazione nella cache della risposta. Viene usato come suggerimento per l'API del server HTTP per la negoziazione del contenuto durante la gestione dalla cache delle risposte del kernel.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 R2 \[\]<br/>                           |
| Intestazione<br/>                   | <dl> <dt>Http.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Costanti dell'API server HTTP versione 2.0](http-server-api-version-2-0-constants.md)
</dt> <dt>

[**RISPOSTA HTTP \_ \_ V1**](/windows/desktop/api/Http/ns-http-http_response_v1)
</dt> </dl>

 

 





