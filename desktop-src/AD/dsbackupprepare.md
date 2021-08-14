---
title: Funzione DsBackupPrepare (Ntdsbcli.h)
description: Prepara la directory nel server specificato per il backup online e restituisce un handle del contesto di backup usato nelle chiamate successive ad altre funzioni di backup.
ms.assetid: 18c6dbcf-b707-4674-9af5-40f2178e6d2b
ms.tgt_platform: multiple
keywords:
- Funzione DsBackupPrepare active Directory
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
ms.openlocfilehash: ea1f24c6cbf3f05ce69d8a71900bfe4d1b08899b98590dc75410b9d5ed92d90a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118191837"
---
# <a name="dsbackupprepare-function"></a>Funzione DsBackupPrepare

\[Questa funzione è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. È possibile che in versioni successive sia stata modificata o non sia più disponibile. A partire da Windows Vista, [usare Servizio Copia Shadow del volume (VSS).](../vss/volume-shadow-copy-service-overview.md)\]

La **funzione DsBackupPrepare** prepara la directory nel server specificato per il backup online e restituisce un handle del contesto di backup usato nelle chiamate successive ad altre funzioni di backup.

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

*szBackupServer* \[ Pollici\]
</dt> <dd>

Puntatore a una stringa con terminazione Null contenente il nome del server di cui eseguire il backup. Le barre rovesciate precedenti sono facoltative. Il server deve essere lo stesso computer da cui viene chiamata questa funzione. Il nome del server non può contenere un carattere di sottolineatura ( \_ ). Un esempio di nome server è \\ \\ "server1".

</dd> <dt>

*grbit* \[ Pollici\]
</dt> <dd>

Determina se verrà eseguito il backup dei file di log. Questo valore deve sempre essere 0 perché i backup incrementali non sono supportati.

</dd> <dt>

*btBackupType* \[ Pollici\]
</dt> <dd>

Specifica il tipo di backup. Può essere uno dei valori seguenti.

<dt>

<span id="BACKUP_TYPE_FULL"></span><span id="backup_type_full"></span>

<span id="BACKUP_TYPE_FULL"></span><span id="backup_type_full"></span>**TIPO \_ DI BACKUP \_ COMPLETO**


</dt> <dd>

Specifica un backup completo. Viene eseguito il backup della directory completa (DIT, file di log e file di aggiornamento). Viene eseguito il backup di tutti i dati e i file di log delle transazioni vengono troncati. Sono supportati solo i backup completi.

</dd> <dt>

<span id="BACKUP_TYPE_LOGS_ONLY"></span><span id="backup_type_logs_only"></span>

<span id="BACKUP_TYPE_LOGS_ONLY"></span><span id="backup_type_logs_only"></span>**SOLO LOG \_ DEI \_ TIPI DI \_ BACKUP**


</dt> <dd>

Questo valore non è supportato. Specifica che verrà eseguito il backup solo dei log del database e non del database stesso. Viene in genere usato quando si esegue un backup differenziale o incrementale.

</dd> <dt>

<span id="BACKUP_TYPE_INCREMENTAL"></span><span id="backup_type_incremental"></span>

<span id="BACKUP_TYPE_INCREMENTAL"></span><span id="backup_type_incremental"></span>**TIPO \_ DI \_ BACKUP INCREMENTALE**


</dt> <dd>

Questo valore non è supportato. **DsBackupPrepare** restituisce **ERROR \_ INVALID \_ PARAMETER**.

</dd> </dl> </dd> <dt>

*ppvExpiryToken* \[ Cambio\]
</dt> <dd>

Puntatore a **un valore PVOID** che riceve un puntatore a un token di scadenza associato a questo backup. *pcbExpiryTokenSize* riceve le dimensioni, in byte, di questi dati. Il chiamante deve salvare il contenuto di questo token con il backup perché il token deve essere passato a [**DsRestorePrepare**](dsrestoreprepare.md) durante il tentativo di ripristino dei dati. Dopo che il token è stato archiviato e non è più necessario, il chiamante deve liberare la memoria allocata [**usando DsBackupFree**](dsbackupfree.md).

</dd> <dt>

*pcbExpiryTokenSize* \[ Cambio\]
</dt> <dd>

Puntatore a **un valore DWORD** che riceve le dimensioni, in byte, del token in *ppvExpiryToken*.

</dd> <dt>

*phbc* \[ Cambio\]
</dt> <dd>

Puntatore a **un valore HBC** che riceve l'handle per il backup. Questo handle viene usato quando si chiamano altre funzioni di backup del servizio directory, ad esempio [**DsBackupOpenFile**](dsbackupopenfile.md) e [**DsBackupEnd**](dsbackupend.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **S \_ OK se** la funzione ha esito positivo o un codice di errore in caso contrario. Nell'elenco seguente sono elencati altri possibili codici di errore.

<dl> <dt>

**ERRORE \_ DI ACCESSO \_ NEGATO**
</dt> <dd>

Il chiamante non dispone dei privilegi di accesso adeguati per chiamare questa funzione. La [**funzione DsSetAuthIdentity**](dssetauthidentity.md) può essere usata per impostare le credenziali da usare per le funzioni di backup e ripristino.

</dd> <dt>

**ERRORE \_ PARAMETRO NON \_ VALIDO**
</dt> <dd>

*szBackupServer* o *phbcBackupContext* non sono validi.

</dd> <dt>

**MEMORIA \_ INSUFFICIENTE \_ PER \_ L'ERRORE**
</dt> <dd>

Si è verificato un errore di allocazione della memoria.

</dd> <dt>

**hrCouldNotConnect**
</dt> <dd>

Impossibile trovare il server in *szBackupServer,* non è un controller di dominio o *szBackupServer* non è formattato correttamente. Questo valore è definito in ntdsbmsg.h.

</dd> <dt>

**hrInvalidParam**
</dt> <dd>

*ppvExpiryToken* e/o *pcbExpiryTokenSize* non sono validi. Questo valore è definito in Ntdsbmsg.h.

</dd> <dt>

**ASSOCIAZIONE \_ RPC S NON \_ \_ VALIDA**
</dt> <dd>

La funzione viene chiamata in modalità remota o il server in *szServerName* non è un controller di dominio.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa funzione richiede che il chiamante abbia il edizione Standard **\_ BACKUP \_ NAME.** La [**funzione DsSetAuthIdentity**](dssetauthidentity.md) può essere usata per modificare il contesto di sicurezza in cui viene chiamata questa funzione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Ntdsbcli.h</dt> </dl>   |
| Libreria<br/>                  | <dl> <dt>Ntdsbcli.lib</dt> </dl> |
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

[Backup di un server Active Directory](backing-up-an-active-directory-server.md)
</dt> <dt>

[Funzioni di backup della directory](directory-backup-functions.md)
</dt> </dl>

 

