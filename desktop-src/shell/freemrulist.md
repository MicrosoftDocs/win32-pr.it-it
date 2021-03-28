---
description: Libera l'handle associato all'elenco degli ultimi elementi usati (MRU) e scrive i dati memorizzati nella cache nel registro di sistema.
title: FreeMRUList (funzione)
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
ms.openlocfilehash: 8140586d5f428a66f27a71ea665ae6761380e3a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104979650"
---
# <a name="freemrulist-function"></a>FreeMRUList (funzione)

Libera l'handle associato all'elenco degli ultimi elementi usati (MRU) e scrive i dati memorizzati nella cache nel registro di sistema.

## <a name="syntax"></a>Sintassi


```C++
int FreeMRUList(
  _In_ HANDLE hMRU
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hMRU* \[ in\]
</dt> <dd>

Tipo: **handle**

Handle dell'elenco MRU da liberare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **int**

Restituisce un valore non negativo se ha esito positivo,-1 in caso contrario.

## <a name="remarks"></a>Commenti

Se l'elenco MRU è stato creato con il flag **\_ CACHEWRITE di MRU** , la chiamata a **FreeMRUList** comporta la scrittura in questo momento di eventuali modifiche non ancora scritte nella versione dell'elenco MRU archiviato nel registro di sistema.

Questa funzione non è inclusa in un'intestazione o in una libreria pubblica. Deve essere estratta da comctl32.dll in base all'ordinale 152.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                     |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                           |
| DLL<br/>                      | <dl> <dt>Comctl32.dll (versione 5,0 o successiva)</dt> </dl> |



 

 




