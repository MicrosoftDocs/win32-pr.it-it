---
description: Libera l'handle associato all'elenco MRU (Most Recently Used) e scrive i dati memorizzati nella cache nel Registro di sistema.
title: Funzione FreeMRUList
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FreeMRUList
api_type:
- DllExport
api_location:
- Comctl32.dll
ms.assetid: 51db9352-7188-4fb7-9c92-1d9579cd7250
ms.openlocfilehash: 7d31d261629853c3b82b9d1564c5e8755e047570
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/12/2021
ms.locfileid: "109840622"
---
# <a name="freemrulist-function"></a>Funzione FreeMRUList

Libera l'handle associato all'elenco MRU (Most Recently Used) e scrive i dati memorizzati nella cache nel Registro di sistema.

## <a name="syntax"></a>Sintassi


```C++
int FreeMRUList(
  _In_ HANDLE hMRU
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hMRU* \[ Pollici\]
</dt> <dd>

Tipo: **HANDLE**

Handle dell'elenco MRU da liberare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **int**

Restituisce un valore non negativo in caso di esito positivo, -1 in caso contrario.

## <a name="remarks"></a>Commenti

Se l'elenco MRU è stato creato usando il flag **MRU \_ CACHEWRITE,** la chiamata a **FreeMRUList** determina la scrittura di tutte le modifiche non ancora scritte nella versione dell'elenco MRU archiviata nel Registro di sistema.

Questa funzione non è inclusa in un'intestazione o in una libreria pubblica. Deve essere estratto da comctl32.dll ordinale 152.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                     |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                           |
| DLL<br/>                      | <dl> <dt>Comctl32.dll (versione 5.0 o successiva)</dt> </dl> |



 

 




