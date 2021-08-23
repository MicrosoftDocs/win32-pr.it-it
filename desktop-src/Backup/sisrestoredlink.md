---
title: Funzione SisRestoredLink (Sisbkup.h)
description: Restituisce i nomi del file o dei file dell'archivio comune a cui punta il collegamento SIS ripristinato specificato.
ms.assetid: 4eefd975-6055-44c0-93ab-900638948f3e
keywords:
- Backup della funzione SisRestoredLink
topic_type:
- apiref
api_name:
- SisRestoredLink
api_location:
- Sisbkup.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34b330e4c6dfc5324f7041343865ea59885a0aedec01fa9c67014d3709a93834
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119021319"
---
# <a name="sisrestoredlink-function"></a>Funzione SisRestoredLink

La **funzione SisRestoredLink** restituisce i nomi del file o dei file dell'archivio comune a cui punta il collegamento SIS ripristinato specificato.

## <a name="syntax"></a>Sintassi


```C++
BOOL SisRestoredLink(
  _In_  PVOID  sisRestoreStructure,
  _In_  PWCHAR restoredFileName,
  _In_  PVOID  reparseData,
  _In_  ULONG  reparseDataSize,
  _Out_ PULONG countOfCommonStoreFilesToRestore,
  _Out_ PWCHAR **commonStoreFilesToRestore
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*sisRestoreStructure* \[ Pollici\]
</dt> <dd>

Puntatore a una struttura di ripristino SIS restituita da [**SisCreateRestoreStructure**](siscreaterestorestructure.md).

</dd> <dt>

*restoredFileName* \[ Pollici\]
</dt> <dd>

Nome file completo del file di collegamento SIS ripristinato.

</dd> <dt>

*reparseData* \[ Pollici\]
</dt> <dd>

Puntatore al contenuto del reparse point SIS. Questo reparse point contiene dati che descrivono il collegamento SIS ripristinato. Per recuperare i dati del reparse point per un file, usare il [**codice di controllo \_ FSCTL GET \_ REPARSE \_ POINT.**](/windows/desktop/api/winioctl/ni-winioctl-fsctl_get_reparse_point)

</dd> <dt>

*reparseDataSize* \[ Pollici\]
</dt> <dd>

Dimensione in byte del contenuto del reparse point SIS a cui *punta reparseData.*

</dd> <dt>

*countOfCommonStoreFilesToRestore* \[ Cambio\]
</dt> <dd>

Numero di file elencati nel *parametro commonStoreFilesToRestore.*

</dd> <dt>

*commonStoreFilesToRestore* \[ Cambio\]
</dt> <dd>

Puntatore a una matrice di nomi di file dell'archivio comune. Questi file devono essere ripristinati contemporaneamente e nello stesso modo dei file di archivio comune richiesti da [**SisCSFilesToBackupForLink**](siscsfilestobackupforlink.md).

Se il valore del parametro *countOfCommonStoreFilesToRestore* non è 0, il valore del parametro *commonStoreFilesToRestore* conterrà i nomi dei file di archivio comune da ripristinare in seguito al ripristino del collegamento SIS. Se il valore è 0, i file dell'archivio comune sono stati restituiti una sola volta o sono già presenti nel volume.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione restituisce **TRUE se** viene completata correttamente e FALSE in **caso contrario.** Chiamare [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) per ottenere altre informazioni sul motivo per cui la chiamata non è riuscita.

## <a name="remarks"></a>Commenti

È necessario chiamare questa funzione per ogni collegamento SIS ripristinato.

Questa funzione restituirà al massimo ogni file di archivio comune per ogni operazione di ripristino. Qualsiasi tentativo di ripristinare collegamenti SIS aggiuntivi che visualizzano lo stesso file di archivio comune non comporta la restituire il nome del file dell'archivio comune.

Questa funzione non restituirà un file di archivio comune che non è stato restituito anche in una chiamata a [**SisCSFilesToBackupForLink**](siscsfilestobackupforlink.md) durante l'operazione di backup, presupponendo che i dati di reparse SIS archiviati nel supporto non siano stati danneggiati.

Quando si ripristina un collegamento SIS, l'operazione di ripristino deve creare solo il file sparse appropriato, inizializzare gli intervalli allocati e quindi scrivere di nuovo i dati di analisi SIS esattamente come sono stati letti durante l'operazione di backup. È fondamentale che l'operazione di ripristino crei file di tipo sparse con intervalli non allocati anziché file di tipo sparse (o file non di tipo non di tipoparse) inizializzati con zeri.

Si noti che questa funzione non identificherà necessariamente il file o i file dell'archivio comune corrispondenti a un set di collegamenti SIS nel supporto di backup se tali file o file dell'archivio comune esistono ancora su disco. Il contenuto del flusso di dati di un file di archivio comune non cambia mai dopo la creazione, quindi se il file esiste già sul disco non è necessario ripristinarlo.

I nomi di file dell'archivio comune sono univoci a livello globale per garantire l'integrità dell'operazione di ripristino anche se non si verifica nello stesso volume abilitato per SIS a cui ha avuto accesso l'operazione di backup.

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

[**SisCreateRestoreStructure**](siscreaterestorestructure.md)
</dt> <dt>

[**SisCSFilesToBackupForLink**](siscsfilestobackupforlink.md)
</dt> </dl>

 

