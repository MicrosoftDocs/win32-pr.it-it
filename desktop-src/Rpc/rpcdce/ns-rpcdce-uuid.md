---
title: UUID
description: Fornisce una designazione univoca di un oggetto, ad esempio un'interfaccia, un vettore del punto di ingresso di gestione o un oggetto client.
ms.localizationpriority: low
ms.topic: reference
ms.date: 09/09/2019
ms.openlocfilehash: 31ff8eb22a234020e0da5b5ebb5799d5ddb0c8d1dca7bc094394f79a5ceb0c0a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118925948"
---
# <a name="uuid-structure"></a>Struttura UUID

La **struttura UUID** definisce un UUID (Universally Unique Identifier). Un **UUID fornisce** una designazione univoca di un oggetto, ad esempio un'interfaccia, un vettore del punto di ingresso di gestione o un oggetto client.

La **struttura UUID** è un sinonimo di `typedef` "d" per la [struttura GUID.](/windows/win32/api/guiddef/ns-guiddef-guid)

## <a name="syntax"></a>Sintassi

```cpp
typedef GUID UUID;
```

## <a name="remarks"></a>Osservazioni

Le librerie di runtime RPC usano **UUID** per verificare la compatibilità tra client e server e per selezionare tra più implementazioni di un'interfaccia.

## <a name="requirements"></a>Requisiti

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Intestazione** | Definito in rpcdce.h; include rpc.h |

## <a name="see-also"></a>Vedi anche

[GUID](/windows/win32/api/guiddef/ns-guiddef-guid) 
 [UUID \_ VETTORE](/windows/win32/api/rpcdce/ns-rpcdce-uuid_vector)