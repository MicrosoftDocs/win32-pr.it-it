---
title: Funzione DsBackupOpenFile (Ntdsbcli.h)
description: Apre il file specificato ed esegue le operazioni client e server necessarie per preparare il file per il backup.
ms.assetid: 1ffb81ee-9e7e-4d88-91fc-f1857377d125
ms.tgt_platform: multiple
keywords:
- Funzione DsBackupOpenFile in Active Directory
topic_type:
- apiref
api_name:
- DsBackupOpenFile
- DsBackupOpenFileA
- DsBackupOpenFileW
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6331dc79a93e515d49c688bc8c5dd3b9e747cfbac91ace9c7685a219ae21e95
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118430013"
---
# <a name="dsbackupopenfile-function"></a>Funzione DsBackupOpenFile

\[Questa funzione è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. È possibile che in versioni successive sia stata modificata o non sia più disponibile. A partire da Windows Vista, [usare Servizio Copia Shadow del volume (VSS).](../vss/volume-shadow-copy-service-overview.md)\]

La **funzione DsBackupOpenFile apre** il file specificato ed esegue le operazioni client e server necessarie per preparare il file per il backup.

## <a name="syntax"></a>Sintassi


```C++
HRESULT DsBackupOpenFile(
  _In_  HBC           hbc,
  _In_  LPCTSTR       szAttachmentName,
  _In_  DWORD         cbReadHintSize,
  _Out_ LARGE_INTEGER *pliFileSize
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hbc* \[ Pollici\]
</dt> <dd>

Contiene l'handle del contesto di backup ottenuto [**con la funzione DsBackupPrepare.**](dsbackupprepare.md)

</dd> <dt>

*szAttachmentName* \[ Pollici\]
</dt> <dd>

Puntatore a una stringa con terminazione Null che specifica il nome del file di backup da aprire.

</dd> <dt>

*cbReadHintSize* \[ Pollici\]
</dt> <dd>

Contiene le possibili dimensioni, in byte, del buffer passato come argomento *pvBuffer* nella [**funzione DsBackupRead.**](dsbackupread.md) Le funzioni di backup usano questo valore come hint per ottimizzare il traffico di rete. Questo valore deve essere un multiplo di 8192 e deve essere maggiore o uguale a 24576.

</dd> <dt>

*pliFileSize* \[ Cambio\]
</dt> <dd>

Puntatore a **un valore LARGE \_ INTEGER** che riceve le dimensioni, in byte, del file di backup aperto.

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

*hbc*, *szAttachmentName* o *pliFileSize* non sono validi.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Ntdsbcli.h</dt> </dl>   |
| Libreria<br/>                  | <dl> <dt>Ntdsbcli.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ntdsbcli.dll</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **DsBackupOpenFileW** (Unicode) e **DsBackupOpenFileA** (ANSI)<br/>             |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**DsBackupRead**](dsbackupread.md)
</dt> <dt>

[Backup di un server Active Directory](backing-up-an-active-directory-server.md)
</dt> <dt>

[Funzioni di backup della directory](directory-backup-functions.md)
</dt> </dl>

 

