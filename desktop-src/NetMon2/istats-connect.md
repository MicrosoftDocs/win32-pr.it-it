---
description: 'Metodo IStats::Connessione : il metodo Connessione connette il NPP alla rete usando una scheda di interfaccia di rete specificata e fornisce informazioni di configurazione per la connessione.'
ms.assetid: 29a12df7-9c81-40ff-ac12-33ce1de833b1
title: Metodo IStats::Connessione (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IStats.Connect
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: e6521e77453ec77f81422c7903b1a394512a4c1b
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122471187"
---
# <a name="istatsconnect-method"></a>Metodo IStats::Connessione

Il **Connessione** connette il NPP alla rete usando una scheda di interfaccia di rete specificata e fornisce informazioni di configurazione per la connessione.

## <a name="syntax"></a>Sintassi


```C++
HRESULT STDMETHODCALLTYPE Connect(
  [in]  HBLOB  hInputBlob,
  [in]  LPVOID StatusCallbackProc,
  [in]  LPVOID UserContext,
  [out] HBLOB  hErrorBlob
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hInputBlob* \[ Pollici\]
</dt> <dd>

Handle al BLOB che specifica la scheda di interfaccia di rete a cui si connette NPP e le informazioni di configurazione per tale connessione.

</dd> <dt>

*StatusCallbackProc* \[ Pollici\]
</dt> <dd>

Indirizzo della funzione di callback dell'utente, che riceve gli aggiornamenti dello stato, ad esempio i trigger. Se non viene usata una funzione di callback, impostare questo parametro e il *parametro UserContext* su **NULL.**

</dd> <dt>

*UserContext* \[ Pollici\]
</dt> <dd>

Valore passato quando viene chiamata la funzione di callback dell'utente. Il valore di questo parametro è in genere HWND o un puntatore 'this'. Se non viene specificata una funzione di callback, impostare questo parametro e il *parametro StatusCallbackProc* su **NULL.**

</dd> <dt>

*hErrorBlob* \[ Cambio\]
</dt> <dd>

Handle a un BLOB di errore che contiene informazioni aggiuntive sull'errore.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, il valore restituito è NMERR \_ SUCCESS.

Se il metodo ha esito negativo, il valore restituito è uno dei codici di errore seguenti,che includono gli errori restituiti dalla chiamata **interna IStats::Configure:**




| Codice restituito | Descrizione | 
|-------------|-------------|
| <dl><dt><strong>NMERR_ALREADY_CONNECTED</strong></dt></dl> | Questa istanza dell'oggetto COM NPP è già connessa alla rete.<br /> | 
| <dl><dt><strong>NMERR_BLOB_CONVERSION_ERROR</strong></dt></dl> | Il BLOB di configurazione è danneggiato. Questo errore viene generato dalla chiamata <strong>IStats::Configure.</strong><br /> | 
| <dl><dt><strong>NMERR_BLOB_ENTRY_DOES_NOT_EXIST</strong></dt></dl> | Il BLOB di input specificato dal <em>parametro hInputBlob</em> non dispone di una voce necessaria per eseguire questa operazione. Questo errore potrebbe essere generato dalla chiamata <strong>IStats::Connessione</strong> <strong>o IStats::Configure.</strong> Esaminare il BLOB di errore restituito <em>da hErrorBlob</em> per determinare quale voce non è stata trovata.<br /> | 
| <dl><dt><strong>NMERR_BLOB_NOT_INITIALIZED</strong></dt></dl> | La <strong>funzione CreateBlob</strong> non è stata chiamata. Questo errore viene generato dalla chiamata <strong>IStats::Configure.</strong><br /> | 
| <dl><dt><strong>NMERR_BLOB_STRING_INVALID</strong></dt></dl> | La stringa non è con terminazione Null. Questo errore viene generato dalla chiamata <strong>IStats::Configure.</strong><br /> | 
| <dl><dt><strong>NMERR_ILLEGAL_TRIGGER</strong></dt></dl> | La parte trigger del BLOB di input è danneggiata. Questo errore viene generato dalla chiamata <strong>IStats::Configure.</strong><br /> | 
| <dl><dt><strong>NMERR_INVALID_BLOB</strong></dt></dl> | L'oggetto specificato in <em>hInputBlob</em> non è un BLOB. Questo errore viene generato dalla chiamata <strong>IStats::Configure.</strong><br /> | 
| <dl><dt><strong>NMERR_NO_DEFAULT_CAPTURE_DIRECTORY</strong></dt></dl> | La directory di acquisizione predefinita non è stata impostata nel Registro di sistema. Per impostare la directory di acquisizione, usare il percorso seguente. <br /><pre class="syntax" data-space="preserve"><code>HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\nm\Parameters\CapturePath</code></pre> | 
| <dl><dt><strong>NMERR_OUT_OF_MEMORY</strong></dt></dl> | La memoria necessaria per eseguire questa operazione non era disponibile. Questo errore viene generato dalla chiamata <strong>IStats::Configure.</strong><br /> | 
| <dl><dt><strong>NMERR_TIMEOUT</strong></dt></dl> | Timeout della richiesta. Questo errore viene generato dalla chiamata <strong>IStats::Configure.</strong><br /> | 
| <dl><dt><strong>NMERR_UPLEVEL_BLOB</strong></dt></dl> | Il numero di versione del BLOB specificato in <em>hInputBlob</em> non è corretto. Questo errore viene generato dalla chiamata <strong>IStats::Configure.</strong><br /> | 




 

## <a name="remarks"></a>Commenti

Quando viene **chiamato Connessione** metodo, Network Monitor chiama automaticamente il metodo **IStats::Configure** usando il BLOB fornito dal *parametro hInputBlob.* Si noti che tutti i codici di errore restituiti dalla chiamata a **IStats::Configure** vengono restituiti dalla chiamata **IStats::Connessione.**

Questo metodo deve essere chiamato prima di poter avviare l'acquisizione di fotogrammi. Si noti che quando ci si connette alla rete usando questo metodo, è necessario continuare a usare **l'interfaccia IStats** per acquisire i frame.

Il BLOB di input specificato da *hInputBlob* può essere ottenuto chiamando i metodi **GetNPPBlobFromUI,** **GetNPPBlobTable** e **SelectNPPBlobFromTable.**

Il BLOB di errore restituito dal parametro *hErrorBlob* contiene voci che Network Monitor impossibile comprendere o trovare nel BLOB di input specificato in *hInputBlob*. Il BLOB degli errori restituito contiene informazioni sugli errori che l'applicazione può usare per la risoluzione dei problemi. Ad esempio, se viene restituito NMERR BLOB ENTRY DOES NOT EXIST, la voce Network Monitor non è stata individuata viene \_ \_ \_ \_ \_ inclusa nel BLOB di errore restituito.



| Per informazioni su                                             | Vedere                                                                          |
|-------------------------------------------------------------------|------------------------------------------------------------------------------|
| Recupero del BLOB di input che rappresenta una scheda di interfaccia di rete | [Selezione di una scheda di interfaccia di rete](selecting-a-network-interface-card.md) |



 

## <a name="requirements"></a>Requisiti



| Requisito | valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                                                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                                                                     |
| Intestazione<br/>                   | <dl> <dt>Netmon.h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[IStat](istats.md)
</dt> <dt>

[IStats::Configure](istats-configure.md)
</dt> <dt>

[IStats::D isconnect](istats-disconnect.md)
</dt> <dt>

[Network Monitor BLOB](network-monitor-blobs.md)
</dt> </dl>

 

 




