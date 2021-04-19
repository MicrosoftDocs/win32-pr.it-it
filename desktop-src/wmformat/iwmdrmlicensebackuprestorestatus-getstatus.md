---
title: Metodo GetStatus di IWMDRMLicenseBackupRestoreStatus (wmdrmsdk. h)
description: Il metodo GetStatus recupera informazioni dettagliate sullo stato di un'operazione di backup o ripristino delle licenze.
ms.assetid: 1a695baf-0971-4dbf-90fa-1b10178a3348
keywords:
- Metodo GetStatus formato Windows Media
- Metodo GetStatus formato Windows Media, interfaccia IWMDRMLicenseBackupRestoreStatus
- Interfaccia IWMDRMLicenseBackupRestoreStatus-formato Windows Media, metodo GetStatus
topic_type:
- apiref
api_name:
- IWMDRMLicenseBackupRestoreStatus.GetStatus
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3373e71bcae9dc1054e97e8b758ac72389b9a712
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332375"
---
# <a name="iwmdrmlicensebackuprestorestatusgetstatus-method"></a>Metodo IWMDRMLicenseBackupRestoreStatus:: GetStatus

Il metodo **GetStatus** recupera informazioni dettagliate sullo stato di un'operazione di backup o ripristino delle licenze.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetStatus(
  [out] WM_BACKUP_RESTORE_STATUS *pStatus
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pStatus* \[ out\]
</dt> <dd>

Puntatore a una struttura di [**\_ stato di \_ ripristino \_ del backup WM**](wm-backup-restore-status.md) che riceve le informazioni sullo stato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un valore **HRESULT**. I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                          | Descrizione                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | Il metodo è riuscito.<br/> |



 

## <a name="remarks"></a>Commenti

Nessuna.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wmdrmsdk. h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>Wmdrmsdk. lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IWMDRMLicenseBackupRestoreStatus**](iwmdrmlicensebackuprestorestatus.md)
</dt> </dl>

 

 





