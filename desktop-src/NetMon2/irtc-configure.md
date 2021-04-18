---
description: Invia i dati di configurazione per un'acquisizione dei dati.
ms.assetid: fb8c8ac8-cef4-45e0-bb06-3cf09c8ad9ac
title: 'Metodo IRTC:: Configure (Netmon. h)'
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
ms.openlocfilehash: 702a3883acdbb7509d79e76d8fcc73af1e167e4a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306558"
---
# <a name="irtcconfigure-method"></a>Metodo IRTC:: Configure

Il metodo [**Configure**](configure.md) invia i dati di configurazione per un'acquisizione dei dati.

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

Handle per un BLOB di errori che contiene dati di errore aggiuntivi.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, il valore restituito è NMERR \_ Success.

Se il metodo ha esito negativo, il valore restituito è uno dei codici di errore seguenti:



| Codice restituito                                                                                                         | Descrizione                                                                                                                                                                                               |
|---------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_BLOB NMERR \_ non \_ inizializzato**</dt> </dl>        | Il metodo **CreateBlob** non è stato chiamato.<br/>                                                                                                                                                 |
| <dl> <dt>**\_BLOB NMERR non valido \_**</dt> </dl>                 | L'oggetto a cui fa riferimento non è un BLOB.<br/>                                                                                                                                                           |
| <dl> <dt>**BLOB a livello di NMERR \_ \_**</dt> </dl>                 | Il numero di versione del BLOB non è corretto.<br/>                                                                                                                                                          |
| <dl> <dt>**la \_ voce del BLOB NMERR \_ \_ \_ esiste già**</dt> </dl>  | BLOB duplicato.<br/>                                                                                                                                                                                |
| <dl> <dt>**\_la voce del BLOB NMERR non \_ \_ \_ \_ esiste**</dt> </dl> | Il BLOB di configurazione specificato da *hConfigurationBlob* non dispone di una voce necessaria per eseguire questa operazione. Visualizzare il BLOB di errore restituito da *hErrorBlob* per determinare quale voce non è stata trovata.<br/> |
| <dl> <dt>**\_identificatore ambiguo NMERR \_**</dt> </dl>          | Mancano i dati del proprietario o della categoria del BLOB.<br/>                                                                                                                                                    |
| <dl> <dt>**il \_ proprietario del BLOB NMERR non è stato \_ \_ \_ trovato**</dt> </dl>       | La sezione del proprietario del BLOB non è stata trovata.<br/>                                                                                                                                                          |
| <dl> <dt>**\_categoria BLOB \_ NMERR \_ non \_ trovata**</dt> </dl>    | La sezione della categoria BLOB non è stata trovata.<br/>                                                                                                                                                       |
| <dl> <dt>**\_categoria NMERR sconosciuta \_**</dt> </dl>             | La sezione relativa alla categoria BLOB è stata trovata, ma non è stata riconosciuta.<br/>                                                                                                                                       |
| <dl> <dt>**NMERR \_ \_ tag sconosciuto**</dt> </dl>                  | La sezione del tag BLOB è stata trovata, ma non è stata riconosciuta.<br/>                                                                                                                                            |
| <dl> <dt>**\_errore di \_ conversione \_ BLOB NMERR**</dt> </dl>       | Il BLOB è danneggiato.<br/>                                                                                                                                                                           |
| <dl> <dt>**TRIGGER NMERR non \_ valido \_**</dt> </dl>              | La parte del trigger del BLOB è danneggiata.<br/>                                                                                                                                                    |
| <dl> <dt>**\_stringa BLOB \_ NMERR \_ non valida**</dt> </dl>         | La stringa non termina con null.<br/>                                                                                                                                                             |



 

## <a name="remarks"></a>Commenti

È necessario applicare questo metodo per riavviare un oggetto NPP che è stato avviato, arrestato, ma non disconnesso.

Il BLOB di errore restituito da *hErrorBlob* contiene voci che Network Monitor non è stato in grado di comprendere o trovare nel BLOB di configurazione specificato in *hConfigurationBlob*. Il BLOB di errori restituito contiene i dati di errore che possono essere usati dall'applicazione per la risoluzione dei problemi. Se, ad esempio, \_ \_ \_ \_ \_ viene restituita la voce del BLOB NMERR non esiste, la voce Network Monitor Impossibile trovare è inclusa nel BLOB di errore restituito.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                                                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                                                                     |
| Intestazione<br/>                   | <dl> <dt>Netmon. h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[IRTC](irtc.md)
</dt> <dt>

[IRTC:: Connect](irtc-connect.md)
</dt> <dt>

[BLOB Network Monitor](network-monitor-blobs.md)
</dt> </dl>

 

 




