---
title: Funzione SisCreateRestoreStructure (sisbkup. h)
description: Crea una struttura di ripristino SIS basata sulle informazioni fornite.
ms.assetid: acdd4258-813d-42af-a2e1-e59a1426f86c
keywords:
- Backup della funzione SisCreateRestoreStructure
topic_type:
- apiref
api_name:
- SisCreateRestoreStructure
api_location:
- Sisbkup.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b83ebcdd609b00fdec19666a6915926692a2048
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873534"
---
# <a name="siscreaterestorestructure-function"></a>SisCreateRestoreStructure (funzione)

La funzione **SisCreateRestoreStructure** crea una struttura di ripristino SIS basata sulle informazioni fornite.

## <a name="syntax"></a>Sintassi


```C++
BOOL SisCreateRestoreStructure(
  _In_  PWCHAR volumeRoot,
  _Out_ PVOID  *sisRestoreStructure,
  _Out_ PWCHAR *commonStoreRootPathname,
  _Out_ PULONG countOfCommonStoreFilesToRestore,
  _Out_ PWCHAR **commonStoreFilesToRestore
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*volumeRoot* \[ in\]
</dt> <dd>

Nome file della radice del volume, senza la barra rovesciata finale, del volume di cui eseguire il backup. Ad esempio, specificare "C:" e non "C: \\ ". Il volume non può essere il volume di sistema o di avvio.

</dd> <dt>

*sisRestoreStructure* \[ out\]
</dt> <dd>

Struttura di ripristino SIS restituita. Questa struttura deve essere considerata opaca dal chiamante.

</dd> <dt>

*commonStoreRootPathname* \[ out\]
</dt> <dd>

Nome percorso completo dell'archivio comune del volume specificato. Ad esempio, "c: \\ SIS Common Store".

</dd> <dt>

*countOfCommonStoreFilesToRestore* \[ out\]
</dt> <dd>

Numero di file elencati nel parametro *commonStoreFilesToRestore* .

</dd> <dt>

*commonStoreFilesToRestore* \[ out\]
</dt> <dd>

Puntatore a una matrice di nomi di file che specifica l'elenco di file interni utilizzati da SIS per gestire il volume specificato. Questi file devono essere ripristinati nello stesso momento e nello stesso modo dei file di archivio comuni richiesti da [**SisCSFilesToBackupForLink**](siscsfilestobackupforlink.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione restituisce **true** se viene completata correttamente e **false** in caso contrario. Chiamare [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) per ottenere altre informazioni sul motivo per cui la chiamata ha avuto esito negativo.

## <a name="remarks"></a>Commenti

Questa funzione stabilisce l'ambiente di ripristino nel volume specificato nel modo in cui [**SisCreateBackupStructure**](siscreatebackupstructure.md) stabilisce l'ambiente di backup nel volume specificato.

Si noti che questa funzione non identificherà necessariamente il file o i file di archivio comuni corrispondenti a un set di collegamenti SIS nei supporti di backup se tali file o file di archivio comuni sono ancora presenti sul disco. Il contenuto del flusso di dati di un file di archivio comune non cambia mai dopo la creazione, quindi, se il file esiste già sul disco, non è necessario ripristinarlo.

I nomi di file di archivio comuni sono univoci a livello globale per garantire l'integrità dell'operazione di ripristino anche se non si verificano nello stesso volume abilitato per SIS a cui è stato eseguito l'accesso all'operazione di backup.

Al termine dell'operazione di ripristino, deallocare la memoria utilizzata dalla matrice di stringhe *commonStoreFilesToRestore* chiamando [**SisFreeAllocatedMemory**](sisfreeallocatedmemory.md).

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

[**SisCSFilesToBackupForLink**](siscsfilestobackupforlink.md)
</dt> <dt>

[**SisFreeAllocatedMemory**](sisfreeallocatedmemory.md)
</dt> <dt>

[**SisFreeBackupStructure**](sisfreebackupstructure.md)
</dt> </dl>

 

