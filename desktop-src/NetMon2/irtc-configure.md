---
description: Invia i dati di configurazione per un'acquisizione dati.
ms.assetid: fb8c8ac8-cef4-45e0-bb06-3cf09c8ad9ac
title: Metodo IRTC::Configure (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRTC.Configure
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 8f70674d8e570a2640fe301179b21a9f48ec612a17de69e43bdf5c38db4e65af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119063911"
---
# <a name="irtcconfigure-method"></a>Metodo IRTC::Configure

Il [**metodo Configure**](configure.md) invia i dati di configurazione per un'acquisizione dati.

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

Handle di un BLOB di errore che contiene dati di errore aggiuntivi.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, il valore restituito è NMERR \_ SUCCESS.

Se il metodo ha esito negativo, il valore restituito è uno dei codici di errore seguenti:



| Codice restituito                                                                                                         | Descrizione                                                                                                                                                                                               |
|---------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**BLOB NMERR \_ \_ NON \_ INIZIALIZZATO**</dt> </dl>        | Il **metodo CreateBlob** non è stato chiamato.<br/>                                                                                                                                                 |
| <dl> <dt>**BLOB NON VALIDO DI NMERR \_ \_**</dt> </dl>                 | L'oggetto a cui punta non è un BLOB.<br/>                                                                                                                                                           |
| <dl> <dt>**BLOB DI \_ LIVELLO SUPERIORE NMERR \_**</dt> </dl>                 | Il numero di versione del BLOB non è corretto.<br/>                                                                                                                                                          |
| <dl> <dt>**LA VOCE BLOB NMERR \_ \_ ESISTE \_ \_ GIÀ**</dt> </dl>  | BLOB duplicato.<br/>                                                                                                                                                                                |
| <dl> <dt>**LA VOCE DEL BLOB NMERR \_ \_ NON \_ \_ \_ ESISTE**</dt> </dl> | Il BLOB di configurazione specificato *da hConfigurationBlob* non dispone di una voce necessaria per eseguire questa operazione. Visualizzare il BLOB di errore restituito *da hErrorBlob* per determinare quale voce non è stata trovata.<br/> |
| <dl> <dt>**IDENTIFICATORE \_ AMBIGUO \_ NMERR**</dt> </dl>          | I dati relativi al proprietario o alla categoria BLOB non sono presenti.<br/>                                                                                                                                                    |
| <dl> <dt>**PROPRIETARIO DEL BLOB NMERR \_ \_ NON \_ \_ TROVATO**</dt> </dl>       | La sezione Proprietario BLOB non è stata trovata.<br/>                                                                                                                                                          |
| <dl> <dt>**CATEGORIA BLOB NMERR \_ \_ NON \_ \_ TROVATA**</dt> </dl>    | La sezione Categoria BLOB non è stata trovata.<br/>                                                                                                                                                       |
| <dl> <dt>**CATEGORIA SCONOSCIUTA DI NMERR \_ \_**</dt> </dl>             | La sezione Categoria BLOB è stata trovata, ma non è stata compresa.<br/>                                                                                                                                       |
| <dl> <dt>**TAG SCONOSCIUTO DI NMERR \_ \_**</dt> </dl>                  | La sezione del tag BLOB è stata trovata, ma non è stata compresa.<br/>                                                                                                                                            |
| <dl> <dt>**ERRORE DI \_ \_ CONVERSIONE BLOB \_ NMERR**</dt> </dl>       | Il BLOB è danneggiato.<br/>                                                                                                                                                                           |
| <dl> <dt>**TRIGGER NMERR \_ NON \_ VALIDO**</dt> </dl>              | La parte trigger del BLOB è danneggiata.<br/>                                                                                                                                                    |
| <dl> <dt>**STRINGA BLOB NMERR \_ \_ NON \_ VALIDA**</dt> </dl>         | La stringa non è con terminazione Null.<br/>                                                                                                                                                             |



 

## <a name="remarks"></a>Commenti

È necessario applicare questo metodo per riavviare un NPP avviato, arrestato ma non disconnesso.

Il BLOB di errore restituito da *hErrorBlob* contiene voci che Network Monitor impossibile comprendere o trovare nel BLOB di configurazione specificato in *hConfigurationBlob*. Il BLOB degli errori restituito contiene i dati degli errori che l'applicazione può usare per la risoluzione dei problemi. Ad esempio, se viene restituito NMERR BLOB ENTRY DOES NOT EXIST, la voce Network Monitor impossibile trovare viene \_ \_ \_ \_ \_ inclusa nel BLOB di errore restituito.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                                                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                                                                     |
| Intestazione<br/>                   | <dl> <dt>Netmon.h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[IRTC](irtc.md)
</dt> <dt>

[IRTC::Connessione](irtc-connect.md)
</dt> <dt>

[Network Monitor BLOB](network-monitor-blobs.md)
</dt> </dl>

 

 




