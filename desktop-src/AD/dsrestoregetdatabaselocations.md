---
title: Funzione DsRestoreGetDatabaseLocations (ntdsbcli. h)
description: Ottiene i percorsi in cui devono essere copiati i file di backup durante un'operazione di ripristino.
ms.assetid: f91d701c-72cf-418a-8d1c-6bf6ef41c2c1
ms.tgt_platform: multiple
keywords:
- Active Directory funzione DsRestoreGetDatabaseLocations
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
ms.openlocfilehash: 7bcebb9f3822332269e1db09f3246c128e4ad1f2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874133"
---
# <a name="dsrestoregetdatabaselocations-function"></a>DsRestoreGetDatabaseLocations (funzione)

\[Questa funzione è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. È possibile che in versioni successive sia stata modificata o non sia più disponibile. A partire da Windows Vista, usare invece [servizio Copia Shadow del volume (VSS)](../vss/volume-shadow-copy-service-overview.md) .\]

La funzione **DsRestoreGetDatabaseLocations** ottiene i percorsi in cui devono essere copiati i file di backup durante un'operazione di ripristino.

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

*HBC* \[ in\]
</dt> <dd>

Contiene l'handle del contesto di ripristino ottenuto con la funzione [**DsRestorePrepare**](dsrestoreprepare.md) .

</dd> <dt>

*pszDatabaseLocationList* \[ out\]
</dt> <dd>

Puntatore a un puntatore di stringa che riceve l'elenco dei percorsi di database come percorsi UNC. Questo elenco riceve un doppio elenco con terminazione null di singole stringhe con terminazione null.

Questo buffer viene allocato dalla funzione **DsRestoreGetDatabaseLocations** e deve essere liberato quando non è più necessario chiamando la funzione [**DsBackupFree**](dsbackupfree.md) .

Il primo carattere di ogni nome file contiene una delle [**costanti BFT**](bft-constants.md) che identificano il tipo di nome. La funzione **DsRestoreGetDatabaseLocations** fornisce solo i tipi di nomi seguenti.

<dt>

<span id="BFT_NTDS_DATABASE"></span><span id="bft_ntds_database"></span>

<span id="BFT_NTDS_DATABASE"></span><span id="bft_ntds_database"></span>**\_database NTDS \_ BFT**


</dt> <dd>

Il file di database NTDS deve essere copiato in questo file. Si tratta del file che è stato identificato come **BFT \_ NTDS \_ database** durante l'esecuzione del backup.

</dd> <dt>

<span id="BFT_LOG_DIR"></span><span id="bft_log_dir"></span>

<span id="BFT_LOG_DIR"></span><span id="bft_log_dir"></span>**\_dir BFT log \_**


</dt> <dd>

Tutti i file di log vengono copiati in questa directory. I file di log sono stati identificati come **\_ log BFT** quando è stato eseguito il backup.

</dd> <dt>

<span id="BFT_CHECKPOINT_DIR"></span><span id="bft_checkpoint_dir"></span>

<span id="BFT_CHECKPOINT_DIR"></span><span id="bft_checkpoint_dir"></span>**\_dir del checkpoint BFT \_**


</dt> <dd>

Tutti i file di patch vengono copiati in questa directory. I file della patch sono stati identificati come **\_ \_ file di patch BFT** quando è stato eseguito il backup.

</dd> </dl> </dd> <dt>

*pcbSize* \[ out\]
</dt> <dd>

Puntatore al valore **DWORD** che riceve le dimensioni, in byte, del buffer *pszDatabaseLocationList* .

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

*HBC*, *pszDatabaseLocationList* o *pcbSize* non sono validi.

</dd> <dt>

**ERRORE \_ di \_ memoria insufficiente \_**
</dt> <dd>

Si è verificato un errore di allocazione della memoria.

</dd> </dl>

## <a name="remarks"></a>Commenti

La funzione **DsRestoreGetDatabaseLocations** può essere usata per ottenere le directory di ripristino senza accedere ai dati di cui è stato eseguito il backup. A tale scopo, chiamare [**DsRestorePrepare**](dsrestoreprepare.md) con **null** per il parametro *pvExpiryToken* . In questo modo **DsRestorePrepare** restituisce un handle di contesto limitato che può essere utilizzato solo con la funzione **DsRestoreGetDatabaseLocations** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                              |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                                        |
| Intestazione<br/>                   | <dl> <dt>Ntdsbcli. h</dt> </dl>                 |
| Libreria<br/>                  | <dl> <dt>Ntdsbcli. lib</dt> </dl>               |
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

 

