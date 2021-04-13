---
title: OP_BLOB
description: Definizione di OP_BLOB IDL
ms.assetid: c215c793-5fad-4baa-97c0-c809040dda1e
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: fab6df11be3bf719f787c40a41a50d948a865474
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/14/2020
ms.locfileid: "104399881"
---
# <a name="op_blob-structure"></a><span data-ttu-id="b6146-103">Struttura OP_BLOB</span><span class="sxs-lookup"><span data-stu-id="b6146-103">OP_BLOB structure</span></span>

<span data-ttu-id="b6146-104">Contiene un buffer di byte opaco.</span><span class="sxs-lookup"><span data-stu-id="b6146-104">Contains an opaque byte buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6146-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b6146-105">Syntax</span></span>

```C++
typedef struct _OP_BLOB
{
    ULONG                       cbBlob;
    [size_is(cbBlob)]   PBYTE   pBlob;
} OP_BLOB, *POP_BLOB;
```

## <a name="members"></a><span data-ttu-id="b6146-106">Members</span><span class="sxs-lookup"><span data-stu-id="b6146-106">Members</span></span>

### <a name="cbblob"></a><span data-ttu-id="b6146-107">cbBlob</span><span class="sxs-lookup"><span data-stu-id="b6146-107">cbBlob</span></span>

<span data-ttu-id="b6146-108">Specifica la dimensione di pBlob in byte.</span><span class="sxs-lookup"><span data-stu-id="b6146-108">Specifies the the size of pBlob in bytes.</span></span>

### <a name="pblob"></a><span data-ttu-id="b6146-109">pBlob</span><span class="sxs-lookup"><span data-stu-id="b6146-109">pBlob</span></span>

<span data-ttu-id="b6146-110">Punta a un buffer di byte.</span><span class="sxs-lookup"><span data-stu-id="b6146-110">Points to a byte buffer.</span></span>

## <a name="see-also"></a><span data-ttu-id="b6146-111">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b6146-111">See also</span></span>

[<span data-ttu-id="b6146-112">**Definizioni IDL di aggiunta al dominio offline**</span><span class="sxs-lookup"><span data-stu-id="b6146-112">**Offline Domain Join IDL Definitions**</span></span>](odj-idl.md)
