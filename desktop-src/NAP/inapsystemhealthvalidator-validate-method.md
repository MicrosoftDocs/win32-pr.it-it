---
title: Metodo Validate INapSystemHealthValidator (NapSystemHealthValidator. h)
description: Sistema di protezione accesso alla rete per convalidare il SoHRequest ricevuto da un client.
ms.assetid: d67dc2c8-f18c-4e06-a51e-a538ca75c3f1
keywords:
- Convalida NAP metodo
- Metodo Validate NAP, interfaccia INapSystemHealthValidator
- Interfaccia INapSystemHealthValidator NAP, metodo Validate
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
ms.openlocfilehash: 4f7589a67b9a3b1454e3c65b17ad6f584ce0e655
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301364"
---
# <a name="inapsystemhealthvalidatorvalidate-method"></a>Metodo INapSystemHealthValidator:: Validate

> [!Note]  
> La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10

 

Il metodo **INapSystemHealthValidator:: Validate** viene definito dallo sviluppatore del servizio di convalida dell'integrità di sistema e chiamato dal sistema NAP per convalidare il [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) ricevuto da un client.

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

*richiesta* \[ in\]
</dt> <dd>

Puntatore COM a un oggetto [**INapSystemHealthValidationRequest**](inapsystemhealthvalidationrequest.md) che identifica l'oggetto della richiesta di convalida.

</dd> <dt>

*hintTimeOutInMsec* \[ in\]
</dt> <dd>

Durata, in millisecondi, del periodo di timeout della comunicazione. Il servizio di convalida dell'integrità di sistema deve rispondere entro questo periodo di tempo; in caso contrario, la risposta viene eliminata.

> [!Note]  
> Il timeout predefinito per tutti SHV è pari a 2000 millisecondi. Se si usa un valore diverso da quello predefinito, il timeout per tutti i SHV registrati viene modificato.

 

</dd> <dt>

*callback* \[ di in\]
</dt> <dd>

Puntatore all'oggetto callback [**INapServerCallback**](inapservercallback.md). Questo puntatore di callback viene usato da SHV quando restituisce **E \_ in sospeso** dalla chiamata a **INapSystemHealthValidator:: Validate**. Viene utilizzato per la convalida asincrona. È previsto che il SHV risponda entro il tempo di *hintTimeOutInMsec* . in caso contrario, la risposta verrà eliminata.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se viene restituito un altro codice di errore, il sistema presuppone che si sia verificato un errore serverComponent ed è stato eseguito il mapping appropriato per il superamento o l'esito negativo.



| Codice restituito                                                                                                | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                       | Indica che il validator ha impostato un SoHResponse sull'oggetto ' request '.<br/>                                                                                                                                                                                                                                                                                                                                                                                                        |
| <dl> <dt>**E \_ in sospeso**</dt> </dl>                  | Indica che OnComplete () verrà chiamato su un thread separato.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <dl> <dt>**\_server RPC \_ non \_ disponibile**</dt> </dl> | Indica che il processo di convalida dell'integrità di sistema (convalida integrità sistema) è stato terminato senza NapServer effettivamente il rilascio di un riferimento. NapServer tenterà di ricreare un nuovo riferimento al servizio di convalida dell'integrità di sistema e eseguirà nuovamente la chiamata di convalida una volta. Se la creazione dell'oggetto o della convalida rieseguita non riesce, il servizio di convalida dell'integrità di sistema viene rimosso dall'elenco dei SHV caricati. L'unico modo in cui è possibile ricaricare il servizio di convalida dell'integrità di sistema è quello di annullare la registrazione e registrare di nuovo il servizio di convalida dell'integrità oppure al riavvio del NapServer.<br/> |



 

## <a name="remarks"></a>Commenti

Per supportare il rilevamento delle intrusioni, a SHV verrà richiesto di convalidare il computer client indipendentemente dal fatto che il client abbia inviato un [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) per il servizio di convalida dell'integrità.

Il servizio di convalida dell'integrità deve eseguire le operazioni seguenti:

