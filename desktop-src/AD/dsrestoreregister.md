---
title: Funzione DsRestoreRegister (Ntdsbcli.h)
description: Registra un'operazione di ripristino.
ms.assetid: 83a56985-89be-4a95-9a8d-7c6f78d61c9a
ms.tgt_platform: multiple
keywords:
- Funzione DsRestoreRegister active Directory
topic_type:
- apiref
api_name:
- DsRestoreRegister
- DsRestoreRegisterA
- DsRestoreRegisterW
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3e878a5d2b9567ae7a483344a2240d3480620ea00706db1ed0c834fd2c5553a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118962460"
---
# <a name="dsrestoreregister-function"></a>Funzione DsRestoreRegister

\[Questa funzione è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. È possibile che in versioni successive sia stata modificata o non sia più disponibile. A partire da Windows Vista, [usare Servizio Copia Shadow del volume (VSS).](../vss/volume-shadow-copy-service-overview.md)\]

La **funzione DsRestoreRegister** registra un'operazione di ripristino. Questa funzione interlocka tutte le operazioni di ripristino successive e impedisce l'avvio della destinazione di ripristino fino a quando non viene chiamata la funzione [**DsRestoreRegisterComplete.**](dsrestoreregistercomplete.md)

## <a name="syntax"></a>Sintassi


```C++
HRESULT DsRestoreRegister(
  _In_ HBC        hbc,
  _In_ LPCTSTR    szCheckPointFilePath,
  _In_ LPCTSTR    szLogPath,
  _In_ EDB_RSTMAP rgrstmap[],
  _In_ LONG       crstmap,
  _In_ LPCTSTR    szBackupLogPath,
  _In_ ULONG      genLow,
  _In_ ULONG      genHigh
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hbc* \[ Pollici\]
</dt> <dd>

Contiene l'handle del contesto di ripristino ottenuto con la [**funzione DsRestorePrepare.**](dsrestoreprepare.md)

</dd> <dt>

*szCheckPointFilePath* \[ Pollici\]
</dt> <dd>

Puntatore a una stringa con terminazione Null che contiene il percorso del file del checkpoint. Questo percorso viene fornito dalla [**funzione DsRestoreGetDatabaseLocations**](dsrestoregetdatabaselocations.md) e ha un valore **BFT** **\_ CHECKPOINT \_ DIR**. In genere corrisponde al percorso del database di sistema. Questo percorso è necessario per la funzione di ripristino del backup appropriata. Questo parametro non può essere **NULL.** Il **passaggio di NULL** in questo parametro causerà un errore durante il processo di ripristino.

</dd> <dt>

*szLogPath* \[ Pollici\]
</dt> <dd>

Puntatore a una stringa con terminazione Null contenente il percorso in cui verranno ripristinati i file di log. Questo percorso viene fornito dalla [**funzione DsRestoreGetDatabaseLocations**](dsrestoregetdatabaselocations.md) e ha un **valore BFT** **LOG \_ \_ DIR**. Se il percorso punta a una directory vuota, vengono creati nuovi file di log. Questo parametro non può essere **NULL.**

</dd> <dt>

*rgrstmap* \[ Pollici\]
</dt> <dd>

Matrice di [**strutture \_ RSTMAP di EDB**](edb-rstmap.md) che contiene i percorsi vecchi e nuovi per ogni database. Esiste una struttura per ogni database. Per la directory è presente una struttura per il database di sistema e un'altra struttura per il database di directory. L'ordine degli elementi nella matrice non è importante. Il *parametro crstmap* contiene il numero di elementi nella matrice.

</dd> <dt>

*crstmap* \[ Pollici\]
</dt> <dd>

Contiene il numero di elementi nella matrice *rgrstmap.*

</dd> <dt>

*szBackupLogPath* \[ Pollici\]
</dt> <dd>

Puntatore a una stringa con terminazione Null che contiene il percorso in cui si trovano attualmente i file di log di cui è stato eseguito il backup. Questo parametro non può essere **NULL.**

</dd> <dt>

*genLow* \[ Pollici\]
</dt> <dd>

Contiene il numero di log più basso da ripristinare in questa sessione di ripristino. Si tratta di un numero esadecimale compreso nell'intervallo 0x00000 a 0xFFFFF.

</dd> <dt>

*genHigh* \[ Pollici\]
</dt> <dd>

Contiene il numero di log più alto da ripristinare in questa sessione di ripristino. Si tratta di un numero esadecimale compreso nell'intervallo 0x00000 a 0xFFFFF.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **S \_ OK se** la funzione ha esito positivo o un codice di errore Win32 o RPC in caso contrario. Nell'elenco seguente sono elencati i possibili codici di errore.

<dl> <dt>

**ERRORE \_ DI ACCESSO \_ NEGATO**
</dt> <dd>

Il chiamante non dispone dei privilegi di accesso adeguati per chiamare questa funzione. La [**funzione DsSetAuthIdentity**](dssetauthidentity.md) può essere usata per impostare le credenziali da usare per le funzioni di backup e ripristino.

</dd> <dt>

**ERRORE \_ PARAMETRO NON \_ VALIDO**
</dt> <dd>

Uno o più parametri non sono validi.

</dd> <dt>

**hrMissingExpiryToken**
</dt> <dd>

Il token di scadenza fornito a [**DsRestorePrepare**](dsrestoreprepare.md) non è valido. Questo valore è definito in Ntdsbmsg.h.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Ntdsbcli.h</dt> </dl>   |
| Libreria<br/>                  | <dl> <dt>Ntdsbcli.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ntdsbcli.dll</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **DsRestoreRegisterW** (Unicode) e **DsRestoreRegisterA** (ANSI)<br/>           |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**DsRestoreRegisterComplete**](dsrestoreregistercomplete.md)
</dt> <dt>

[**DsRestorePrepare**](dsrestoreprepare.md)
</dt> <dt>

[**DsRestoreGetDatabaseLocations**](dsrestoregetdatabaselocations.md)
</dt> <dt>

[**DsRestoreEnd**](dsrestoreend.md)
</dt> <dt>

[**EDB \_ RSTMAP**](edb-rstmap.md)
</dt> <dt>

[Ripristino di Active Directory](restoring-an-active-directory-server.md)
</dt> <dt>

[Funzioni di backup della directory](directory-backup-functions.md)
</dt> </dl>

 

