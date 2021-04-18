---
description: Valuta un'espressione e visualizza un messaggio di diagnostica se l'espressione è FALSE. Ignorato nelle compilazioni al dettaglio.
ms.assetid: 8c3815bb-3164-4066-a947-974e791af5cd
title: Macro ASSERT (Wxdebug. h)
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
ms.openlocfilehash: 8617d1c86f655cc9b44ea6619931f73888ae2a67
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328275"
---
# <a name="assert-macro"></a>ASSERT (macro)

Valuta un'espressione e visualizza un messaggio di diagnostica se l'espressione è **false**. Ignorato nelle compilazioni al dettaglio.

## <a name="syntax"></a>Sintassi


```C++
void ASSERT(
   BOOL cond
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*cond* 
</dt> <dd>

Espressione da valutare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa macro non restituisce un valore.

## <a name="remarks"></a>Commenti

Nelle compilazioni di debug, se l'espressione è **false**, questa macro Visualizza una finestra di messaggio con il testo dell'espressione, il nome del file di origine e il numero di riga. L'utente può ignorare l'asserzione, immettere il debugger o chiudere l'applicazione.

## <a name="examples"></a>Esempio


```
ASSERT(rtStartTime <= rtEndTime);
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Wxdebug. h (include Streams. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Macro di asserzione e punti di interruzione](assert-and-breakpoint-macros.md)
</dt> </dl>

 

 




