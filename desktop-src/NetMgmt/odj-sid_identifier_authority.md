---
title: SID_IDENTIFIER_AUTHORITY
description: SID_IDENTIFIER_AUTHORITY definizione IDL
ms.assetid: 88fe41f4-1c67-4290-ac21-fd43ff12d825
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: 8d2ac3b8763026c0aea31214169ff8a0e2c6260086456c8c7c2431f69b13b2d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117796879"
---
# <a name="sid_identifier_authority-structure"></a>SID_IDENTIFIER_AUTHORITY struttura

Contiene un'autorità identificatore SID.

## <a name="syntax"></a>Sintassi

```C++
typedef struct _SID_IDENTIFIER_AUTHORITY
{
    UCHAR Value[6];
} SID_IDENTIFIER_AUTHORITY, *PSID_IDENTIFIER_AUTHORITY;
```

## <a name="members"></a>Members

### <a name="value"></a>Valore

Deve essere impostato su sei byte dell'autorità identificatore SID.

## <a name="see-also"></a>Vedi anche

[**Definizioni IDL di aggiunta a un dominio offline**](odj-idl.md)