---
title: Funzione DsBackupRead (Ntdsbcli.h)
description: Legge un blocco di dati dal file aperto corrente in un buffer.
ms.assetid: 01576d41-3cd6-4540-966b-7d98561f7b8c
ms.tgt_platform: multiple
keywords:
- Funzione DsBackupRead in Active Directory
topic_type:
- apiref
api_name:
- DsBackupRead
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16b5ea4da5b004bb4584eb119419b8c89658f36fed7e8c47514bae47d44e31b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118430003"
---
# <a name="dsbackupread-function"></a>Funzione DsBackupRead

\[Questa funzione è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. È possibile che in versioni successive sia stata modificata o non sia più disponibile. A partire Windows Vista, [usare Servizio Copia Shadow del volume (VSS).](../vss/volume-shadow-copy-service-overview.md)\]

La **funzione DsBackupRead** legge un blocco di dati dal file aperto corrente in un buffer. È previsto che l'applicazione client chiami questa funzione ripetutamente fino a quando non viene ricevuto l'intero file di backup. La [**funzione DsBackupOpenFile**](dsbackupopenfile.md) fornisce l'intera dimensione del file di backup.

## <a name="syntax"></a>Sintassi


```C++
HRESULT DsBackupRead(
  _In_  HBC    hbc,
  _In_  PVOID  pvBuffer,
  _In_  DWORD  cbBuffer,
  _Out_ PDWORD pcbRead
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hbc* \[ Pollici\]
</dt> <dd>

Contiene l'handle del contesto di backup ottenuto [**con la funzione DsBackupPrepare.**](dsbackupprepare.md)

</dd> <dt>

*pvBuffer* \[ Pollici\]
</dt> <dd>

Puntatore a un buffer che riceve i dati. Le dimensioni di questo buffer devono *essere almeno cbBuffer* byte.

</dd> <dt>

*cbBuffer* \[ Pollici\]
</dt> <dd>

Contiene le dimensioni, in byte, del buffer in *pvBuffer.* Questo valore deve essere un multiplo di 8192 e deve essere maggiore o uguale a 24576.

</dd> <dt>

*pcbRead* \[ Cambio\]
</dt> <dd>

Puntatore a **un valore DWORD** che riceve il numero effettivo di byte letti. Può essere inferiore al numero di byte richiesti perché alcuni trasporti frammentano il buffer trasmesso anziché riempire l'intero buffer con dati.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **S \_ OK se** la funzione ha esito positivo oppure un codice di errore Win32 o RPC in caso contrario. I codici di errore possibili includono i seguenti.

<dl> <dt>

**ERRORE \_ PARAMETRO NON \_ VALIDO**
</dt> <dd>

Uno o più parametri non sono validi.

</dd> <dt>

**EOF \_ DELL'HANDLE \_ DI ERRORE**
</dt> <dd>

È stata raggiunta la fine del file di backup.

</dd> </dl>

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

[**DsBackupOpenFile**](dsbackupopenfile.md)
</dt> <dt>

[**DsBackupPrepare**](dsbackupprepare.md)
</dt> <dt>

[**DsBackupFree**](dsbackupfree.md)
</dt> <dt>

[Backup di un server Active Directory](backing-up-an-active-directory-server.md)
</dt> <dt>

[Funzioni di backup della directory](directory-backup-functions.md)
</dt> </dl>

 

