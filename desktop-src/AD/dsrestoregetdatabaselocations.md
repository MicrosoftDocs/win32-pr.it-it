---
title: Funzione DsRestoreGetDatabaseLocations (Ntdsbcli.h)
description: Ottiene i percorsi in cui copiare i file di backup durante un'operazione di ripristino.
ms.assetid: f91d701c-72cf-418a-8d1c-6bf6ef41c2c1
ms.tgt_platform: multiple
keywords:
- Funzione DsRestoreGetDatabaseLocations in Active Directory
topic_type:
- apiref
api_name:
- DsRestoreGetDatabaseLocations
- DsRestoreGetDatabaseLocationsA
- DsRestoreGetDatabaseLocationsW
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3c5626e2e0dc679a4669bb5d8be8096b6ae0629aeed7c833f397b5f9bca45db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118429993"
---
# <a name="dsrestoregetdatabaselocations-function"></a>Funzione DsRestoreGetDatabaseLocations

\[Questa funzione è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. È possibile che in versioni successive sia stata modificata o non sia più disponibile. A partire Windows Vista, [usare Servizio Copia Shadow del volume (VSS).](../vss/volume-shadow-copy-service-overview.md)\]

La **funzione DsRestoreGetDatabaseLocations** ottiene i percorsi in cui copiare i file di backup durante un'operazione di ripristino.

## <a name="syntax"></a>Sintassi


```C++
HRESULT DsRestoreGetDatabaseLocations(
  _In_  HBC     hbc,
  _Out_ LPWSTR  *pszDatabaseLocationList,
  _Out_ LPDWORD pcbSize
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hbc* \[ Pollici\]
</dt> <dd>

Contiene l'handle del contesto di ripristino ottenuto [**con la funzione DsRestorePrepare.**](dsrestoreprepare.md)

</dd> <dt>

*pszDatabaseLocationList* \[ Cambio\]
</dt> <dd>

Puntatore a un puntatore di stringa che riceve l'elenco di percorsi di database come percorsi UNC. Questo elenco riceve un elenco doppio con terminazione Null di singole stringhe con terminazione Null.

Questo buffer viene allocato dalla funzione **DsRestoreGetDatabaseLocations** e deve essere liberato quando non è più necessario chiamando la [**funzione DsBackupFree.**](dsbackupfree.md)

Il primo carattere di ogni nome file contiene una delle [**costanti BFT**](bft-constants.md) che identifica il tipo di nome. La **funzione DsRestoreGetDatabaseLocations** fornisce solo i tipi di nome seguenti.

<dt>

<span id="BFT_NTDS_DATABASE"></span><span id="bft_ntds_database"></span>

<span id="BFT_NTDS_DATABASE"></span><span id="bft_ntds_database"></span>**BFT \_ NTDS \_ DATABASE**


</dt> <dd>

Il file di database NTDS deve essere copiato in questo file. Si tratta del file identificato come **BFT \_ NTDS \_ DATABASE** al momento dell'esecuzione del backup.

</dd> <dt>

<span id="BFT_LOG_DIR"></span><span id="bft_log_dir"></span>

<span id="BFT_LOG_DIR"></span><span id="bft_log_dir"></span>**BFT \_ LOG \_ DIR**


</dt> <dd>

Tutti i file di log vengono copiati in questa directory. I file di log sono stati identificati **come BFT \_ LOG** al momento dell'esecuzione del backup.

</dd> <dt>

<span id="BFT_CHECKPOINT_DIR"></span><span id="bft_checkpoint_dir"></span>

<span id="BFT_CHECKPOINT_DIR"></span><span id="bft_checkpoint_dir"></span>**BFT \_ CHECKPOINT \_ DIR**


</dt> <dd>

Tutti i file di patch vengono copiati in questa directory. I file di patch sono stati identificati **come \_ \_ FILE PATCH BFT** al momento dell'esecuzione del backup.

</dd> </dl> </dd> <dt>

*pcbSize* \[ Cambio\]
</dt> <dd>

Puntatore **al valore DWORD** che riceve le dimensioni, in byte, del buffer *pszDatabaseLocationList.*

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **S \_ OK se** la funzione ha esito positivo oppure un codice di errore Win32 o RPC in caso contrario. Nell'elenco seguente sono elencati i codici di errore possibili.

<dl> <dt>

**ERRORE \_ DI \_ ACCESSO NEGATO**
</dt> <dd>

Il chiamante non dispone dei privilegi di accesso adeguati per chiamare questa funzione. La [**funzione DsSetAuthIdentity**](dssetauthidentity.md) può essere usata per impostare le credenziali da usare per le funzioni di backup e ripristino.

</dd> <dt>

**ERRORE \_ PARAMETRO NON \_ VALIDO**
</dt> <dd>

*hbc*, *pszDatabaseLocationList* o *pcbSize* non sono validi.

</dd> <dt>

**ERRORE \_ MEMORIA \_ \_ INSUFFICIENTE**
</dt> <dd>

Si è verificato un errore di allocazione della memoria.

</dd> </dl>

## <a name="remarks"></a>Commenti

La **funzione DsRestoreGetDatabaseLocations** può essere usata per ottenere le directory di ripristino senza accedere ai dati sottoposti a backup. A tale scopo, chiamare [**DsRestorePrepare**](dsrestoreprepare.md) con **NULL** per il *parametro pvExpiryToken.* In questo **modo DsRestorePrepare** restituisce un handle di contesto con restrizioni che può essere usato solo con **la funzione DsRestoreGetDatabaseLocations.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                              |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                                        |
| Intestazione<br/>                   | <dl> <dt>Ntdsbcli.h</dt> </dl>                 |
| Libreria<br/>                  | <dl> <dt>Ntdsbcli.lib</dt> </dl>               |
| DLL<br/>                      | <dl> <dt>Ntdsbcli.dll</dt> </dl>               |
| Nomi Unicode e ANSI<br/>   | **DsRestoreGetDatabaseLocationsW** (Unicode) e **DsRestoreGetDatabaseLocationsA** (ANSI)<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**DsRestorePrepare**](dsrestoreprepare.md)
</dt> <dt>

[**DsBackupFree**](dsbackupfree.md)
</dt> <dt>

[Funzioni di backup della directory](directory-backup-functions.md)
</dt> <dt>

[Ripristino di Active Directory](restoring-an-active-directory-server.md)
</dt> </dl>

 

