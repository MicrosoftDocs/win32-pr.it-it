---
title: Funzione DsBackupRead (ntdsbcli. h)
description: Legge un blocco di dati dal file aperto corrente in un buffer.
ms.assetid: 01576d41-3cd6-4540-966b-7d98561f7b8c
ms.tgt_platform: multiple
keywords:
- Active Directory funzione DsBackupRead
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
ms.openlocfilehash: 409c2a7d93503aad4edff88070c0458efc961d23
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964125"
---
# <a name="dsbackupread-function"></a>DsBackupRead (funzione)

\[Questa funzione è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. È possibile che in versioni successive sia stata modificata o non sia più disponibile. A partire da Windows Vista, usare invece [servizio Copia Shadow del volume (VSS)](../vss/volume-shadow-copy-service-overview.md) .\]

La funzione **DsBackupRead** legge un blocco di dati dal file aperto corrente in un buffer. Si prevede che l'applicazione client chiami ripetutamente questa funzione fino a quando non viene ricevuto l'intero file di backup. La funzione [**DsBackupOpenFile**](dsbackupopenfile.md) fornisce l'intera dimensione del file di backup.

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

*HBC* \[ in\]
</dt> <dd>

Contiene l'handle del contesto di backup ottenuto con la funzione [**DsBackupPrepare**](dsbackupprepare.md) .

</dd> <dt>

*pvBuffer* \[ in\]
</dt> <dd>

Puntatore a un buffer che riceve i dati. Il buffer deve avere una dimensione di almeno *cbBuffer* byte.

</dd> <dt>

*cbBuffer* \[ in\]
</dt> <dd>

Contiene la dimensione, in byte, del buffer in corrispondenza di *pvBuffer*. Questo valore deve essere un multiplo di 8192 e deve essere maggiore o uguale a 24576.

</dd> <dt>

*pcbRead* \[ out\]
</dt> <dd>

Puntatore a un valore **DWORD** che riceve il numero effettivo di byte letti. Può essere minore del numero di byte richiesti perché alcuni trasporti frammentano il buffer trasmesso invece di riempire l'intero buffer con i dati.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **\_ OK** se la funzione ha esito positivo o un codice di errore Win32 o RPC in caso contrario. I codici di errore possibili includono i seguenti.

<dl> <dt>

**ERRORE \_ parametro non valido \_**
</dt> <dd>

Uno o più parametri non sono validi.

</dd> <dt>

**HANDLE di errore \_ \_ EOF**
</dt> <dd>

È stata raggiunta la fine del file di backup.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Ntdsbcli. h</dt> </dl>   |
| Libreria<br/>                  | <dl> <dt>Ntdsbcli. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ntdsbcli.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**DsBackupOpenFile**](dsbackupopenfile.md)
</dt> <dt>

[**DsBackupPrepare**](dsbackupprepare.md)
</dt> <dt>

[**DsBackupFree**](dsbackupfree.md)
</dt> <dt>

[Esecuzione del backup di un server di Active Directory](backing-up-an-active-directory-server.md)
</dt> <dt>

[Funzioni di backup della directory](directory-backup-functions.md)
</dt> </dl>

 

