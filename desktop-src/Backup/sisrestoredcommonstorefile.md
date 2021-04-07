---
title: Funzione SisRestoredCommonStoreFile (sisbkup. h)
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
ms.openlocfilehash: 093ff5f20db42bcafe62ee0ec57d5027abcf9f22
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963948"
---
# <a name="sisrestoredcommonstorefile-function"></a>SisRestoredCommonStoreFile (funzione)

La funzione **SisRestoredCommonStoreFile** segnala all'architettura SIS che è stato scritto un file di archivio comune.

## <a name="syntax"></a>Sintassi


```C++
BOOL SisRestoredCommonStoreFile(
  _In_ PVOID  sisRestoreStructure,
  _In_ PWCHAR commonStoreFileName
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*sisRestoreStructure* \[ in\]
</dt> <dd>

Puntatore a una struttura di ripristino SIS restituita da [**SisCreateRestoreStructure**](siscreaterestorestructure.md).

</dd> <dt>

*commonStoreFileName* \[ in\]
</dt> <dd>

Nome del file di archivio comune ripristinato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione restituisce **true** se viene completata correttamente e **false** in caso contrario. Chiamare [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) per ottenere altre informazioni sul motivo per cui la chiamata ha avuto esito negativo.

## <a name="remarks"></a>Commenti

Questa funzione deve essere chiamata dopo il ripristino di un file di archivio comune. Informa l'architettura SIS che è stato scritto un nuovo file di archivio comune, in modo che l'architettura SIS possa eseguire attività di manutenzione interne, ad esempio l'inizializzazione delle strutture di dati interne o la correzione dei collegamenti al file di archivio comune.

L'operazione di ripristino dovrebbe ripristinare solo i file di archivio comuni segnalati da [**SisRestoredLink**](sisrestoredlink.md), anche se nel supporto di backup sono presenti file di archivio comuni aggiuntivi. L'operazione di ripristino consente di ripristinare i collegamenti SIS e i file di archivio comuni in qualsiasi ordine scelto; Tuttavia, deve chiamare **SisRestoredLink** dopo che il collegamento è stato ripristinato ed è necessario chiamare questa funzione dopo che è stato ripristinato un file di archivio comune. Poiché l'operazione di ripristino non è in grado di identificare i file di archivio comuni che verranno ripristinati fino a quando non vengono segnalati i nomi dei file in seguito al ripristino di un collegamento, l'operazione di ripristino ripristinerà sempre un file di archivio comune dopo che è stato ripristinato almeno un collegamento che vi fa riferimento. È tuttavia possibile ripristinare collegamenti SIS aggiuntivi che puntano a tale file di archivio comune.

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

[**SisRestoredLink**](sisrestoredlink.md)
</dt> </dl>

 

