---
title: Funzione AllocCountedString (NapUtil.h)
description: Alloca memoria per una stringa con terminazione Null e la restituisce in una struttura CountedString.
ms.assetid: 6dd503bf-8853-499b-adcd-54de696f01d6
keywords:
- Funzione AllocCountedString nap
topic_type:
- apiref
api_name:
- AllocCountedString
api_location:
- qutil.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef205cf7211f25253a3e6ba0cb7cd84ac37dbdb49848b36e844595d632552331
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119891741"
---
# <a name="alloccountedstring-function"></a>Funzione AllocCountedString

> [!Note]  
> La piattaforma Protezione accesso alla rete non è disponibile a partire da Windows 10

 

La **funzione AllocCountedString** alloca memoria per una stringa con terminazione Null e la restituisce in [**una struttura CountedString.**](/windows/win32/api/naptypes/ns-naptypes-countedstring)

## <a name="syntax"></a>Sintassi


```C++
NAPAPI HRESULT WINAPI AllocCountedString(
  _Inout_       CountedString **countedString,
  _In_    const WCHAR         *string
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*countedString* \[ in, out\]
</dt> <dd>

Puntatore all'indirizzo di una struttura [**CountedString appena**](/windows/win32/api/naptypes/ns-naptypes-countedstring) allocata.

</dd> <dt>

*string* \[ Pollici\]
</dt> <dd>

Puntatore alla stringa con terminazione Null che deve essere restituita in *countedString*.

</dd> </dl>

## <a name="return-value"></a>Valore restituito



| Codice restituito                                                                                   | Descrizione                                                                |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | L'operazione è stata completata correttamente.<br/>                       |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | È stato passato un argomento non valido.<br/>                                 |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | La memoria virtuale del sistema è insufficiente. L'operazione non è riuscita.<br/> |



 

## <a name="remarks"></a>Commenti

Tutte le interfacce COM supportate dal sistema di Protezione accesso alla rete usano regole di gestione della memoria COM standard e allocatori di memoria COM (**CoTaskMemAlloc** e **CoTaskMemFree**):

-   **I** parametri in vengono allocati e liberati dal chiamante.
-   **I** parametri out vengono allocati dal chiamato e liberati dal chiamante usando **CoTaskMem**.
-   **I parametri in/out** vengono allocati dal chiamante, liberati e riallocati dal chiamato e infine liberati dal chiamante, usando **CoTaskMem**.

Tutte le funzioni di Protezione accesso alla rete per liberare memoria liberano anche tutti i puntatori incorporati.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                       |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>NapUtil.h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qutil.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**FreeCountedString**](freecountedstring-func.md)
</dt> </dl>

 

 





