---
title: ODJ_UNICODE_STRING
description: ODJ_UNICODE_STRING definizione IDL
ms.assetid: a7999df0-d961-4fd7-ae5e-65ad79a9c17c
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: 3578c62f110eafd053ed97bbe1f8b5015156d02c4b879ff8111ff13f28dfab33
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119891240"
---
# <a name="odj_unicode_string-structure"></a>ODJ_UNICODE_STRING struttura

Contiene una stringa Unicode.

## <a name="syntax"></a>Sintassi

```C++
typedef struct _ODJ_UNICODE_STRING
{
    USHORT Length;
    USHORT MaximumLength;
    [size_is(MaximumLength/2), length_is(Length/2)] PWSTR Buffer;
} ODJ_UNICODE_STRING, *PODJ_UNICODE_STRING;
```

## <a name="members"></a>Members

### <a name="length"></a>Length

Deve essere impostato sul numero di byte nel buffer contenente la stringa, senza includere il carattere di terminazione NULL.

### <a name="maximumlength"></a>MaximumLength

Deve essere impostato sul numero totale di byte nel buffer, senza includere il carattere di terminazione NULL.

### <a name="buffer"></a>Buffer

Deve essere una stringa Unicode.

## <a name="see-also"></a>Vedi anche

[**Definizioni IDL di aggiunta a un dominio offline**](odj-idl.md)
