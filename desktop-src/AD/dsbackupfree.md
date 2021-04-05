---
title: Funzione DsBackupFree (ntdsbcli. h)
description: Rilascia la memoria allocata dal Active Directory Domain Services funzioni di backup e ripristino.
ms.assetid: cde2a530-60e6-440c-9d4e-a90d55846973
ms.tgt_platform: multiple
keywords:
- Active Directory funzione DsBackupFree
topic_type:
- apiref
api_name:
- DsBackupFree
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27855eeb3417eede371357528457248857c3e626
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873677"
---
# <a name="dsbackupfree-function"></a>DsBackupFree (funzione)

\[Questa funzione è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. È possibile che in versioni successive sia stata modificata o non sia più disponibile. A partire da Windows Vista, usare invece [servizio Copia Shadow del volume (VSS)](../vss/volume-shadow-copy-service-overview.md) .\]

La funzione **DsBackupFree** rilascia la memoria allocata dal Active Directory Domain Services funzioni di backup e ripristino. Le funzioni seguenti allocano memoria che deve essere rilasciata con la funzione **DsBackupFree** .

-   [**DsBackupGetBackupLogs**](dsbackupgetbackuplogs.md)
-   [**DsBackupGetDatabaseNames**](dsbackupgetdatabasenames.md)
-   [**DsBackupPrepare**](dsbackupprepare.md)
-   [**DsRestoreGetDatabaseLocations**](dsrestoregetdatabaselocations.md)

## <a name="syntax"></a>Sintassi


```C++
VOID NTDSBCLI_API DsBackupFree(
  _In_ PVOID pvBuffer
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pvBuffer* \[ in\]
</dt> <dd>

Puntatore al buffer di memoria da liberare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

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

[**DsBackupGetBackupLogs**](dsbackupgetbackuplogs.md)
</dt> <dt>

[**DsBackupGetDatabaseNames**](dsbackupgetdatabasenames.md)
</dt> <dt>

[**DsBackupPrepare**](dsbackupprepare.md)
</dt> <dt>

[**DsRestoreGetDatabaseLocations**](dsrestoregetdatabaselocations.md)
</dt> <dt>

[Esecuzione del backup di un server di Active Directory](backing-up-an-active-directory-server.md)
</dt> <dt>

[Funzioni di backup della directory](directory-backup-functions.md)
</dt> </dl>

 

