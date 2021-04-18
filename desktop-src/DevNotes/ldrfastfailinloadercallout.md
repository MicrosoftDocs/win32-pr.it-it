---
description: Questa funzione interrompe in modo forzato il programma chiamante se viene richiamato all'interno di un callout del caricatore. In caso contrario, non ha alcun effetto.
ms.assetid: 5C10BF04-B7C7-4481-A184-FDD418FE5F52
title: LdrFastFailInLoaderCallout (funzione)
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
ms.openlocfilehash: f74b9cdc0aec666242a8267fab8d6255c75dc94b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324697"
---
# <a name="ldrfastfailinloadercallout-function"></a>LdrFastFailInLoaderCallout (funzione)

\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale. Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]

Questa funzione interrompe in modo forzato il programma chiamante se viene richiamato all'interno di un callout del caricatore. In caso contrario, non ha alcun effetto.

## <a name="syntax"></a>Sintassi


```C++
VOID NTAPI LdrFastFailInLoaderCallout(void);
```



## <a name="parameters"></a>Parametri

Questa funzione non ha parametri.

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

Questa routine non rileva tutti i potenziali casi di deadlock; è possibile che un thread all'interno di un callout del caricatore acquisisca un blocco mentre un thread esterno a un callout del caricatore contiene lo stesso blocco ed effettua una chiamata al caricatore. In altre parole, può essere presente un'inversione dell'ordine di blocco tra il blocco del caricatore e un blocco client.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------|
| Libreria<br/> | <dl> <dt>NTDll. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>NTDll.dll</dt> </dl> |



 

 




