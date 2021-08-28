---
description: Questa funzione termina forzatamente il programma chiamante se viene richiamato all'interno di un callout del caricatore. In caso contrario, non ha alcun effetto.
ms.assetid: 5C10BF04-B7C7-4481-A184-FDD418FE5F52
title: Funzione LdrFastFailInLoaderCallout
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LdrFastFailInLoaderCallout
api_type:
- DllExport
api_location:
- NTDll.dll
ms.openlocfilehash: f944de64f26d814af799d1f8d2419c2dd9ade04970774e2581f446c0bd32c0fc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120001331"
---
# <a name="ldrfastfailinloadercallout-function"></a>Funzione LdrFastFailInLoaderCallout

\[Alcune informazioni riguardano prodotti pre-rilasciati che possono essere modificati in modo sostanziale prima che venga rilasciato commercialmente. Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]

Questa funzione termina forzatamente il programma chiamante se viene richiamato all'interno di un callout del caricatore. In caso contrario, non ha alcun effetto.

## <a name="syntax"></a>Sintassi


```C++
VOID NTAPI LdrFastFailInLoaderCallout(void);
```



## <a name="parameters"></a>Parametri

Questa funzione non ha parametri.

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

Questa routine non rileva tutti i potenziali casi di deadlock. è possibile che un thread all'interno di un callout del caricatore acquisisca un blocco mentre un thread all'esterno di un callout del caricatore mantiene lo stesso blocco ed esegue una chiamata al caricatore. In altre parole, può esserci un'inversione dell'ordine di blocco tra il blocco del caricatore e un blocco client.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------|
| Libreria<br/> | <dl> <dt>NTDll.lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>NTDll.dll</dt> </dl> |



 

 




