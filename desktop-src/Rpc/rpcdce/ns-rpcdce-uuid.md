---
title: UUID
description: Fornisce una designazione univoca di un oggetto, ad esempio un'interfaccia, un vettore del punto di ingresso di gestione o un oggetto client.
ms.localizationpriority: low
ms.topic: reference
ms.date: 09/09/2019
ms.openlocfilehash: 95d2d420502a5d92af64c902ffa82c709639d872
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104117177"
---
# <a name="uuid-structure"></a>UUID (struttura)

La struttura **UUID** definisce un identificatore univoco universale (UUID). Un **UUID** fornisce una designazione univoca di un oggetto, ad esempio un'interfaccia, un vettore del punto di ingresso di gestione o un oggetto client.

La struttura **UUID** è un `typedef` sinonimo della struttura [GUID](/windows/win32/api/guiddef/ns-guiddef-guid) .

## <a name="syntax"></a>Sintassi

```cpp
typedef GUID UUID;
```

## <a name="remarks"></a>Osservazioni

Le librerie di runtime RPC utilizzano **UUID** s per verificare la compatibilità tra client e server e per scegliere tra più implementazioni di un'interfaccia.

## <a name="requirements"></a>Requisiti

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Intestazione** | Definito in rpcdce. h; Includi RPC. h |

## <a name="see-also"></a>Vedi anche

[GUID](/windows/win32/api/guiddef/ns-guiddef-guid) 
 [UUID \_ VETTORE](/windows/win32/api/rpcdce/ns-rpcdce-uuid_vector) di