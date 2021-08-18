---
description: Il messaggio LINE AGENTSESSIONSTATUS viene inviato quando lo stato di una sessione dell'agente ACD cambia in un gestore dell'agente per cui l'applicazione ha \_ attualmente una riga aperta. Questo messaggio viene generato usando la funzione lineProxyMessage.
ms.assetid: bb9d2292-8c41-4557-989e-6c5eb785313f
title: LINE_AGENTSESSIONSTATUS messaggio (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25209abda7cfec3864c45bfd58a35a9fad21a1aa5e5645669a7fdad6ec907d5b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119003219"
---
# <a name="line_agentsessionstatus-message"></a>MESSAGGIO \_ LINE AGENTSESSIONSTATUS

Il **messaggio LINE \_ AGENTSESSIONSTATUS** viene inviato quando lo stato di una sessione dell'agente ACD cambia in un gestore dell'agente per cui l'applicazione ha attualmente una riga aperta. Questo messaggio viene generato usando la [**funzione lineProxyMessage.**](/windows/desktop/api/Tapi/nf-tapi-lineproxymessage)


```C++
        
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*dwDevice* 
</dt> <dd>

Handle dell'applicazione per il dispositivo linea in cui è stato modificato lo stato della sessione dell'agente.

</dd> <dt>

*dwCallbackInstance* 
</dt> <dd>

Istanza di callback fornita all'apertura della riga.

</dd> <dt>

*dwParam1* 
</dt> <dd>

Handle della sessione dell'agente il cui stato è stato modificato.

</dd> <dt>

*dwParam2* 
</dt> <dd>

Specifica lo stato della sessione dell'agente che è stato modificato. Può essere uno o più di **LINE \_ AGENTSESSIONSTATUS**.

</dd> <dt>

*dwParam3* 
</dt> <dd>

Se *dwParam2* include il bit LINEAGENTSTATUSEX \_ STATE, *dwParam3* indica il nuovo valore dello stato dell'agente, che è una delle costanti [**\_ LINEAGENTSTATEEX**](lineagentstateex--constants.md).

In caso contrario, *dwParam3* viene impostato su zero.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 2.2<br/>                                                      |
| Intestazione<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**lineGetAgentSessionInfo**](/windows/desktop/api/Tapi/nf-tapi-linegetagentsessioninfo)
</dt> <dt>

[**lineProxyMessage**](/windows/desktop/api/Tapi/nf-tapi-lineproxymessage)
</dt> </dl>

 

 




