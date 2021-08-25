---
title: Funzione AllocFixupInfo (NapUtil.h)
description: Alloca memoria per una struttura FixupInfo delle dimensioni specificate.
ms.assetid: e0b66a08-9714-4451-a22d-3822153c6a36
keywords:
- Funzione AllocFixupInfo NAP
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
ms.openlocfilehash: 95ce329a433439716700b6ffc990d446c5d22faab91fa256f6abc0c73734327d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119803491"
---
# <a name="allocfixupinfo-function"></a>Funzione AllocFixupInfo

> [!Note]  
> La piattaforma Protezione accesso alla rete non è disponibile a partire da Windows 10

 

La **funzione AllocFixupInfo** alloca memoria per una [**struttura FixupInfo**](/windows/win32/api/naptypes/ns-naptypes-fixupinfo) delle dimensioni specificate.

## <a name="syntax"></a>Sintassi


```C++
NAPAPI HRESULT WINAPI AllocFixupInfo(
  _Inout_ FixupInfo **fixupInfo,
  _In_    UINT16    countResultCodes
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*fixupInfo* \[ in, out\]
</dt> <dd>

Puntatore all'indirizzo di una struttura [**FixupInfo appena allocata.**](/windows/win32/api/naptypes/ns-naptypes-fixupinfo)

</dd> <dt>

*countResultCodes* \[ Pollici\]
</dt> <dd>

Numero di codici di risultato da allocare *a fixupInfo.*

</dd> </dl>

## <a name="return-value"></a>Valore restituito



| Codice restituito                                                                                   | Descrizione                                                                |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | L'operazione è stata completata correttamente.<br/>                       |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | È stato passato un argomento non valido.<br/>                                 |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | La memoria virtuale del sistema è insufficiente. L'operazione non è riuscita.<br/> |



 

## <a name="remarks"></a>Commenti

Tutte le interfacce COM supportate dal sistema nap usano le regole di gestione della memoria COM standard e gli allocatori di memoria COM (**CoTaskMemAlloc** e **CoTaskMemFree**):

-   **In** i parametri vengono allocati e liberati dal chiamante.
-   **I** parametri out vengono allocati dal chiamato e liberati dal chiamante usando **CoTaskMem.**
-   **I parametri in/out** vengono allocati dal chiamante, liberati e riallocati dal chiamato e infine liberati dal chiamante, usando **CoTaskMem.**

Tutte le funzioni di Protezione accesso alla rete per liberare memoria liberano anche tutti i puntatori incorporati.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                       |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>NapUtil.h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qutil.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**FreeFixupInfo**](freefixupinfo-func.md)
</dt> </dl>

 

 





