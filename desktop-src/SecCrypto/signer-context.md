---
description: Contiene un BLOB firmato.
ms.assetid: c12d9007-c779-4363-8e28-6387a665a0d6
title: Struttura SIGNER_CONTEXT
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SIGNER_CONTEXT
api_type:
- NA
api_location: ''
ms.openlocfilehash: 4ebc7d5380438fc6cd28a43136273387c1919713
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317694"
---
# <a name="signer_context-structure"></a><span data-ttu-id="7b47d-103">Struttura del contesto del FIRMATARIo \_</span><span class="sxs-lookup"><span data-stu-id="7b47d-103">SIGNER\_CONTEXT structure</span></span>

<span data-ttu-id="7b47d-104">La struttura del **\_ contesto del firmatario** contiene un [*BLOB*](../secgloss/b-gly.md)firmato.</span><span class="sxs-lookup"><span data-stu-id="7b47d-104">The **SIGNER\_CONTEXT** structure contains a signed [*BLOB*](../secgloss/b-gly.md).</span></span>

> [!Note]  
> <span data-ttu-id="7b47d-105">Questa struttura non è definita in alcun file di intestazione.</span><span class="sxs-lookup"><span data-stu-id="7b47d-105">This structure is not defined in any header file.</span></span> <span data-ttu-id="7b47d-106">Per usare questa struttura, è necessario definirla come illustrato in questo argomento.</span><span class="sxs-lookup"><span data-stu-id="7b47d-106">To use this structure, you must define it yourself as shown in this topic.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="7b47d-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7b47d-107">Syntax</span></span>


```C++
typedef struct _SIGNER_CONTEXT {
  DWORD cbSize;
  DWORD cbBlob;
  BYTE  *pbBlob;
} SIGNER_CONTEXT, *PSIGNER_CONTEXT;
```



## <a name="members"></a><span data-ttu-id="7b47d-108">Members</span><span class="sxs-lookup"><span data-stu-id="7b47d-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="7b47d-109">**cbSize**</span><span class="sxs-lookup"><span data-stu-id="7b47d-109">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="7b47d-110">Dimensione, in byte, della struttura.</span><span class="sxs-lookup"><span data-stu-id="7b47d-110">The size, in bytes, of the structure.</span></span>

</dd> <dt>

<span data-ttu-id="7b47d-111">**cbBlob**</span><span class="sxs-lookup"><span data-stu-id="7b47d-111">**cbBlob**</span></span>
</dt> <dd>

<span data-ttu-id="7b47d-112">Dimensione, in byte, del membro **pbBlob** .</span><span class="sxs-lookup"><span data-stu-id="7b47d-112">The size, in bytes, of the **pbBlob** member.</span></span>

</dd> <dt>

<span data-ttu-id="7b47d-113">**pbBlob**</span><span class="sxs-lookup"><span data-stu-id="7b47d-113">**pbBlob**</span></span>
</dt> <dd>

<span data-ttu-id="7b47d-114">Puntatore al BLOB firmato.</span><span class="sxs-lookup"><span data-stu-id="7b47d-114">A pointer to the signed BLOB.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7b47d-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7b47d-115">Requirements</span></span>



| <span data-ttu-id="7b47d-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="7b47d-116">Requirement</span></span> | <span data-ttu-id="7b47d-117">Valore</span><span class="sxs-lookup"><span data-stu-id="7b47d-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="7b47d-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7b47d-118">Minimum supported client</span></span><br/> | <span data-ttu-id="7b47d-119">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="7b47d-119">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="7b47d-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7b47d-120">Minimum supported server</span></span><br/> | <span data-ttu-id="7b47d-121">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="7b47d-121">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7b47d-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7b47d-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b47d-123">**SignerSign**</span><span class="sxs-lookup"><span data-stu-id="7b47d-123">**SignerSign**</span></span>](signersign.md)
</dt> <dt>

[<span data-ttu-id="7b47d-124">**SignerSignEx**</span><span class="sxs-lookup"><span data-stu-id="7b47d-124">**SignerSignEx**</span></span>](signersignex.md)
</dt> </dl>

 

 
