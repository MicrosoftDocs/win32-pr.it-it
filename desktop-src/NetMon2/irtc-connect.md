---
description: 'Metodo IRTC::Connessione: il metodo Connessione connette il NPP alla rete usando una scheda di interfaccia di rete specificata e fornisce informazioni di configurazione per la connessione.'
ms.assetid: d017c2a3-a832-4084-b21b-0cca428c5360
title: Metodo IRTC::Connessione (Netmon.h)
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
ms.openlocfilehash: da7ff72414a1702a1849f76f658f0fbf85116b9b831e800148d5a6165da7ac17
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118132900"
---
# <a name="irtcconnect-method"></a>Metodo IRTC::Connessione

Il **Connessione** connette il NPP alla rete usando una scheda di interfaccia di rete specificata e fornisce informazioni di configurazione per la connessione.

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

*hInputBlob* \[ Pollici\]
</dt> <dd>

Handle al BLOB che specifica la scheda di interfaccia di rete a cui ci si connette e le informazioni di configurazione per tale connessione.

</dd> <dt>

*StatusCallbackProc* \[ Pollici\]
</dt> <dd>

Indirizzo della funzione di callback dello stato dell'utente, che riceve gli aggiornamenti dello stato, ad esempio i trigger. Questo parametro può essere impostato su **NULL.**

</dd> <dt>

*FramesCallbackProc* \[ Pollici\]
</dt> <dd>

Indirizzo della funzione di callback dei frame dell'utente, usata per ricevere gli aggiornamenti dello stato, ad esempio i trigger. Questo parametro può essere impostato su **NULL.**

</dd> <dt>

*UserContext* \[ Pollici\]
</dt> <dd>

Valore passato quando viene chiamata la funzione di callback dello stato e del frame dell'utente. Se vengono specificate entrambe le funzioni di callback, devono usare lo stesso valore del contesto utente. Il valore di questo parametro è in genere HWND o un puntatore 'this'.

</dd> <dt>

*hErrorBlob* \[ Cambio\]
</dt> <dd>

Handle a un BLOB di errori che contiene informazioni aggiuntive sull'errore. Per informazioni su ciò che si trova nel BLOB degli errori, vedere Note nella parte inferiore di questo argomento.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, il valore restituito è NMERR \_ SUCCESS.

Se il metodo ha esito negativo, il valore restituito è uno dei codici di errore seguenti,che includono gli errori restituiti dalla chiamata **interna IRTC::Configure:**



| Codice restituito                                                                                                         | Descrizione                                                                                                                                                                                                                                                                                  |
|---------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ GIÀ \_ CONNESSO**</dt> </dl>            | Questa istanza dell'oggetto COM NPP è già connessa alla rete.<br/>                                                                                                                                                                                                          |
| <dl> <dt>**ERRORE DI \_ \_ CONVERSIONE BLOB \_ NMERR**</dt> </dl>       | Il BLOB di configurazione è danneggiato. Questo errore viene generato dalla chiamata **IRTC::Configure.**<br/>                                                                                                                                                                                       |
| <dl> <dt>**LA VOCE BLOB NMERR \_ \_ NON \_ \_ \_ ESISTE**</dt> </dl> | Il BLOB di input specificato dal *parametro hInputBlob* non dispone di una voce necessaria per eseguire questa operazione. Questo errore può essere generato dalla chiamata **IRTC::Connessione** **o IRTC::Configure.** Esaminare il BLOB di errore restituito *da hErrorBlob* per determinare quale voce non è stata trovata.<br/> |
| <dl> <dt>**BLOB NMERR \_ \_ NON \_ INIZIALIZZATO**</dt> </dl>        | La **funzione CreateBlob** non è stata chiamata. Questo errore viene generato dalla chiamata **IRTC::Configure.**<br/>                                                                                                                                                                         |
| <dl> <dt>**STRINGA BLOB NMERR \_ \_ NON \_ VALIDA**</dt> </dl>         | La stringa non è con terminazione Null. Questo errore viene generato dalla chiamata **IRTC::Configure.**<br/>                                                                                                                                                                                       |
| <dl> <dt>**TRIGGER NMERR \_ NON \_ VALIDO**</dt> </dl>              | La parte trigger del BLOB di input è danneggiata. Questo errore viene generato dalla chiamata **IRTC::Configure.**<br/>                                                                                                                                                                        |
| <dl> <dt>**BLOB NON VALIDO DI NMERR \_ \_**</dt> </dl>                 | L'oggetto specificato in *hInputBlob* non è un BLOB. Questo errore viene generato dalla chiamata **IRTC::Configure.**<br/>                                                                                                                                                                      |
| <dl> <dt>**MEMORIA INSUFFICIENTE DI NMERR \_ \_ \_**</dt> </dl>               | La memoria necessaria per eseguire questa operazione non è disponibile. Questo errore viene generato dalla chiamata **IRTC::Configure.**<br/>                                                                                                                                                              |
| <dl> <dt>**NMERR \_ TIMEOUT**</dt> </dl>                       | Timeout della richiesta. Questo errore viene generato dalla chiamata **IRTC::Configure.**<br/>                                                                                                                                                                                               |
| <dl> <dt>**BLOB DI \_ LIVELLO SUPERIORE NMERR \_**</dt> </dl>                 | Il numero di versione del BLOB specificato in *hInputBlob* non è corretto. Questo errore viene generato dalla chiamata **IRTC::Configure.**<br/>                                                                                                                                                   |



 

## <a name="remarks"></a>Commenti

Quando viene **chiamato Connessione** metodo , NPP chiama automaticamente il metodo **IRTC::Configure** usando il BLOB fornito da *hInputBlob*. Si noti che tutti i codici di errore restituiti dalla chiamata a **IRTC::Configure** vengono passati nuovamente e restituiti dalla chiamata **IRTC::Connessione.**

Questo metodo deve essere chiamato prima di poter avviare l'acquisizione di frame. Si noti che quando ci si connette alla rete usando questo metodo, è necessario continuare a usare **l'interfaccia IRTC** per acquisire i frame.

Quando si chiama questa funzione, è necessario specificare una funzione di callback di stato o frame, anche se funge solo da segnaposto.

Il BLOB di input specificato da *hInputBlob* può essere ottenuto chiamando i metodi **GetNPPBlobFromUI,** **GetNPPBlobTable** e **SelectNPPBlobFromTable.**

Il BLOB di errore restituito in *hErrorBlob* contiene informazioni sugli errori che possono essere usate dallo sviluppatore o dall'applicazione per la risoluzione dei problemi. Il BLOB di errore restituito da *hErrorBlob* contiene voci che Network Monitor impossibile comprendere o trovare nel BLOB di input specificato in *hInputBlob*. Ad esempio, se viene restituito NMERR BLOB ENTRY DOES NOT EXIST, la voce Network Monitor impossibile trovare viene \_ \_ \_ \_ \_ inclusa nel BLOB degli errori restituiti.



| Per informazioni su                          | Vedere                                                                          |
|------------------------------------------------|------------------------------------------------------------------------------|
| Recupero del BLOB di input che rappresenta una scheda di interfaccia di rete | [Selezione di una scheda di interfaccia di rete](selecting-a-network-interface-card.md) |



 

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

[IRTC::Configure](irtc-configure.md)
</dt> <dt>

[IRTC::D isconnect](irtc-disconnect.md)
</dt> <dt>

[IRTC::Start](irtc-start.md)
</dt> </dl>

 

 




