---
title: Metodo INapEnforcementClientConnection SetCorrelationId (NapEnforcementClient.h)
description: Imposta l'ID usato per correlare soh-requests e SoH-responses.
ms.assetid: 8f9d5bde-95b1-4566-84ee-31c6ed5e8986
keywords:
- Metodo SetCorrelationId nap
- Metodo SetCorrelationId NAP , interfaccia INapEnforcementClientConnection
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
ms.openlocfilehash: 9be8a7fbcbe9e2accd074768b8a0e50d6ce2dcaa2bda53e063cb76d294ff92c5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118368261"
---
# <a name="inapenforcementclientconnectionsetcorrelationid-method"></a>Metodo INapEnforcementClientConnection::SetCorrelationId

> [!Note]  
> La piattaforma Protezione accesso alla rete non è disponibile a partire da Windows 10

 

Il **metodo INapEnforcementClientConnection::SetCorrelationId** imposta l'ID usato per correlare le richieste SoH e le risposte SoH.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetCorrelationId(
  [in] CorrelationId correlationId
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*correlationId* \[ Pollici\]
</dt> <dd>

Struttura [**CorrelationId univoca**](/windows/win32/api/naptypes/ns-naptypes-correlationid) che identifica uno scambio SoH specifico.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Possono essere restituiti anche altri codici di errore specifici di COM.



| Codice restituito                                                                                     | Descrizione                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | Operazione riuscita.<br/>                                    |
| <dl> <dt>**E \_ ACCESSO NEGATO**</dt> </dl> | Errore di autorizzazioni, accesso negato.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Limite di risorse di sistema: impossibile eseguire l'operazione.<br/> |



 

## <a name="remarks"></a>Commenti

Correlation-id viene impostato da NapAgent e in base all'ID connessione.

Questo ID viene usato per correlare richieste e risposte, ad esempio descrive in modo univoco uno scambio SoH e contiene sempre l'ID del set SoH più recente nell'oggetto connessione.

Quando viene ricevuto SoH-Response, NapAgent garantisce prima di tutto che gli ID corrispondano. In caso contrario, viene restituito un errore e l'applicatore deve eliminare il pacchetto. Per altri dettagli, vedere [**INapEnforcementClientBinding::P rocessSoHResponse.**](inapenforcementclientbinding-processsohresponse-method.md)

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

[**INapEnforcementClientConnection**](inapenforcementclientconnection.md)
</dt> </dl>

 

 





