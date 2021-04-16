---
title: Metodo INapEnforcementClientConnection GetStringCorrelationId (NapEnforcementClient. h)
description: Ottiene la versione in formato stringa dell'ID utilizzato per correlare le richieste e le risposte.
ms.assetid: d744fa4e-5e30-429e-810d-7326047bb3f8
keywords:
- NAP metodo GetStringCorrelationId
- Metodo GetStringCorrelationId NAP, interfaccia INapEnforcementClientConnection
- Interfaccia INapEnforcementClientConnection NAP, metodo GetStringCorrelationId
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.GetStringCorrelationId
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6a01ca16bffb627f4ca5be38ef547980951c0ee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517578"
---
# <a name="inapenforcementclientconnectiongetstringcorrelationid-method"></a>Metodo INapEnforcementClientConnection:: GetStringCorrelationId

> [!Note]  
> La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10

 

Il metodo **INapEnforcementClientConnection:: GetStringCorrelationId** ottiene la versione in formato stringa dell'ID usato per correlare le richieste e le risposte.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetStringCorrelationId(
  [out] CountedString **correlationId
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

ID correlazione  \[ out\]
</dt> <dd>

Puntatore a una struttura [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) che contiene la versione in formato stringa dell'oggetto [**CorrelationId**](/windows/win32/api/naptypes/ns-naptypes-correlationid)della connessione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

È possibile che vengano restituiti anche altri codici di errore specifici di COM.



| Codice restituito                                                                                     | Descrizione                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | Operazione riuscita.<br/>                                    |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Errore delle autorizzazioni, accesso negato.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Limite di risorse di sistema. Impossibile eseguire l'operazione.<br/> |



 

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

 

 





