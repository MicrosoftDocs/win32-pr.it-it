---
title: Funzione AllocFixupInfo (NapUtil. h)
description: Alloca memoria per una struttura FixupInfo della dimensione specificata.
ms.assetid: e0b66a08-9714-4451-a22d-3822153c6a36
keywords:
- NAP funzione AllocFixupInfo
topic_type:
- apiref
api_name:
- AllocFixupInfo
api_location:
- qutil.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0dffda7e5e44302173ac06e460414455eb19c6c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873413"
---
# <a name="allocfixupinfo-function"></a>AllocFixupInfo (funzione)

> [!Note]  
> La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10

 

La funzione **AllocFixupInfo** alloca memoria per una struttura [**FixupInfo**](/windows/win32/api/naptypes/ns-naptypes-fixupinfo) della dimensione specificata.

## <a name="syntax"></a>Sintassi


```C++
NAPAPI HRESULT WINAPI AllocFixupInfo(
  _Inout_ FixupInfo **fixupInfo,
  _In_    UINT16    countResultCodes
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*fixupInfo* \[ in uscita\]
</dt> <dd>

Puntatore all'indirizzo di una struttura [**FixupInfo**](/windows/win32/api/naptypes/ns-naptypes-fixupinfo) appena allocata.

</dd> <dt>

*countResultCodes* \[ in\]
</dt> <dd>

Numero di codici di risultato da allocare a *fixupInfo*.

</dd> </dl>

## <a name="return-value"></a>Valore restituito



| Codice restituito                                                                                   | Descrizione                                                                |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | L'operazione è stata completata correttamente.<br/>                       |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | È stato passato un argomento non valido.<br/>                                 |
| <dl> <dt>**E \_ OutOfMemory**</dt> </dl> | Memoria virtuale insufficiente nel sistema. Operazione non riuscita.<br/> |



 

## <a name="remarks"></a>Commenti

Tutte le interfacce COM supportate dal sistema NAP utilizzano le regole di gestione della memoria COM standard e gli allocatori di memoria COM (**CoTaskMemAlloc** e **CoTaskMemFree**):

-   I parametri **in** vengono allocati e liberati dal chiamante.
-   I parametri **out** vengono allocati dal chiamato e liberati dal chiamante utilizzando **CoTaskMem**.
-   I parametri **in/out** vengono allocati dal chiamante, liberati e riallocati dal chiamato e infine liberati dal chiamante, usando **CoTaskMem**.

Tutte le funzioni di protezione accesso alla rete per liberare memoria liberano anche tutti i puntatori incorporati.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>NapUtil. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qutil.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**FreeFixupInfo**](freefixupinfo-func.md)
</dt> </dl>

 

 





