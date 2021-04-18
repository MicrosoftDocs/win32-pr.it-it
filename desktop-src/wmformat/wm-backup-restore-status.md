---
title: Struttura WM_BACKUP_RESTORE_STATUS (wmdrmsdk. h)
description: La \_ \_ struttura dello stato di ripristino del backup WM \_ include informazioni su un'operazione di backup o ripristino delle licenze in sospeso.
ms.assetid: 74e94bc6-376b-4848-a9f9-11c9cb4005f2
keywords:
- Formato di Windows Media per la struttura WM_BACKUP_RESTORE_STATUS
- struttura Windows Media Format
topic_type:
- apiref
api_name:
- WM_BACKUP_RESTORE_STATUS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 476cd4ddab42ec9f8f44ff51b492bd3913824cf7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331298"
---
# <a name="wm_backup_restore_status-structure"></a>\_Struttura di \_ Stato ripristino backup \_ WM

La **struttura \_ \_ \_ dello stato di ripristino del backup WM** include informazioni su un'operazione di backup o ripristino delle licenze in sospeso.

## <a name="syntax"></a>Sintassi


```C++
typedef struct WM_BACKUP_RESTORE_STATUS {
  MSDRM_STATUS eStatus;
  BSTR         bstrError;
} ;
```



## <a name="members"></a>Members

<dl> <dt>

**eStatus**
</dt> <dd>

Membro dell'enumerazione [**di \_ stato MSDRM**](msdrm-status.md) che specifica lo stato.

</dd> <dt>

**bstrError**
</dt> <dd>

Stringa contenente l'errore.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa struttura viene ricevuta quando si chiama il metodo [**IWMDRMLicenseBackupRestoreStatus:: GetStatus**](iwmdrmlicensebackuprestorestatus-getstatus.md) . Contiene lo stato dell'operazione di backup o ripristino in sospeso al momento della chiamata.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Strutture**](drm-structures.md)
</dt> </dl>

 

 





