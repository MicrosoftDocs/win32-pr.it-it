---
title: Metodo INapSystemHealthValidator Validate (NapSystemHealthValidator.h)
description: Sistema nap per convalidare l'oggetto SoHRequest ricevuto da un client.
ms.assetid: d67dc2c8-f18c-4e06-a51e-a538ca75c3f1
keywords:
- Convalida metodo Nap
- Convalidare il metodo NAP, interfaccia INapSystemHealthValidator
- Interfaccia INapSystemHealthValidator NAP , metodo Validate
topic_type:
- apiref
api_name:
- INapSystemHealthValidator.Validate
api_location:
- NapSystemHealthValidator.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1c200e96024075d0c2880b294c197938a5ec0a6f3e1da4cb019d5ecd3ed32b9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119802771"
---
# <a name="inapsystemhealthvalidatorvalidate-method"></a>Metodo INapSystemHealthValidator::Validate

> [!Note]  
> La piattaforma Protezione accesso alla rete non è disponibile a partire da Windows 10

 

Il **metodo INapSystemHealthValidator::Validate** viene definito dallo sviluppatore SHV e chiamato dal sistema NAP per convalidare l'oggetto [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) ricevuto da un client.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Validate(
  [in] INapSystemHealthValidationRequest *request,
  [in] UINT32                            hintTimeOutInMsec,
  [in] INapServerCallback                *callback
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*richiesta* \[ Pollici\]
</dt> <dd>

Puntatore COM a un oggetto [**INapSystemHealthValidationRequest**](inapsystemhealthvalidationrequest.md) che identifica l'oggetto richiesta di convalida.

</dd> <dt>

*hintTimeOutInMsec* \[ Pollici\]
</dt> <dd>

Durata, in millisecondi, del periodo di timeout della comunicazione. La convalida dell'integrità del sistema (SHV) deve rispondere entro questo periodo di tempo; in caso contrario, la risposta viene eliminata.

> [!Note]  
> Il timeout predefinito per tutti gli SHV è 2000 millisecondi. L'uso di un valore diverso da quello predefinito modificherà il timeout per tutti gli SHV registrati.

 

</dd> <dt>

*callback* \[ Pollici\]
</dt> <dd>

Puntatore all'oggetto callback [**INapServerCallback.**](inapservercallback.md) Questo puntatore di callback viene usato dagli SHV quando restituiscono **E \_ PENDING** dalla chiamata a **INapSystemHealthValidator::Validate.** Viene usato per la convalida asincrona. È previsto che gli SHV rispondano entro il tempo *hintTimeOutInMsec,* altrimenti la risposta verrà eliminata.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se viene restituito un altro codice di errore, il sistema presuppone che si sia verificato un errore serverComponent e che il mapping appropriato sia stato superato/non riuscito.



| Codice restituito                                                                                                | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                       | Indica che il validator ha impostato un oggetto SoHResponse sull'oggetto 'request'.<br/>                                                                                                                                                                                                                                                                                                                                                                                                        |
| <dl> <dt>**E \_ IN SOSPESO**</dt> </dl>                  | Indica che OnComplete() verrà chiamato su un thread separato.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <dl> <dt>**RPC \_ S \_ SERVER \_ UNAVAILABLE**</dt> </dl> | Indica che il processo shv (System Health Validator) è terminato senza che NapServer rilasci effettivamente un riferimento a esso. NapServer tenterà di creare nuovamente un nuovo riferimento all'shv e rieseguirà la chiamata Validate una sola volta. Se la creazione dell'oggetto o la convalida rieseguiti hanno esito negativo, l'shv viene rimosso dall'elenco di SHV caricati. L'unico modo per ricaricare questo SHV è annullare la registrazione e registrarla di nuovo oppure al riavvio di NapServer<br/> |



 

## <a name="remarks"></a>Commenti

Per supportare il rilevamento delle intrusioni, agli shv verrà richiesto di convalidare il computer client indipendentemente dal fatto che il client ha inviato un [**oggetto SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) destinato a SHV.

