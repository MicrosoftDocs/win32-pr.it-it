---
title: Interfaccia INapEnforcementClientConnection (NapEnforcementClient. h)
description: Consente la gestione della connessione client. | Interfaccia INapEnforcementClientConnection (NapEnforcementClient. h)
ms.assetid: 96b94995-24b8-47ed-880e-6182d1bfe925
keywords:
- NAP interfaccia INapEnforcementClientConnection
- Interfaccia NAP di INapEnforcementClientConnection, descrizione
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
ms.openlocfilehash: 5c5f132da021e7970ec2f15a872091c101cd5c42
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104234688"
---
# <a name="inapenforcementclientconnection-interface"></a>Interfaccia INapEnforcementClientConnection

> [!Note]  
> La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10

 

**INapEnforcementClientConnection** fornisce metodi che consentono la gestione della connessione client.

> [!Note]  
> [**INapEnforcementClientConnection2**](inapenforcementclientconnection2.md) eredita tutti i metodi di questa interfaccia e deve essere usato in alternativa.

 

## <a name="members"></a>Membri

L'interfaccia **INapEnforcementClientConnection** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **INapEnforcementClientConnection** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **INapEnforcementClientConnection** dispone di questi metodi.



| Metodo                                                                                                                           | Descrizione                                                                                                                               |
|:---------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------|
| [**INapEnforcementClientConnection:: GetConnectionId**](inapenforcementclientconnection-getconnectionid-method.md)               | Ottiene l'ID connessione del client.<br/>                                                                                          |
| [**INapEnforcementClientConnection::GetCorrelationId**](inapenforcementclientconnection-getcorrelationid-method.md)             | Ottiene l'ID usato per correlare le richieste di rapporto di integrità e le risposte a rapporto di integrità.<br/>                                                                  |
| [**INapEnforcementClientConnection::GetEnforcerPrivateData**](inapenforcementclientconnection-getenforcerprivatedata-method.md) | Utilizzato dall'applicazione per ottenere i dati privati.<br/>                                                                                      |
| [**INapEnforcementClientConnection:: GetFlags**](inapenforcementclientconnection-getflags-method.md)                             | Ottiene il valore del flag che distingue le risposte per la prima volta dalle risposte dovute a SoHRequests memorizzate nella cache dalle forze di esecuzione.<br/> |
| [**INapEnforcementClientConnection::GetIsolationInfo**](inapenforcementclientconnection-getisolationinfo-method.md)             | Usato per ottenere le informazioni di isolamento del client.<br/>                                                                              |
| [**INapEnforcementClientConnection::GetMaxSize**](inapenforcementclientconnection-getmaxsize-method.md)                         | Ottiene la dimensione massima del pacchetto di rapporto di integrità per il client.<br/>                                                                       |
| [**INapEnforcementClientConnection::GetPrivateData**](inapenforcementclientconnection-getprivatedata-method.md)                 | Usato da NapAgent per ottenere i dati privati.<br/>                                                                                      |
| [**INapEnforcementClientConnection::GetSoHRequest**](inapenforcementclientconnection-getsohrequest-method.md)                   | Ottiene la richiesta di rapporto di integrità.<br/>                                                                                                          |
| [**INapEnforcementClientConnection::GetSoHResponse**](inapenforcementclientconnection-getsohresponse-method.md)                 | Ottiene la SoH-Response ricevuta dal client di imposizione.<br/>                                                                      |
| [**INapEnforcementClientConnection::GetStringCorrelationId**](inapenforcementclientconnection-getstringcorrelationid-method.md) | Ottiene la versione in formato stringa dell'oggetto CorrelationId. Utilizzato principalmente per scopi di registrazione.<br/>                                             |
| [**INapEnforcementClientConnection:: Initialize**](inapenforcementclientconnection-initialize-method.md)                         | Inizializza la raccolta.<br/>                                                                                                    |
| [**INapEnforcementClientConnection::SetConnectionId**](inapenforcementclientconnection-setconnectionid-method.md)               | Imposta l'ID connessione del client.<br/>                                                                                          |
| [**INapEnforcementClientConnection::SetCorrelationId**](inapenforcementclientconnection-setcorrelationid-method.md)             | Imposta l'ID usato per correlare le richieste di rapporto di integrità e le risposte a rapporto di integrità.<br/>                                                                  |
| [**INapEnforcementClientConnection::SetEnforcerPrivateData**](inapenforcementclientconnection-setenforcerprivatedata-method.md) | Utilizzato dall'applicazione per impostare i dati privati.<br/>                                                                                      |
| [**INapEnforcementClientConnection:: Flags**](inapenforcementclientconnection-setflags-method.md)                             | Imposta il flag che distingue le risposte per la prima volta dalle risposte dovute a SoHRequests memorizzate nella cache da Enforcer.<br/>                  |
| [**INapEnforcementClientConnection::SetIsolationInfo**](inapenforcementclientconnection-setisolationinfo-method.md)             | Utilizzato da NapAgent per impostare le informazioni di isolamento del client.<br/>                                                           |
| [**INapEnforcementClientConnection::SetMaxSize**](inapenforcementclientconnection-setmaxsize-method.md)                         | Imposta la dimensione massima del pacchetto di rapporto di integrità per il client.<br/>                                                                       |
| [**INapEnforcementClientConnection::SetPrivateData**](inapenforcementclientconnection-setprivatedata-method.md)                 | Usato da NapAgent per impostare i dati privati.<br/>                                                                                      |
| [**INapEnforcementClientConnection::SetSoHRequest**](inapenforcementclientconnection-setsohrequest-method.md)                   | Imposta la richiesta di rapporto di integrità.<br/>                                                                                                          |
| [**INapEnforcementClientConnection::SetSoHResponse**](inapenforcementclientconnection-setsohresponse-method.md)                 | Imposta il SoH-Response e viene utilizzato dal client di imposizione per la ricezione di un pacchetto.<br/>                                             |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                      |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                                |
| Intestazione<br/>                   | <dl> <dt>NapEnforcementClient. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapEnforcementClient. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>               |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Interfacce NAP](nap-interfaces.md)
</dt> <dt>

[Riferimento NAP](nap-reference.md)
</dt> </dl>

 

