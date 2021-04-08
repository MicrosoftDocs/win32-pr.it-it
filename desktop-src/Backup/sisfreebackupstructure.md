---
title: Funzione SisFreeBackupStructure (sisbkup. h)
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
ms.openlocfilehash: d3a135c4787ff116ec10efd61fa1492033393c88
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740695"
---
# <a name="sisfreebackupstructure-function"></a>SisFreeBackupStructure (funzione)

La funzione **SisFreeBackupStructure** libera la struttura di backup SIS specificata.

## <a name="syntax"></a>Sintassi


```C++
BOOL SisFreeBackupStructure(
  _In_ PVOID sisBackupStructure
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*sisBackupStructure* \[ in\]
</dt> <dd>

Puntatore alla struttura di backup SIS restituita da [**SisCreateBackupStructure**](siscreatebackupstructure.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione restituisce **true** se viene completata correttamente e **false** in caso contrario. Chiamare [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) per ottenere altre informazioni sul motivo per cui la chiamata ha avuto esito negativo.

## <a name="remarks"></a>Commenti

Questa funzione deve essere chiamata dopo il completamento dell'operazione di backup per il volume identificato dal valore del parametro *sisBackupStructure* .

Si noti che non è sicuro presupporre che questa operazione dealloca solo la memoria. Questa funzione, ad esempio, può eseguire anche operazioni amministrative aggiuntive per l'architettura SIS. Chiamare pertanto questa funzione anche se l'operazione di backup verrà chiusa immediatamente dopo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                            |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                   |
| Intestazione<br/>                   | <dl> <dt>Sisbkup. h</dt> </dl>   |
| Libreria<br/>                  | <dl> <dt>Sisbkup. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Sisbkup.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SisCreateBackupStructure**](siscreatebackupstructure.md)
</dt> </dl>

 

