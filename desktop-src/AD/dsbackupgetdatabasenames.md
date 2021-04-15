---
title: Funzione DsBackupGetDatabaseNames (ntdsbcli. h)
description: Ottiene l'elenco dei file di database di cui eseguire il backup per il contesto di backup specificato.
ms.assetid: ba0447a1-38b0-4c0a-8c63-abaefb5b908f
ms.tgt_platform: multiple
keywords:
- Active Directory funzione DsBackupGetDatabaseNames
topic_type:
- apiref
api_name:
- DsBackupGetDatabaseNames
- DsBackupGetDatabaseNamesA
- DsBackupGetDatabaseNamesW
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6643b17a85727f6e0df4e8deea9609f73afd1e76
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477135"
---
# <a name="dsbackupgetdatabasenames-function"></a>DsBackupGetDatabaseNames (funzione)

\[Questa funzione è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. È possibile che in versioni successive sia stata modificata o non sia più disponibile. A partire da Windows Vista, usare invece [servizio Copia Shadow del volume (VSS)](../vss/volume-shadow-copy-service-overview.md) .\]

La funzione **DsBackupGetDatabaseNames** Ottiene l'elenco dei file di database di cui eseguire il backup per il contesto di backup specificato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT DsBackupGetDatabaseNames(
  _In_  HBC     hbc,
  _Out_ LPTSTR  *pszAttachmentInfo,
  _Out_ LPDWORD pcbSize
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*HBC* \[ in\]
</dt> <dd>

Contiene l'handle del contesto di backup ottenuto con la funzione [**DsBackupPrepare**](dsbackupprepare.md) .

</dd> <dt>

*pszAttachmentInfo* \[ out\]
</dt> <dd>

Puntatore a un puntatore di stringa che riceve l'elenco dei nomi di file di database come percorsi UNC. Questo valore deve essere inizializzato su **null** prima di chiamare **DsBackupGetDatabaseNames**.

Questo elenco riceve un doppio elenco con terminazione null di singole stringhe con terminazione null.

Questo buffer viene allocato dalla funzione **DsBackupGetDatabaseNames** e deve essere liberato quando non è più necessario chiamando la funzione [**DsBackupFree**](dsbackupfree.md) .

Il primo carattere di ogni nome di file contiene una delle [**costanti BFT**](bft-constants.md) che identificano il tipo di nome. La funzione [**DsRestoreGetDatabaseLocations**](dsrestoregetdatabaselocations.md) fornisce solo i tipi di nomi seguenti.

<dt>

<span id="BFT_NTDS_DATABASE"></span><span id="bft_ntds_database"></span>

<span id="BFT_NTDS_DATABASE"></span><span id="bft_ntds_database"></span>**\_database NTDS \_ BFT**


</dt> <dd>

Il file è un file di database NTDS. Questo file deve essere copiato nel file identificato come **BFT \_ NTDS \_ database** quando vengono ripristinati i dati.

</dd> <dt>

<span id="BFT_LOG"></span><span id="bft_log"></span>

<span id="BFT_LOG"></span><span id="bft_log"></span>**\_log BFT**


</dt> <dd>

Il file è un file di log. Tutti i file di log vengono copiati nella directory identificata come directory di **\_ log \_ BFT** quando vengono ripristinati i dati.

</dd> <dt>

<span id="BFT_PATCH_FILE"></span><span id="bft_patch_file"></span>

<span id="BFT_PATCH_FILE"></span><span id="bft_patch_file"></span>**\_file patch \_ BFT**


</dt> <dd>

Il file è un file di patch. Tutti i file di patch vengono copiati nella directory identificata come **BFT \_ Checkpoint \_** quando i dati vengono ripristinati.

</dd> </dl> </dd> <dt>

*pcbSize* \[ out\]
</dt> <dd>

Puntatore al valore **DWORD** che riceve le dimensioni, in byte, del buffer *pszAttachmentInfo* .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **\_ OK** se la funzione ha esito positivo o un codice di errore Win32 o RPC in caso contrario. Nell'elenco seguente sono elencati altri possibili codici di errore.

<dl> <dt>

**ERRORE di \_ accesso \_ negato**
</dt> <dd>

Il chiamante non dispone dei privilegi di accesso appropriati per chiamare questa funzione. La funzione [**DsSetAuthIdentity**](dssetauthidentity.md) può essere utilizzata per impostare le credenziali da utilizzare per le funzioni di backup e ripristino.

</dd> <dt>

**ERRORE \_ parametro non valido \_**
</dt> <dd>

*HBC*, *pszAttachmentInfo* o *pcbSize* non sono validi.

</dd> <dt>

**ERRORE \_ di \_ memoria insufficiente \_**
</dt> <dd>

Si è verificato un errore di allocazione della memoria.

</dd> </dl>

## <a name="remarks"></a>Commenti

La funzione **DsBackupGetDatabaseNames** fornisce un elenco dei file di database necessari per un backup. Un backup completo è costituito dai file di database e dai file di log forniti dalla funzione [**DsBackupGetBackupLogs**](dsbackupgetbackuplogs.md) . I backup incrementali dei server Active Directory non sono supportati.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                    |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                              |
| Intestazione<br/>                   | <dl> <dt>Ntdsbcli. h</dt> </dl>       |
| Libreria<br/>                  | <dl> <dt>Ntdsbcli. lib</dt> </dl>     |
| DLL<br/>                      | <dl> <dt>Ntdsbcli.dll</dt> </dl>     |
| Nomi Unicode e ANSI<br/>   | **DsBackupGetDatabaseNamesW** (Unicode) e **DsBackupGetDatabaseNamesA** (ANSI)<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**DsBackupPrepare**](dsbackupprepare.md)
</dt> <dt>

[**DsBackupFree**](dsbackupfree.md)
</dt> <dt>

[**DsBackupGetBackupLogs**](dsbackupgetbackuplogs.md)
</dt> <dt>

[**Costanti BFT**](bft-constants.md)
</dt> <dt>

[Esecuzione del backup di un server di Active Directory](backing-up-an-active-directory-server.md)
</dt> <dt>

[Funzioni di backup della directory](directory-backup-functions.md)
</dt> </dl>

 

