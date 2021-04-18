---
description: Il metodo Connect connette l'oggetto NPP alla rete utilizzando una scheda di interfaccia di rete specificata e fornisce le informazioni di configurazione per la connessione.
ms.assetid: d017c2a3-a832-4084-b21b-0cca428c5360
title: 'Metodo IRTC:: Connect (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRTC.Connect
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: a14e34aeb0be30165aa18ddc7da18028d715be01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306557"
---
# <a name="irtcconnect-method"></a>Metodo IRTC:: Connect

Il metodo **Connect** connette l'oggetto NPP alla rete utilizzando una scheda di interfaccia di rete specificata e fornisce le informazioni di configurazione per la connessione.

## <a name="syntax"></a>Sintassi


```C++
HRESULT STDMETHODCALLTYPE Connect(
  [in]  HBLOB  hInputBlob,
  [in]  LPVOID StatusCallbackProc,
  [in]  LPVOID FramesCallbackProc,
  [in]  LPVOID UserContext,
  [out] HBLOB  hErrorBlob
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hInputBlob* \[ in\]
</dt> <dd>

Handle per il BLOB che specifica la scheda di interfaccia di rete a cui ci si connette e le informazioni di configurazione per tale connessione.

</dd> <dt>

*StatusCallbackProc* \[ in\]
</dt> <dd>

Indirizzo della funzione di callback dello stato dell'utente, che riceve gli aggiornamenti di stato, ad esempio i trigger. Questo parametro può essere impostato su **null**.

</dd> <dt>

*FramesCallbackProc* \[ in\]
</dt> <dd>

Indirizzo della funzione di richiamata frame dell'utente, utilizzata per ricevere aggiornamenti di stato, ad esempio i trigger. Questo parametro può essere impostato su **null**.

</dd> <dt>

*UserContext* \[ in\]
</dt> <dd>

Valore passato quando viene chiamata la funzione di callback dello stato e del frame dell'utente. Se vengono specificate entrambe le funzioni di callback, è necessario che utilizzino lo stesso valore del contesto utente. Il valore di questo parametro è in genere HWND o un puntatore ' This '.

</dd> <dt>

*hErrorBlob* \[ out\]
</dt> <dd>

Handle per un BLOB di errori che contiene informazioni aggiuntive sull'errore. Per informazioni sul contenuto del BLOB degli errori, vedere la sezione Osservazioni nella parte inferiore di questo argomento.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, il valore restituito è NMERR \_ Success.

Se il metodo ha esito negativo, il valore restituito è uno dei codici di errore seguenti (che includono gli errori restituiti dalla chiamata interna **IRTC:: Configure** ):



| Codice restituito                                                                                                         | Descrizione                                                                                                                                                                                                                                                                                  |
|---------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ già \_ connesso**</dt> </dl>            | Questa istanza dell'oggetto COM NPP è già connessa alla rete.<br/>                                                                                                                                                                                                          |
| <dl> <dt>**\_errore di \_ conversione \_ BLOB NMERR**</dt> </dl>       | Il BLOB di configurazione è danneggiato. Questo errore viene generato dalla chiamata **IRTC:: Configure** .<br/>                                                                                                                                                                                       |
| <dl> <dt>**\_la voce del BLOB NMERR non \_ \_ \_ \_ esiste**</dt> </dl> | Il BLOB di input specificato dal parametro *hInputBlob* non dispone di una voce necessaria per eseguire questa operazione. Questo errore può essere generato dalla chiamata **IRTC:: Connect** o **IRTC:: Configure** . Esaminare il BLOB di errore restituito da *hErrorBlob* per determinare quale voce non è stata trovata.<br/> |
| <dl> <dt>**\_BLOB NMERR \_ non \_ inizializzato**</dt> </dl>        | La funzione **CreateBlob** non è stata chiamata. Questo errore viene generato dalla chiamata **IRTC:: Configure** .<br/>                                                                                                                                                                         |
| <dl> <dt>**\_stringa BLOB \_ NMERR \_ non valida**</dt> </dl>         | La stringa non termina con null. Questo errore viene generato dalla chiamata **IRTC:: Configure** .<br/>                                                                                                                                                                                       |
| <dl> <dt>**TRIGGER NMERR non \_ valido \_**</dt> </dl>              | La parte del trigger del BLOB di input è danneggiata. Questo errore viene generato dalla chiamata **IRTC:: Configure** .<br/>                                                                                                                                                                        |
| <dl> <dt>**\_BLOB NMERR non valido \_**</dt> </dl>                 | L'oggetto specificato in *hInputBlob* non è un BLOB. Questo errore viene generato dalla chiamata **IRTC:: Configure** .<br/>                                                                                                                                                                      |
| <dl> <dt>**\_ \_ \_ memoria insufficiente NMERR**</dt> </dl>               | La memoria necessaria per eseguire questa operazione non è disponibile. Questo errore viene generato dalla chiamata **IRTC:: Configure** .<br/>                                                                                                                                                              |
| <dl> <dt>**\_timeout NMERR**</dt> </dl>                       | Timeout della richiesta. Questo errore viene generato dalla chiamata **IRTC:: Configure** .<br/>                                                                                                                                                                                               |
| <dl> <dt>**BLOB a livello di NMERR \_ \_**</dt> </dl>                 | Il numero di versione del BLOB specificato in *hInputBlob* non è corretto. Questo errore viene generato dalla chiamata **IRTC:: Configure** .<br/>                                                                                                                                                   |



 

## <a name="remarks"></a>Commenti

Quando viene chiamato il metodo **Connect** , l'oggetto NPP chiama automaticamente il metodo **IRTC:: Configure** usando il BLOB fornito da *hInputBlob*. Si noti che tutti i codici di errore restituiti dalla chiamata a **IRTC:: Configure** vengono passati nuovamente e restituiti dalla chiamata **IRTC:: Connect** .

Questo metodo deve essere chiamato prima che sia possibile avviare l'acquisizione di frame. Si noti che quando ci si connette alla rete usando questo metodo, è necessario continuare a usare l'interfaccia **IRTC** per acquisire i frame.

Quando si chiama questa funzione, è necessario specificare una funzione di callback dello stato o del frame, anche se agisce solo come segnaposto.

Il BLOB di input specificato da *hInputBlob* può essere ottenuto chiamando i metodi **GetNPPBlobFromUI**, **GetNPPBlobTable** e **SelectNPPBlobFromTable** .

Il BLOB di errori restituito in *hErrorBlob* contiene informazioni sull'errore che lo sviluppatore o l'applicazione può utilizzare per la risoluzione dei problemi. Il BLOB di errore restituito da *hErrorBlob* contiene voci che Network Monitor non è stato in grado di comprendere o trovare nel BLOB di input specificato in *hInputBlob*. Ad esempio, se \_ \_ \_ \_ \_ viene restituita la voce del BLOB NMERR non esiste, la voce Network Monitor Impossibile trovare è inclusa nel BLOB di errore restituito.



| Per informazioni su                          | Vedere                                                                          |
|------------------------------------------------|------------------------------------------------------------------------------|
| Recupero del BLOB di input che rappresenta una scheda di interfaccia di rete | [Selezione di una scheda di interfaccia di rete](selecting-a-network-interface-card.md) |



 

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

[IRTC:: Configure](irtc-configure.md)
</dt> <dt>

[IRTC::D la connessione](irtc-disconnect.md)
</dt> <dt>

[IRTC:: Start](irtc-start.md)
</dt> </dl>

 

 




