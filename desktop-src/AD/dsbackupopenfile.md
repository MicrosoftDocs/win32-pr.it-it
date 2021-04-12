---
title: Funzione DsBackupOpenFile (ntdsbcli. h)
description: Apre il file specificato ed esegue le operazioni client e server necessarie per preparare il file per il backup.
ms.assetid: 1ffb81ee-9e7e-4d88-91fc-f1857377d125
ms.tgt_platform: multiple
keywords:
- Active Directory funzione DsBackupOpenFile
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
ms.openlocfilehash: e2f9c4eac9c9825f510848583d7f707a2c244c52
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120022"
---
# <a name="dsbackupopenfile-function"></a>DsBackupOpenFile (funzione)

\[Questa funzione è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. È possibile che in versioni successive sia stata modificata o non sia più disponibile. A partire da Windows Vista, usare invece [servizio Copia Shadow del volume (VSS)](../vss/volume-shadow-copy-service-overview.md) .\]

La funzione **DsBackupOpenFile** apre il file specificato ed esegue le operazioni client e server necessarie per preparare il file per il backup.

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

*HBC* \[ in\]
</dt> <dd>

Contiene l'handle del contesto di backup ottenuto con la funzione [**DsBackupPrepare**](dsbackupprepare.md) .

</dd> <dt>

*szAttachmentName* \[ in\]
</dt> <dd>

Puntatore a una stringa con terminazione null che specifica il nome del file di backup da aprire.

</dd> <dt>

*cbReadHintSize* \[ in\]
</dt> <dd>

Contiene le dimensioni possibili, in byte, del buffer passato come argomento *pvBuffer* nella funzione [**DsBackupRead**](dsbackupread.md) . Le funzioni di backup utilizzano questo valore come hint per ottimizzare il traffico di rete. Questo valore deve essere un multiplo di 8192 e deve essere maggiore o uguale a 24576.

</dd> <dt>

*pliFileSize* \[ out\]
</dt> <dd>

Puntatore a un **valore \_ Integer grande** che riceve le dimensioni, in byte, del file di backup aperto.

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

*HBC*, *szAttachmentName* o *pliFileSize* non sono validi.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Ntdsbcli. h</dt> </dl>   |
| Libreria<br/>                  | <dl> <dt>Ntdsbcli. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ntdsbcli.dll</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **DsBackupOpenFileW** (Unicode) e **DsBackupOpenFileA** (ANSI)<br/>             |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**DsBackupRead**](dsbackupread.md)
</dt> <dt>

[Esecuzione del backup di un server di Active Directory](backing-up-an-active-directory-server.md)
</dt> <dt>

[Funzioni di backup della directory](directory-backup-functions.md)
</dt> </dl>

 

