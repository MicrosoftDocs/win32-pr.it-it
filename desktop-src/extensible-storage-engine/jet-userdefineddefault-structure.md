---
description: 'Altre informazioni su: JET_USERDEFINEDDEFAULT Structure'
title: JET_USERDEFINEDDEFAULT struttura
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
ms.openlocfilehash: a8e5cfe4fadf0dead2e11787255089d251a98f67
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122479307"
---
# <a name="jet_userdefineddefault-structure"></a>JET_USERDEFINEDDEFAULT struttura


_**Si applica a:** Windows | Windows Server_

## <a name="jet_userdefineddefault-structure"></a>JET_USERDEFINEDDEFAULT struttura

La **JET_USERDEFINEDDEFAULT** viene specificata in combinazione con JET_bitColumnUserDefinedDefault per assegnare a una nuova colonna un valore predefinito determinato tramite un callback. Questa tecnica può essere usata per implementare colonne calcolate.

**Windows XP:** La **JET_USERDEFINEDDEFAULT** è stata introdotta in Windows XP.

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

Nome di esportazione della funzione che implementa il callback in formato "module \! function".

Il callback viene mantenuto come parte dello schema della colonna. L'eseguibile host effettivo e il nome di esportazione della funzione devono essere mantenuti per consentire la ricerca dell'indirizzo effettivo della funzione in fase di esecuzione.

Il nome del modulo è il nome del file binario host che contiene la funzione. Il nome della funzione è il nome dell'esportazione per tale funzione. Queste due informazioni verranno usate dal motore di database in fase di esecuzione per individuare l'indirizzo reale del callback eseguendo una chiamata [LoadLibrary](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) sul nome del modulo seguito da una [chiamata GetProcAddress](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) sul nome della funzione.

Ad esempio, se il callback è stato implementato in una DLL denominata MyCallback.DLL e tale DLL è stata archiviata in C: MyApplication e la funzione che implementa il callback è stata esportata dalla DLL come UserDefinedDefaultCallback, la stringa richiesta sarà \\ "C: \\ MyApplication \\MyCallback.DLL\! UserDefinedDefaultCallback".

**Nota:**  Embedded " \! " I caratteri nella parte del modulo del nome di callback non sono supportati.

È consigliabile usare un nome di callback che non sia una funzione dell'architettura host. Ad esempio, non usare le esportazioni decorate come stdcall ( ) perché questa convenzione UserDefinedDefaultCallback@32 di chiamata è supportata solo nei computer x86. Se è stato usato un callback di questo tipo, il database può essere usato solo in un computer x86. In questo caso, è necessario usare un alias per eseguire un'esportazione indipendente dalla piattaforma.

È consigliabile usare il percorso completo del nome del modulo che implementa il callback. Se si usa un percorso relativo, il processo che ospita il database potrebbe essere soggetto ad attacchi da parte di un file binario non autorizzato.

L'applicazione deve passare solo callback attendibili al motore di database. Il motore di database carica il file binario per verificarne l'esistenza quando viene creata la colonna associata. Se il percorso del file binario non viene convalidato o considerato attendibile, potrebbe attaccare il processo che ospita il database.

**pbUserData**

Blocco autonomo di dati definiti dall'utente da passare al callback quando viene richiamato. Il blocco di dati fornito verrà mantenuto come parte dello schema della colonna. Di conseguenza, il blocco di dati deve essere completamente indipendente e non può fare riferimento a dati esterni all'ambito del database.

Se **pbUserData** è zero, il valore di **cbUserData** viene ignorato. In questo caso, non verrà passato alcun dato definito dall'utente al callback quando viene richiamato.

**cbUserData**

Vedere **pbUserData**.

**szDependantColumns**

Riservato per utilizzi futuri.

Questo membro deve sempre essere impostato su NULL.

### <a name="requirements"></a>Requisiti


| | | <p><strong>Client</strong></p> | <p>Richiede Windows Vista, Windows XP o Windows 2000 Professional.</p> | | <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | | <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | | <p><strong>Unicode</strong></p> | <p>Implementato come <strong>JET_ USERDEFINEDDEFAULT_W</strong> (Unicode) <strong>e JET_ USERDEFINEDDEFAULT_A</strong> (ANSI).</p> | 



### <a name="see-also"></a>Vedere anche

[JET_CBTYP](./jet-cbtyp.md)  
[JET_COLUMNCREATE](./jet-columncreate-structure.md)  
[JET_COLUMNDEF](./jet-columndef-structure.md)
