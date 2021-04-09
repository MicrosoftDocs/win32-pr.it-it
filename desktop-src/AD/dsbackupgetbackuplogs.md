---
title: Funzione DsBackupGetBackupLogs (ntdsbcli. h)
description: Ottiene l'elenco dei file di log di cui è necessario eseguire il backup per il contesto di backup specificato.
ms.assetid: 09b3fdac-41ea-471c-a0dd-54414181f6fe
ms.tgt_platform: multiple
keywords:
- Active Directory funzione DsBackupGetBackupLogs
topic_type:
- apiref
api_name:
- DsBackupGetBackupLogs
- DsBackupGetBackupLogsA
- DsBackupGetBackupLogsW
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a02c5c7234810623a95dea030f0c623cca92293
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964340"
---
# <a name="dsbackupgetbackuplogs-function"></a>DsBackupGetBackupLogs (funzione)

\[Questa funzione è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. È possibile che in versioni successive sia stata modificata o non sia più disponibile. A partire da Windows Vista, usare invece [servizio Copia Shadow del volume (VSS)](../vss/volume-shadow-copy-service-overview.md) .\]

La funzione **DsBackupGetBackupLogs** Ottiene l'elenco dei file di log di cui è necessario eseguire il backup per il contesto di backup specificato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT DsBackupGetBackupLogs(
  _In_  HBC     hbc,
  _Out_ LPTSTR  *pszBackupLogFiles,
  _Out_ LPDWORD pcbSize
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*HBC* \[ in\]
</dt> <dd>

Contiene l'handle del contesto di backup ottenuto con la funzione [**DsBackupPrepare**](dsbackupprepare.md) .

</dd> <dt>

*pszBackupLogFiles* \[ out\]
</dt> <dd>

Puntatore a un puntatore di stringa che riceve l'elenco dei nomi dei file di log come percorsi UNC. Inizializzare questo valore su **null** prima di chiamare **DsBackupGetBackupLogs**.

Questo elenco riceve un doppio elenco con terminazione null di singole stringhe con terminazione null.

Questo buffer viene allocato dalla funzione **DsBackupGetBackupLogs** e deve essere liberato quando non è più necessario chiamando la funzione [**DsBackupFree**](dsbackupfree.md) .

Il primo carattere di ogni nome file contiene una delle [**costanti BFT**](bft-constants.md) che identificano il tipo di nome.

</dd> <dt>

*pcbSize* \[ out\]
</dt> <dd>

Puntatore al valore **DWORD** che riceve le dimensioni, in byte, del buffer *pszBackupLogFiles* .

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

*HBC*, *pszBackupLogFiles* o *pcbSize* non è valido.

</dd> <dt>

**ERRORE \_ di \_ memoria insufficiente \_**
</dt> <dd>

Si è verificato un errore di allocazione della memoria.

</dd> </dl>

## <a name="remarks"></a>Commenti

La funzione **DsBackupGetBackupLogs** fornisce un elenco dei file di log necessari per un backup. Un backup completo è costituito dai file di database forniti dalla funzione [**DsBackupGetDatabaseNames**](dsbackupgetdatabasenames.md) e dai file di log. I backup incrementali dei server Active Directory non sono supportati.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Ntdsbcli. h</dt> </dl>   |
| Libreria<br/>                  | <dl> <dt>Ntdsbcli. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ntdsbcli.dll</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **DsBackupGetBackupLogsW** (Unicode) e **DsBackupGetBackupLogsA** (ANSI)<br/>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**DsBackupFree**](dsbackupfree.md)
</dt> <dt>

[**DsBackupGetDatabaseNames**](dsbackupgetdatabasenames.md)
</dt> <dt>

[**Costanti BFT**](bft-constants.md)
</dt> <dt>

[Esecuzione del backup di un server di Active Directory](backing-up-an-active-directory-server.md)
</dt> <dt>

[Funzioni di backup della directory](directory-backup-functions.md)
</dt> </dl>

 

