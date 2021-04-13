---
title: Metodo INapEnforcementClientBinding ProcessSoHResponse (NapEnforcementClient. h)
description: Viene usato dai client di imposizione per elaborare un SoHResponse ogni volta che ricevono un BLOB di dati SoHResponse dal server di imposizione.
ms.assetid: 6ff6d2c5-9ebe-4d8c-aa27-03147e2e1122
keywords:
- NAP metodo ProcessSoHResponse
- Metodo ProcessSoHResponse NAP, interfaccia INapEnforcementClientBinding
- Interfaccia INapEnforcementClientBinding NAP, metodo ProcessSoHResponse
topic_type:
- apiref
api_name:
- INapEnforcementClientBinding.ProcessSoHResponse
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2ac8c87314ca1e28163428bf53e4a1fc6e31106
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519174"
---
# <a name="inapenforcementclientbindingprocesssohresponse-method"></a>INapEnforcementClientBinding::P metodo rocessSoHResponse

> [!Note]  
> La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10

 

Il metodo **INapEnforcementClientBinding::P rocesssohresponse** viene usato dai client di imposizione per elaborare un SoHResponse ogni volta che ricevono un BLOB di dati SoHResponse dal server di imposizione.

## <a name="syntax"></a>Sintassi


```C++
HRESULT ProcessSoHResponse(
  [in] INapEnforcementClientConnection *connection
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*connessione* \[ a in\]
</dt> <dd>

Puntatore COM all'interfaccia [**INapEnforcementClientConnection**](inapenforcementclientconnection.md) della connessione client. Il NapAgent non tiene i riferimenti all'oggetto associato a questa interfaccia dopo il completamento della chiamata al metodo.

È necessario usare una connessione stabilita in precedenza per elaborare i BLOB di dati SOHResponse.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

È possibile che vengano restituiti anche altri codici di errore specifici di COM.



| Codice restituito                                                                                             | Descrizione                                                                                                                                                                                                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                   | L'operazione è riuscita.<br/>                                                                                                                                                                                                                                                                                            |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>            | Nessuna connessione è stata creata in precedenza nel client di imposizione. <br/>                                                                                                                                                                                                                                                 |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl>         | Errore delle autorizzazioni, accesso negato.<br/>                                                                                                                                                                                                                                                                                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>          | Limite di risorse di sistema. Impossibile eseguire l'operazione.<br/>                                                                                                                                                                                                                                                                 |
| <dl> <dt>**NAP \_ E \_ pacchetto non valido \_**</dt> </dl>  | Se questo valore viene restituito, il client di imposizione deve eliminare il pacchetto se NapAgent restituisce NAP \_ E \_ pacchetto non valido \_ . In questo caso, l'applicazione deve presupporre che il server a cui si sta comunicando non sia abilitato per la protezione accesso alla rete e rimuovere la connessione dall'elenco attivo (ad esempio, notificare il NapAgent di uno stato di connessione).<br/> |
| <dl> <dt>**\_ID NAP E non \_ corrispondente \_**</dt> </dl>   | Se questo valore viene restituito, significa che l'ID di correlazione nel pacchetto di SoH-Response non corrisponde alla risposta con rapporto di integrità in attesa. In questo caso, l'applicazione deve eliminare il pacchetto e attendere un altro pacchetto di SoH-Response più recente.<br/> Questo problema può essere causato da una risposta a un messaggio di richiesta precedente.<br/>        |
| <dl> <dt>**NAP \_ E \_ non \_ inizializzato**</dt> </dl> | L'applicazione non è stata inizializzata in precedenza.<br/>                                                                                                                                                                                                                                                                       |



 

## <a name="remarks"></a>Commenti

Il NapAgent interroga il BLOB di dati SoH-Response dall'oggetto connessione, lo elabora e imposta la decisione risultante, ad esempio accesso completo/limitato/e così via) per l'oggetto connessione.

Il client di imposizione deve chiamare il metodo [**INapEnforcementClientBinding:: Initialize**](inapenforcementclientbinding-initialize-method.md) prima di chiamare questo o qualsiasi altro metodo dell'interfaccia [**INapEnforcementClientBinding**](inapenforcementclientbinding.md) .

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


</dt> <dt>

[**INapEnforcementClientBinding**](inapenforcementclientbinding.md)
</dt> <dt>

[**INapEnforcementClientConnection**](inapenforcementclientconnection.md)
</dt> </dl>

 

 





