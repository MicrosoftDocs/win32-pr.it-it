---
description: 'Altre informazioni su: struttura JET_USERDEFINEDDEFAULT'
title: Struttura JET_USERDEFINEDDEFAULT
TOCTitle: JET_USERDEFINEDDEFAULT Structure
ms:assetid: 1f0a5419-9fae-4a93-a271-2f9772ecc996
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269200(v=EXCHG.10)
ms:contentKeyID: 32765503
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e5f588588a1a6769e997264321f8911a86e169c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318104"
---
# <a name="jet_userdefineddefault-structure"></a>Struttura JET_USERDEFINEDDEFAULT


_**Si applica a:** Windows | Windows Server_

## <a name="jet_userdefineddefault-structure"></a>Struttura JET_USERDEFINEDDEFAULT

La struttura **JET_USERDEFINEDDEFAULT** viene specificata in combinazione con JET_bitColumnUserDefinedDefault per assegnare a una nuova colonna un valore predefinito che viene determinato tramite un callback. Questa tecnica può essere utilizzata per implementare le colonne calcolate.

**Windows XP:** La struttura **JET_USERDEFINEDDEFAULT** è stata introdotta in Windows XP.

```cpp
    typedef struct tag_JET_USERDEFINEDDEFAULT {
      tchar* szCallback;
      unsigned char* pbUserData;
      unsigned long cbUserData;
      tchar* szDependantColumns;
    } JET_USERDEFINEDDEFAULT;
```

### <a name="members"></a>Membri

**szCallback**

Nome di esportazione della funzione che implementa il callback nel \! formato "funzione modulo".

Il callback viene mantenuto come parte dello schema della colonna. Il file eseguibile host effettivo e il nome di esportazione della funzione devono essere salvati in modo permanente per abilitare la ricerca dell'indirizzo reale della funzione in fase di esecuzione.

Il nome del modulo è il nome del file binario host che contiene la funzione. Il nome della funzione è il nome dell'esportazione per la funzione. Queste due informazioni verranno usate dal motore di database in fase di esecuzione per individuare il vero indirizzo del callback eseguendo una chiamata [LoadLibrary](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) sul nome del modulo seguito da una chiamata [GetProcAddress](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) sul nome della funzione.

Se, ad esempio, il callback è stato implementato in una DLL denominata MyCallback.DLL e tale DLL è stata archiviata in C: \\ MyApplication e la funzione che implementa il callback è stata esportata dalla dll come UserDefinedDefaultCallback, la stringa richiesta sarà "C: \\ MyApplication \\MyCallback.DLL\! UserDefinedDefaultCallback".

**Nota**  Incorporato " \! " i caratteri nella parte del modulo del nome del callback non sono supportati.

Si consiglia vivamente di utilizzare un nome di callback che non sia una funzione dell'architettura host. Ad esempio, non usare le esportazioni decorate come stdcall ( UserDefinedDefaultCallback@32 ) perché questa convenzione di chiamata è supportata solo su computer x86. Se è stato usato un callback di questo tipo, il database può essere usato solo in un computer x86. In questo caso, è necessario usare un alias per eseguire un'esportazione indipendente dalla piattaforma.

Si consiglia vivamente di usare il percorso completo del nome del modulo che implementa il callback. Se viene utilizzato un percorso relativo, il processo che ospita il database potrebbe essere soggetto ad attacchi da parte di un file binario non autorizzato.

L'applicazione deve passare solo i callback attendibili al motore di database. Il motore di database caricherà il file binario per verificarne l'esistenza quando viene creata la colonna associata. Se il percorso del file binario non viene convalidato o considerato attendibile, potrebbe attaccare il processo che ospita il database.

**pbUserData**

Blocco autonomo di dati definiti dall'utente da passare al callback quando viene richiamato. Il blocco di dati fornito verrà mantenuto come parte dello schema della colonna. Di conseguenza, il blocco di dati deve essere completamente indipendente e non può fare riferimento ad alcun dato esterno all'ambito del database.

Se **pbUserData** è zero, il valore di **cbUserData** viene ignorato. In questo caso, non verrà passato alcun dato definito dall'utente al callback quando viene richiamato.

**cbUserData**

Vedere **pbUserData**.

**szDependantColumns**

Riservato per utilizzi futuri.

Questo membro deve essere sempre impostato su NULL.

### <a name="requirements"></a>Requisiti

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Client</strong></p></td>
<td><p>Richiede Windows Vista, Windows XP o Windows 2000 Professional.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Intestazione</strong></p></td>
<td><p>Dichiarata in esent. h.</p></td>
</tr>
<tr class="even">
<td><p><strong>Unicode</strong></p></td>
<td><p>Implementato come <strong>JET_ USERDEFINEDDEFAULT_W</strong> (Unicode) e <strong>JET_ USERDEFINEDDEFAULT_A</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Vedere anche

[JET_CBTYP](./jet-cbtyp.md)  
[JET_COLUMNCREATE](./jet-columncreate-structure.md)  
[JET_COLUMNDEF](./jet-columndef-structure.md)
