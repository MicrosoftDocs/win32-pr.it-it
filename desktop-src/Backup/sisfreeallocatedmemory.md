---
title: Funzione SisFreeAllocatedMemory (sisbkup. h)
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
ms.openlocfilehash: 724970817b89f6a9f2490b0776775f6a3a4e69ca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873533"
---
# <a name="sisfreeallocatedmemory-function"></a>SisFreeAllocatedMemory (funzione)

La funzione **SisFreeAllocatedMemory** libera la memoria allocata dalle funzioni API SIS.

## <a name="syntax"></a>Sintassi


```C++
void SisFreeAllocatedMemory(
  _In_ PVOID allocatedSpace
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*allocatedSpace* \[ in\]
</dt> <dd>

Puntatore alla memoria allocata dall'API SIS.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

Al termine della chiamata a questa funzione, il chiamante potrebbe non accedere più alla memoria liberata.

Questa chiamata deve essere utilizzata per deallocare la memoria allocata per le stringhe di parametri *commonStoreRootPathname* restituite da [**SisCreateBackupStructure**](siscreatebackupstructure.md) e [**SisCreateRestoreStructure**](siscreaterestorestructure.md)e la matrice di stringhe contenente i nomi di file di archivio comuni restituiti da **SisCreateBackupStructure**, [**SisCSFilesToBackupForLink**](siscsfilestobackupforlink.md), **SisCreateRestoreStructure** e [**SisRestoredLink**](sisrestoredlink.md). Nel secondo caso, la matrice deve anche essere liberata chiamando **SisFreeAllocatedMemory**.

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
</dt> <dt>

[**SisCreateRestoreStructure**](siscreaterestorestructure.md)
</dt> <dt>

[**SisCSFilesToBackupForLink**](siscsfilestobackupforlink.md)
</dt> <dt>

[**SisRestoredLink**](sisrestoredlink.md)
</dt> </dl>

 

 





