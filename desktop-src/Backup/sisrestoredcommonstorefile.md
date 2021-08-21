---
title: Funzione SisRestoredCommonStoreFile (Sisbkup.h)
description: Segnala all'architettura SIS che è stato scritto un file di archivio comune.
ms.assetid: 2b1cd9e7-a19c-4474-a40a-5a27d4feeab7
keywords:
- Backup della funzione SisRestoredCommonStoreFile
topic_type:
- apiref
api_name:
- SisRestoredCommonStoreFile
api_location:
- Sisbkup.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 389d40b76614fe64038133c8cc0623706d4f2be82e68b3e096b59b3023f08bf2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119529491"
---
# <a name="sisrestoredcommonstorefile-function"></a>Funzione SisRestoredCommonStoreFile

La **funzione SisRestoredCommonStoreFile** segnala all'architettura SIS che è stato scritto un file di archivio comune.

## <a name="syntax"></a>Sintassi


```C++
BOOL SisRestoredCommonStoreFile(
  _In_ PVOID  sisRestoreStructure,
  _In_ PWCHAR commonStoreFileName
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*sisRestoreStructure* \[ Pollici\]
</dt> <dd>

Puntatore a una struttura di ripristino SIS restituita [**da SisCreateRestoreStructure.**](siscreaterestorestructure.md)

</dd> <dt>

*commonStoreFileName* \[ Pollici\]
</dt> <dd>

Nome del file di archivio comune ripristinato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione restituisce **TRUE se** viene completata correttamente e FALSE in **caso contrario.** Chiamare [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) per ottenere altre informazioni sul motivo per cui la chiamata non è riuscita.

## <a name="remarks"></a>Commenti

Questa funzione deve essere chiamata dopo aver ripristinato un file di archivio comune. Notifica all'architettura SIS che è stato scritto un nuovo file di archivio comune, in modo che l'architettura SIS possa eseguire attività di manutenzione interne, ad esempio l'inizializzazione delle strutture di dati interne o la correzione dei collegamenti al file common-store.

L'operazione di ripristino dovrebbe ripristinare solo i file di archivio comune segnalati da [**SisRestoredLink,**](sisrestoredlink.md)anche se sono presenti file di archivio comune aggiuntivi nei supporti di backup. L'operazione di ripristino può ripristinare i collegamenti SIS e i file di archivio comune in qualsiasi ordine scelto; Tuttavia, deve chiamare **SisRestoredLink** dopo aver ripristinato qualsiasi collegamento e deve chiamare questa funzione dopo aver ripristinato qualsiasi file di archivio comune. Poiché l'operazione di ripristino non è in grado di identificare i file di archivio comune che verranno ripristinati fino a quando non vengono segnalati i nomi dei file in seguito al ripristino di un collegamento, l'operazione di ripristino ripristina sempre un file di archivio comune dopo il ripristino di almeno un collegamento che vi fa riferimento. È tuttavia possibile ripristinare collegamenti SIS aggiuntivi che puntano a tale file di archivio comune.

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
</dt> <dt>

[**SisRestoredLink**](sisrestoredlink.md)
</dt> </dl>

 

