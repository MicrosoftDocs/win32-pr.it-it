---
title: Funzione SisCSFilesToBackupForLink (sisbkup. h)
description: Restituisce informazioni che descrivono i file dell'archivio comune a cui punta il collegamento SIS specificato.
ms.assetid: 0580c34e-195a-4a2c-893f-bc339dcc88d7
keywords:
- Backup della funzione SisCSFilesToBackupForLink
topic_type:
- apiref
api_name:
- SisCSFilesToBackupForLink
api_location:
- Sisbkup.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27d4f52728d662f43efed85d662874bd4b008947
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301278"
---
# <a name="siscsfilestobackupforlink-function"></a>SisCSFilesToBackupForLink (funzione)

La funzione **SisCSFilesToBackupForLink** restituisce informazioni che descrivono i file dell'archivio comune a cui punta il collegamento SIS specificato.

## <a name="syntax"></a>Sintassi


```C++
BOOL SisCSFilesToBackupForLink(
  _In_  PVOID  sisBackupStructure,
  _In_  PVOID  reparseData,
  _In_  ULONG  reparseDataSize,
  _Out_ PVOID  thisFileContext,
  _Out_ PVOID  *matchingFileContext,
  _Out_ PULONG countOfCommonStoreFilesToBackUp,
  _Out_ PWCHAR **commonStoreFilesToBackUp
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*sisBackupStructure* \[ in\]
</dt> <dd>

Puntatore alla struttura di backup SIS restituita da [**SisCreateBackupStructure**](siscreatebackupstructure.md).

</dd> <dt>

*reparseData* \[ in\]
</dt> <dd>

Puntatore al contenuto del punto di analisi SIS. Questo reparse point contiene dati che descrivono un collegamento SIS. Per recuperare i dati di reparse point per un file, usare il codice di controllo [**FSCTL \_ get \_ reparse \_ Point**](/windows/desktop/api/winioctl/ni-winioctl-fsctl_get_reparse_point) .

</dd> <dt>

*reparseDataSize* \[ in\]
</dt> <dd>

Dimensioni del contenuto del punto di analisi SIS a cui punta *reparseData* in byte.

</dd> <dt>

*thisFileContext* \[ out\]
</dt> <dd>

Puntatore a una stringa di contesto fornita dall'applicazione di backup che chiama questa funzione. Il contenuto di questa stringa di contenuto è determinato interamente da questa applicazione di backup e non è interpretato dall'API di backup SIS. Questo parametro è facoltativo; Se non viene usato, impostare il valore di questo parametro su **null**. Il valore di questo parametro non verrà elaborato in questo caso.

</dd> <dt>

*matchingFileContext* \[ out\]
</dt> <dd>

Puntatore doppiamente indiretto alla stringa di contesto del collegamento SIS identificato dalle informazioni passate nei primi quattro parametri della funzione. Questo parametro è facoltativo; Se non viene specificata una stringa di contesto come valore del parametro *thisFileContext* , impostare il valore di questo parametro su **null**. Il valore di questo parametro non verrà elaborato in questo caso.

</dd> <dt>

*countOfCommonStoreFilesToBackUp* \[ out\]
</dt> <dd>

Numero di file elencati nel parametro *commonStoreFilesToBackUp* .

</dd> <dt>

*commonStoreFilesToBackUp* \[ out\]
</dt> <dd>

Puntatore a una matrice di nomi di file. È necessario eseguire il backup di questi file nello stesso momento e nello stesso modo dei file di archivio comuni richiesti da [**SisCreateBackupStructure**](siscreatebackupstructure.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione restituisce **true** se viene completata correttamente e **false** in caso contrario. Chiamare [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) per ottenere altre informazioni sul motivo per cui la chiamata ha avuto esito negativo.

## <a name="remarks"></a>Commenti

L'applicazione di backup deve chiamare questa funzione una sola volta per ogni file di collegamento SIS di cui viene eseguito il backup.

L'applicazione di backup è in grado di identificare un punto di analisi SIS in base al tag, IO \_ reparse \_ tag \_ SIS. Questo tag è definito in Winnt. h.

Se questo punto di analisi identificato dal valore del parametro *reparseData* descrive la prima istanza di un file di cui eseguire il backup, la funzione restituirà **null** come valore del parametro *matchingFileContext* e inizializza il valore della matrice *commonStoreFilesToBackUp* di stringhe con i nomi del file o dei file di archivio comuni di cui eseguire il backup. In caso contrario, questa funzione imposterà il valore del parametro *matchingFileContext* sulla stringa di contesto corrispondente alla prima istanza del file specificato e imposterà il valore del parametro *countOfCommonStoreFilesToBackUp* su 0. Se sono presenti più file di archivio comuni che corrispondono al collegamento specificato, il valore del parametro *thisFileContext* sarà la stringa di contesto corrispondente al primo file di archivio comune restituito nella matrice, ovvero commonStoreFilesToBackUp \[ 0 \] .

La versione corrente di questa funzione restituirà al massimo un file di archivio comune, ma è possibile che nelle versioni future un solo collegamento possa essere supportato da diversi file di archivio comuni, ad esempio uno per ogni flusso del file, in modo che l'applicazione di backup debba supportare più file in ogni chiamata a questa funzione. In ogni caso, ogni file di archivio comune verrà restituito al massimo una volta per ogni passaggio di backup.

L'applicazione di backup deve eseguire il backup o il ripristino del file o dei file dell'archivio comune identificato dal nome file o dai nomi file restituiti nel parametro *commonStoreFilesToBackUp* . Indipendentemente dal fatto che esista un file di archivio comune corrispondente, l'applicazione di backup deve eseguire il backup del file di collegamento SIS così come esiste sul disco, ad esempio, come un reparse point e un file sparse e probabilmente senza intervalli compilati. L'applicazione di backup può eseguire il backup o ripristinare immediatamente il file o i file dell'archivio comune, posticiparne il backup o combinarli in modo necessario.

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

[**SisFreeAllocatedMemory**](sisfreeallocatedmemory.md)
</dt> <dt>

[**SisCreateBackupStructure**](siscreatebackupstructure.md)
</dt> </dl>

 

