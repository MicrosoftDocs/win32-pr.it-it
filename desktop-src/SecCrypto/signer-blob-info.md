---
description: Specifica un BLOB da firmare.
ms.assetid: 214c9c05-5c95-4803-8993-23a87266f991
title: Struttura SIGNER_BLOB_INFO
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SIGNER_BLOB_INFO
api_type:
- NA
api_location: ''
ms.openlocfilehash: a05e99cc4d7fa2eff196159bb449fa7dbfbf3026
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530289"
---
# <a name="signer_blob_info-structure"></a><span data-ttu-id="d932e-103">Struttura di \_ informazioni BLOB del firmatario \_</span><span class="sxs-lookup"><span data-stu-id="d932e-103">SIGNER\_BLOB\_INFO structure</span></span>

<span data-ttu-id="d932e-104">\[La struttura delle **\_ \_ informazioni BLOB del firmatario** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="d932e-104">\[The **SIGNER\_BLOB\_INFO** structure is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="d932e-105">È possibile che in versioni successive sia stata modificata o non sia più disponibile.\]</span><span class="sxs-lookup"><span data-stu-id="d932e-105">It may be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="d932e-106">La struttura di **\_ \_ informazioni BLOB del firmatario** specifica un [*BLOB*](../secgloss/b-gly.md) da firmare.</span><span class="sxs-lookup"><span data-stu-id="d932e-106">The **SIGNER\_BLOB\_INFO** structure specifies a [*BLOB*](../secgloss/b-gly.md) to sign.</span></span>

> [!Note]  
> <span data-ttu-id="d932e-107">Questa struttura non è definita in alcun file di intestazione.</span><span class="sxs-lookup"><span data-stu-id="d932e-107">This structure is not defined in any header file.</span></span> <span data-ttu-id="d932e-108">Per usare questa struttura, è necessario definirla come illustrato in questo argomento.</span><span class="sxs-lookup"><span data-stu-id="d932e-108">To use this structure, you must define it yourself as shown in this topic.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="d932e-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d932e-109">Syntax</span></span>


```C++
typedef struct _SIGNER_BLOB_INFO {
  DWORD   cbSize;
  GUID    *pGuidSubject;
  DWORD   cbBlob;
  BYTE    *pbBlob;
  LPCWSTR pwszDisplayName;
} SIGNER_BLOB_INFO, *PSIGNER_BLOB_INFO;
```



## <a name="members"></a><span data-ttu-id="d932e-110">Members</span><span class="sxs-lookup"><span data-stu-id="d932e-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="d932e-111">**cbSize**</span><span class="sxs-lookup"><span data-stu-id="d932e-111">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="d932e-112">Dimensione, in byte, della struttura.</span><span class="sxs-lookup"><span data-stu-id="d932e-112">The size, in bytes, of the structure.</span></span>

</dd> <dt>

<span data-ttu-id="d932e-113">**pGuidSubject**</span><span class="sxs-lookup"><span data-stu-id="d932e-113">**pGuidSubject**</span></span>
</dt> <dd>

<span data-ttu-id="d932e-114">Puntatore a un **GUID** che specifica il SIP (Subject Interface Package) da caricare.</span><span class="sxs-lookup"><span data-stu-id="d932e-114">A pointer to a **GUID** that specifies the Subject Interface Package (SIP) to load.</span></span>

</dd> <dt>

<span data-ttu-id="d932e-115">**cbBlob**</span><span class="sxs-lookup"><span data-stu-id="d932e-115">**cbBlob**</span></span>
</dt> <dd>

<span data-ttu-id="d932e-116">Dimensione, in byte, del BLOB da firmare.</span><span class="sxs-lookup"><span data-stu-id="d932e-116">The size, in bytes, of the BLOB to sign.</span></span>

</dd> <dt>

<span data-ttu-id="d932e-117">**pbBlob**</span><span class="sxs-lookup"><span data-stu-id="d932e-117">**pbBlob**</span></span>
</dt> <dd>

<span data-ttu-id="d932e-118">Puntatore al BLOB da firmare.</span><span class="sxs-lookup"><span data-stu-id="d932e-118">A pointer to the BLOB to sign.</span></span>

</dd> <dt>

<span data-ttu-id="d932e-119">**pwszDisplayName**</span><span class="sxs-lookup"><span data-stu-id="d932e-119">**pwszDisplayName**</span></span>
</dt> <dd>

<span data-ttu-id="d932e-120">Nome visualizzato del BLOB.</span><span class="sxs-lookup"><span data-stu-id="d932e-120">The display name of the BLOB.</span></span> <span data-ttu-id="d932e-121">Questo membro può essere impostato su **null**.</span><span class="sxs-lookup"><span data-stu-id="d932e-121">This member can be set to **NULL**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d932e-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d932e-122">Requirements</span></span>



| <span data-ttu-id="d932e-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="d932e-123">Requirement</span></span> | <span data-ttu-id="d932e-124">Valore</span><span class="sxs-lookup"><span data-stu-id="d932e-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="d932e-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d932e-125">Minimum supported client</span></span><br/> | <span data-ttu-id="d932e-126">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="d932e-126">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="d932e-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d932e-127">Minimum supported server</span></span><br/> | <span data-ttu-id="d932e-128">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d932e-128">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d932e-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d932e-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d932e-130">**informazioni sul soggetto del FIRMATARIo \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d932e-130">**SIGNER\_SUBJECT\_INFO**</span></span>](signer-subject-info.md)
</dt> </dl>

 

 
