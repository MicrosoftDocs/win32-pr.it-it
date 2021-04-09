---
description: Il metodo Connect connette l'oggetto NPP alla rete utilizzando una scheda di interfaccia di rete specificata e fornisce le informazioni di configurazione relative alla connessione.
ms.assetid: aae9ff9c-d077-4db2-a900-9916e4f7bb8b
title: 'Metodo IDelaydC:: Connect (Netmon. h)'
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
ms.openlocfilehash: b2cd1fb5ad694493c4a225aa3bf109d7775b9dd6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878642"
---
# <a name="idelaydcconnect-method"></a>Metodo IDelaydC:: Connect

Il metodo **Connect** connette l'oggetto NPP alla rete utilizzando una scheda di interfaccia di rete specificata e fornisce le informazioni di configurazione relative alla connessione.

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

*hInputBlob* \[ in\]
</dt> <dd>

Handle per il BLOB che specifica la scheda di interfaccia di rete a cui ci si connette e le informazioni di configurazione relative a tale connessione.

</dd> <dt>

*StatusCallbackProc* \[ in\]
</dt> <dd>

Indirizzo della funzione di callback dell'utente, che viene usata per ricevere gli aggiornamenti di stato, ad esempio i trigger. Se non viene usata alcuna funzione di callback, impostare questo parametro e il parametro *userContext* su **null**.

</dd> <dt>

*UserContext* \[ in\]
</dt> <dd>

Valore passato quando viene chiamata la funzione di callback dell'utente. Il valore di questo parametro è in genere HWND o un puntatore ' This '. Se non viene specificata una funzione di callback, impostare questo parametro e il parametro *StatusCallbackProc* su **null**.

</dd> <dt>

*hErrorBlob* \[ out\]
</dt> <dd>

Handle per un BLOB di errori che contiene informazioni aggiuntive sull'errore.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, il valore restituito è NMERR \_ Success.

Se il metodo ha esito negativo, il valore restituito è uno dei codici di errore seguenti (che includono gli errori restituiti dalla chiamata interna **IDelaydC:: Configure** ):



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Codice restituito</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><dl> <dt><strong>NMERR_ALREADY_CONNECTED</strong></dt> </dl></td>
<td>Questa istanza dell'oggetto COM NPP è già connessa alla rete.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>NMERR_BLOB_CONVERSION_ERROR</strong></dt> </dl></td>
<td>Il BLOB di configurazione è danneggiato. Questo errore viene generato dalla chiamata <strong>IDelaydC:: Configure</strong> .<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>NMERR_BLOB_ENTRY_DOES_NOT_EXIST</strong></dt> </dl></td>
<td>Per il BLOB di input specificato da <em>hInputBlob</em> manca una voce necessaria per eseguire questa operazione. Questo errore può essere generato dalla chiamata <strong>IDelaydC:: Connect</strong> o <strong>IDelaydC:: Configure</strong> . Esaminare il BLOB di errore restituito da <em>hErrorBlob</em> per determinare quale voce non è stata trovata.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>NMERR_BLOB_NOT_INITIALIZED</strong></dt> </dl></td>
<td>La funzione <strong>CreateBlob</strong> non è stata chiamata. Questo errore viene generato dalla chiamata <strong>IDelaydC:: Configure</strong> .<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>NMERR_BLOB_STRING_INVALID</strong></dt> </dl></td>
<td>La stringa non termina con null. Questo errore viene generato dalla chiamata <strong>IDelaydC:: Configure</strong> .<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>NMERR_ILLEGAL_TRIGGER</strong></dt> </dl></td>
<td>La parte del trigger del BLOB di input è danneggiata. Questo errore viene generato dalla chiamata <strong>IDelaydC:: Configure</strong> .<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>NMERR_INVALID_BLOB</strong></dt> </dl></td>
<td>L'oggetto specificato in <em>hInputBlob</em> non è un BLOB. Questo errore viene generato dalla chiamata <strong>IDelaydC:: Configure</strong> .<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>NMERR_NO_DEFAULT_CAPTURE_DIRECTORY</strong></dt> </dl></td>
<td>La directory di acquisizione predefinita non è stata impostata nel registro di sistema. Usare il percorso seguente per impostare la directory di acquisizione. <br/>
<pre class="syntax" data-space="preserve"><code>HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\nm\Parameters\CapturePath</code></pre></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>NMERR_OUT_OF_MEMORY</strong></dt> </dl></td>
<td>Memoria non disponibile per l'esecuzione di questa operazione. Questo errore viene generato dalla chiamata <strong>IDelaydC:: Configure</strong> .<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>NMERR_TIMEOUT</strong></dt> </dl></td>
<td>Timeout della richiesta. Questo errore viene generato dalla chiamata <strong>IDelaydC:: Configure</strong> .<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>NMERR_UPLEVEL_BLOB</strong></dt> </dl></td>
<td>Il numero di versione del BLOB specificato in <em>hInputBlob</em> non è corretto. Questo errore viene generato dalla chiamata <strong>IDelaydC:: Configure</strong> .<br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Commenti

Quando viene chiamato il metodo **Connect** , l'oggetto NPP chiama automaticamente **IDelaydC:: Configure** usando il BLOB fornito da *hInputBlob*. Si noti che tutti i codici di errore restituiti dalla chiamata a **IDelaydC:: Configure** vengono passati nuovamente e restituiti dalla chiamata **IDelaydC:: Connect** .

Questo metodo deve essere chiamato prima che sia possibile avviare l'acquisizione di frame. Si noti che quando ci si connette alla rete usando questo metodo, è necessario continuare a usare i metodi dell'interfaccia **IDelaydC** per acquisire i frame.

Il BLOB di input specificato dal parametro *hInputBlob* può essere ottenuto chiamando **GetNPPBlobFromUI**, **GetNPPBlobTable** e **SelectNPPBlobFromTable**.

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

[IDelaydC](idelaydc.md)
</dt> <dt>

[IDelaydC:: Configure](idelaydc-configure.md)
</dt> <dt>

[IDelaydC::D la connessione](idelaydc-disconnect.md)
</dt> <dt>

[IDelaydC:: Start](idelaydc-start.md)
</dt> </dl>

 

 




