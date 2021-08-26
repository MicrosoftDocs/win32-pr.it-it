---
description: Elenca i file protetti.
ms.assetid: 46a1ff83-afed-4ce3-bb62-551446efdb78
title: Funzione SfcGetFiles (Sfcfiles.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SfcGetFiles
api_type:
- DllExport
api_location:
- Sfcfiles.dll
ms.openlocfilehash: 3201621808708229419542acd7fa0caab0aa7f6e7d38bfe723b7f53bc68c4005
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119999281"
---
# <a name="sfcgetfiles-function"></a>Funzione SfcGetFiles

\[Questa funzione è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. Il supporto per questa funzione è stato rimosso in Windows Vista e Windows Server 2008. Usare invece le funzioni supportate elencate in [Funzioni WRP.](wfp-functions.md)\]

Elenca i file protetti.

## <a name="syntax"></a>Sintassi


```C++
NTSTATUS WINAPI SfcGetFiles(
  _Out_ PPROTECT_FILE_ENTRY ProtFileData,
  _Out_ PULONG              FileCount
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ProtFileData* \[ Cambio\]
</dt> <dd>

Puntatore a una [**struttura PPROTECT \_ FILE \_ ENTRY**](pprotect-file-entry.md) che contiene l'elenco di file protetti.

</dd> <dt>

*Conteggio file* \[ Cambio\]
</dt> <dd>

Puntatore a un percorso contenente un valore ULONG che rappresenta il numero di file protetti.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è STATUS \_ SUCCESS. Se la funzione ha esito negativo, restituisce il codice di errore NTSTATUS appropriato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                             |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                    |
| Fine del supporto client<br/>    | Windows XP<br/>                                                                   |
| Fine del supporto server<br/>    | Windows Server 2003<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Sfcfiles.h</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Sfcfiles.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**PPROTECT \_ FILE \_ ENTRY**](pprotect-file-entry.md)
</dt> </dl>

 

 




