---
description: Il \_ messaggio di riga AGENTSTATUSEX viene inviato quando lo stato di un agente ACD viene modificato in un gestore dell'agente per il quale l'applicazione dispone attualmente di una linea aperta. Questo messaggio viene generato tramite la funzione lineProxyMessage.
ms.assetid: a0709367-9105-43af-9772-0161d94c098a
title: Messaggio di LINE_AGENTSTATUSEX (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c9ff1a39fd6aacf69922693a54198426d267720
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331034"
---
# <a name="line_agentstatusex-message"></a>\_Messaggio linea AGENTSTATUSEX

Il messaggio di **riga \_ AGENTSTATUSEX** viene inviato quando lo stato di un agente ACD viene modificato in un gestore dell'agente per il quale l'applicazione dispone attualmente di una linea aperta. Questo messaggio viene generato tramite la funzione [**lineProxyMessage**](/windows/desktop/api/Tapi/nf-tapi-lineproxymessage) .


```C++
        
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*dwDevice* 
</dt> <dd>

Handle dell'applicazione per il dispositivo linea. Questo si riferisce al gestore agenti.

</dd> <dt>

*dwCallbackInstance* 
</dt> <dd>

Istanza di callback fornita all'apertura della riga.

</dd> <dt>

*dwParam1* 
</dt> <dd>

Handle dell'agente il cui stato è stato modificato.

</dd> <dt>

*dwParam2* 
</dt> <dd>

Specifica lo stato della coda che è stato modificato. Può essere una o più delle [**\_ costanti LINEQUEUESTATUS**](linequeuestatus--constants.md).

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

[**lineGetAgentInfo**](/windows/desktop/api/Tapi/nf-tapi-linegetagentinfo)
</dt> <dt>

[**lineProxyMessage**](/windows/desktop/api/Tapi/nf-tapi-lineproxymessage)
</dt> </dl>

 

 




