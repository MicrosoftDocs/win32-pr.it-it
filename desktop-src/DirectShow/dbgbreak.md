---
description: Visualizza una finestra di messaggio con la stringa specificata, il nome del file di origine e il numero di riga. L'utente può ignorare il messaggio, immettere il debugger o chiudere l'applicazione. Ignorato nelle compilazioni al dettaglio.
ms.assetid: ac4da7da-f9d0-44ae-9ad1-9a5908b288fb
title: Macro DbgBreak (Wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgBreak
api_type:
- HeaderDef
api_location:
- Wxdebug.h
ms.openlocfilehash: 099344a295de2657b40218b993ab9c4cb6411353
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332705"
---
# <a name="dbgbreak-macro"></a>DbgBreak (macro)

Visualizza una finestra di messaggio con la stringa specificata, il nome del file di origine e il numero di riga. L'utente può ignorare il messaggio, immettere il debugger o chiudere l'applicazione. Ignorato nelle compilazioni al dettaglio.

## <a name="syntax"></a>Sintassi


```C++
void DbgBreak(
    strLiteral
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*strLiteral* 
</dt> <dd>

Stringa di testo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa macro non restituisce un valore.

## <a name="examples"></a>Esempio


```C++
DbgBreak("Unrecoverable error occurred.");
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Wxdebug. h (include Streams. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Macro di asserzione e punti di interruzione](assert-and-breakpoint-macros.md)
</dt> </dl>

 

 




