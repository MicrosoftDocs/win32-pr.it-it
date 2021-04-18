---
description: Il messaggio di riga \_ AGENTSESSIONSTATUS viene inviato quando lo stato di una sessione dell'agente ACD viene modificato in un gestore dell'agente per il quale l'applicazione dispone attualmente di una linea aperta. Questo messaggio viene generato tramite la funzione lineProxyMessage.
ms.assetid: bb9d2292-8c41-4557-989e-6c5eb785313f
title: Messaggio di LINE_AGENTSESSIONSTATUS (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d53c14290dfb6bda3889e7d2b87d8d3ca5e651c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331043"
---
# <a name="line_agentsessionstatus-message"></a>\_Messaggio linea AGENTSESSIONSTATUS

Il messaggio di **riga \_ AGENTSESSIONSTATUS** viene inviato quando lo stato di una sessione dell'agente ACD viene modificato in un gestore dell'agente per il quale l'applicazione dispone attualmente di una linea aperta. Questo messaggio viene generato tramite la funzione [**lineProxyMessage**](/windows/desktop/api/Tapi/nf-tapi-lineproxymessage) .


```C++
        
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*dwDevice* 
</dt> <dd>

Handle dell'applicazione per il dispositivo della linea in cui è stato modificato lo stato della sessione dell'agente.

</dd> <dt>

*dwCallbackInstance* 
</dt> <dd>

Istanza di callback fornita all'apertura della riga.

</dd> <dt>

*dwParam1* 
</dt> <dd>

Handle della sessione di Agent il cui stato è stato modificato.

</dd> <dt>

*dwParam2* 
</dt> <dd>

Specifica lo stato della sessione dell'agente che è stato modificato. Può essere una o più **righe \_ AGENTSESSIONSTATUS**.

</dd> <dt>

*dwParam3* 
</dt> <dd>

Se *dwParam2* include il \_ bit di stato LINEAGENTSTATUSEX, *dwParam3* indica il nuovo valore dello stato dell'agente, che corrisponde a una [**delle \_ costanti LINEAGENTSTATEEX**](lineagentstateex--constants.md).

In caso contrario, *dwParam3* è impostato su zero.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 2,2<br/>                                                      |
| Intestazione<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**lineGetAgentSessionInfo**](/windows/desktop/api/Tapi/nf-tapi-linegetagentsessioninfo)
</dt> <dt>

[**lineProxyMessage**](/windows/desktop/api/Tapi/nf-tapi-lineproxymessage)
</dt> </dl>

 

 




