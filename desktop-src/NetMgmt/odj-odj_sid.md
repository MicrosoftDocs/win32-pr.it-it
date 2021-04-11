---
title: ODJ_SID
description: Definizione di ODJ_SID IDL
ms.assetid: 1d06f725-6cd4-42cf-b171-c78a095690cb
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: dd51f2e8a54eaf5be566e5a25f013ca1d87b9341
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/14/2020
ms.locfileid: "104047551"
---
# <a name="odj_sid-structure"></a>Struttura ODJ_SID

Contiene un ID di sicurezza (SID).

## <a name="syntax"></a>Sintassi

```C++
typedef struct _ODJ_SID
{
    UCHAR Revision;
    UCHAR SubAuthorityCount;
    SID_IDENTIFIER_AUTHORITY IdentifierAuthority;
    [size_is(SubAuthorityCount)] ULONG SubAuthority[*];
}   ODJ_SID, *PODJ_SID;
```

## <a name="members"></a>Members

### <a name="revision"></a>Revisione

Deve essere impostato sulla revisione SID.

### <a name="subauthoritycount"></a>SubAuthorityCount

Deve essere impostato sul numero di elementi nella sottoautorizzazione.

### <a name="identifierauthority"></a>IdentifierAuthority

Deve essere impostato sull'identificatore dell'autorità SID.

### <a name="subauthority"></a>SubAuthority

Deve contenere una matrice di sottoautorità SID.

## <a name="see-also"></a>Vedi anche

[**Definizioni IDL di aggiunta al dominio offline**](odj-idl.md)

[**\_ \_ autorità identificatore SID \_ ODJ**](odj-sid_identifier_authority.md)
