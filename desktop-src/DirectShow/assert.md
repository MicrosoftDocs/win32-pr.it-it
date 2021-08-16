---
description: Valuta un'espressione e visualizza un messaggio di diagnostica se l'espressione è FALSE. Ignorato nelle build di vendita al dettaglio.
ms.assetid: 8c3815bb-3164-4066-a947-974e791af5cd
title: Macro ASSERT (Wxdebug.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ASSERT
api_type:
- HeaderDef
api_location:
- Wxdebug.h
ms.openlocfilehash: 1c64ae2256ae132fccdca6e483fae3f79d28b0cda66d7701acbe95abb1222d14
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117824430"
---
# <a name="assert-macro"></a>ASSERT (macro)

Valuta un'espressione e visualizza un messaggio di diagnostica se l'espressione è **FALSE.** Ignorato nelle build di vendita al dettaglio.

## <a name="syntax"></a>Sintassi


```C++
void ASSERT(
   BOOL cond
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Cond* 
</dt> <dd>

Espressione da valutare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa macro non restituisce un valore.

## <a name="remarks"></a>Commenti

Nelle build di debug, se l'espressione è **FALSE,** questa macro visualizza una finestra di messaggio con il testo dell'espressione, il nome del file di origine e il numero di riga. L'utente può ignorare l'asserzione, immettere il debugger o uscire dall'applicazione.

## <a name="examples"></a>Esempio


```
ASSERT(rtStartTime <= rtEndTime);
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Wxdebug.h (includere Flussi.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Macro di asserzione e punto di interruzione](assert-and-breakpoint-macros.md)
</dt> </dl>

 

 




