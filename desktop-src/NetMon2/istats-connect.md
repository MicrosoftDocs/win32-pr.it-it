---
description: Il metodo Connect connette l'oggetto NPP alla rete utilizzando una scheda di interfaccia di rete specificata e fornisce le informazioni di configurazione per la connessione.
ms.assetid: 29a12df7-9c81-40ff-ac12-33ce1de833b1
title: 'Metodo IStats:: Connect (Netmon. h)'
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
ms.openlocfilehash: 7705600c3ce68b719014c928ac4d02c62cba64cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885846"
---
# <a name="istatsconnect-method"></a>IStats:: Connect (metodo)

Il metodo **Connect** connette l'oggetto NPP alla rete utilizzando una scheda di interfaccia di rete specificata e fornisce le informazioni di configurazione per la connessione.

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

Handle per il BLOB che specifica la scheda di interfaccia di rete a cui si connette l'oggetto NPP e le informazioni di configurazione per tale connessione.

</dd> <dt>

*StatusCallbackProc* \[ in\]
</dt> <dd>

Indirizzo della funzione di callback dell'utente, che riceve gli aggiornamenti di stato, ad esempio i trigger. Se non viene utilizzata una funzione di callback, impostare questo parametro e il parametro *userContext* su **null**.

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

Se il metodo ha esito positivo, il valore restituito è NMERR \_ Success.

Se il metodo ha esito negativo, il valore restituito è uno dei codici di errore seguenti (che includono gli errori restituiti dalla chiamata Internal **IStats:: Configure** ):



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
<td>Il BLOB di configurazione è danneggiato. Questo errore viene generato dalla chiamata <strong>IStats:: Configure</strong> .<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>NMERR_BLOB_ENTRY_DOES_NOT_EXIST</strong></dt> </dl></td>
<td>Il BLOB di input specificato dal parametro <em>hInputBlob</em> non dispone di una voce necessaria per eseguire questa operazione. Questo errore potrebbe essere generato dalla chiamata <strong>IStats:: Connect</strong> o <strong>IStats:: Configure</strong> . Esaminare il BLOB di errore restituito da <em>hErrorBlob</em> per determinare quale voce non è stata trovata.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>NMERR_BLOB_NOT_INITIALIZED</strong></dt> </dl></td>
<td>La funzione <strong>CreateBlob</strong> non è stata chiamata. Questo errore viene generato dalla chiamata <strong>IStats:: Configure</strong> .<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>NMERR_BLOB_STRING_INVALID</strong></dt> </dl></td>
<td>La stringa non termina con null. Questo errore viene generato dalla chiamata <strong>IStats:: Configure</strong> .<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>NMERR_ILLEGAL_TRIGGER</strong></dt> </dl></td>
<td>La parte del trigger del BLOB di input è danneggiata. Questo errore viene generato dalla chiamata <strong>IStats:: Configure</strong> .<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>NMERR_INVALID_BLOB</strong></dt> </dl></td>
<td>L'oggetto specificato in <em>hInputBlob</em> non è un BLOB. Questo errore viene generato dalla chiamata <strong>IStats:: Configure</strong> .<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>NMERR_NO_DEFAULT_CAPTURE_DIRECTORY</strong></dt> </dl></td>
<td>La directory di acquisizione predefinita non è stata impostata nel registro di sistema. Per impostare la directory di acquisizione, utilizzare il percorso seguente. <br/>
<pre class="syntax" data-space="preserve"><code>HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\nm\Parameters\CapturePath</code></pre></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>NMERR_OUT_OF_MEMORY</strong></dt> </dl></td>
<td>La memoria necessaria per eseguire questa operazione non è disponibile. Questo errore viene generato dalla chiamata <strong>IStats:: Configure</strong> .<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>NMERR_TIMEOUT</strong></dt> </dl></td>
<td>Timeout della richiesta. Questo errore viene generato dalla chiamata <strong>IStats:: Configure</strong> .<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>NMERR_UPLEVEL_BLOB</strong></dt> </dl></td>
<td>Il numero di versione del BLOB specificato in <em>hInputBlob</em> non è corretto. Questo errore viene generato dalla chiamata <strong>IStats:: Configure</strong> .<br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Commenti

Quando viene chiamato il metodo **Connect** , Network Monitor chiama automaticamente il metodo **IStats:: Configure** usando il BLOB fornito dal parametro *hInputBlob* . Si noti che qualsiasi codice di errore restituito dalla chiamata a **IStats:: Configure** viene passato nuovamente e restituito dalla chiamata **IStats:: Connect** .

Questo metodo deve essere chiamato prima che sia possibile avviare l'acquisizione di frame. Si noti che quando ci si connette alla rete usando questo metodo, è necessario continuare a usare l'interfaccia **IStats** per acquisire i frame.

Il BLOB di input specificato da *hInputBlob* può essere ottenuto chiamando i metodi **GetNPPBlobFromUI**, **GetNPPBlobTable** e **SelectNPPBlobFromTable** .

Il BLOB di errori restituito dal parametro *hErrorBlob* contiene voci che Network Monitor non è stato in grado di comprendere o trovare nel BLOB di input specificato in *hInputBlob*. Il BLOB di errori restituito contiene informazioni sugli errori che possono essere utilizzate dall'applicazione per la risoluzione dei problemi. Se, ad esempio, \_ \_ \_ \_ \_ viene restituita la voce del BLOB NMERR non esiste, la voce che Network Monitor non è stata trovata è inclusa nel BLOB di errore restituito.



| Per informazioni su                                             | Vedere                                                                          |
|-------------------------------------------------------------------|------------------------------------------------------------------------------|
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

[IStats](istats.md)
</dt> <dt>

[IStats:: Configure](istats-configure.md)
</dt> <dt>

[IStats::D la connessione](istats-disconnect.md)
</dt> <dt>

[BLOB Network Monitor](network-monitor-blobs.md)
</dt> </dl>

 

 




