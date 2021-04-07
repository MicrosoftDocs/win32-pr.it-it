---
title: Metodo INapEnforcementClientConnection GetCorrelationId (NapEnforcementClient. h)
description: Ottiene l'ID usato per correlare le richieste di rapporto di integrità e le risposte a rapporto di integrità.
ms.assetid: f59880d4-5de6-4163-ae01-1095ff52bf38
keywords:
- NAP metodo GetCorrelationId
- Metodo GetCorrelationId NAP, interfaccia INapEnforcementClientConnection
- Interfaccia INapEnforcementClientConnection NAP, metodo GetCorrelationId
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.GetCorrelationId
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82572cc499a61d453a70c47391e48f2004dca24d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048759"
---
# <a name="inapenforcementclientconnectiongetcorrelationid-method"></a>Metodo INapEnforcementClientConnection:: GetCorrelationId

> [!Note]  
> La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10

 

Il metodo **INapEnforcementClientConnection:: GetCorrelationId** Ottiene l'ID usato per correlare le richieste e le risposte a rapporto di integrità.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetCorrelationId(
  [out] CorrelationId *correlationId
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

ID correlazione  \[ out\]
</dt> <dd>

Struttura [**CorrelationId**](/windows/win32/api/naptypes/ns-naptypes-correlationid) univoca che identifica questo scambio di rapporto di integrità.

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

 

 





