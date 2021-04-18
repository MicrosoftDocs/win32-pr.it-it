---
description: La \_ struttura BLOB KEYSVC definisce un BLOB del servizio Key. Questa struttura viene utilizzata dalla funzione RKeyPFXInstall.
ms.assetid: 255b5fab-6271-4d3f-9c56-a63278b8b104
title: Struttura KEYSVC_BLOB (Rkeysvcc. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KEYSVC_BLOB
api_type:
- HeaderDef
api_location:
- Rkeysvcc.h
ms.openlocfilehash: 801be5f5a0d431f488da6e13e1f3082d147c5974
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319353"
---
# <a name="keysvc_blob-structure"></a><span data-ttu-id="6eb6e-104">\_Struttura BLOB KEYSVC</span><span class="sxs-lookup"><span data-stu-id="6eb6e-104">KEYSVC\_BLOB structure</span></span>

<span data-ttu-id="6eb6e-105">La **struttura \_ BLOB KEYSVC** definisce un BLOB del servizio Key.</span><span class="sxs-lookup"><span data-stu-id="6eb6e-105">The **KEYSVC\_BLOB** structure defines a key service BLOB.</span></span> <span data-ttu-id="6eb6e-106">Questa struttura viene utilizzata dalla funzione [**RKeyPFXInstall**](rkeypfxinstall.md) .</span><span class="sxs-lookup"><span data-stu-id="6eb6e-106">This structure is used by the [**RKeyPFXInstall**](rkeypfxinstall.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="6eb6e-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6eb6e-107">Syntax</span></span>


```C++
typedef struct _KEYSVC_BLOB {
  ULONG cb;
  BYTE  *pb;
} KEYSVC_BLOB, *PKEYSVC_BLOB;
```



## <a name="members"></a><span data-ttu-id="6eb6e-108">Members</span><span class="sxs-lookup"><span data-stu-id="6eb6e-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="6eb6e-109">**CB**</span><span class="sxs-lookup"><span data-stu-id="6eb6e-109">**cb**</span></span>
</dt> <dd>

<span data-ttu-id="6eb6e-110">Valore **ULONG** che specifica la dimensione, in byte, del **PB**.</span><span class="sxs-lookup"><span data-stu-id="6eb6e-110">A **ULONG** value that specifies the size, in bytes, of **pb**.</span></span>

</dd> <dt>

<span data-ttu-id="6eb6e-111">**PB**</span><span class="sxs-lookup"><span data-stu-id="6eb6e-111">**pb**</span></span>
</dt> <dd>

<span data-ttu-id="6eb6e-112">Puntatore a un **byte** che contiene il BLOB, in formato [*PKCS \# 12*](../secgloss/p-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="6eb6e-112">A pointer to a **BYTE** that contains the BLOB, in [*PKCS \#12*](../secgloss/p-gly.md) format.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6eb6e-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6eb6e-113">Requirements</span></span>



| <span data-ttu-id="6eb6e-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="6eb6e-114">Requirement</span></span> | <span data-ttu-id="6eb6e-115">Valore</span><span class="sxs-lookup"><span data-stu-id="6eb6e-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6eb6e-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6eb6e-116">Minimum supported client</span></span><br/> | <span data-ttu-id="6eb6e-117">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="6eb6e-117">None supported</span></span><br/>                                                             |
| <span data-ttu-id="6eb6e-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6eb6e-118">Minimum supported server</span></span><br/> | <span data-ttu-id="6eb6e-119">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="6eb6e-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6eb6e-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6eb6e-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="6eb6e-121"><dt>Rkeysvcc. h</dt></span><span class="sxs-lookup"><span data-stu-id="6eb6e-121"><dt>Rkeysvcc.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6eb6e-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6eb6e-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6eb6e-123">**RKeyPFXInstall**</span><span class="sxs-lookup"><span data-stu-id="6eb6e-123">**RKeyPFXInstall**</span></span>](rkeypfxinstall.md)
</dt> <dt>

[<span data-ttu-id="6eb6e-124">**\_stringa Unicode \_ KEYSVC**</span><span class="sxs-lookup"><span data-stu-id="6eb6e-124">**KEYSVC\_UNICODE\_STRING**</span></span>](keysvc-unicode-string.md)
</dt> </dl>

 

 
