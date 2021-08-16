---
title: Funzione SisCSFilesToBackupForLink (Sisbkup.h)
description: Restituisce informazioni che descrivono i file di archivio comune a cui punta il collegamento SIS specificato.
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
ms.openlocfilehash: 2e39d4370e68b67a5c05c1f259c52190be3b931dd02164da191bacf879cd6cb0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117835559"
---
# <a name="siscsfilestobackupforlink-function"></a>Funzione SisCSFilesToBackupForLink

La **funzione SisCSFilesToBackupForLink** restituisce informazioni che descrivono i file dell'archivio comune a cui punta il collegamento SIS specificato.

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

*sisBackupStructure* \[ Pollici\]
</dt> <dd>

Puntatore alla struttura di backup SIS restituita [**da SisCreateBackupStructure.**](siscreatebackupstructure.md)

</dd> <dt>

*reparseData* \[ Pollici\]
</dt> <dd>

Puntatore al contenuto del reparse point SIS. Questo reparse point contiene dati che descrivono un collegamento SIS. Per recuperare i dati del reparse point per un file, usare il codice di controllo [**\_ FSCTL GET \_ REPARSE \_ POINT.**](/windows/desktop/api/winioctl/ni-winioctl-fsctl_get_reparse_point)

</dd> <dt>

*reparseDataSize* \[ Pollici\]
</dt> <dd>

Dimensioni del contenuto del reparse point SIS a cui punta *reparseData*, in byte.

</dd> <dt>

*thisFileContext* \[ Cambio\]
</dt> <dd>

Puntatore a una stringa di contesto fornita dall'applicazione di backup che chiama questa funzione. Il contenuto di questa stringa di contenuto è interamente determinato da questa applicazione di backup e non viene interpretato dall'API di backup SIS. Questo parametro è facoltativo. Se non viene usato, impostare il valore di questo parametro su **NULL.** Il valore di questo parametro non verrà elaborato in questo caso.

</dd> <dt>

*matchingFileContext* \[ Cambio\]
</dt> <dd>

Puntatore indiretto doppiamente alla stringa di contesto del collegamento SIS identificato dalle informazioni passate nei primi quattro parametri di questa funzione. Questo parametro è facoltativo. Se non viene specificata una stringa di contesto come valore del *parametro thisFileContext,* impostare il valore di questo parametro su **NULL.** Il valore di questo parametro non verrà elaborato in questo caso.

</dd> <dt>

*countOfCommonStoreFilesToBackUp* \[ Cambio\]
</dt> <dd>

Numero di file elencati nel *parametro commonStoreFilesToBackUp.*

</dd> <dt>

*commonStoreFilesToBackUp* \[ Cambio\]
</dt> <dd>

Puntatore a una matrice di nomi di file. Il backup di questi file deve essere eseguito contemporaneamente e nello stesso modo dei file di archivio comune richiesti da [**SisCreateBackupStructure.**](siscreatebackupstructure.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione restituisce **TRUE se** viene completata correttamente e FALSE in **caso contrario.** Chiamare [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) per ottenere altre informazioni sul motivo per cui la chiamata non è riuscita.

## <a name="remarks"></a>Commenti

L'applicazione di backup deve chiamare questa funzione una sola volta per ogni file di collegamento SIS di cui viene eseguito il backup.

L'applicazione di backup può identificare un reparse point SIS in base al tag IO \_ REPARSE \_ TAG \_ SIS. Questo tag è definito in Winnt.h.

Se questo reparse point identificato dal valore del parametro *reparseData* descrive la prima istanza di un file di cui eseguire il backup, questa funzione restituirà **NULL** come valore del parametro *matchingFileContext* e inizializza il valore della matrice di stringhe *commonStoreFilesToBackUp* con i nomi del file o dei file dell'archivio comune di cui eseguire il backup. In caso contrario, questa funzione imposta il valore del parametro *matchingFileContext* sulla stringa di contesto corrispondente alla prima istanza del file specificato e imposta il valore del parametro *countOfCommonStoreFilesToBackUp* su 0. Se sono presenti più file di archivio comune corrispondenti al collegamento specificato, il valore del parametro *thisFileContext* sarà la stringa di contesto corrispondente al primo file di archivio comune restituito nella matrice, commonStoreFilesToBackUp \[ \] 0.

La versione corrente di questa funzione restituirà al massimo un file di archivio comune, ma è possibile che nelle versioni future un singolo collegamento possa essere supportato da diversi file di archivio comune, ad esempio uno per ogni flusso nel file, in modo che l'applicazione di backup supporti più file in ogni chiamata a questa funzione. In ogni caso, ogni file di archivio comune verrà restituito al massimo una volta per ogni passaggio di backup.

L'applicazione di backup deve eseguire il backup o il ripristino del file o dei file dell'archivio comune identificati dal nome file o dai nomi file restituiti nel *parametro commonStoreFilesToBackUp.* Indipendentemente dal fatto che sia presente un file di archivio comune corrispondente, l'applicazione di backup deve eseguire il backup del file di collegamento SIS esistente sul disco, ad esempio come reparse point e file sparse e molto probabilmente senza intervalli compilati. L'applicazione di backup può eseguire immediatamente il backup o il ripristino del file o dei file dell'archivio comune, posticiparlo o combinarli in base alle esigenze.

Al termine dell'operazione di backup, deallocare la memoria usata dalla matrice di stringhe *commonStoreFilesToBackUp* chiamando [**SisFreeAllocatedMemory**](sisfreeallocatedmemory.md).

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

[**SisFreeAllocatedMemory**](sisfreeallocatedmemory.md)
</dt> <dt>

[**SisCreateBackupStructure**](siscreatebackupstructure.md)
</dt> </dl>

 

