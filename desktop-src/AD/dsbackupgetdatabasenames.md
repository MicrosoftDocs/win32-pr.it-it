---
title: Funzione DsBackupGetDatabaseNames (Ntdsbcli.h)
description: Ottiene l'elenco dei file di database di cui eseguire il backup per il contesto di backup specificato.
ms.assetid: ba0447a1-38b0-4c0a-8c63-abaefb5b908f
ms.tgt_platform: multiple
keywords:
- Funzione DsBackupGetDatabaseNames active Directory
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
ms.openlocfilehash: 620ad77f84aa2cb52a7bd99a96a22e7de560b53b2c3ba2022598609dde3737fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118191857"
---
# <a name="dsbackupgetdatabasenames-function"></a>Funzione DsBackupGetDatabaseNames

\[Questa funzione è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. È possibile che in versioni successive sia stata modificata o non sia più disponibile. A partire da Windows Vista, [usare Servizio Copia Shadow del volume (VSS).](../vss/volume-shadow-copy-service-overview.md)\]

La **funzione DsBackupGetDatabaseNames** ottiene l'elenco dei file di database di cui eseguire il backup per il contesto di backup specificato.

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

*hbc* \[ Pollici\]
</dt> <dd>

Contiene l'handle del contesto di backup ottenuto con [**la funzione DsBackupPrepare.**](dsbackupprepare.md)

</dd> <dt>

*pszAttachmentInfo* \[ Cambio\]
</dt> <dd>

Puntatore a un puntatore di stringa che riceve l'elenco di nomi di file di database come percorsi UNC. Questo valore deve essere inizializzato su **NULL prima** di chiamare **DsBackupGetDatabaseNames**.

Questo elenco riceve un elenco con terminazione Null doppia di singole stringhe con terminazione Null.

Questo buffer viene allocato dalla funzione **DsBackupGetDatabaseNames** e deve essere liberato quando non è più necessario chiamando la [**funzione DsBackupFree.**](dsbackupfree.md)

Il primo carattere di ogni nome file contiene una delle [**costanti BFT**](bft-constants.md) che identifica il tipo di nome. La [**funzione DsRestoreGetDatabaseLocations**](dsrestoregetdatabaselocations.md) fornisce solo i tipi di nomi seguenti.

<dt>

<span id="BFT_NTDS_DATABASE"></span><span id="bft_ntds_database"></span>

<span id="BFT_NTDS_DATABASE"></span><span id="bft_ntds_database"></span>**BFT \_ NTDS \_ DATABASE**


</dt> <dd>

Il file è un file di database NTDS. Questo file deve essere copiato nel file identificato come **BFT \_ NTDS \_ DATABASE** quando i dati vengono ripristinati.

</dd> <dt>

<span id="BFT_LOG"></span><span id="bft_log"></span>

<span id="BFT_LOG"></span><span id="bft_log"></span>**BFT \_ LOG**


</dt> <dd>

Il file è un file di log. Tutti i file di log vengono copiati nella directory identificata come **BFT \_ LOG \_ DIR** quando i dati vengono ripristinati.

</dd> <dt>

<span id="BFT_PATCH_FILE"></span><span id="bft_patch_file"></span>

<span id="BFT_PATCH_FILE"></span><span id="bft_patch_file"></span>**BFT \_ PATCH \_ FILE**


</dt> <dd>

Il file è un file di patch. Tutti i file di patch vengono copiati nella directory identificata come **BFT \_ CHECKPOINT \_ DIR** quando i dati vengono ripristinati.

</dd> </dl> </dd> <dt>

*pcbSize* \[ Cambio\]
</dt> <dd>

Puntatore **al valore DWORD** che riceve le dimensioni, in byte, del buffer *pszAttachmentInfo.*

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

*hbc,* *pszAttachmentInfo* o *pcbSize* non sono validi.

</dd> <dt>

**MEMORIA \_ INSUFFICIENTE \_ PER \_ L'ERRORE**
</dt> <dd>

Si è verificato un errore di allocazione della memoria.

</dd> </dl>

## <a name="remarks"></a>Commenti

La **funzione DsBackupGetDatabaseNames** fornisce un elenco dei file di database necessari per un backup. Un backup completo è costituito dai file di database e dai file di log forniti dalla [**funzione DsBackupGetBackupLogs.**](dsbackupgetbackuplogs.md) I backup incrementali dei server Active Directory non sono supportati.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                    |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                              |
| Intestazione<br/>                   | <dl> <dt>Ntdsbcli.h</dt> </dl>       |
| Libreria<br/>                  | <dl> <dt>Ntdsbcli.lib</dt> </dl>     |
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

[Backup di un server Active Directory](backing-up-an-active-directory-server.md)
</dt> <dt>

[Funzioni di backup della directory](directory-backup-functions.md)
</dt> </dl>

 

