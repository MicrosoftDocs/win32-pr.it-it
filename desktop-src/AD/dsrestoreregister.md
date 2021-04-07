---
title: Funzione DsRestoreRegister (ntdsbcli. h)
description: Registra un'operazione di ripristino.
ms.assetid: 83a56985-89be-4a95-9a8d-7c6f78d61c9a
ms.tgt_platform: multiple
keywords:
- Active Directory funzione DsRestoreRegister
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
ms.openlocfilehash: 610d49c73ade9bab47c95e90af73bac606f4bd23
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048483"
---
# <a name="dsrestoreregister-function"></a>DsRestoreRegister (funzione)

\[Questa funzione è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. È possibile che in versioni successive sia stata modificata o non sia più disponibile. A partire da Windows Vista, usare invece [servizio Copia Shadow del volume (VSS)](../vss/volume-shadow-copy-service-overview.md) .\]

La funzione **DsRestoreRegister** registra un'operazione di ripristino. Questa funzione consente di bloccare tutte le successive operazioni di ripristino e impedisce l'avvio della destinazione di ripristino fino a quando non viene chiamata la funzione [**DsRestoreRegisterComplete**](dsrestoreregistercomplete.md) .

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

*HBC* \[ in\]
</dt> <dd>

Contiene l'handle del contesto di ripristino ottenuto con la funzione [**DsRestorePrepare**](dsrestoreprepare.md) .

</dd> <dt>

*szCheckPointFilePath* \[ in\]
</dt> <dd>

Puntatore a una stringa con terminazione null che contiene il percorso del file del checkpoint. Questo percorso viene fornito dalla funzione [**DsRestoreGetDatabaseLocations**](dsrestoregetdatabaselocations.md) e ha un valore **BFT** di **BFT \_ Checkpoint \_ dir**. Corrisponde in genere al percorso del database di sistema. Questo percorso è necessario per la corretta funzione di ripristino del backup. Questo parametro non può essere **null**. Il passaggio di un **valore null** in questo parametro causerà un errore durante il processo di ripristino.

</dd> <dt>

*szLogPath* \[ in\]
</dt> <dd>

Puntatore a una stringa con terminazione null che contiene il percorso in cui verranno ripristinati i file di log. Questo percorso viene fornito dalla funzione [**DsRestoreGetDatabaseLocations**](dsrestoregetdatabaselocations.md) e ha un valore **BFT** di **BFT \_ log \_ dir**. Se il percorso punta a una directory vuota, vengono creati nuovi file di log. Questo parametro non può essere **null**.

</dd> <dt>

*rgrstmap* \[ in\]
</dt> <dd>

Matrice di strutture [**\_ RSTMAP edb**](edb-rstmap.md) che contiene i percorsi vecchi e nuovi per ogni database. Esiste una struttura per ogni database. Per la directory, esiste una struttura per il database di sistema e un'altra struttura per il database di directory. L'ordine degli elementi nella matrice non è rilevante. Il parametro *crstmap* contiene il numero di elementi nella matrice.

</dd> <dt>

*crstmap* \[ in\]
</dt> <dd>

Contiene il numero di elementi nella matrice *rgrstmap* .

</dd> <dt>

*szBackupLogPath* \[ in\]
</dt> <dd>

Puntatore a una stringa con terminazione null che contiene il percorso in cui risiedono attualmente i file di log di cui è stato eseguito il backup. Questo parametro non può essere **null**.

</dd> <dt>

*genLow* \[ in\]
</dt> <dd>

Contiene il numero di log più basso da ripristinare in questa sessione di ripristino. Si tratta di un numero esadecimale compreso nell'intervallo tra 0x00000 e 0xFFFFF.

</dd> <dt>

*genHigh* \[ in\]
</dt> <dd>

Contiene il numero massimo di log da ripristinare in questa sessione di ripristino. Si tratta di un numero esadecimale compreso nell'intervallo tra 0x00000 e 0xFFFFF.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **\_ OK** se la funzione ha esito positivo o un codice di errore Win32 o RPC in caso contrario. Nell'elenco seguente sono elencati i possibili codici di errore.

<dl> <dt>

**ERRORE di \_ accesso \_ negato**
</dt> <dd>

Il chiamante non dispone dei privilegi di accesso appropriati per chiamare questa funzione. La funzione [**DsSetAuthIdentity**](dssetauthidentity.md) può essere utilizzata per impostare le credenziali da utilizzare per le funzioni di backup e ripristino.

</dd> <dt>

**ERRORE \_ parametro non valido \_**
</dt> <dd>

Uno o più parametri non sono validi.

</dd> <dt>

**hrMissingExpiryToken**
</dt> <dd>

Il token di scadenza fornito a [**DsRestorePrepare**](dsrestoreprepare.md) non è valido. Questo valore è definito in ntdsbmsg. h.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Ntdsbcli. h</dt> </dl>   |
| Libreria<br/>                  | <dl> <dt>Ntdsbcli. lib</dt> </dl> |
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

[**\_RSTMAP edb**](edb-rstmap.md)
</dt> <dt>

[Ripristino di Active Directory](restoring-an-active-directory-server.md)
</dt> <dt>

[Funzioni di backup della directory](directory-backup-functions.md)
</dt> </dl>

 

