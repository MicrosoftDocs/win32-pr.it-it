---
title: Funzione DsBackupTruncateLogs (Ntdsbcli.h)
description: Tronca i log di backup letti in precedenza.
ms.assetid: fae2e19f-08b8-410f-a735-dd4d41fc71a6
ms.tgt_platform: multiple
keywords:
- Funzione DsBackupTruncateLogs in Active Directory
topic_type:
- apiref
api_name:
- DsBackupTruncateLogs
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ef435214248d8b7972e62419ce60626f7dd6ec9f6dc27a8813598e623d7a156
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118191847"
---
# <a name="dsbackuptruncatelogs-function"></a>Funzione DsBackupTruncateLogs

\[Questa funzione è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. È possibile che in versioni successive sia stata modificata o non sia più disponibile. A partire Windows Vista, [usare Servizio Copia Shadow del volume (VSS).](../vss/volume-shadow-copy-service-overview.md)\]

La **funzione DsBackupTruncateLogs** tronca i log di backup letti in precedenza.

## <a name="syntax"></a>Sintassi


```C++
HRESULT DsBackupTruncateLogs(
  _In_ HBC hbc
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hbc* \[ Pollici\]
</dt> <dd>

Contiene l'handle del contesto di backup ottenuto [**con la funzione DsBackupPrepare.**](dsbackupprepare.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **S \_ OK se** la funzione ha esito positivo oppure un codice di errore Win32 o RPC in caso contrario. Nell'elenco seguente sono elencati altri possibili codici di errore.

<dl> <dt>

**ERRORE \_ DI \_ ACCESSO NEGATO**
</dt> <dd>

Il chiamante non dispone dei privilegi di accesso adeguati per chiamare questa funzione. La [**funzione DsSetAuthIdentity**](dssetauthidentity.md) può essere usata per impostare le credenziali da usare per le funzioni di backup e ripristino.

</dd> <dt>

**ERRORE \_ PARAMETRO NON \_ VALIDO**
</dt> <dd>

*hbc* non è valido.

</dd> </dl>

## <a name="remarks"></a>Commenti

Usare la **funzione DsBackupTruncateLogs** quando un backup completo o incrementale è stato completato correttamente.

> [!Caution]  
> Se questa funzione viene chiamata dopo un backup differenziale, tutte le informazioni di backup incrementale andranno perse.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Ntdsbcli.h</dt> </dl>   |
| Libreria<br/>                  | <dl> <dt>Ntdsbcli.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ntdsbcli.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**DsBackupPrepare**](dsbackupprepare.md)
</dt> <dt>

[**DsBackupGetBackupLogs**](dsbackupgetbackuplogs.md)
</dt> <dt>

[**DsSetCurrentBackupLog**](dssetcurrentbackuplog.md)
</dt> <dt>

[Backup di un server Active Directory](backing-up-an-active-directory-server.md)
</dt> <dt>

[Funzioni di backup della directory](directory-backup-functions.md)
</dt> </dl>

 

