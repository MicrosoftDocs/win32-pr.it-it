---
description: Rappresenta un handle per un set di funzioni installabili dell'identificatore di oggetto (OID).
ms.assetid: 83b76466-dc55-4269-91a3-17c2e6102126
title: HCRYPTOIDFUNCSET (Wincrypt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 437511de32de97d4fb226d299f224427267381ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316157"
---
# <a name="hcryptoidfuncset"></a><span data-ttu-id="abd74-103">HCRYPTOIDFUNCSET</span><span class="sxs-lookup"><span data-stu-id="abd74-103">HCRYPTOIDFUNCSET</span></span>

<span data-ttu-id="abd74-104">Il tipo di dati **HCRYPTOIDFUNCSET** rappresenta un handle per un set di funzioni installabili da un [*identificatore di oggetto*](../secgloss/o-gly.md) (OID).</span><span class="sxs-lookup"><span data-stu-id="abd74-104">The **HCRYPTOIDFUNCSET** data type represents a handle to a set of [*object identifier*](../secgloss/o-gly.md) (OID) installable functions.</span></span> <span data-ttu-id="abd74-105">Le funzioni [**CryptGetDefaultOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetdefaultoidfunctionaddress), [**CryptGetOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetoidfunctionaddress), [**CryptFreeOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptfreeoidfunctionaddress)e [**CryptInitOIDFunctionSet**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptinitoidfunctionset) utilizzano questo tipo di dati.</span><span class="sxs-lookup"><span data-stu-id="abd74-105">The [**CryptGetDefaultOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetdefaultoidfunctionaddress), [**CryptGetOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetoidfunctionaddress), [**CryptFreeOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptfreeoidfunctionaddress), and [**CryptInitOIDFunctionSet**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptinitoidfunctionset) functions use this data type.</span></span>


```C++
typedef void* HCRYPTOIDFUNCSET;
```



## <a name="requirements"></a><span data-ttu-id="abd74-106">Requisiti</span><span class="sxs-lookup"><span data-stu-id="abd74-106">Requirements</span></span>



| <span data-ttu-id="abd74-107">Requisito</span><span class="sxs-lookup"><span data-stu-id="abd74-107">Requirement</span></span> | <span data-ttu-id="abd74-108">Valore</span><span class="sxs-lookup"><span data-stu-id="abd74-108">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="abd74-109">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="abd74-109">Minimum supported client</span></span><br/> | <span data-ttu-id="abd74-110">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="abd74-110">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="abd74-111">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="abd74-111">Minimum supported server</span></span><br/> | <span data-ttu-id="abd74-112">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="abd74-112">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="abd74-113">Intestazione</span><span class="sxs-lookup"><span data-stu-id="abd74-113">Header</span></span><br/>                   | <dl> <span data-ttu-id="abd74-114"><dt>Wincrypt. h</dt></span><span class="sxs-lookup"><span data-stu-id="abd74-114"><dt>Wincrypt.h</dt></span></span> </dl> |



 

 
