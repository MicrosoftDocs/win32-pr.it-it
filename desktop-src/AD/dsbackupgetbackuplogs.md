---
title: Funzione DsBackupGetBackupLogs (Ntdsbcli.h)
description: Ottiene l'elenco dei file di log di cui è necessario eseguire il backup per il contesto di backup specificato.
ms.assetid: 09b3fdac-41ea-471c-a0dd-54414181f6fe
ms.tgt_platform: multiple
keywords:
- Funzione DsBackupGetBackupLogs active Directory
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
ms.openlocfilehash: 6d4a240ef514fc62450a04f512f04d985380b79fa20daaee9ff4b27ccb71027a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118430104"
---
# <a name="dsbackupgetbackuplogs-function"></a>Funzione DsBackupGetBackupLogs

\[Questa funzione è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. È possibile che in versioni successive sia stata modificata o non sia più disponibile. A partire da Windows Vista, [usare Servizio Copia Shadow del volume (VSS).](../vss/volume-shadow-copy-service-overview.md)\]

La **funzione DsBackupGetBackupLogs** ottiene l'elenco dei file di log di cui è necessario eseguire il backup per il contesto di backup specificato.

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

*hbc* \[ Pollici\]
</dt> <dd>

Contiene l'handle del contesto di backup ottenuto con [**la funzione DsBackupPrepare.**](dsbackupprepare.md)

</dd> <dt>

*pszBackupLogFiles* \[ Cambio\]
</dt> <dd>

Puntatore a un puntatore di stringa che riceve l'elenco di nomi di file di log come percorsi UNC. Inizializzare questo valore **su NULL** prima di **chiamare DsBackupGetBackupLogs**.

Questo elenco riceve un elenco con terminazione Null doppia di singole stringhe con terminazione Null.

Questo buffer viene allocato dalla funzione **DsBackupGetBackupLogs** e deve essere liberato quando non è più necessario chiamando la funzione [**DsBackupFree.**](dsbackupfree.md)

Il primo carattere di ognuno dei nomi di file contiene una delle [**costanti BFT**](bft-constants.md) che identifica il tipo di nome.

</dd> <dt>

*pcbSize* \[ Cambio\]
</dt> <dd>

Puntatore **al valore DWORD** che riceve le dimensioni, in byte, del buffer *pszBackupLogFiles.*

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **S \_ OK se** la funzione ha esito positivo o un codice di errore Win32 o RPC in caso contrario. Nell'elenco seguente sono elencati altri possibili codici di errore.

<dl> <dt>

**ERRORE \_ DI ACCESSO \_ NEGATO**
</dt> <dd>

Il chiamante non dispone dei privilegi di accesso adeguati per chiamare questa funzione. La [**funzione DsSetAuthIdentity**](dssetauthidentity.md) può essere usata per impostare le credenziali da usare per le funzioni di backup e ripristino.

</dd> <dt>

**ERRORE \_ PARAMETRO NON \_ VALIDO**
</dt> <dd>

*hbc,* *pszBackupLogFiles* o *pcbSize* non è valido.

</dd> <dt>

**MEMORIA \_ INSUFFICIENTE \_ PER \_ L'ERRORE**
</dt> <dd>

Si è verificato un errore di allocazione della memoria.

</dd> </dl>

## <a name="remarks"></a>Commenti

La **funzione DsBackupGetBackupLogs** fornisce un elenco dei file di log necessari per un backup. Un backup completo è costituito dai file di database forniti dalla [**funzione DsBackupGetDatabaseNames**](dsbackupgetdatabasenames.md) e dai file di log. I backup incrementali dei server Active Directory non sono supportati.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Ntdsbcli.h</dt> </dl>   |
| Libreria<br/>                  | <dl> <dt>Ntdsbcli.lib</dt> </dl> |
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

[Backup di un server Active Directory](backing-up-an-active-directory-server.md)
</dt> <dt>

[Funzioni di backup della directory](directory-backup-functions.md)
</dt> </dl>

 

