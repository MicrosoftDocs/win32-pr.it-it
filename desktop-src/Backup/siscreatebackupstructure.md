---
title: Funzione SisCreateBackupStructure (sisbkup. h)
description: Crea una struttura di backup SIS basata sulle informazioni fornite.
ms.assetid: a8c48961-fa24-4eb6-92cd-1b9bc83cec41
keywords:
- Backup della funzione SisCreateBackupStructure
topic_type:
- apiref
api_name:
- SisCreateBackupStructure
api_location:
- Sisbkup.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad432095f9d264e124df1d84070056fc827c625e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475928"
---
# <a name="siscreatebackupstructure-function"></a>SisCreateBackupStructure (funzione)

La funzione **SisCreateBackupStructure** crea una struttura di backup SIS basata sulle informazioni fornite.

## <a name="syntax"></a>Sintassi


```C++
BOOL SisCreateBackupStructure(
  _In_  PWCHAR volumeRoot,
  _Out_ PVOID  *sisBackupStructure,
  _Out_ PWCHAR *commonStoreRootPathname,
  _Out_ PULONG countOfCommonStoreFilesToBackUp,
  _Out_ PWCHAR **commonStoreFilesToBackUp
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*volumeRoot* \[ in\]
</dt> <dd>

Nome file della radice del volume, senza la barra rovesciata finale, del volume di cui eseguire il backup. Ad esempio, specificare "C:" e non "C: \\ ".

</dd> <dt>

*sisBackupStructure* \[ out\]
</dt> <dd>

Struttura di backup SIS restituita.

</dd> <dt>

*commonStoreRootPathname* \[ out\]
</dt> <dd>

Nome percorso completo dell'archivio comune del volume specificato. Ad esempio, "c: \\ SIS Common Store".

</dd> <dt>

*countOfCommonStoreFilesToBackUp* \[ out\]
</dt> <dd>

Numero di file elencati nel parametro *commonStoreFilesToBackUp* .

</dd> <dt>

*commonStoreFilesToBackUp* \[ out\]
</dt> <dd>

Puntatore a una matrice di nomi di file che specifica un elenco di file interni utilizzati da SIS per gestire il volume specificato. È necessario eseguire il backup di questi file nello stesso momento e nello stesso modo dei file di archivio comuni richiesti da [ **SisCSFilesToBackupForLink**](siscsfilestobackupforlink.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione restituisce **true** se viene completata correttamente e **false** in caso contrario. Chiamare [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) per ottenere altre informazioni sul motivo per cui la chiamata ha avuto esito negativo.

## <a name="remarks"></a>Commenti

Questa funzione crea una struttura di backup SIS, che viene usata dall'API di backup SIS per creare e gestire un elenco di collegamenti di file nel volume e i file originali a cui puntano i collegamenti. Questa funzione deve essere chiamata una sola volta per ogni volume abilitato per SIS di cui viene eseguito il backup. Tutti i file all'interno del volume specificato devono essere considerati come file di archivio comuni e sottoposti a backup solo se SIS indica che dovrebbero.

I parametri *countOfCommonStoreFilesToBackUp* e *commonStoreFilesToBackUp* restituiscono insieme un elenco di file di cui è necessario eseguire il backup indipendentemente dai collegamenti di cui viene eseguito il backup.

Se *countOfCommonStoreFilesToBackUp* è 0, *commonStoreFilesToBackUp* può essere un puntatore **null** . Il valore del parametro *commonStoreFilesToBackUp* deve essere ignorato.

Al termine dell'operazione di backup, deallocare la memoria utilizzata dalla matrice di stringhe *commonStoreFilesToBackUp* chiamando [**SisFreeAllocatedMemory**](sisfreeallocatedmemory.md).

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
</dt> <dt>

[**SisCSFilesToBackupForLink**](siscsfilestobackupforlink.md)
</dt> <dt>

[**SisFreeAllocatedMemory**](sisfreeallocatedmemory.md)
</dt> </dl>

 

