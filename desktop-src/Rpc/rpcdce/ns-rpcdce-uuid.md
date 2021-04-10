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
# <a name="uuid-structure"></a><span data-ttu-id="e455d-103">UUID (struttura)</span><span class="sxs-lookup"><span data-stu-id="e455d-103">UUID structure</span></span>

<span data-ttu-id="e455d-104">La struttura **UUID** definisce un identificatore univoco universale (UUID).</span><span class="sxs-lookup"><span data-stu-id="e455d-104">The **UUID** structure defines a Universally Unique Identifier (UUID).</span></span> <span data-ttu-id="e455d-105">Un **UUID** fornisce una designazione univoca di un oggetto, ad esempio un'interfaccia, un vettore del punto di ingresso di gestione o un oggetto client.</span><span class="sxs-lookup"><span data-stu-id="e455d-105">A **UUID** provides a unique designation of an object such as an interface, a manager entry-point vector, or a client object.</span></span>

<span data-ttu-id="e455d-106">La struttura **UUID** è un `typedef` sinonimo della struttura [GUID](/windows/win32/api/guiddef/ns-guiddef-guid) .</span><span class="sxs-lookup"><span data-stu-id="e455d-106">The **UUID** structure is a `typedef`'d synonym for the [GUID](/windows/win32/api/guiddef/ns-guiddef-guid) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="e455d-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e455d-107">Syntax</span></span>

```cpp
typedef GUID UUID;
```

## <a name="remarks"></a><span data-ttu-id="e455d-108">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="e455d-108">Remarks</span></span>

<span data-ttu-id="e455d-109">Le librerie di runtime RPC utilizzano **UUID** s per verificare la compatibilità tra client e server e per scegliere tra più implementazioni di un'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="e455d-109">The RPC run-time libraries use **UUID** s to check for compatibility between clients and servers, and to select among multiple implementations of an interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="e455d-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e455d-110">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="e455d-111">**Intestazione**</span><span class="sxs-lookup"><span data-stu-id="e455d-111">**Header**</span></span> | <span data-ttu-id="e455d-112">Definito in rpcdce. h; Includi RPC. h</span><span class="sxs-lookup"><span data-stu-id="e455d-112">Defined in rpcdce.h; include rpc.h</span></span> |

## <a name="see-also"></a><span data-ttu-id="e455d-113">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e455d-113">See also</span></span>

<span data-ttu-id="e455d-114">[GUID](/windows/win32/api/guiddef/ns-guiddef-guid) 
 [UUID \_ VETTORE](/windows/win32/api/rpcdce/ns-rpcdce-uuid_vector) di</span><span class="sxs-lookup"><span data-stu-id="e455d-114">[GUID](/windows/win32/api/guiddef/ns-guiddef-guid)
[UUID\_VECTOR](/windows/win32/api/rpcdce/ns-rpcdce-uuid_vector)</span></span>