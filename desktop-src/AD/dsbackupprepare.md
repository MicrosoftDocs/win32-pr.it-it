---
title: Funzione DsBackupPrepare (ntdsbcli. h)
description: Prepara la directory sul server specificato per il backup online e restituisce un handle del contesto di backup utilizzato nelle chiamate successive ad altre funzioni di backup.
ms.assetid: 18c6dbcf-b707-4674-9af5-40f2178e6d2b
ms.tgt_platform: multiple
keywords:
- Active Directory funzione DsBackupPrepare
topic_type:
- apiref
api_name:
- DsBackupPrepare
- DsBackupPrepareA
- DsBackupPrepareW
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa561a7e41164ece68fb18fd882a8b05d6357cec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477134"
---
# <a name="dsbackupprepare-function"></a>DsBackupPrepare (funzione)

\[Questa funzione è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. È possibile che in versioni successive sia stata modificata o non sia più disponibile. A partire da Windows Vista, usare invece [servizio Copia Shadow del volume (VSS)](../vss/volume-shadow-copy-service-overview.md) .\]

La funzione **DsBackupPrepare** prepara la directory sul server specificato per il backup online e restituisce un handle del contesto di backup utilizzato nelle chiamate successive ad altre funzioni di backup.

## <a name="syntax"></a>Sintassi


```C++
HRESULT DsBackupPrepare(
  _In_  LPCTSTR szBackupServer,
  _In_  ULONG   grbit,
  _In_  ULONG   btBackupType,
  _Out_ PVOID   *ppvExpiryToken,
  _Out_ LPDWORD pcbExpiryTokenSize,
  _Out_ HBC     *phbc
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*szBackupServer* \[ in\]
</dt> <dd>

Puntatore a una stringa con terminazione null che contiene il nome del server di cui eseguire il backup. Le barre rovesciate precedenti sono facoltative. Il server deve essere lo stesso computer da cui viene chiamata la funzione. Il nome del server non può contenere un carattere di sottolineatura ( \_ ). Un esempio di nome di server è " \\ \\ Server1".

</dd> <dt>

*grbit* \[ in\]
</dt> <dd>

Determina se verrà eseguito il backup dei file di log. Questo valore deve essere sempre 0 perché i backup incrementali non sono supportati.

</dd> <dt>

*btBackupType* \[ in\]
</dt> <dd>

Specifica il tipo di backup. Può corrispondere a uno dei valori seguenti.

<dt>

<span id="BACKUP_TYPE_FULL"></span><span id="backup_type_full"></span>

<span id="BACKUP_TYPE_FULL"></span><span id="backup_type_full"></span>**tipo di BACKUP \_ \_ completo**


</dt> <dd>

Specifica un backup completo. Viene eseguito il backup della directory completa (DIT, file di log e file di aggiornamento). Viene eseguito il backup di tutti i dati e i file di log delle transazioni vengono troncati. Sono supportati solo backup completi.

</dd> <dt>

<span id="BACKUP_TYPE_LOGS_ONLY"></span><span id="backup_type_logs_only"></span>

<span id="BACKUP_TYPE_LOGS_ONLY"></span><span id="backup_type_logs_only"></span>**\_ \_ solo log dei tipi di backup \_**


</dt> <dd>

Questo valore non è supportato. Specifica che verrà eseguito il backup solo dei log del database e non del database stesso. Questa operazione viene in genere utilizzata durante l'esecuzione di un backup differenziale o incrementale.

</dd> <dt>

<span id="BACKUP_TYPE_INCREMENTAL"></span><span id="backup_type_incremental"></span>

<span id="BACKUP_TYPE_INCREMENTAL"></span><span id="backup_type_incremental"></span>**tipo di BACKUP \_ \_ incrementale**


</dt> <dd>

Questo valore non è supportato. **DsBackupPrepare** restituisce **l' \_ errore \_ parametro non valido**.

</dd> </dl> </dd> <dt>

*ppvExpiryToken* \[ out\]
</dt> <dd>

Puntatore a un valore **PVOID** che riceve un puntatore a un token di scadenza associato a questo backup. *pcbExpiryTokenSize* riceve le dimensioni, in byte, di questi dati. Il chiamante deve salvare il contenuto di questo token con il backup perché il token deve essere passato a [**DsRestorePrepare**](dsrestoreprepare.md) durante il tentativo di ripristino dei dati. Dopo che il token è stato archiviato e non è più necessario, il chiamante deve liberare la memoria allocata usando [**DsBackupFree**](dsbackupfree.md).

</dd> <dt>

*pcbExpiryTokenSize* \[ out\]
</dt> <dd>

Puntatore a un valore **DWORD** che riceve le dimensioni, in byte, del token in *ppvExpiryToken*.

</dd> <dt>

*phbc* \[ out\]
</dt> <dd>

Puntatore a un valore **HBC** che riceve l'handle per il backup. Questo handle viene utilizzato per chiamare altre funzioni di backup del servizio directory, ad esempio [**DsBackupOpenFile**](dsbackupopenfile.md) e [**DsBackupEnd**](dsbackupend.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **\_ OK** se la funzione ha esito positivo o un codice di errore. Nell'elenco seguente sono elencati altri possibili codici di errore.

<dl> <dt>

**ERRORE di \_ accesso \_ negato**
</dt> <dd>

Il chiamante non dispone dei privilegi di accesso appropriati per chiamare questa funzione. La funzione [**DsSetAuthIdentity**](dssetauthidentity.md) può essere utilizzata per impostare le credenziali da utilizzare per le funzioni di backup e ripristino.

</dd> <dt>

**ERRORE \_ parametro non valido \_**
</dt> <dd>

*szBackupServer* o *phbcBackupContext* non sono validi.

</dd> <dt>

**ERRORE \_ di \_ memoria insufficiente \_**
</dt> <dd>

Si è verificato un errore di allocazione della memoria.

</dd> <dt>

**hrCouldNotConnect**
</dt> <dd>

Il server in *szBackupServer* non è stato trovato, non è un controller di dominio o *szBackupServer* non è formattato correttamente. Questo valore è definito in ntdsbmsg. h.

</dd> <dt>

**hrInvalidParam**
</dt> <dd>

*ppvExpiryToken* e/o *pcbExpiryTokenSize* non sono validi. Questo valore è definito in ntdsbmsg. h.

</dd> <dt>

**\_binding RPC S \_ non valido \_**
</dt> <dd>

La funzione viene chiamata in modalità remota o il server in *szServerName* non è un controller di dominio.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa funzione richiede che il chiamante disponga del **privilegio \_ \_ nome backup se** . La funzione [**DsSetAuthIdentity**](dssetauthidentity.md) può essere utilizzata per modificare il contesto di sicurezza in cui viene chiamata la funzione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Ntdsbcli. h</dt> </dl>   |
| Libreria<br/>                  | <dl> <dt>Ntdsbcli. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ntdsbcli.dll</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **DsBackupPrepareW** (Unicode) e **DsBackupPrepareA** (ANSI)<br/>               |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**DsRestorePrepare**](dsrestoreprepare.md)
</dt> <dt>

[**DsBackupFree**](dsbackupfree.md)
</dt> <dt>

[**DsBackupOpenFile**](dsbackupopenfile.md)
</dt> <dt>

[**DsBackupEnd**](dsbackupend.md)
</dt> <dt>

[**DsSetAuthIdentity**](dssetauthidentity.md)
</dt> <dt>

[Esecuzione del backup di un server di Active Directory](backing-up-an-active-directory-server.md)
</dt> <dt>

[Funzioni di backup della directory](directory-backup-functions.md)
</dt> </dl>

 

