---
title: Funzione SisFreeRestoreStructure (sisbkup. h)
description: Libera la memoria allocata per la struttura di ripristino SIS specificata ed esegue attività che preparano il filtro SIS per impostare correttamente i collegamenti creati durante l'operazione di ripristino.
ms.assetid: dbdccb53-b38e-465d-a6d0-ee86923a5879
keywords:
- Backup della funzione SisFreeRestoreStructure
topic_type:
- apiref
api_name:
- SisFreeRestoreStructure
api_location:
- Sisbkup.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7293514d798fe65c82863a83549039b05ec8eb3e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478730"
---
# <a name="sisfreerestorestructure-function"></a>SisFreeRestoreStructure (funzione)

La funzione **SisFreeRestoreStructure** libera la memoria allocata per la struttura di ripristino SIS specificata ed esegue attività che preparano il filtro SIS per impostare correttamente i collegamenti creati durante l'operazione di ripristino.

## <a name="syntax"></a>Sintassi


```C++
BOOL SisFreeRestoreStructure(
  _In_ PVOID sisRestoreStructure
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*sisRestoreStructure* \[ in\]
</dt> <dd>

Puntatore a una struttura di ripristino SIS restituita da [**SisCreateRestoreStructure**](siscreaterestorestructure.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione restituisce **true** se viene completata correttamente e **false** in caso contrario. Chiamare [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) per ottenere altre informazioni sul motivo per cui la chiamata ha avuto esito negativo.

## <a name="remarks"></a>Commenti

L'accesso ai collegamenti SIS prima del completamento della chiamata a questa funzione può comportare un controllo del volume o una lettura parziale del contenuto del collegamento.

Si noti che non è sicuro presupporre che questa operazione dealloca solo la memoria. Questa funzione, ad esempio, può eseguire anche operazioni amministrative aggiuntive per l'architettura SIS. Chiamare pertanto questa funzione anche se l'operazione di ripristino verrà chiusa immediatamente dopo.

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

[**SisCreateRestoreStructure**](siscreaterestorestructure.md)
</dt> </dl>

 

