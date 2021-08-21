---
title: Funzione SisFreeAllocatedMemory (Sisbkup.h)
description: Libera la memoria allocata dalle funzioni API SIS.
ms.assetid: 8fab79c8-593c-46df-a885-09a59620a977
keywords:
- Backup della funzione SisFreeAllocatedMemory
topic_type:
- apiref
api_name:
- SisFreeAllocatedMemory
api_location:
- Sisbkup.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4510e464c2201952823d144721614caa7b5f1397c68f4f129dac73a4015b86a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119702181"
---
# <a name="sisfreeallocatedmemory-function"></a>Funzione SisFreeAllocatedMemory

La **funzione SisFreeAllocatedMemory** libera la memoria allocata dalle funzioni API SIS.

## <a name="syntax"></a>Sintassi


```C++
void SisFreeAllocatedMemory(
  _In_ PVOID allocatedSpace
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*allocatedSpace* \[ Pollici\]
</dt> <dd>

Puntatore alla memoria allocata dall'API SIS.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

Al termine della chiamata a questa funzione, il chiamante potrebbe non accedere più alla memoria liberata.

Questa chiamata deve essere usata per deallocare la memoria allocata per le stringhe di parametro *commonStoreRootPathname* restituite da [**SisCreateBackupStructure**](siscreatebackupstructure.md) e [**SisCreateRestoreStructure**](siscreaterestorestructure.md)e la matrice di stringhe contenenti nomi di file dell'archivio comune restituiti da **SisCreateBackupStructure**, [**SisCSFilesToBackupForLink**](siscsfilestobackupforlink.md), **SisCreateRestoreStructure** e [**SisRestoredLink**](sisrestoredlink.md). Nel secondo caso, anche la matrice stessa deve essere liberata chiamando **SisFreeAllocatedMemory**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                            |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                   |
| Intestazione<br/>                   | <dl> <dt>Sisbkup.h</dt> </dl>   |
| Libreria<br/>                  | <dl> <dt>Sisbkup.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Sisbkup.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SisCreateBackupStructure**](siscreatebackupstructure.md)
</dt> <dt>

[**SisCreateRestoreStructure**](siscreaterestorestructure.md)
</dt> <dt>

[**SisCSFilesToBackupForLink**](siscsfilestobackupforlink.md)
</dt> <dt>

[**SisRestoredLink**](sisrestoredlink.md)
</dt> </dl>

 

 





