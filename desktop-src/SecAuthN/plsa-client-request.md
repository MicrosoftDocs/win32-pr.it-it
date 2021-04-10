---
description: Tipo di dati opaco.
ms.assetid: 384dd6e0-726f-4100-a036-1cca6a332a64
title: PLSA_CLIENT_REQUEST (Ntsecpkg. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a3685c3cd38843edfd4ae708a18761b6ee698c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104231711"
---
# <a name="plsa_client_request"></a><span data-ttu-id="0b043-103">\_richiesta client \_ PLSA</span><span class="sxs-lookup"><span data-stu-id="0b043-103">PLSA\_CLIENT\_REQUEST</span></span>

<span data-ttu-id="0b043-104">Il tipo di dati della **\_ \_ richiesta client PLSA** è un tipo di dati opaco.</span><span class="sxs-lookup"><span data-stu-id="0b043-104">The **PLSA\_CLIENT\_REQUEST** data type is an opaque data type.</span></span>

<span data-ttu-id="0b043-105">L' [*autorità di sicurezza locale*](../secgloss/l-gly.md) (LSA) la usa internamente per mantenere le informazioni client correlate alle singole richieste.</span><span class="sxs-lookup"><span data-stu-id="0b043-105">The [*Local Security Authority*](../secgloss/l-gly.md) (LSA) uses it internally to maintain client information related to individual requests.</span></span>


```C++
#include <windows.h>

typedef PVOID *PLSA_CLIENT_REQUEST;
```



## <a name="requirements"></a><span data-ttu-id="0b043-106">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0b043-106">Requirements</span></span>



| <span data-ttu-id="0b043-107">Requisito</span><span class="sxs-lookup"><span data-stu-id="0b043-107">Requirement</span></span> | <span data-ttu-id="0b043-108">Valore</span><span class="sxs-lookup"><span data-stu-id="0b043-108">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0b043-109">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0b043-109">Minimum supported client</span></span><br/> | <span data-ttu-id="0b043-110">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="0b043-110">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="0b043-111">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0b043-111">Minimum supported server</span></span><br/> | <span data-ttu-id="0b043-112">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="0b043-112">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0b043-113">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0b043-113">Header</span></span><br/>                   | <dl> <span data-ttu-id="0b043-114"><dt>Ntsecpkg. h</dt></span><span class="sxs-lookup"><span data-stu-id="0b043-114"><dt>Ntsecpkg.h</dt></span></span> </dl> |



 

 
