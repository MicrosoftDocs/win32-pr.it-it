---
description: Specifica gli attributi per una firma Authenticode.
ms.assetid: 1c1052c3-c5c5-48ae-8266-0b367800a84a
title: Struttura SIGNER_ATTR_AUTHCODE
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SIGNER_ATTR_AUTHCODE
api_type:
- NA
api_location: ''
ms.openlocfilehash: 952ed0f55a185d9a7ef9eeed3366f64c84423ddd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968650"
---
# <a name="signer_attr_authcode-structure"></a><span data-ttu-id="d09f2-103">Struttura del FIRMATARIo \_ attr \_ AUTHCODE</span><span class="sxs-lookup"><span data-stu-id="d09f2-103">SIGNER\_ATTR\_AUTHCODE structure</span></span>

<span data-ttu-id="d09f2-104">La struttura del **firmatario \_ attr \_ AUTHCODE** specifica gli attributi per una firma [*Authenticode*](../secgloss/a-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="d09f2-104">The **SIGNER\_ATTR\_AUTHCODE** structure specifies attributes for an [*Authenticode*](../secgloss/a-gly.md) signature.</span></span>

> [!Note]  
> <span data-ttu-id="d09f2-105">Questa struttura non è definita in alcun file di intestazione.</span><span class="sxs-lookup"><span data-stu-id="d09f2-105">This structure is not defined in any header file.</span></span> <span data-ttu-id="d09f2-106">Per usare questa struttura, è necessario definirla come illustrato in questo argomento.</span><span class="sxs-lookup"><span data-stu-id="d09f2-106">To use this structure, you must define it yourself as shown in this topic.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="d09f2-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d09f2-107">Syntax</span></span>


```C++
typedef struct _SIGNER_ATTR_AUTHCODE {
  DWORD   cbSize;
  BOOL    fCommercial;
  BOOL    fIndividual;
  LPCWSTR pwszName;
  LPCWSTR pwszInfo;
} SIGNER_ATTR_AUTHCODE, *PSIGNER_ATTR_AUTHCODE;
```



## <a name="members"></a><span data-ttu-id="d09f2-108">Members</span><span class="sxs-lookup"><span data-stu-id="d09f2-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="d09f2-109">**cbSize**</span><span class="sxs-lookup"><span data-stu-id="d09f2-109">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="d09f2-110">Dimensione, in byte, della struttura.</span><span class="sxs-lookup"><span data-stu-id="d09f2-110">The size, in bytes, of the structure.</span></span>

</dd> <dt>

<span data-ttu-id="d09f2-111">**fCommercial**</span><span class="sxs-lookup"><span data-stu-id="d09f2-111">**fCommercial**</span></span>
</dt> <dd>

<span data-ttu-id="d09f2-112">**True** per firmare l'oggetto come server di pubblicazione commerciale; in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="d09f2-112">**TRUE** to sign the subject as a commercial publisher; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="d09f2-113">**fIndividual**</span><span class="sxs-lookup"><span data-stu-id="d09f2-113">**fIndividual**</span></span>
</dt> <dd>

<span data-ttu-id="d09f2-114">**True** per firmare l'oggetto come singolo editore; in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="d09f2-114">**TRUE** to sign the subject as an individual publisher; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="d09f2-115">**pwszName**</span><span class="sxs-lookup"><span data-stu-id="d09f2-115">**pwszName**</span></span>
</dt> <dd>

<span data-ttu-id="d09f2-116">Nome visualizzato del file dopo il download.</span><span class="sxs-lookup"><span data-stu-id="d09f2-116">The display name of the file upon download.</span></span>

</dd> <dt>

<span data-ttu-id="d09f2-117">**pwszInfo**</span><span class="sxs-lookup"><span data-stu-id="d09f2-117">**pwszInfo**</span></span>
</dt> <dd>

<span data-ttu-id="d09f2-118">Nome visualizzato dell'URL del file durante il download.</span><span class="sxs-lookup"><span data-stu-id="d09f2-118">The display name of the URL of the file upon download.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d09f2-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d09f2-119">Requirements</span></span>



| <span data-ttu-id="d09f2-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="d09f2-120">Requirement</span></span> | <span data-ttu-id="d09f2-121">Valore</span><span class="sxs-lookup"><span data-stu-id="d09f2-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="d09f2-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d09f2-122">Minimum supported client</span></span><br/> | <span data-ttu-id="d09f2-123">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="d09f2-123">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="d09f2-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d09f2-124">Minimum supported server</span></span><br/> | <span data-ttu-id="d09f2-125">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d09f2-125">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d09f2-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d09f2-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d09f2-127">**informazioni sulla firma del FIRMATARIo \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d09f2-127">**SIGNER\_SIGNATURE\_INFO**</span></span>](signer-signature-info.md)
</dt> </dl>

 

 
