---
description: Il metodo Configure invia le informazioni di configurazione dell'acquisizione.
ms.assetid: 739ed1df-1a84-4c48-a1ac-2dba7a614cdd
title: Metodo IStats::Configure (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IStats.Configure
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 357d0dd9dbb6e0f57a7ecd3dffcec4c0d1e546ce0bc058ce0144796ca8836113
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118364968"
---
# <a name="istatsconfigure-method"></a>Metodo IStats::Configure

Il **metodo Configure** invia le informazioni di configurazione dell'acquisizione.

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

Handle a un BLOB di errore che contiene informazioni aggiuntive sull'errore.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, il valore restituito è NMERR \_ SUCCESS.

Se il metodo ha esito negativo, il valore restituito è uno dei codici di errore seguenti:



| Codice restituito                                                                                                         | Descrizione                                                                                                                                                                                                                              |
|---------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**STRINGA BLOB NMERR \_ \_ NON \_ VALIDA**</dt> </dl>         | La stringa non ha terminazione Null.<br/>                                                                                                                                                                                            |
| <dl> <dt>**BLOB NMERR \_ \_ NON \_ INIZIALIZZATO**</dt> </dl>        | Il **metodo CreateBlob** non è stato chiamato.<br/>                                                                                                                                                                                |
| <dl> <dt>**BLOB NON VALIDO DI NMERR \_ \_**</dt> </dl>                 | L'oggetto a cui punta non è un BLOB.<br/>                                                                                                                                                                                  |
| <dl> <dt>**BLOB DI \_ LIVELLO SUPERIORE NMERR \_**</dt> </dl>                 | Il numero di versione del BLOB non è corretto.<br/>                                                                                                                                                                                         |
| <dl> <dt>**LA VOCE BLOB NMERR \_ \_ ESISTE \_ \_ GIÀ**</dt> </dl>  | Esiste già una voce BLOB.<br/>                                                                                                                                                                                                  |
| <dl> <dt>**LA VOCE BLOB NMERR \_ \_ NON \_ \_ \_ ESISTE**</dt> </dl> | Nel BLOB di configurazione specificato dal *parametro hConfigurationBlob* manca una voce necessaria per eseguire questa operazione. Esaminare il BLOB di errore restituito dal *parametro hErrorBlob* per determinare quale voce non è stata trovata.<br/> |
| <dl> <dt>**IDENTIFICATORE \_ AMBIGUO \_ NMERR**</dt> </dl>          | Il BLOB non contiene informazioni sul proprietario o sulla categoria.<br/>                                                                                                                                                                                 |
| <dl> <dt>**PROPRIETARIO BLOB NMERR \_ \_ NON \_ \_ TROVATO**</dt> </dl>       | La sezione Owner del BLOB non è stata trovata.<br/>                                                                                                                                                                                  |
| <dl> <dt>**CATEGORIA BLOB NMERR \_ \_ NON \_ \_ TROVATA**</dt> </dl>    | La sezione Category del BLOB non è stata trovata.<br/>                                                                                                                                                                               |
| <dl> <dt>**CATEGORIA SCONOSCIUTA NMERR \_ \_**</dt> </dl>             | Informazioni sulla categoria trovate ma non comprese.<br/>                                                                                                                                                                            |
| <dl> <dt>**TAG SCONOSCIUTO NMERR \_ \_**</dt> </dl>                  | Le informazioni sui tag sono stati trovati ma non sono stati compresi.<br/>                                                                                                                                                                                 |
| <dl> <dt>**ERRORE DI CONVERSIONE \_ BLOB NMERR \_ \_**</dt> </dl>       | Il BLOB è danneggiato.<br/>                                                                                                                                                                                                          |
| <dl> <dt>**TRIGGER NMERR \_ NON \_ VALIDO**</dt> </dl>              | La parte del trigger del BLOB è danneggiata.<br/>                                                                                                                                                                                   |



 

## <a name="remarks"></a>Commenti

È necessario applicare questo metodo per riavviare un NPP avviato, arrestato ma non disconnesso.

Il BLOB di errore restituito da *hErrorBlob* contiene voci che Network Monitor non sono in grado di comprendere o trovare nel BLOB di configurazione specificato nel *parametro hConfigurationBlob.* Il BLOB dell'errore restituito contiene informazioni sull'errore che l'applicazione può usare per la risoluzione dei problemi. Ad esempio, se viene restituito NMERR BLOB ENTRY DOES NOT EXIST, la voce Network Monitor impossibile trovare è inclusa nel \_ \_ BLOB di errore \_ \_ \_ restituito.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                                                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                                                                     |
| Intestazione<br/>                   | <dl> <dt>Netmon.h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[IStats](istats.md)
</dt> <dt>

[ISTATS::Connessione](istats-connect.md)
</dt> <dt>

[Network Monitor BLOB](network-monitor-blobs.md)
</dt> </dl>

 

 




