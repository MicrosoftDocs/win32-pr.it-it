---
title: Interfaccia INapEnforcementClientConnection (NapEnforcementClient.h)
description: Consentire la gestione delle connessioni client. | Interfaccia INapEnforcementClientConnection (NapEnforcementClient.h)
ms.assetid: 96b94995-24b8-47ed-880e-6182d1bfe925
keywords:
- Interfaccia INapEnforcementClientConnection nap
- Interfaccia INapEnforcementClientConnection nap , descritta
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ba017ca0948c5769466be9ad43ef68dc5ff60e75ecea430c96a1e8b0c36ab1d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119686251"
---
# <a name="inapenforcementclientconnection-interface"></a>Interfaccia INapEnforcementClientConnection

> [!Note]  
> La piattaforma Protezione accesso alla rete non è disponibile a partire da Windows 10

 

**INapEnforcementClientConnection** fornisce metodi che consentono la gestione delle connessioni client.

> [!Note]  
> [**INapEnforcementClientConnection2**](inapenforcementclientconnection2.md) eredita tutti i metodi di questa interfaccia e deve essere usato.

 

## <a name="members"></a>Membri

**L'interfaccia INapEnforcementClientConnection** eredita dall'interfaccia [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **INapEnforcementClientConnection** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia INapEnforcementClientConnection** include questi metodi.



| Metodo                                                                                                                           | Descrizione                                                                                                                               |
|:---------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------|
| [**INapEnforcementClientConnection::GetConnectionId**](inapenforcementclientconnection-getconnectionid-method.md)               | Ottiene l'ID connessione del client.<br/>                                                                                          |
| [**INapEnforcementClientConnection::GetCorrelationId**](inapenforcementclientconnection-getcorrelationid-method.md)             | Ottiene l'ID utilizzato per correlare soh-requests e SoH-responses.<br/>                                                                  |
| [**INapEnforcementClientConnection::GetEnforcerPrivateData**](inapenforcementclientconnection-getenforcerprivatedata-method.md) | Usato dall'esecutore per ottenere dati privati.<br/>                                                                                      |
| [**INapEnforcementClientConnection::GetFlags**](inapenforcementclientconnection-getflags-method.md)                             | Ottiene il valore del flag che differenzia le risposte della prima volta dalle risposte a causa di SoHRequests memorizzate nella cache dagli imponitori.<br/> |
| [**INapEnforcementClientConnection::GetIsolationInfo**](inapenforcementclientconnection-getisolationinfo-method.md)             | Usato per ottenere le informazioni di isolamento del client.<br/>                                                                              |
| [**INapEnforcementClientConnection::GetMaxSize**](inapenforcementclientconnection-getmaxsize-method.md)                         | Ottiene le dimensioni massime del pacchetto SoH per questo client.<br/>                                                                       |
| [**INapEnforcementClientConnection::GetPrivateData**](inapenforcementclientconnection-getprivatedata-method.md)                 | Usato da NapAgent per ottenere dati privati.<br/>                                                                                      |
| [**INapEnforcementClientConnection::GetSoHRequest**](inapenforcementclientconnection-getsohrequest-method.md)                   | Ottiene la richiesta SoH.<br/>                                                                                                          |
| [**INapEnforcementClientConnection::GetSoHResponse**](inapenforcementclientconnection-getsohresponse-method.md)                 | Ottiene il SoH-Response ricevuto dal client di imposizione.<br/>                                                                      |
| [**INapEnforcementClientConnection::GetStringCorrelationId**](inapenforcementclientconnection-getstringcorrelationid-method.md) | Ottiene la versione stringa di CorrelationId. Usato principalmente a scopo di registrazione.<br/>                                             |
| [**INapEnforcementClientConnection::Initialize**](inapenforcementclientconnection-initialize-method.md)                         | Inizializza la raccolta.<br/>                                                                                                    |
| [**INapEnforcementClientConnection::SetConnectionId**](inapenforcementclientconnection-setconnectionid-method.md)               | Imposta l'ID di connessione del client.<br/>                                                                                          |
| [**INapEnforcementClientConnection::SetCorrelationId**](inapenforcementclientconnection-setcorrelationid-method.md)             | Imposta l'ID usato per correlare soh-requests e SoH-responses.<br/>                                                                  |
| [**INapEnforcementClientConnection::SetEnforcerPrivateData**](inapenforcementclientconnection-setenforcerprivatedata-method.md) | Usato dall'applicatore per impostare i dati privati.<br/>                                                                                      |
| [**INapEnforcementClientConnection::SetFlags**](inapenforcementclientconnection-setflags-method.md)                             | Imposta il flag che differenzia le risposte per la prima volta dalle risposte a causa di SoHRequest memorizzate nella cache dagli imponitori.<br/>                  |
| [**INapEnforcementClientConnection::SetIsolationInfo**](inapenforcementclientconnection-setisolationinfo-method.md)             | Usato da NapAgent per impostare le informazioni di isolamento del client.<br/>                                                           |
| [**INapEnforcementClientConnection::SetMaxSize**](inapenforcementclientconnection-setmaxsize-method.md)                         | Imposta le dimensioni massime del pacchetto SoH per questo client.<br/>                                                                       |
| [**INapEnforcementClientConnection::SetPrivateData**](inapenforcementclientconnection-setprivatedata-method.md)                 | Usato da NapAgent per impostare i dati privati.<br/>                                                                                      |
| [**INapEnforcementClientConnection::SetSoHRequest**](inapenforcementclientconnection-setsohrequest-method.md)                   | Imposta la richiesta SoH.<br/>                                                                                                          |
| [**INapEnforcementClientConnection::SetSoHResponse**](inapenforcementclientconnection-setsohresponse-method.md)                 | Imposta il SoH-Response e viene utilizzato dal client di imposizione alla ricezione di un pacchetto.<br/>                                             |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                                      |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                                |
| Intestazione<br/>                   | <dl> <dt>NapEnforcementClient.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapEnforcementClient.idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>               |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Interfacce di Protezione accesso alla rete](nap-interfaces.md)
</dt> <dt>

[Informazioni di riferimento su Protezione accesso alla rete](nap-reference.md)
</dt> </dl>

 

