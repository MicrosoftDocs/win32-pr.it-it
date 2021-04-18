---
title: ODJ_PROVISION_DATA
description: Definizione di ODJ_PROVISION_DATA IDL
ms.assetid: ff623d04-ad3f-4846-b9de-aaa280713018
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: f07d8c200103fa21afc080c60157645fe6730766
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/14/2020
ms.locfileid: "106300656"
---
# <a name="odj_provision_data-structure"></a>Struttura ODJ_PROVISION_DATA

Specifica la struttura di serializzazione più esterna utilizzata dalle API di aggiunta al dominio offline.

## <a name="syntax"></a>Sintassi

```C++
typedef struct _ODJ_PROVISION_DATA
{
    ULONG ulVersion;
    ULONG ulcBlobs;
    [size_is(ulcBlobs)] PODJ_BLOB pBlobs;
} ODJ_PROVISION_DATA;
```

## <a name="members"></a>Members

### <a name="ulversion"></a>ulVersion

Deve essere impostato su 1.

### <a name="ulcblobs"></a>ulcBlobs

Deve essere impostato sul numero di elementi nella matrice pBlobs.

### <a name="pblobs"></a>pBlobs

Punta a una matrice di strutture di ODJ_BLOB.

## <a name="see-also"></a>Vedi anche

[**Definizioni IDL di aggiunta al dominio offline**](odj-idl.md)

[**\_BLOB ODJ**](odj-odj_blob.md)


