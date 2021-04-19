---
title: OP_PACKAGE
description: Definizione di OP_PACKAGE IDL
ms.assetid: 065266a6-6db5-4113-bd2b-22ac6063236d
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: 6220b3815ad6ff360af7255a91fc34d71125f38c
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/14/2020
ms.locfileid: "106300648"
---
# <a name="op_package-structure"></a><span data-ttu-id="906e2-103">Struttura OP_PACKAGE</span><span class="sxs-lookup"><span data-stu-id="906e2-103">OP_PACKAGE structure</span></span>

<span data-ttu-id="906e2-104">Contiene una struttura che contiene un OP_PACKAGE_COLLECTION serializzato.</span><span class="sxs-lookup"><span data-stu-id="906e2-104">Contains a structure that contains a serialized OP_PACKAGE_COLLECTION.</span></span>

## <a name="syntax"></a><span data-ttu-id="906e2-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="906e2-105">Syntax</span></span>

```C++
typedef struct _OP_PACKAGE
{
    GUID    EncryptionType;
    OP_BLOB EncryptionContext;
    OP_BLOB WrappedPartCollection;
    ULONG   cbDecryptedPartCollection;
    OP_BLOB Extension;
} OP_PACKAGE, *POP_PACKAGE;
```

## <a name="members"></a><span data-ttu-id="906e2-106">Members</span><span class="sxs-lookup"><span data-stu-id="906e2-106">Members</span></span>

### <a name="encryptiontype"></a><span data-ttu-id="906e2-107">EncryptionType</span><span class="sxs-lookup"><span data-stu-id="906e2-107">EncryptionType</span></span>

<span data-ttu-id="906e2-108">Riservato per utilizzi futuri e deve essere impostato su GUID_NULL.</span><span class="sxs-lookup"><span data-stu-id="906e2-108">Reserved for future use and MUST be set to GUID_NULL.</span></span>

### <a name="encryptioncontext"></a><span data-ttu-id="906e2-109">EncryptionContext</span><span class="sxs-lookup"><span data-stu-id="906e2-109">EncryptionContext</span></span>

<span data-ttu-id="906e2-110">Riservato per utilizzi futuri e deve essere impostato su tutti zeri.</span><span class="sxs-lookup"><span data-stu-id="906e2-110">Reserved for future use and MUST be set to all zeros.</span></span>

### <a name="wrappedpartcollection"></a><span data-ttu-id="906e2-111">WrappedPartCollection</span><span class="sxs-lookup"><span data-stu-id="906e2-111">WrappedPartCollection</span></span>

<span data-ttu-id="906e2-112">Struttura di OP_BLOB contenente una struttura OP_PACKAGE_COLLECTION serializzata.</span><span class="sxs-lookup"><span data-stu-id="906e2-112">An OP_BLOB structure that contains a serialized OP_PACKAGE_COLLECTION structure.</span></span>

### <a name="cbdecryptedpartcollection"></a><span data-ttu-id="906e2-113">cbDecryptedPartCollection</span><span class="sxs-lookup"><span data-stu-id="906e2-113">cbDecryptedPartCollection</span></span>

<span data-ttu-id="906e2-114">Riservato per utilizzi futuri e deve essere impostato su zero.</span><span class="sxs-lookup"><span data-stu-id="906e2-114">Reserved for future use and MUST be set to zero.</span></span>

### <a name="extension"></a><span data-ttu-id="906e2-115">Estensione</span><span class="sxs-lookup"><span data-stu-id="906e2-115">Extension</span></span>

<span data-ttu-id="906e2-116">Riservato per utilizzi futuri e deve essere impostato su tutti zeri.</span><span class="sxs-lookup"><span data-stu-id="906e2-116">Reserved for future use and MUST be set to all zeros.</span></span>

## <a name="see-also"></a><span data-ttu-id="906e2-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="906e2-117">See also</span></span>

[<span data-ttu-id="906e2-118">**Definizioni IDL di aggiunta al dominio offline**</span><span class="sxs-lookup"><span data-stu-id="906e2-118">**Offline Domain Join IDL Definitions**</span></span>](odj-idl.md)

[<span data-ttu-id="906e2-119">**\_BLOB op**</span><span class="sxs-lookup"><span data-stu-id="906e2-119">**OP\_BLOB**</span></span>](odj-op_blob.md)

[<span data-ttu-id="906e2-120">**\_raccolta pacchetti \_ op**</span><span class="sxs-lookup"><span data-stu-id="906e2-120">**OP\_PACKAGE\_COLLECTION**</span></span>](odj-op_package_collection.md)
