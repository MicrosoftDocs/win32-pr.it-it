---
title: Funzione SisFreeBackupStructure (Sisbkup.h)
description: Libera la struttura di backup SIS specificata.
ms.assetid: 34d5e919-e4bf-4105-ac15-a2ff5adfbdee
keywords:
- Backup della funzione SisFreeBackupStructure
topic_type:
- apiref
api_name:
- SisFreeBackupStructure
api_location:
- Sisbkup.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e506881110ad9fbb60ea12479c64f8ef8024f8e0f9ddee753813795d31f3dd6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119021359"
---
# <a name="sisfreebackupstructure-function"></a>Funzione SisFreeBackupStructure

La **funzione SisFreeBackupStructure** libera la struttura di backup SIS specificata.

## <a name="syntax"></a>Sintassi


```C++
BOOL SisFreeBackupStructure(
  _In_ PVOID sisBackupStructure
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*sisBackupStructure* \[ Pollici\]
</dt> <dd>

Puntatore alla struttura di backup SIS restituita [**da SisCreateBackupStructure.**](siscreatebackupstructure.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione restituisce **TRUE se** viene completata correttamente e FALSE in **caso contrario.** Chiamare [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) per ottenere altre informazioni sul motivo per cui la chiamata non è riuscita.

## <a name="remarks"></a>Commenti

Questa funzione deve essere chiamata dopo il completamento dell'operazione di backup per il volume identificato dal valore del *parametro sisBackupStructure.*

Si noti che non è sicuro presupporre che questa operazione dealloci solo la memoria. Ad esempio, questa funzione può anche eseguire operazioni amministrative aggiuntive per l'architettura SIS. Chiamare quindi questa funzione anche se l'operazione di backup verrà chiusa immediatamente dopo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                            |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                   |
| Intestazione<br/>                   | <dl> <dt>Sisbkup.h</dt> </dl>   |
| Libreria<br/>                  | <dl> <dt>Sisbkup.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Sisbkup.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SisCreateBackupStructure**](siscreatebackupstructure.md)
</dt> </dl>

 

