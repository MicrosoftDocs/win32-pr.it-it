---
title: Funzione DsBackupFree (Ntdsbcli.h)
description: Rilascia la memoria allocata dalle Active Directory Domain Services di backup e ripristino.
ms.assetid: cde2a530-60e6-440c-9d4e-a90d55846973
ms.tgt_platform: multiple
keywords:
- Funzione DsBackupFree in Active Directory
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
ms.openlocfilehash: 682bc8d8c4938544c85d22658b1ea175223a6e89d07416aa1fa3717285c67892
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118191894"
---
# <a name="dsbackupfree-function"></a>Funzione DsBackupFree

\[Questa funzione è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. È possibile che in versioni successive sia stata modificata o non sia più disponibile. A partire Windows Vista, [usare Servizio Copia Shadow del volume (VSS).](../vss/volume-shadow-copy-service-overview.md)\]

La **funzione DsBackupFree rilascia** la memoria allocata dalle Active Directory Domain Services di backup e ripristino. Le funzioni seguenti allocano memoria che deve essere rilasciata con **la funzione DsBackupFree.**

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

*pvBuffer* \[ Pollici\]
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
| Intestazione<br/>                   | <dl> <dt>Ntdsbcli.h</dt> </dl>   |
| Libreria<br/>                  | <dl> <dt>Ntdsbcli.lib</dt> </dl> |
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

[Backup di un server Active Directory](backing-up-an-active-directory-server.md)
</dt> <dt>

[Funzioni di backup della directory](directory-backup-functions.md)
</dt> </dl>

 

