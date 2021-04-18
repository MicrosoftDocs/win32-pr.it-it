---
description: Il metodo Configure Invia le informazioni di configurazione per un'acquisizione.
ms.assetid: b8cbbae1-3c07-489f-8e8f-77c95ec03209
title: 'Metodo IESP:: Configure (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IESP.Configure
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 53efbe7eb2887165dacc4cb904822de953b84017
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305880"
---
# <a name="iespconfigure-method"></a>Metodo IESP:: Configure

Il metodo **Configure** Invia le informazioni di configurazione per un'acquisizione.

## <a name="syntax"></a>Sintassi


```C++
HRESULT STDMETHODCALLTYPE Configure(
  [in]  HBLOB hConfigurationBlob,
  [out] HBLOB hErrorBlob
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hConfigurationBlob* \[ in\]
</dt> <dd>

Handle per il BLOB configurato dal chiamante.

</dd> <dt>

*hErrorBlob* \[ out\]
</dt> <dd>

Handle per un BLOB di errori che contiene informazioni aggiuntive sull'errore. Per informazioni sul contenuto di un BLOB di errore, vedere la sezione Osservazioni in questo argomento.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, il valore restituito è NMERR \_ Success.

Se il metodo ha esito negativo, il valore restituito è uno dei codici di errore seguenti:



| Codice restituito                                                                                                         | Descrizione                                                                                                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ non \_ connesso**</dt> </dl>                | L'oggetto NPP non è connesso alla rete.<br/>                                                                                                                                                               |
| <dl> <dt>**NMERR \_ non \_ ESP**</dt> </dl>                      | L'oggetto NPP è connesso alla rete, ma non con il metodo [IESP:: Connect](iesp-connect.md) .<br/>                                                                                                         |
| <dl> <dt>**\_acquisizione NMERR**</dt> </dl>                     | Il NPP segnala che la sessione di acquisizione è stata avviata.<br/>                                                                                                                                                  |
| <dl> <dt>**TRIGGER NMERR non \_ valido \_**</dt> </dl>              | La parte del trigger del BLOB di configurazione è danneggiata.<br/>                                                                                                                                              |
| <dl> <dt>**\_la voce del BLOB NMERR non \_ \_ \_ \_ esiste**</dt> </dl> | Per il BLOB di configurazione specificato da *hConfigurationBlob* manca una voce necessaria per eseguire questa operazione. Esaminare il BLOB di errore restituito da *hErrorBlob* per determinare quale voce non è stata trovata.<br/> |
| <dl> <dt>**\_errore di \_ conversione \_ BLOB NMERR**</dt> </dl>       | Il BLOB è danneggiato.<br/>                                                                                                                                                                                   |
| <dl> <dt>**\_BLOB NMERR \_ non \_ inizializzato**</dt> </dl>        | Il metodo **CreateBlob** non è stato chiamato.<br/>                                                                                                                                                         |
| <dl> <dt>**\_BLOB NMERR non valido \_**</dt> </dl>                 | L'oggetto a cui si fa riferimento non è un BLOB.<br/>                                                                                                                                                           |
| <dl> <dt>**\_stringa BLOB \_ NMERR \_ non valida**</dt> </dl>         | La stringa non termina con null.<br/>                                                                                                                                                                     |
| <dl> <dt>**BLOB a livello di NMERR \_ \_**</dt> </dl>                 | Il numero di versione del BLOB non è corretto.<br/>                                                                                                                                                                  |
| <dl> <dt>**\_ \_ \_ memoria insufficiente NMERR**</dt> </dl>               | Memoria non disponibile. Arrestare Windows per liberare risorse.<br/>                                                                                                                                       |
| <dl> <dt>**\_timeout NMERR**</dt> </dl>                       | Timeout della richiesta.<br/>                                                                                                                                                                             |



 

## <a name="remarks"></a>Commenti

È necessario applicare questo metodo per riavviare un oggetto NPP che è stato avviato e arrestato, ma non disconnesso.

Il BLOB di errori restituito dal parametro *hErrorBlob* contiene voci che Network Monitor non è stato in grado di comprendere o trovare nel BLOB di configurazione specificato in *hConfigurationBlob*. Il BLOB di errori restituito contiene informazioni sugli errori che possono essere utilizzate dall'applicazione per la risoluzione dei problemi. Ad esempio, se \_ \_ \_ \_ \_ viene restituita la voce del BLOB NMERR non esiste, la voce Network Monitor Impossibile trovare è inclusa nel BLOB di errore restituito.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                                                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                                                                     |
| Intestazione<br/>                   | <dl> <dt>Netmon. h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



 

 




