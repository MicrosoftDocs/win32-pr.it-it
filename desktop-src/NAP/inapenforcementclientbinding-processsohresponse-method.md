---
title: Metodo INapEnforcementClientBinding ProcessSoHResponse (NapEnforcementClient.h)
description: Viene usato dai client di imposizione per elaborare un oggetto SoHResponse ogni volta che ricevono un BLOB di dati SoHResponse dal server di imposizione.
ms.assetid: 6ff6d2c5-9ebe-4d8c-aa27-03147e2e1122
keywords:
- Metodo ProcessSoHResponse NAP
- Metodo ProcessSoHResponse NAP , interfaccia INapEnforcementClientBinding
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
ms.openlocfilehash: 4cffd2caeaf3a39bd5c28b4850fc560dc9567a3552aad88929581efd2729acce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118621710"
---
# <a name="inapenforcementclientbindingprocesssohresponse-method"></a>Metodo INapEnforcementClientBinding::P rocessSoHResponse

> [!Note]  
> La piattaforma Protezione accesso alla rete non è disponibile a partire da Windows 10

 

Il **metodo INapEnforcementClientBinding::P rocessSoHResponse** viene usato dai client di imposizione per elaborare un oggetto SoHResponse ogni volta che ricevono un BLOB di dati SoHResponse dal server di imposizione.

## <a name="syntax"></a>Sintassi


```C++
HRESULT ProcessSoHResponse(
  [in] INapEnforcementClientConnection *connection
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*connessione* \[ Pollici\]
</dt> <dd>

Puntatore COM [**all'interfaccia INapEnforcementClientConnection**](inapenforcementclientconnection.md) della connessione client. NapAgent non contiene riferimenti all'oggetto associato a questa interfaccia al termine della chiamata al metodo.

È necessario usare una connessione stabilita in precedenza per l'elaborazione dei BLOB di dati SOHResponse.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Possono essere restituiti anche altri codici di errore specifici di COM.



| Codice restituito                                                                                             | Descrizione                                                                                                                                                                                                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                   | L'operazione è riuscita.<br/>                                                                                                                                                                                                                                                                                            |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>            | Nessuna connessione è stata creata in precedenza nel client di imposizione. <br/>                                                                                                                                                                                                                                                 |
| <dl> <dt>**E \_ ACCESSO NEGATO**</dt> </dl>         | Errore di autorizzazioni, accesso negato.<br/>                                                                                                                                                                                                                                                                                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>          | Limite risorse di sistema: impossibile eseguire l'operazione.<br/>                                                                                                                                                                                                                                                                 |
| <dl> <dt>**PACCHETTO \_ NON VALIDO DI PROTEZIONE ACCESSO ALLA \_ RETE E \_**</dt> </dl>  | Se viene restituito questo valore, il client di imposizione deve eliminare il pacchetto se NapAgent restituisce NAP \_ E \_ INVALID \_ PACKET. In questo caso, l'imponitore deve presupporre che il server con cui sta comunicando non sia abilitato per Protezione accesso alla rete e rimuovere la connessione dall'elenco attivo,ad esempio notificare a NapAgent lo stato di connessione in basso.<br/> |
| <dl> <dt>**ID DI PROTEZIONE ACCESSO ALLA RETE NON \_ \_ \_ CORRISPONDENTE**</dt> </dl>   | Se viene restituito questo valore, indica che l'ID di correlazione nel pacchetto SoH-Response non corrisponde alla risposta SoH in sospeso. In questo caso, l'imponitore deve eliminare il pacchetto e attendere un altro pacchetto SoH-Response più recente.<br/> Ciò può essere causato da una risposta a un messaggio di richiesta meno recente.<br/>        |
| <dl> <dt>**PROTEZIONE \_ ACCESSO ALLA RETE NON \_ \_ INIZIALIZZATA**</dt> </dl> | L'applicazione non è stata inizializzata in precedenza.<br/>                                                                                                                                                                                                                                                                       |



 

## <a name="remarks"></a>Commenti

NapAgent esegue una query SoH-Response BLOB di dati dall'oggetto connessione, lo elabora e imposta la decisione risultante (ad esempio. accesso completo/con restrizioni/e così via) nell'oggetto connessione.

Il client di imposizione deve chiamare il metodo [**INapEnforcementClientBinding::Initialize**](inapenforcementclientbinding-initialize-method.md) prima di chiamare questo o qualsiasi altro metodo [**dell'interfaccia INapEnforcementClientBinding.**](inapenforcementclientbinding.md)

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


</dt> <dt>

[**INapEnforcementClientBinding**](inapenforcementclientbinding.md)
</dt> <dt>

[**INapEnforcementClientConnection**](inapenforcementclientconnection.md)
</dt> </dl>

 

 





