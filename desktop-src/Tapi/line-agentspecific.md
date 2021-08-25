---
description: Il messaggio TAPI LINE AGENTSPECIFIC viene inviato quando lo stato di un agente ACD cambia in una riga attualmente \_ aperta dell'applicazione. L'applicazione può richiamare lineGetAgentStatus per determinare lo stato corrente dell'agente.
ms.assetid: 67e1796c-02e5-4f81-8086-7c2ff3112ae0
title: LINE_AGENTSPECIFIC messaggio (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a87b0e6f5c6c96842f70ebe46c0b72e33e6767c996fa2cc5b4d8e95ff0f08cd7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119867161"
---
# <a name="line_agentspecific-message"></a>LINE \_ AGENTSPECIFIC message

Il messaggio TAPI **LINE \_ AGENTSPECIFIC** viene inviato quando lo stato di un agente ACD cambia in una riga attualmente aperta dell'applicazione. L'applicazione può richiamare [**lineGetAgentStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetagentstatusa) per determinare lo stato corrente dell'agente.


```C++
            
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hDevice* 
</dt> <dd>

Handle dell'applicazione per il dispositivo line.

</dd> <dt>

*dwCallbackInstance* 
</dt> <dd>

Istanza di callback fornita all'apertura della riga della chiamata.

</dd> <dt>

*dwParam1* 
</dt> <dd>

Indice nella matrice di identificatori di estensione del gestore nella [**struttura LINEAGENTCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineagentcaps) dell'estensione del gestore a cui è associato il messaggio.

</dd> <dt>

*dwParam2* 
</dt> <dd>

Specifica dell'estensione del gestore. In genere, questo valore viene usato per fare in modo che l'applicazione richiama una [**funzione lineAgentSpecific**](/windows/desktop/api/Tapi/nf-tapi-lineagentspecific) per recuperare altri dettagli sul messaggio.

</dd> <dt>

*dwParam3* 
</dt> <dd>

Specifica dell'estensione del gestore.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Il **messaggio \_ LINE AGENTSPECIFIC** non viene inviato alle applicazioni che supportano le versioni precedenti di TAPI.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 2.0 o versione successiva<br/>                                             |
| Intestazione<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**LINEAGENTCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineagentcaps)
</dt> <dt>

[**lineAgentSpecific**](/windows/desktop/api/Tapi/nf-tapi-lineagentspecific)
</dt> <dt>

[**lineGetAgentStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetagentstatusa)
</dt> </dl>

 

 