-   Recuperare il [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) da *Request* chiamando [**Request. GetSoHRequest ()**](inapsystemhealthvalidationrequest-getsohrequest-method.md).
-   Se il pacchetto [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) è null:
    -   Se il servizio di convalida dell'integrità di sistema è un sistema di rilevamento delle intrusioni, popolare un pacchetto [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) con il [**codice di errore NAP**](nap-error-constants.md) appropriato per il motivo per cui il computer client è dannoso
    -   Tutti gli altri SHV devono popolare un pacchetto [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) con un codice di errore [**NAP \_ E \_ Missing \_ SOH**](nap-error-constants.md).
-   Se *napSystemGenerated* è **true** dalla chiamata a [**Request. GetSoHRequest ()**](inapsystemhealthvalidationrequest-getsohrequest-method.md), il servizio di convalida dell'integrità deve prevedere un pacchetto di rapporto di [**integrità**](/windows/win32/api/naptypes/ns-naptypes-soh) con i seguenti 3 TLVs: [**sohAttributeTypeSystemHealthId**](sohattributetype-enum.md), **sohAttributeTypeFailureCategory**, **sohAttributeTypeErrorCodes**. Questo **SoHRequest** viene generato da napagent per conto dell'agente integrità sistema (SHA) perché si è verificato un errore durante il recupero di un pacchetto di richiesta dall'SHA.
-   Convalidare il pacchetto [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) .
    -   Se il [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) non è valido, costruire un pacchetto **SoHResponse** con il [**\_ pacchetto NAP E il \_ \_ pacchetto non valido**](nap-error-constants.md).
    -   Se il servizio di convalida dell'integrità di sistema usa solo le informazioni memorizzate nella cache per convalidare il pacchetto [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) (ovvero non viene eseguita alcuna operazione di i/O), può costruire il **SoHResponse**, impostarlo sull'oggetto nella *richiesta* e restituire **S \_ OK**.
    -   Se il servizio di convalida dell'integrità di sistema esegue operazioni di I/O per comunicare con i server back-end per convalidare l'integrità del client, deve accodare l'i/O e restituire questa funzione con **e \_ in sospeso**. In questo caso, il servizio di convalida dell'integrità di sistema deve chiamare [**callback. OnComplete ()**](inapservercallback-oncomplete-method.md) in un thread separato entro il periodo di timeout, *hintTimeOutInMsec*. In caso contrario, la risposta di convalida integrità sistema verrà eliminata.
-   Non restituire altri errori diversi da quelli elencati in precedenza. Se il servizio di convalida dell'integrità di sistema restituisce un altro codice di errore (ad esempio, un errore di sistema), il pacchetto verrà rimosso.

Un servizio di convalida dell'integrità di sistema deve restituire un **sohAttributeTypeComplianceResultCodes** o **sohAttributeTypeFailureCategory** TLV nel relativo [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh).

-   [**SOHATTRIBUTETYPECOMPLIANCERESULTCODES TLV**](sohattributetype-enum.md): se il servizio di convalida dell'integrità di sistema può convalidare l'integrità del client (ad esempio integro o non integro), viene restituito questo TLV.
-   [**SOHATTRIBUTETYPEFAILURECATEGORY TLV**](sohattributetype-enum.md): se si è verificato un errore di comunicazione o componente nel client o nel server, questo deve essere indicato da questo TLV. Questo TLV verrà ulteriormente mappato a integro o non integro a seconda della configurazione del servizio di convalida dell'integrità di sistema. Per altri dettagli, vedere l'interfaccia [**INapServerManagement**](inapservermanagement.md) e la struttura [**FailureCategoryMapping**](/windows/win32/api/naptypes/ns-naptypes-failurecategorymapping) .

Il servizio di convalida dell'integrità di sistema non deve conservare riferimenti alla *richiesta* o al *callback* al completamento della chiamata asincrono.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                                               |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                                    |
| Intestazione<br/>                   | <dl> <dt>NapSystemHealthValidator. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapSystemHealthValidator. idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**INapSystemHealthValidator**](inapsystemhealthvalidator.md)
</dt> </dl>

 

 





