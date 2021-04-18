---
title: ODJ_UNICODE_STRING
description: Definizione di ODJ_UNICODE_STRING IDL
ms.assetid: a7999df0-d961-4fd7-ae5e-65ad79a9c17c
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: f1134d7b95cca6948932bf9d79fe976d6745448a
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/14/2020
ms.locfileid: "106300653"
---
# <a name="odj_unicode_string-structure"></a>Struttura ODJ_UNICODE_STRING

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

Deve essere impostato sul numero di byte nel buffer contenente la stringa, escluso il carattere di terminazione NULL.

### <a name="maximumlength"></a>MaximumLength

DEVE essere impostato sul numero totale di byte nel buffer, escluso il carattere di terminazione NULL.

### <a name="buffer"></a>Buffer

Deve essere una stringa Unicode.

## <a name="see-also"></a>Vedi anche

[**Definizioni IDL di aggiunta al dominio offline**](odj-idl.md)
