---
description: La \_ \_ struttura di stringhe Unicode KEYSVC definisce una stringa Unicode e una lunghezza massima per la stringa. Questa struttura viene utilizzata dalla funzione RKeyPFXInstall.
ms.assetid: 12142543-5c53-4638-9fd7-f523594142c8
title: Struttura KEYSVC_UNICODE_STRING (Rkeysvcc. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KEYSVC_UNICODE_STRING
api_type:
- HeaderDef
api_location:
- Rkeysvcc.h
ms.openlocfilehash: 5424fa103b2bbbadd735dbda0bb92f9dea21787b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319352"
---
# <a name="keysvc_unicode_string-structure"></a><span data-ttu-id="f3e88-104">\_Struttura di \_ stringhe Unicode KEYSVC</span><span class="sxs-lookup"><span data-stu-id="f3e88-104">KEYSVC\_UNICODE\_STRING structure</span></span>

<span data-ttu-id="f3e88-105">La struttura di **\_ \_ stringhe Unicode KEYSVC** definisce una stringa [*Unicode*](../secgloss/u-gly.md) e una lunghezza massima per la stringa.</span><span class="sxs-lookup"><span data-stu-id="f3e88-105">The **KEYSVC\_UNICODE\_STRING** structure defines a [*Unicode*](../secgloss/u-gly.md) string and a maximum length for the string.</span></span> <span data-ttu-id="f3e88-106">Questa struttura viene utilizzata dalla funzione [**RKeyPFXInstall**](rkeypfxinstall.md) .</span><span class="sxs-lookup"><span data-stu-id="f3e88-106">This structure is used by the [**RKeyPFXInstall**](rkeypfxinstall.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3e88-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f3e88-107">Syntax</span></span>


```C++
typedef struct _KEYSVC_UNICODE_STRING {
  USHORT Length;
  USHORT MaximumLength;
  USHORT *Buffer;
} KEYSVC_UNICODE_STRING, *PKEYSVC_UNICODE_STRING;
```



## <a name="members"></a><span data-ttu-id="f3e88-108">Members</span><span class="sxs-lookup"><span data-stu-id="f3e88-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="f3e88-109">**Length**</span><span class="sxs-lookup"><span data-stu-id="f3e88-109">**Length**</span></span>
</dt> <dd>

<span data-ttu-id="f3e88-110">Valore **ushort** che specifica la lunghezza, in byte, utilizzata per il **buffer**.</span><span class="sxs-lookup"><span data-stu-id="f3e88-110">A **USHORT** value that specifies the length, in bytes, used for **Buffer**.</span></span>

</dd> <dt>

<span data-ttu-id="f3e88-111">**MaximumLength**</span><span class="sxs-lookup"><span data-stu-id="f3e88-111">**MaximumLength**</span></span>
</dt> <dd>

<span data-ttu-id="f3e88-112">Valore **ushort** che specifica la lunghezza massima, in byte, consentita per il **buffer**.</span><span class="sxs-lookup"><span data-stu-id="f3e88-112">A **USHORT** value that specifies the maximum length, in bytes, allowed for **Buffer**.</span></span>

</dd> <dt>

<span data-ttu-id="f3e88-113">**Buffer**</span><span class="sxs-lookup"><span data-stu-id="f3e88-113">**Buffer**</span></span>
</dt> <dd>

<span data-ttu-id="f3e88-114">Puntatore a un **ushort** che rappresenta la stringa Unicode.</span><span class="sxs-lookup"><span data-stu-id="f3e88-114">A pointer to a **USHORT** that represents the Unicode string.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f3e88-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f3e88-115">Requirements</span></span>



| <span data-ttu-id="f3e88-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="f3e88-116">Requirement</span></span> | <span data-ttu-id="f3e88-117">Valore</span><span class="sxs-lookup"><span data-stu-id="f3e88-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f3e88-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f3e88-118">Minimum supported client</span></span><br/> | <span data-ttu-id="f3e88-119">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="f3e88-119">None supported</span></span><br/>                                                             |
| <span data-ttu-id="f3e88-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f3e88-120">Minimum supported server</span></span><br/> | <span data-ttu-id="f3e88-121">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f3e88-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f3e88-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f3e88-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="f3e88-123"><dt>Rkeysvcc. h</dt></span><span class="sxs-lookup"><span data-stu-id="f3e88-123"><dt>Rkeysvcc.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f3e88-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f3e88-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3e88-125">**RKeyPFXInstall**</span><span class="sxs-lookup"><span data-stu-id="f3e88-125">**RKeyPFXInstall**</span></span>](rkeypfxinstall.md)
</dt> <dt>

[<span data-ttu-id="f3e88-126">**\_BLOB KEYSVC**</span><span class="sxs-lookup"><span data-stu-id="f3e88-126">**KEYSVC\_BLOB**</span></span>](keysvc-blob.md)
</dt> </dl>

 

 
