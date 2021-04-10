---
description: Contiene informazioni su una firma digitale.
ms.assetid: 0b86fdf9-533f-4640-8c70-c3c8f4ef2c68
title: Struttura SIGNER_SIGNATURE_INFO
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SIGNER_SIGNATURE_INFO
api_type:
- NA
api_location: ''
ms.openlocfilehash: 8e2b1fa68da51a649a01d4356ebfb1519ceeffb4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104231707"
---
# <a name="signer_signature_info-structure"></a><span data-ttu-id="993cd-103">Struttura delle \_ informazioni sulla firma del firmatario \_</span><span class="sxs-lookup"><span data-stu-id="993cd-103">SIGNER\_SIGNATURE\_INFO structure</span></span>

<span data-ttu-id="993cd-104">La struttura delle **\_ \_ informazioni sulla firma del firmatario** contiene informazioni su una firma digitale.</span><span class="sxs-lookup"><span data-stu-id="993cd-104">The **SIGNER\_SIGNATURE\_INFO** structure contains information about a digital signature.</span></span>

> [!Note]  
> <span data-ttu-id="993cd-105">Questa struttura non è definita in alcun file di intestazione.</span><span class="sxs-lookup"><span data-stu-id="993cd-105">This structure is not defined in any header file.</span></span> <span data-ttu-id="993cd-106">Per usare questa struttura, è necessario definirla come illustrato in questo argomento.</span><span class="sxs-lookup"><span data-stu-id="993cd-106">To use this structure, you must define it yourself as shown in this topic.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="993cd-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="993cd-107">Syntax</span></span>


```C++
typedef struct _SIGNER_SIGNATURE_INFO {
  DWORD             cbSize;
  ALG_ID            algidHash;
  DWORD             dwAttrChoice;
  union {
    SIGNER_ATTR_AUTHCODE *pAttrAuthcode;
  };
  PCRYPT_ATTRIBUTES psAuthenticated;
  PCRYPT_ATTRIBUTES psUnauthenticated;
} SIGNER_SIGNATURE_INFO, *PSIGNER_SIGNATURE_INFO;
```



## <a name="members"></a><span data-ttu-id="993cd-108">Members</span><span class="sxs-lookup"><span data-stu-id="993cd-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="993cd-109">**cbSize**</span><span class="sxs-lookup"><span data-stu-id="993cd-109">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="993cd-110">Dimensione, in byte, della struttura.</span><span class="sxs-lookup"><span data-stu-id="993cd-110">The size, in bytes, of the structure.</span></span>

</dd> <dt>

<span data-ttu-id="993cd-111">**algidHash**</span><span class="sxs-lookup"><span data-stu-id="993cd-111">**algidHash**</span></span>
</dt> <dd>

<span data-ttu-id="993cd-112">Algoritmo hash utilizzato per la firma digitale.</span><span class="sxs-lookup"><span data-stu-id="993cd-112">The hash algorithm used for the digital signature.</span></span>

</dd> <dt>

<span data-ttu-id="993cd-113">**dwAttrChoice**</span><span class="sxs-lookup"><span data-stu-id="993cd-113">**dwAttrChoice**</span></span>
</dt> <dd>

<span data-ttu-id="993cd-114">Specifica se la firma ha attributi [*Authenticode*](../secgloss/a-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="993cd-114">Specifies whether the signature has [*Authenticode*](../secgloss/a-gly.md) attributes.</span></span> <span data-ttu-id="993cd-115">Il membro può essere costituito da uno o più dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="993cd-115">This member can be one or more of the following values.</span></span>



| <span data-ttu-id="993cd-116">Valore</span><span class="sxs-lookup"><span data-stu-id="993cd-116">Value</span></span>                                                                                                                                                                                                                                      | <span data-ttu-id="993cd-117">Significato</span><span class="sxs-lookup"><span data-stu-id="993cd-117">Meaning</span></span>                                                                                                                                   |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SIGNER_AUTHCODE_ATTR"></span><span id="signer_authcode_attr"></span><dl> <span data-ttu-id="993cd-118"><dt>**\_ Firmatario AUTHCODE \_ attr**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="993cd-118"><dt>**SIGNER\_AUTHCODE\_ATTR**</dt> <dt>1</dt></span></span> </dl> | <span data-ttu-id="993cd-119">Firma con attributi [*Authenticode*](../secgloss/a-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="993cd-119">The signature has [*Authenticode*](../secgloss/a-gly.md) attributes.</span></span><br/>           |
| <span id="SIGNER_NO_ATTR"></span><span id="signer_no_attr"></span><dl> <span data-ttu-id="993cd-120"><dt>**\_ Firmatario Nessun \_ attr**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="993cd-120"><dt>**SIGNER\_NO\_ATTR**</dt> <dt>0</dt></span></span> </dl>                   | <span data-ttu-id="993cd-121">La firma non ha attributi [*Authenticode*](../secgloss/a-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="993cd-121">The signature does not have [*Authenticode*](../secgloss/a-gly.md) attributes.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="993cd-122">**pAttrAuthcode**</span><span class="sxs-lookup"><span data-stu-id="993cd-122">**pAttrAuthcode**</span></span>
</dt> <dd>

<span data-ttu-id="993cd-123">Specifica gli attributi per una firma [*Authenticode*](../secgloss/a-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="993cd-123">Specifies attributes for an [*Authenticode*](../secgloss/a-gly.md) signature.</span></span> <span data-ttu-id="993cd-124">Questo membro è obbligatorio se il valore del membro **dwAttrChoice** è **Signer \_ AUTHCODE \_ attr**.</span><span class="sxs-lookup"><span data-stu-id="993cd-124">This member is required if the value of the **dwAttrChoice** member is **SIGNER\_AUTHCODE\_ATTR**.</span></span>

</dd> <dt>

<span data-ttu-id="993cd-125">**psAuthenticated**</span><span class="sxs-lookup"><span data-stu-id="993cd-125">**psAuthenticated**</span></span>
</dt> <dd>

<span data-ttu-id="993cd-126">Attributi specificati dall'utente autenticati aggiunti alla firma digitale.</span><span class="sxs-lookup"><span data-stu-id="993cd-126">Authenticated user-supplied attributes added to the digital signature.</span></span>

</dd> <dt>

<span data-ttu-id="993cd-127">**psUnauthenticated**</span><span class="sxs-lookup"><span data-stu-id="993cd-127">**psUnauthenticated**</span></span>
</dt> <dd>

<span data-ttu-id="993cd-128">Attributi non autenticati specificati dall'utente aggiunti alla firma digitale.</span><span class="sxs-lookup"><span data-stu-id="993cd-128">Unauthenticated user-supplied attributes added to the digital signature.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="993cd-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="993cd-129">Requirements</span></span>



| <span data-ttu-id="993cd-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="993cd-130">Requirement</span></span> | <span data-ttu-id="993cd-131">Valore</span><span class="sxs-lookup"><span data-stu-id="993cd-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="993cd-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="993cd-132">Minimum supported client</span></span><br/> | <span data-ttu-id="993cd-133">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="993cd-133">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="993cd-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="993cd-134">Minimum supported server</span></span><br/> | <span data-ttu-id="993cd-135">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="993cd-135">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="993cd-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="993cd-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="993cd-137">**SignerSign**</span><span class="sxs-lookup"><span data-stu-id="993cd-137">**SignerSign**</span></span>](signersign.md)
</dt> <dt>

[<span data-ttu-id="993cd-138">**SignerSignEx**</span><span class="sxs-lookup"><span data-stu-id="993cd-138">**SignerSignEx**</span></span>](signersignex.md)
</dt> </dl>

 

 
