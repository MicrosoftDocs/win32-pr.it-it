---
description: Il tipo di dati HCRYPTKEY viene utilizzato per rappresentare gli handle delle chiavi crittografiche.
ms.assetid: d62f1d40-4f42-4684-96d7-de88db67dceb
title: HCRYPTKEY (Wincrypt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56bda14169aa2f4d7c6e502d3444473ea0f00408
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316159"
---
# <a name="hcryptkey"></a><span data-ttu-id="12df7-103">HCRYPTKEY</span><span class="sxs-lookup"><span data-stu-id="12df7-103">HCRYPTKEY</span></span>

<span data-ttu-id="12df7-104">Il tipo di dati **HCRYPTKEY** viene utilizzato per rappresentare gli handle delle [*chiavi crittografiche*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="12df7-104">The **HCRYPTKEY** data type is used to represent handles to [*cryptographic keys*](../secgloss/c-gly.md).</span></span> <span data-ttu-id="12df7-105">Questi handle vengono usati per indicare al modulo CSP quale chiave viene usata in un'operazione specifica.</span><span class="sxs-lookup"><span data-stu-id="12df7-105">These handles are used to indicate to the CSP module which key is being used in a specific operation.</span></span> <span data-ttu-id="12df7-106">Il modulo CSP non consente l'accesso diretto ai valori di chiave.</span><span class="sxs-lookup"><span data-stu-id="12df7-106">The CSP module does not enable direct access to the key values.</span></span> <span data-ttu-id="12df7-107">Al contrario, l'utente esegue le funzioni usando il valore della chiave tramite l'handle di chiave.</span><span class="sxs-lookup"><span data-stu-id="12df7-107">Instead, the user performs functions by using the key value through the key handle.</span></span>


```C++
typedef ULONG_PTR HCRYPTKEY;
```



## <a name="requirements"></a><span data-ttu-id="12df7-108">Requisiti</span><span class="sxs-lookup"><span data-stu-id="12df7-108">Requirements</span></span>



| <span data-ttu-id="12df7-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="12df7-109">Requirement</span></span> | <span data-ttu-id="12df7-110">Valore</span><span class="sxs-lookup"><span data-stu-id="12df7-110">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="12df7-111">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="12df7-111">Minimum supported client</span></span><br/> | <span data-ttu-id="12df7-112">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="12df7-112">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="12df7-113">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="12df7-113">Minimum supported server</span></span><br/> | <span data-ttu-id="12df7-114">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="12df7-114">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="12df7-115">Intestazione</span><span class="sxs-lookup"><span data-stu-id="12df7-115">Header</span></span><br/>                   | <dl> <span data-ttu-id="12df7-116"><dt>Wincrypt. h</dt></span><span class="sxs-lookup"><span data-stu-id="12df7-116"><dt>Wincrypt.h</dt></span></span> </dl> |



 

 
