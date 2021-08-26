---
description: Il Connessione connette il NPP alla rete usando una scheda di interfaccia di rete specificata e fornisce informazioni di configurazione sulla connessione.
ms.assetid: aae9ff9c-d077-4db2-a900-9916e4f7bb8b
title: Metodo IDelaydC::Connessione (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDelaydC.Connect
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: e91db1dae0c67c5f35e46841867d3d3e15058cf0
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122477306"
---
# <a name="idelaydcconnect-method"></a>Metodo IDelaydC::Connessione

Il **Connessione** connette il protocollo NPP alla rete usando una scheda di interfaccia di rete specificata e fornisce informazioni di configurazione sulla connessione.

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

Handle al BLOB che specifica la scheda di interfaccia di rete a cui ci si connette e le informazioni di configurazione relative a tale connessione.

</dd> <dt>

*StatusCallbackProc* \[ Pollici\]
</dt> <dd>

Indirizzo della funzione di callback dell'utente, usata per ricevere gli aggiornamenti dello stato, ad esempio i trigger. Se non viene usata alcuna funzione di callback, impostare questo parametro e *il parametro UserContext* su **NULL.**

</dd> <dt>

*Oggetto UserContext* \[ Pollici\]
</dt> <dd>

Valore passato quando viene chiamata la funzione di callback dell'utente. Il valore di questo parametro è in genere HWND o un puntatore 'this'. Se non viene specificata una funzione di callback, impostare questo parametro e *il parametro StatusCallbackProc* su **NULL.**

</dd> <dt>

*hErrorBlob* \[ Cambio\]
</dt> <dd>

Handle a un BLOB di errore che contiene informazioni aggiuntive sull'errore.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, il valore restituito è NMERR \_ SUCCESS.

Se il metodo ha esito negativo, il valore restituito è uno dei codici di errore seguenti( che includono gli errori restituiti dalla chiamata **interna IDelaydC::Configure):**




| Codice restituito | Descrizione | 
|-------------|-------------|
| <dl><dt><strong>NMERR_ALREADY_CONNECTED</strong></dt></dl> | Questa istanza dell'oggetto COM NPP è già connessa alla rete.<br /> | 
| <dl><dt><strong>NMERR_BLOB_CONVERSION_ERROR</strong></dt></dl> | Il BLOB di configurazione è danneggiato. Questo errore viene generato dalla <strong>chiamata di IDelaydC::Configure.</strong><br /> | 
| <dl><dt><strong>NMERR_BLOB_ENTRY_DOES_NOT_EXIST</strong></dt></dl> | Nel BLOB di input specificato <em>da hInputBlob</em> manca una voce necessaria per eseguire questa operazione. Questo errore può essere generato dalla <strong>chiamata di IDelaydC::Connessione</strong> <strong>o IDelaydC::Configure.</strong> Esaminare il BLOB di errore restituito <em>da hErrorBlob</em> per determinare quale voce non è stata trovata.<br /> | 
| <dl><dt><strong>NMERR_BLOB_NOT_INITIALIZED</strong></dt></dl> | La <strong>funzione CreateBlob</strong> non è stata chiamata. Questo errore viene generato dalla <strong>chiamata di IDelaydC::Configure.</strong><br /> | 
| <dl><dt><strong>NMERR_BLOB_STRING_INVALID</strong></dt></dl> | La stringa non ha terminazione Null. Questo errore viene generato dalla <strong>chiamata di IDelaydC::Configure.</strong><br /> | 
| <dl><dt><strong>NMERR_ILLEGAL_TRIGGER</strong></dt></dl> | La parte trigger del BLOB di input è danneggiata. Questo errore viene generato dalla <strong>chiamata di IDelaydC::Configure.</strong><br /> | 
| <dl><dt><strong>NMERR_INVALID_BLOB</strong></dt></dl> | L'oggetto specificato in <em>hInputBlob</em> non è un BLOB. Questo errore viene generato dalla <strong>chiamata di IDelaydC::Configure.</strong><br /> | 
| <dl><dt><strong>NMERR_NO_DEFAULT_CAPTURE_DIRECTORY</strong></dt></dl> | La directory di acquisizione predefinita non è stata impostata nel Registro di sistema. Usare il percorso seguente per impostare la directory di acquisizione. <br /><pre class="syntax" data-space="preserve"><code>HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\nm\Parameters\CapturePath</code></pre> | 
| <dl><dt><strong>NMERR_OUT_OF_MEMORY</strong></dt></dl> | Non era disponibile memoria per eseguire questa operazione. Questo errore viene generato dalla <strong>chiamata di IDelaydC::Configure.</strong><br /> | 
| <dl><dt><strong>NMERR_TIMEOUT</strong></dt></dl> | Timeout della richiesta. Questo errore viene generato dalla <strong>chiamata di IDelaydC::Configure.</strong><br /> | 
| <dl><dt><strong>NMERR_UPLEVEL_BLOB</strong></dt></dl> | Il numero di versione del BLOB specificato in <em>hInputBlob</em> non è corretto. Questo errore viene generato dalla <strong>chiamata di IDelaydC::Configure.</strong><br /> | 




 

## <a name="remarks"></a>Commenti

Quando viene **Connessione** metodo , il NPP chiama **automaticamente IDelaydC::Configure** usando il BLOB fornito da *hInputBlob*. Si noti che tutti i codici di errore restituiti dalla chiamata a **IDelaydC::Configure** vengono restituiti dalla chiamata a **IDelaydC::Connessione.**

Questo metodo deve essere chiamato prima di poter avviare l'acquisizione di frame. Si noti che quando ci si connette alla rete usando questo metodo, è necessario continuare a usare i metodi dell'interfaccia **IDelaydC** per acquisire i frame.

Il BLOB di input specificato dal parametro *hInputBlob* può essere ottenuto chiamando **GetNPPBlobFromUI,** **GetNPPBlobTable** e **SelectNPPBlobFromTable.**

Il BLOB di errore restituito in *hErrorBlob contiene* informazioni sull'errore che possono essere usate dallo sviluppatore o dall'applicazione per la risoluzione dei problemi. Il BLOB di errore restituito da *hErrorBlob* contiene voci che Network Monitor non sono in grado di comprendere o trovare nel BLOB di input specificato in *hInputBlob*. Ad esempio, se viene restituito NMERR BLOB ENTRY DOES NOT EXIST, la voce Network Monitor impossibile trovare è \_ \_ \_ \_ \_ inclusa nel BLOB di errore restituito.



| Per informazioni su                          | Vedere                                                                          |
|------------------------------------------------|------------------------------------------------------------------------------|
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

[IDelaydC](idelaydc.md)
</dt> <dt>

[IDelaydC::Configure](idelaydc-configure.md)
</dt> <dt>

[IDelaydC::D isconnect](idelaydc-disconnect.md)
</dt> <dt>

[IDelaydC::Start](idelaydc-start.md)
</dt> </dl>

 

 




