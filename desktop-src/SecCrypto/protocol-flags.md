---
description: Costanti predefinite per i protocolli di crittografia. Questi valori sono definiti in WinCrypt. h.
ms.assetid: 61dc0eff-2033-464a-a558-1798a92d48a2
title: Flag di protocollo (Wincrypt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c25804763e407ff2a12e5657878e343f483d353e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968125"
---
# <a name="protocol-flags"></a><span data-ttu-id="94d35-104">Flag di protocollo</span><span class="sxs-lookup"><span data-stu-id="94d35-104">Protocol Flags</span></span>

<span data-ttu-id="94d35-105">Di seguito sono riportate le costanti predefinite per i protocolli di crittografia.</span><span class="sxs-lookup"><span data-stu-id="94d35-105">The following are predefined constants for cryptography protocols.</span></span> <span data-ttu-id="94d35-106">Questi valori sono definiti in WinCrypt. h.</span><span class="sxs-lookup"><span data-stu-id="94d35-106">These values are defined in Wincrypt.h.</span></span>



| <span data-ttu-id="94d35-107">Costante/valore</span><span class="sxs-lookup"><span data-stu-id="94d35-107">Constant/value</span></span>                                                                                                                                                                                                                            | <span data-ttu-id="94d35-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="94d35-108">Description</span></span>                                                           |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------|
| <span id="CRYPT_FLAG_IPSEC"></span><span id="crypt_flag_ipsec"></span><dl> <span data-ttu-id="94d35-109"><dt>**Crypt \_ FLAG \_**</dt> <dt>0x0010</dt> IPSec</span><span class="sxs-lookup"><span data-stu-id="94d35-109"><dt>**CRYPT\_FLAG\_IPSEC**</dt> <dt>0x0010</dt></span></span> </dl>       | <span data-ttu-id="94d35-110">Protocollo IPsec (Internet Protocol Security).</span><span class="sxs-lookup"><span data-stu-id="94d35-110">Internet protocol security (IPsec) protocol.</span></span><br/>               |
| <span id="CRYPT_FLAG_PCT1"></span><span id="crypt_flag_pct1"></span><dl> <span data-ttu-id="94d35-111"><dt>**Crypt \_ FLAG \_ PCT1**</dt> <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="94d35-111"><dt>**CRYPT\_FLAG\_PCT1**</dt> <dt>0x0001</dt></span></span> </dl>          | <span data-ttu-id="94d35-112">Protocollo PCT (Private Communications Transport) versione 1.</span><span class="sxs-lookup"><span data-stu-id="94d35-112">Private communications transport (PCT) version 1 protocol.</span></span><br/> |
| <span id="CRYPT_FLAG_SIGNING"></span><span id="crypt_flag_signing"></span><dl> <span data-ttu-id="94d35-113"><dt>**Crypt \_ FLAG di \_ firma**</dt> <dt>0x0020</dt></span><span class="sxs-lookup"><span data-stu-id="94d35-113"><dt>**CRYPT\_FLAG\_SIGNING**</dt> <dt>0x0020</dt></span></span> </dl> | <span data-ttu-id="94d35-114">Protocollo di firma.</span><span class="sxs-lookup"><span data-stu-id="94d35-114">Signing protocol.</span></span><br/>                                          |
| <span id="CRYPT_FLAG_SSL2"></span><span id="crypt_flag_ssl2"></span><dl> <span data-ttu-id="94d35-115"><dt>**Crypt \_ FLAG \_ SSL2**</dt> <dt>0x0002</dt></span><span class="sxs-lookup"><span data-stu-id="94d35-115"><dt>**CRYPT\_FLAG\_SSL2**</dt> <dt>0x0002</dt></span></span> </dl>          | <span data-ttu-id="94d35-116">Protocollo Secure Sockets Layer (SSL) versione 2.</span><span class="sxs-lookup"><span data-stu-id="94d35-116">Secure sockets layer (SSL) version 2 protocol.</span></span><br/>             |
| <span id="CRYPT_FLAG_SSL3"></span><span id="crypt_flag_ssl3"></span><dl> <span data-ttu-id="94d35-117"><dt>**Crypt \_ FLAG \_ SSL3**</dt> <dt>0x0004</dt></span><span class="sxs-lookup"><span data-stu-id="94d35-117"><dt>**CRYPT\_FLAG\_SSL3**</dt> <dt>0x0004</dt></span></span> </dl>          | <span data-ttu-id="94d35-118">Protocollo SSL versione 3.</span><span class="sxs-lookup"><span data-stu-id="94d35-118">SSL version 3 protocol.</span></span><br/>                                    |
| <span id="CRYPT_FLAG_TLS1"></span><span id="crypt_flag_tls1"></span><dl> <span data-ttu-id="94d35-119"><dt>**Crypt \_ FLAG \_ TLS1**</dt> <dt>0x0008</dt></span><span class="sxs-lookup"><span data-stu-id="94d35-119"><dt>**CRYPT\_FLAG\_TLS1**</dt> <dt>0x0008</dt></span></span> </dl>          | <span data-ttu-id="94d35-120">Protocollo TLS (Transport Layer Security) versione 1.</span><span class="sxs-lookup"><span data-stu-id="94d35-120">Transport layer security (TLS) version 1 protocol.</span></span><br/>         |



## <a name="requirements"></a><span data-ttu-id="94d35-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="94d35-121">Requirements</span></span>



| <span data-ttu-id="94d35-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="94d35-122">Requirement</span></span> | <span data-ttu-id="94d35-123">Valore</span><span class="sxs-lookup"><span data-stu-id="94d35-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="94d35-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="94d35-124">Minimum supported client</span></span><br/> | <span data-ttu-id="94d35-125">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="94d35-125">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="94d35-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="94d35-126">Minimum supported server</span></span><br/> | <span data-ttu-id="94d35-127">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="94d35-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="94d35-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="94d35-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="94d35-129"><dt>Wincrypt. h</dt></span><span class="sxs-lookup"><span data-stu-id="94d35-129"><dt>Wincrypt.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="94d35-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="94d35-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94d35-131">**PROVA \_ ENUMALGS \_ ex**</span><span class="sxs-lookup"><span data-stu-id="94d35-131">**PROV\_ENUMALGS\_EX**</span></span>](/windows/desktop/api/Wincrypt/ns-wincrypt-prov_enumalgs_ex)
</dt> </dl>

 

 




