---
title: ODJ_PROVISION_DATA
description: ODJ_PROVISION_DATA definizione IDL
ms.assetid: ff623d04-ad3f-4846-b9de-aaa280713018
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: 02762a80be9bd60b7f9c8648c9bfb848f3d76184f249567c9e9522189692e0e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119064351"
---
# <a name="odj_provision_data-structure"></a>ODJ_PROVISION_DATA struttura

Specifica la struttura di serializzazione più esterna utilizzata dalle API di aggiunta a un dominio offline.

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

Punta a una matrice di ODJ_BLOB struttura .

## <a name="see-also"></a>Vedi anche

[**Definizioni IDL di aggiunta a un dominio offline**](odj-idl.md)

[**ODJ \_ BLOB**](odj-odj_blob.md)


