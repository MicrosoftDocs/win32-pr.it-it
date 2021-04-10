---
title: Funzione SisRestoredLink (sisbkup. h)
description: Restituisce i nomi del file o dei file dell'archivio comune a cui fa riferimento il collegamento SIS ripristinato specificato.
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
ms.openlocfilehash: fd539d1ad6c203441b2bcd469a7d8f2fe8bdfc7c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963947"
---
# <a name="sisrestoredlink-function"></a>SisRestoredLink (funzione)

La funzione **SisRestoredLink** restituisce i nomi del file o dei file dell'archivio comune a cui fa riferimento il collegamento SIS ripristinato specificato.

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

*sisRestoreStructure* \[ in\]
</dt> <dd>

Puntatore a una struttura di ripristino SIS restituita da [**SisCreateRestoreStructure**](siscreaterestorestructure.md).

</dd> <dt>

*restoredFileName* \[ in\]
</dt> <dd>

Nome file completo del file di collegamento SIS ripristinato.

</dd> <dt>

*reparseData* \[ in\]
</dt> <dd>

Puntatore al contenuto del punto di analisi SIS. Questo reparse point contiene i dati che descrivono il collegamento SIS ripristinato. Per recuperare i dati di reparse point per un file, usare il codice di controllo [**FSCTL \_ get \_ reparse \_ Point**](/windows/desktop/api/winioctl/ni-winioctl-fsctl_get_reparse_point) .

</dd> <dt>

*reparseDataSize* \[ in\]
</dt> <dd>

Dimensioni del contenuto del punto di analisi SIS a cui punta *reparseData* in byte.

</dd> <dt>

*countOfCommonStoreFilesToRestore* \[ out\]
</dt> <dd>

Numero di file elencati nel parametro *commonStoreFilesToRestore* .

</dd> <dt>

*commonStoreFilesToRestore* \[ out\]
</dt> <dd>

Puntatore a una matrice di nomi di file di archivio comuni. Questi file devono essere ripristinati nello stesso momento e nello stesso modo dei file di archivio comuni richiesti da [**SisCSFilesToBackupForLink**](siscsfilestobackupforlink.md).

Se il valore del parametro *countOfCommonStoreFilesToRestore* è diverso da 0, il valore del parametro *commonStoreFilesToRestore* conterrà i nomi dei file dell'archivio comune da ripristinare in seguito al ripristino del collegamento SIS. Se il valore è 0, i file di archivio comuni sono stati restituiti una volta o sono già presenti nel volume.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione restituisce **true** se viene completata correttamente e **false** in caso contrario. Chiamare [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) per ottenere altre informazioni sul motivo per cui la chiamata ha avuto esito negativo.

## <a name="remarks"></a>Commenti

È necessario chiamare questa funzione per ogni collegamento SIS che è stato ripristinato.

Questa funzione restituirà ogni file di archivio comune al massimo una volta per ogni operazione di ripristino. qualsiasi tentativo di ripristinare collegamenti SIS aggiuntivi che visualizzano lo stesso file di archivio comune non comporterà la restituzione di un nome file di archivio comune.

Questa funzione non restituirà un file di archivio comune che non è stato restituito anche in una chiamata a [**SisCSFilesToBackupForLink**](siscsfilestobackupforlink.md) durante l'operazione di backup, supponendo che i dati di reparse SIS archiviati nel supporto non siano danneggiati.

Quando si ripristina un collegamento SIS, l'operazione di ripristino deve creare solo il file di tipo sparse appropriato, inizializzare tutti gli intervalli allocati, quindi scrivere i dati di rianalisi SIS esattamente come sono stati letti durante l'operazione di backup. È fondamentale che l'operazione di ripristino crei file sparse con intervalli non allocati piuttosto che file sparse (o file diversi) inizializzati con zeri.

Si noti che questa funzione non identificherà necessariamente il file o i file di archivio comuni corrispondenti a un set di collegamenti SIS nei supporti di backup se tali file o file di archivio comuni sono ancora presenti sul disco. Il contenuto del flusso di dati di un file di archivio comune non cambia mai dopo la creazione, quindi, se il file esiste già sul disco, non è necessario ripristinarlo.

I nomi di file di archivio comuni sono univoci a livello globale per garantire l'integrità dell'operazione di ripristino anche se non si verificano nello stesso volume abilitato per SIS a cui è stato eseguito l'accesso all'operazione di backup.

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
</dt> </dl>

 

