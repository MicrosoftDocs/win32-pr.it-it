---
description: Contiene una firma dell'elenco di revoche globale (GRL).
ms.assetid: 388a901c-6202-41cf-9c3d-f29d8ccca76b
title: Struttura MF_SIGNATURE
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MF_SIGNATURE
api_type:
- NA
api_location: ''
ms.openlocfilehash: 4827fea8e4259609cbb54f2b58a3d1c88ad6c23e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233621"
---
# <a name="mf_signature-structure"></a><span data-ttu-id="f9f8a-103">\_Struttura della firma MF</span><span class="sxs-lookup"><span data-stu-id="f9f8a-103">MF\_SIGNATURE structure</span></span>

<span data-ttu-id="f9f8a-104">Contiene una firma dell'elenco di revoche globale (GRL).</span><span class="sxs-lookup"><span data-stu-id="f9f8a-104">Contains a global revocation list (GRL) signature.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9f8a-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f9f8a-105">Syntax</span></span>


```C++
typedef struct _MF_SIGNATURE {
  DWORD dwSignVer;
  DWORD cbSign;
  BYTE  rgSign[1];
} MF_SIGNATURE;
```



## <a name="members"></a><span data-ttu-id="f9f8a-106">Members</span><span class="sxs-lookup"><span data-stu-id="f9f8a-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="f9f8a-107">**dwSignVer**</span><span class="sxs-lookup"><span data-stu-id="f9f8a-107">**dwSignVer**</span></span>
</dt> <dd>

<span data-ttu-id="f9f8a-108">Numero di versione della firma.</span><span class="sxs-lookup"><span data-stu-id="f9f8a-108">The signature version number.</span></span>

</dd> <dt>

<span data-ttu-id="f9f8a-109">**cbSign**</span><span class="sxs-lookup"><span data-stu-id="f9f8a-109">**cbSign**</span></span>
</dt> <dd>

<span data-ttu-id="f9f8a-110">Dimensioni in byte della firma.</span><span class="sxs-lookup"><span data-stu-id="f9f8a-110">The size of the signature in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="f9f8a-111">**rgSign**</span><span class="sxs-lookup"><span data-stu-id="f9f8a-111">**rgSign**</span></span>
</dt> <dd>

<span data-ttu-id="f9f8a-112">Matrice di byte di dimensioni **cbSign** che contiene la firma.</span><span class="sxs-lookup"><span data-stu-id="f9f8a-112">A byte array of size **cbSign** that contains the signature.</span></span> <span data-ttu-id="f9f8a-113">La dimensione effettiva della matrice è maggiore delle dimensioni specificate nella dichiarazione della struttura.</span><span class="sxs-lookup"><span data-stu-id="f9f8a-113">The actual array size is larger than the size given in the structure declaration.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f9f8a-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="f9f8a-114">Remarks</span></span>

<span data-ttu-id="f9f8a-115">Questa struttura non è dichiarata in un'intestazione SDK.</span><span class="sxs-lookup"><span data-stu-id="f9f8a-115">This structure is not declared in an SDK header.</span></span> <span data-ttu-id="f9f8a-116">Per usare questa struttura, aggiungere la dichiarazione mostrata qui al codice sorgente.</span><span class="sxs-lookup"><span data-stu-id="f9f8a-116">To use this structure, add the declaration shown here to your source code.</span></span>

## <a name="requirements"></a><span data-ttu-id="f9f8a-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f9f8a-117">Requirements</span></span>



| <span data-ttu-id="f9f8a-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="f9f8a-118">Requirement</span></span> | <span data-ttu-id="f9f8a-119">Valore</span><span class="sxs-lookup"><span data-stu-id="f9f8a-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f9f8a-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f9f8a-120">Minimum supported client</span></span><br/> | <span data-ttu-id="f9f8a-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f9f8a-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="f9f8a-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f9f8a-122">Minimum supported server</span></span><br/> | <span data-ttu-id="f9f8a-123">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f9f8a-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f9f8a-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f9f8a-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9f8a-125">Revoca del certificato OPM</span><span class="sxs-lookup"><span data-stu-id="f9f8a-125">OPM Certificate Revocation</span></span>](opm-certificate-revocation.md)
</dt> <dt>

[<span data-ttu-id="f9f8a-126">Strutture OPM</span><span class="sxs-lookup"><span data-stu-id="f9f8a-126">OPM Structures</span></span>](opm-structures.md)
</dt> </dl>

 

 




