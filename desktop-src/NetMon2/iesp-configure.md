---
description: Il metodo Configure invia le informazioni di configurazione per un'acquisizione.
ms.assetid: b8cbbae1-3c07-489f-8e8f-77c95ec03209
title: Metodo IESP::Configure (Netmon.h)
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
ms.openlocfilehash: 5ae0fba6885db46d987e59517cdc30dab484974869c67c85a257044e5eec58b7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118365670"
---
# <a name="iespconfigure-method"></a>Metodo IESP::Configure

Il **metodo Configure** invia le informazioni di configurazione per un'acquisizione.

## <a name="syntax"></a>Sintassi


```C++
HRESULT STDMETHODCALLTYPE Configure(
  [in]  HBLOB hConfigurationBlob,
  [out] HBLOB hErrorBlob
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hConfigurationBlob* \[ Pollici\]
</dt> <dd>

Handle per il BLOB configurato dal chiamante.

</dd> <dt>

*hErrorBlob* \[ Cambio\]
</dt> <dd>

Handle a un BLOB di errore che contiene informazioni aggiuntive sull'errore. Per informazioni sul contenuto di un BLOB di errori, vedere la sezione Osservazioni in questo argomento.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, il valore restituito è NMERR \_ SUCCESS.

Se il metodo ha esito negativo, il valore restituito è uno dei codici di errore seguenti:



| Codice restituito                                                                                                         | Descrizione                                                                                                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ NON \_ CONNESSO**</dt> </dl>                | Il NPP non è connesso alla rete.<br/>                                                                                                                                                               |
| <dl> <dt>**NMERR \_ NON \_ ESP**</dt> </dl>                      | Il NPP è connesso alla rete, ma non con il [metodo IESP::Connessione.](iesp-connect.md)<br/>                                                                                                         |
| <dl> <dt>**ACQUISIZIONE DI \_ NMERR**</dt> </dl>                     | Il NPP segnala che la sessione di acquisizione è stata avviata.<br/>                                                                                                                                                  |
| <dl> <dt>**TRIGGER NMERR \_ NON \_ VALIDO**</dt> </dl>              | La parte del trigger del BLOB di configurazione è danneggiata.<br/>                                                                                                                                              |
| <dl> <dt>**LA VOCE BLOB NMERR \_ \_ NON \_ \_ \_ ESISTE**</dt> </dl> | Nel BLOB di configurazione specificato *da hConfigurationBlob* manca una voce necessaria per eseguire questa operazione. Esaminare il BLOB di errore restituito *da hErrorBlob* per determinare quale voce non è stata trovata.<br/> |
| <dl> <dt>**ERRORE DI CONVERSIONE \_ BLOB NMERR \_ \_**</dt> </dl>       | Il BLOB è danneggiato.<br/>                                                                                                                                                                                   |
| <dl> <dt>**BLOB NMERR \_ \_ NON \_ INIZIALIZZATO**</dt> </dl>        | Il **metodo CreateBlob** non è stato chiamato.<br/>                                                                                                                                                         |
| <dl> <dt>**BLOB NON VALIDO DI NMERR \_ \_**</dt> </dl>                 | L'oggetto a cui punta non è un BLOB.<br/>                                                                                                                                                           |
| <dl> <dt>**STRINGA BLOB NMERR \_ \_ NON \_ VALIDA**</dt> </dl>         | La stringa non ha terminazione Null.<br/>                                                                                                                                                                     |
| <dl> <dt>**BLOB DI \_ LIVELLO SUPERIORE NMERR \_**</dt> </dl>                 | Il numero di versione del BLOB non è corretto.<br/>                                                                                                                                                                  |
| <dl> <dt>**MEMORIA INSUFFICIENTE \_ DI NMERR \_ \_**</dt> </dl>               | Non era disponibile memoria. Arrestare le finestre per liberare risorse.<br/>                                                                                                                                       |
| <dl> <dt>**NMERR \_ TIMEOUT**</dt> </dl>                       | Timeout della richiesta.<br/>                                                                                                                                                                             |



 

## <a name="remarks"></a>Commenti

È necessario applicare questo metodo per riavviare un NPP avviato e arrestato, ma non disconnesso.

Il BLOB di errore restituito dal parametro *hErrorBlob* contiene voci che Network Monitor non sono in grado di comprendere o trovare nel BLOB di configurazione specificato in *hConfigurationBlob*. Il BLOB dell'errore restituito contiene informazioni sull'errore che l'applicazione può usare per la risoluzione dei problemi. Ad esempio, se viene restituito NMERR BLOB ENTRY DOES NOT EXIST, la voce Network Monitor impossibile trovare è inclusa nel \_ \_ BLOB di errore \_ \_ \_ restituito.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                                                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                                                                     |
| Intestazione<br/>                   | <dl> <dt>Netmon.h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



 

 




