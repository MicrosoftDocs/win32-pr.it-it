---
description: Rappresenta un handle per una funzione installabile dell'identificatore di oggetto (OID).
ms.assetid: 06492b94-9717-40e0-be96-f97f42ac34af
title: HCRYPTOIDFUNCADDR (Wincrypt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4f083d87234e598e8464491f2968868fa2b3c8a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316156"
---
# <a name="hcryptoidfuncaddr"></a><span data-ttu-id="d2fac-103">HCRYPTOIDFUNCADDR</span><span class="sxs-lookup"><span data-stu-id="d2fac-103">HCRYPTOIDFUNCADDR</span></span>

<span data-ttu-id="d2fac-104">Il tipo di dati **HCRYPTOIDFUNCADDR** rappresenta un handle per una funzione installabile dell' [*identificatore di oggetto*](../secgloss/o-gly.md) (OID).</span><span class="sxs-lookup"><span data-stu-id="d2fac-104">The **HCRYPTOIDFUNCADDR** data type represents a handle to an [*object identifier*](../secgloss/o-gly.md) (OID) installable function.</span></span> <span data-ttu-id="d2fac-105">Le funzioni [**CryptGetDefaultOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetdefaultoidfunctionaddress), [**CryptGetOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetoidfunctionaddress)e [**CryptFreeOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptfreeoidfunctionaddress) e la struttura di [**\_ \_ prova \_ dell'archivio certificati**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_store_prov_info) utilizzano questo tipo di dati.</span><span class="sxs-lookup"><span data-stu-id="d2fac-105">The [**CryptGetDefaultOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetdefaultoidfunctionaddress), [**CryptGetOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetoidfunctionaddress), and [**CryptFreeOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptfreeoidfunctionaddress) functions, and the [**CERT\_STORE\_PROV\_INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_store_prov_info) structure use this data type.</span></span>


```C++
typedef void* HCRYPTOIDFUNCADDR;
```



## <a name="requirements"></a><span data-ttu-id="d2fac-106">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d2fac-106">Requirements</span></span>



| <span data-ttu-id="d2fac-107">Requisito</span><span class="sxs-lookup"><span data-stu-id="d2fac-107">Requirement</span></span> | <span data-ttu-id="d2fac-108">Valore</span><span class="sxs-lookup"><span data-stu-id="d2fac-108">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d2fac-109">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d2fac-109">Minimum supported client</span></span><br/> | <span data-ttu-id="d2fac-110">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="d2fac-110">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="d2fac-111">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d2fac-111">Minimum supported server</span></span><br/> | <span data-ttu-id="d2fac-112">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d2fac-112">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d2fac-113">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d2fac-113">Header</span></span><br/>                   | <dl> <span data-ttu-id="d2fac-114"><dt>Wincrypt. h</dt></span><span class="sxs-lookup"><span data-stu-id="d2fac-114"><dt>Wincrypt.h</dt></span></span> </dl> |



 

 
