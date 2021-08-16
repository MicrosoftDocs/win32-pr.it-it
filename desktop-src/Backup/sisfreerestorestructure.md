---
title: Funzione SisFreeRestoreStructure (Sisbkup.h)
description: Libera la memoria allocata per la struttura di ripristino SIS specificata ed esegue attività che preparano il filtro SIS per configurare correttamente i collegamenti creati durante l'operazione di ripristino.
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
ms.openlocfilehash: a787283f933ae4ccd2d8100c39e6118b40c545c030bb236a27a2f1598417742e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117835549"
---
# <a name="sisfreerestorestructure-function"></a>Funzione SisFreeRestoreStructure

La **funzione SisFreeRestoreStructure** libera la memoria allocata per la struttura di ripristino SIS specificata ed esegue attività che preparano il filtro SIS per configurare correttamente i collegamenti creati durante l'operazione di ripristino.

## <a name="syntax"></a>Sintassi


```C++
BOOL SisFreeRestoreStructure(
  _In_ PVOID sisRestoreStructure
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*sisRestoreStructure* \[ Pollici\]
</dt> <dd>

Puntatore a una struttura di ripristino SIS restituita [**da SisCreateRestoreStructure.**](siscreaterestorestructure.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione restituisce **TRUE se** viene completata correttamente e FALSE in **caso contrario.** Chiamare [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) per ottenere altre informazioni sul motivo per cui la chiamata non è riuscita.

## <a name="remarks"></a>Commenti

L'accesso ai collegamenti SIS prima del completamento della chiamata a questa funzione può comportare un controllo del volume o una lettura parziale del contenuto del collegamento.

Si noti che non è sicuro presupporre che questa operazione dealloci solo la memoria. Ad esempio, questa funzione può anche eseguire operazioni amministrative aggiuntive per l'architettura SIS. Chiamare quindi questa funzione anche se l'operazione di ripristino verrà chiusa immediatamente dopo.

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

[**SisCreateRestoreStructure**](siscreaterestorestructure.md)
</dt> </dl>

 

