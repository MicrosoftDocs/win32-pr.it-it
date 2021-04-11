---
title: SID_IDENTIFIER_AUTHORITY
description: Definizione di SID_IDENTIFIER_AUTHORITY IDL
ms.assetid: 88fe41f4-1c67-4290-ac21-fd43ff12d825
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: d9a80ed0717a279f39ac7a105a95807911232c82
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/14/2020
ms.locfileid: "104118634"
---
# <a name="sid_identifier_authority-structure"></a>Struttura SID_IDENTIFIER_AUTHORITY

Contiene un'autorità di identificazione SID.

## <a name="syntax"></a>Sintassi

```C++
typedef struct _SID_IDENTIFIER_AUTHORITY
{
    UCHAR Value[6];
} SID_IDENTIFIER_AUTHORITY, *PSID_IDENTIFIER_AUTHORITY;
```

## <a name="members"></a>Members

### <a name="value"></a>Valore

Deve essere impostato sui sei byte dell'autorità di identificazione SID.

## <a name="see-also"></a>Vedi anche

[**Definizioni IDL di aggiunta al dominio offline**](odj-idl.md)