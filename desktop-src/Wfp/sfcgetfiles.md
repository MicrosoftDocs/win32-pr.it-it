---
description: Elenca i file protetti.
ms.assetid: 46a1ff83-afed-4ce3-bb62-551446efdb78
title: Funzione SfcGetFiles (sfcfiles. h)
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
ms.openlocfilehash: 6b38b761372db656308e778fd96ea48607cf1f21
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882621"
---
# <a name="sfcgetfiles-function"></a>SfcGetFiles (funzione)

\[Questa funzione è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. Il supporto per questa funzione è stato rimosso in Windows Vista e Windows Server 2008. Usare invece le funzioni supportate elencate in [WRP Functions](wfp-functions.md) .\]

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

*ProtFileData* \[ out\]
</dt> <dd>

Puntatore a una struttura [**di \_ \_ voce di file PPROTECT**](pprotect-file-entry.md) che contiene l'elenco dei file protetti.

</dd> <dt>

*FileCount* \[ out\]
</dt> <dd>

Puntatore a una posizione contenente un valore ULONG che rappresenta il numero di file protetti.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è STATUS \_ Success. Se la funzione ha esito negativo, viene restituito il codice di errore NTSTATUS appropriato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                             |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                    |
| Fine del supporto client<br/>    | Windows XP<br/>                                                                   |
| Fine del supporto server<br/>    | Windows Server 2003<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Sfcfiles. h</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Sfcfiles.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_voce di file PPROTECT \_**](pprotect-file-entry.md)
</dt> </dl>

 

 




