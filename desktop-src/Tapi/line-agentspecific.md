---
description: Il messaggio della linea TAPI \_ AGENTSPECIFIC viene inviato quando lo stato di un agente ACD viene modificato su una linea attualmente aperta dall'applicazione. L'applicazione può richiamare lineGetAgentStatus per determinare lo stato corrente dell'agente.
ms.assetid: 67e1796c-02e5-4f81-8086-7c2ff3112ae0
title: Messaggio di LINE_AGENTSPECIFIC (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20ca03138ce00f11520e2e0f1df8e810e21d1186
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331041"
---
# <a name="line_agentspecific-message"></a>\_Messaggio linea AGENTSPECIFIC

Il messaggio della **linea TAPI \_ AGENTSPECIFIC** viene inviato quando lo stato di un agente ACD viene modificato su una linea attualmente aperta dall'applicazione. L'applicazione può richiamare [**lineGetAgentStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetagentstatusa) per determinare lo stato corrente dell'agente.


```C++
            
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hDevice* 
</dt> <dd>

Handle dell'applicazione per il dispositivo linea.

</dd> <dt>

*dwCallbackInstance* 
</dt> <dd>

Istanza di callback fornita all'apertura della riga della chiamata.

</dd> <dt>

*dwParam1* 
</dt> <dd>

Indice nella matrice di identificatori di estensione del gestore nella struttura [**LINEAGENTCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineagentcaps) dell'estensione del gestore a cui è associato il messaggio.

</dd> <dt>

*dwParam2* 
</dt> <dd>

Specifico dell'estensione del gestore. In genere, questo valore viene usato per fare in modo che l'applicazione richiami una funzione [**lineAgentSpecific**](/windows/desktop/api/Tapi/nf-tapi-lineagentspecific) per recuperare ulteriori dettagli sul messaggio.

</dd> <dt>

*dwParam3* 
</dt> <dd>

Specifico dell'estensione del gestore.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Il messaggio di **riga \_ AGENTSPECIFIC** non viene inviato ad applicazioni che supportano le versioni precedenti di TAPI.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 2,0 o versione successiva<br/>                                             |
| Intestazione<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**LINEAGENTCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineagentcaps)
</dt> <dt>

[**lineAgentSpecific**](/windows/desktop/api/Tapi/nf-tapi-lineagentspecific)
</dt> <dt>

[**lineGetAgentStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetagentstatusa)
</dt> </dl>

 

 




