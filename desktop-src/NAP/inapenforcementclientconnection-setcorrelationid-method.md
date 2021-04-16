---
title: Metodo INapEnforcementClientConnection SetCorrelationId (NapEnforcementClient. h)
description: Imposta l'ID usato per correlare le richieste di rapporto di integrità e le risposte a rapporto di integrità.
ms.assetid: 8f9d5bde-95b1-4566-84ee-31c6ed5e8986
keywords:
- NAP metodo SetCorrelationId
- Metodo SetCorrelationId NAP, interfaccia INapEnforcementClientConnection
- Interfaccia INapEnforcementClientConnection NAP, metodo SetCorrelationId
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.SetCorrelationId
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c99576b8302f7fcf949f132cf110a5ac5f675ec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517577"
---
# <a name="inapenforcementclientconnectionsetcorrelationid-method"></a>Metodo INapEnforcementClientConnection:: SetCorrelationId

> [!Note]  
> La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10

 

Il metodo **INapEnforcementClientConnection:: SetCorrelationId** imposta l'ID usato per correlare le richieste e le risposte a rapporto di integrità.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetCorrelationId(
  [in] CorrelationId correlationId
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

ID correlazione  \[ in\]
</dt> <dd>

Struttura [**CorrelationId**](/windows/win32/api/naptypes/ns-naptypes-correlationid) univoca che identifica uno scambio di rapporto di integrità specifico.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

È possibile che vengano restituiti anche altri codici di errore specifici di COM.



| Codice restituito                                                                                     | Descrizione                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | Operazione riuscita.<br/>                                    |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Errore delle autorizzazioni, accesso negato.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Limite di risorse di sistema. Impossibile eseguire l'operazione.<br/> |



 

## <a name="remarks"></a>Commenti

L'ID di correlazione viene impostato da NapAgent e in base all'ID connessione.

Questo ID viene usato per correlare le richieste e le risposte, ovvero descrive in modo univoco uno scambio di rapporto di integrità e contiene sempre l'ID del set di integrità più recente per l'oggetto connessione.

Quando viene ricevuta una SoH-Response, il NapAgent garantisce prima di tutto gli ID corrispondenti; in caso contrario, viene restituito un errore e l'applicazione deve eliminare il pacchetto. Per ulteriori informazioni, vedere [**INapEnforcementClientBinding::P rocesssohresponse**](inapenforcementclientbinding-processsohresponse-method.md) .

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

[**INapEnforcementClientConnection**](inapenforcementclientconnection.md)
</dt> </dl>

 

 





