---
description: Specifica un oggetto da firmare.
ms.assetid: ba569443-e50f-450b-82cc-b7328f0ca25a
title: Struttura SIGNER_SUBJECT_INFO
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SIGNER_SUBJECT_INFO
api_type:
- NA
api_location: ''
ms.openlocfilehash: 05b5d780e50f8ea10fcf68cc90ae7092bbc2c473
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310936"
---
# <a name="signer_subject_info-structure"></a><span data-ttu-id="f3636-103">Struttura delle \_ informazioni sul soggetto del firmatario \_</span><span class="sxs-lookup"><span data-stu-id="f3636-103">SIGNER\_SUBJECT\_INFO structure</span></span>

<span data-ttu-id="f3636-104">La struttura delle **\_ \_ informazioni sul soggetto del firmatario** specifica un oggetto da firmare.</span><span class="sxs-lookup"><span data-stu-id="f3636-104">The **SIGNER\_SUBJECT\_INFO** structure specifies a subject to sign.</span></span>

> [!Note]  
> <span data-ttu-id="f3636-105">Questa struttura non è definita in alcun file di intestazione.</span><span class="sxs-lookup"><span data-stu-id="f3636-105">This structure is not defined in any header file.</span></span> <span data-ttu-id="f3636-106">Per usare questa struttura, è necessario definirla come illustrato in questo argomento.</span><span class="sxs-lookup"><span data-stu-id="f3636-106">To use this structure, you must define it yourself as shown in this topic.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="f3636-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f3636-107">Syntax</span></span>


```C++
typedef struct _SIGNER_SUBJECT_INFO {
  DWORD cbSize;
  DWORD *pdwIndex;
  DWORD dwSubjectChoice;
  union {
    SIGNER_FILE_INFO *pSignerFileInfo;
    SIGNER_BLOB_INFO *pSignerBlobInfo;
  };
} SIGNER_SUBJECT_INFO, *PSIGNER_SUBJECT_INFO;
```



## <a name="members"></a><span data-ttu-id="f3636-108">Members</span><span class="sxs-lookup"><span data-stu-id="f3636-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="f3636-109">**cbSize**</span><span class="sxs-lookup"><span data-stu-id="f3636-109">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="f3636-110">Dimensione, in byte, della struttura.</span><span class="sxs-lookup"><span data-stu-id="f3636-110">The size, in bytes, of the structure.</span></span>

</dd> <dt>

<span data-ttu-id="f3636-111">**pdwIndex**</span><span class="sxs-lookup"><span data-stu-id="f3636-111">**pdwIndex**</span></span>
</dt> <dd>

<span data-ttu-id="f3636-112">Questo membro è riservato.</span><span class="sxs-lookup"><span data-stu-id="f3636-112">This member is reserved.</span></span> <span data-ttu-id="f3636-113">Deve essere impostato su zero.</span><span class="sxs-lookup"><span data-stu-id="f3636-113">It must be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="f3636-114">**dwSubjectChoice**</span><span class="sxs-lookup"><span data-stu-id="f3636-114">**dwSubjectChoice**</span></span>
</dt> <dd>

<span data-ttu-id="f3636-115">Specifica se l'oggetto è un file o un [*BLOB*](../secgloss/b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="f3636-115">Specifies whether the subject is a file or a [*BLOB*](../secgloss/b-gly.md).</span></span> <span data-ttu-id="f3636-116">Il membro può essere costituito da uno o più dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="f3636-116">This member can be one or more of the following values.</span></span>



| <span data-ttu-id="f3636-117">Valore</span><span class="sxs-lookup"><span data-stu-id="f3636-117">Value</span></span>                                                                                                                                                                                                                                         | <span data-ttu-id="f3636-118">Significato</span><span class="sxs-lookup"><span data-stu-id="f3636-118">Meaning</span></span>                           |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------|
| <span id="SIGNER_SUBJECT_BLOB"></span><span id="signer_subject_blob"></span><dl> <span data-ttu-id="f3636-119"><dt>**\_ Firmatario OGGETTO \_ BLOB**</dt> <dt>2 (0x2)</dt></span><span class="sxs-lookup"><span data-stu-id="f3636-119"><dt>**SIGNER\_SUBJECT\_BLOB**</dt> <dt>2 (0x2)</dt></span></span> </dl> | <span data-ttu-id="f3636-120">Il soggetto è un BLOB.</span><span class="sxs-lookup"><span data-stu-id="f3636-120">The subject is a BLOB.</span></span><br/> |
| <span id="SIGNER_SUBJECT_FILE"></span><span id="signer_subject_file"></span><dl> <span data-ttu-id="f3636-121"><dt>**\_ Firmatario \_File oggetto**</dt> <dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="f3636-121"><dt>**SIGNER\_SUBJECT\_FILE**</dt> <dt>1 (0x1)</dt></span></span> </dl> | <span data-ttu-id="f3636-122">Il soggetto è un file.</span><span class="sxs-lookup"><span data-stu-id="f3636-122">The subject is a file.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="f3636-123">**pSignerFileInfo**</span><span class="sxs-lookup"><span data-stu-id="f3636-123">**pSignerFileInfo**</span></span>
</dt> <dd>

<span data-ttu-id="f3636-124">Puntatore a una struttura di [**\_ \_ informazioni sul file del firmatario**](signer-file-info.md) che specifica il file da firmare.</span><span class="sxs-lookup"><span data-stu-id="f3636-124">A pointer to a [**SIGNER\_FILE\_INFO**](signer-file-info.md) structure that specifies the file to sign.</span></span>

</dd> <dt>

<span data-ttu-id="f3636-125">**pSignerBlobInfo**</span><span class="sxs-lookup"><span data-stu-id="f3636-125">**pSignerBlobInfo**</span></span>
</dt> <dd>

<span data-ttu-id="f3636-126">Puntatore a una struttura di [**\_ \_ informazioni BLOB del firmatario**](signer-blob-info.md) che specifica il BLOB da firmare.</span><span class="sxs-lookup"><span data-stu-id="f3636-126">A pointer to a [**SIGNER\_BLOB\_INFO**](signer-blob-info.md) structure that specifies the BLOB to sign.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f3636-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f3636-127">Requirements</span></span>



| <span data-ttu-id="f3636-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="f3636-128">Requirement</span></span> | <span data-ttu-id="f3636-129">Valore</span><span class="sxs-lookup"><span data-stu-id="f3636-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f3636-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f3636-130">Minimum supported client</span></span><br/> | <span data-ttu-id="f3636-131">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="f3636-131">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="f3636-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f3636-132">Minimum supported server</span></span><br/> | <span data-ttu-id="f3636-133">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f3636-133">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f3636-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f3636-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3636-135">**SignerSign**</span><span class="sxs-lookup"><span data-stu-id="f3636-135">**SignerSign**</span></span>](signersign.md)
</dt> <dt>

[<span data-ttu-id="f3636-136">**SignerSignEx**</span><span class="sxs-lookup"><span data-stu-id="f3636-136">**SignerSignEx**</span></span>](signersignex.md)
</dt> </dl>

 

 