ShV deve eseguire le operazioni seguenti:

-   Recuperare [**l'oggetto SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) *dalla richiesta* chiamando [**request. GetSoHRequest()**](inapsystemhealthvalidationrequest-getsohrequest-method.md).
-   Se il [**pacchetto SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) è Null:
    -   Se shv è un sistema di rilevamento delle intrusioni, popolare un pacchetto [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) con il codice di errore [**nap**](nap-error-constants.md) appropriato per capire perché il computer client è dannoso.
    -   Tutti gli altri shv devono popolare un pacchetto [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) con il codice di errore [**NAP E MISSING \_ \_ \_ SOH**](nap-error-constants.md).
-   Se *napSystemGenerated è* **TRUE** dalla chiamata a [**request. GetSoHRequest(),**](inapsystemhealthvalidationrequest-getsohrequest-method.md)shv deve prevedere un pacchetto [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) con le 3 DLL seguenti: [**sohAttributeTypeSystemHealthId**](sohattributetype-enum.md), **sohAttributeTypeFailureCategory**, **sohAttributeTypeErrorCodes**. Questo **Oggetto SoHRequest** viene generato da NapAgent per conto dell'agente integrità sistema (SHA) perché si è verificato un errore durante il recupero di un pacchetto di richiesta dall'sha.
-   Convalidare [**il pacchetto SoHRequest.**](/windows/win32/api/naptypes/ns-naptypes-soh)
    -   Se il [**formato di SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) non è corretto, costruire un pacchetto **SoHResponse** con codice di errore [**NAP E INVALID \_ \_ \_ PACKET**](nap-error-constants.md).
    -   Se shv usa solo informazioni memorizzate nella cache per convalidare il pacchetto [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) (ovvero non viene eseguito alcun I/O), può costruire **l'oggetto SoHResponse**, impostarlo sull'oggetto nella richiesta e restituire **S \_ OK**. 
    -   Se shv esegue operazioni di I/O per la conversazione con i server back-end per convalidare l'integrità del client, deve accodare l'I/O e restituire questa funzione con **E \_ PENDING**. In questo caso, SHV deve chiamare [**callback. OnComplete()**](inapservercallback-oncomplete-method.md) in un thread separato entro il periodo di timeout, *hintTimeOutInMsec.* In caso contrario, la risposta dell'shv verrà eliminata.
-   Non restituire altri errori diversi da quelli elencati in precedenza. Se un altro codice di errore viene restituito da SHV (ad esempio errore di sistema), il pacchetto verrà eliminato.

Un shv deve restituire un valore TLV **sohAttributeTypeComplianceResultCodes** o **sohAttributeTypeFailureCategory** in [**SoHRequest.**](/windows/win32/api/naptypes/ns-naptypes-soh)

-   [**sohAttributeTypeComplianceResultCodes TLV:**](sohattributetype-enum.md)se shv può convalidare l'integrità del client (ad esempio integro o non integro), viene restituito questo TLV.
-   [**sohAttributeTypeFailureCategory TLV:**](sohattributetype-enum.md)se si è verificato un errore di comunicazione o componente nel client o nel server, deve essere indicato da questa TLV. Questo TLV verrà ulteriormente mappato a integro o non integro a seconda della configurazione dell'shv. Per altri dettagli, vedere [**l'interfaccia INapServerManagement**](inapservermanagement.md) e la [**struttura FailureCategoryMapping.**](/windows/win32/api/naptypes/ns-naptypes-failurecategorymapping)

L'shv non deve contenere riferimenti *alla richiesta o* al *callback* al termine della chiamata asincrona.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                                               |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                                    |
| Intestazione<br/>                   | <dl> <dt>NapSystemHealthValidator.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapSystemHealthValidator.idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**INapSystemHealthValidator**](inapsystemhealthvalidator.md)
</dt> </dl>

 

 





