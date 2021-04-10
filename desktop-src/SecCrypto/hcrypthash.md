---
description: Il tipo di dati HCRYPTHASH viene utilizzato per rappresentare gli handle per gli oggetti hash.
ms.assetid: 3b872bf0-cf1b-465b-82a2-c6fd154e1125
title: HCRYPTHASH (Wincrypt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a009350ed910627c1e6ec9ae33997ed20c7fec2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884057"
---
# <a name="hcrypthash"></a><span data-ttu-id="9f5b3-103">HCRYPTHASH</span><span class="sxs-lookup"><span data-stu-id="9f5b3-103">HCRYPTHASH</span></span>

<span data-ttu-id="9f5b3-104">Il tipo di dati **HCRYPTHASH** viene utilizzato per rappresentare gli handle per [*gli oggetti hash*](../secgloss/h-gly.md).</span><span class="sxs-lookup"><span data-stu-id="9f5b3-104">The **HCRYPTHASH** data type is used to represent handles to [*hash objects*](../secgloss/h-gly.md).</span></span> <span data-ttu-id="9f5b3-105">Questi handle indicano al modulo CSP quale hash viene usato in una determinata operazione.</span><span class="sxs-lookup"><span data-stu-id="9f5b3-105">These handles indicate to the CSP module which hash is being used in a particular operation.</span></span> <span data-ttu-id="9f5b3-106">Il modulo CSP non consente la manipolazione diretta dei valori hash.</span><span class="sxs-lookup"><span data-stu-id="9f5b3-106">The CSP module does not enable direct manipulation of the hash values.</span></span> <span data-ttu-id="9f5b3-107">Il valore hash viene invece modificato dall'utente tramite l'handle hash.</span><span class="sxs-lookup"><span data-stu-id="9f5b3-107">Instead, the user manipulates the hash values through the hash handle.</span></span>


```C++
typedef ULONG_PTR HCRYPTHASH;
```



## <a name="requirements"></a><span data-ttu-id="9f5b3-108">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9f5b3-108">Requirements</span></span>



| <span data-ttu-id="9f5b3-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="9f5b3-109">Requirement</span></span> | <span data-ttu-id="9f5b3-110">Valore</span><span class="sxs-lookup"><span data-stu-id="9f5b3-110">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9f5b3-111">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9f5b3-111">Minimum supported client</span></span><br/> | <span data-ttu-id="9f5b3-112">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="9f5b3-112">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="9f5b3-113">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9f5b3-113">Minimum supported server</span></span><br/> | <span data-ttu-id="9f5b3-114">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="9f5b3-114">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9f5b3-115">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9f5b3-115">Header</span></span><br/>                   | <dl> <span data-ttu-id="9f5b3-116"><dt>Wincrypt. h</dt></span><span class="sxs-lookup"><span data-stu-id="9f5b3-116"><dt>Wincrypt.h</dt></span></span> </dl> |



 

 
