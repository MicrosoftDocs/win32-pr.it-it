---
description: Rappresenta un handle per una risposta OCSP associata a una catena di certificati del server.
ms.assetid: baf173f1-99dc-49f9-9a17-fee79b393db7
title: HCERT_SERVER_OCSP_RESPONSE (Wincrypt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ceab319b5d8370dd15ef3dcd288124e4f2adf9ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884058"
---
# <a name="hcert_server_ocsp_response"></a><span data-ttu-id="3c69c-103">\_ \_ risposta OCSP del server HCERT \_</span><span class="sxs-lookup"><span data-stu-id="3c69c-103">HCERT\_SERVER\_OCSP\_RESPONSE</span></span>

<span data-ttu-id="3c69c-104">Il tipo di dati **\_ \_ \_ risposta OCSP del server HCERT** rappresenta un handle per una risposta OCSP associata a una catena di certificati del server.</span><span class="sxs-lookup"><span data-stu-id="3c69c-104">The **HCERT\_SERVER\_OCSP\_RESPONSE** data type represents a handle to an OCSP response associated with a server certificate chain.</span></span>

<span data-ttu-id="3c69c-105">Questo tipo viene usato dalle API seguenti.</span><span class="sxs-lookup"><span data-stu-id="3c69c-105">This type is used by the following APIs.</span></span>

-   [<span data-ttu-id="3c69c-106">**CertOpenServerOcspResponse**</span><span class="sxs-lookup"><span data-stu-id="3c69c-106">**CertOpenServerOcspResponse**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenserverocspresponse)
-   [<span data-ttu-id="3c69c-107">**CertAddRefServerOcspResponse**</span><span class="sxs-lookup"><span data-stu-id="3c69c-107">**CertAddRefServerOcspResponse**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddrefserverocspresponse)
-   [<span data-ttu-id="3c69c-108">**CertCloseServerOcspResponse**</span><span class="sxs-lookup"><span data-stu-id="3c69c-108">**CertCloseServerOcspResponse**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certcloseserverocspresponse)
-   [<span data-ttu-id="3c69c-109">**CertGetServerOcspResponseContext**</span><span class="sxs-lookup"><span data-stu-id="3c69c-109">**CertGetServerOcspResponseContext**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetserverocspresponsecontext)


```C++
typedef VOID* HCERT_SERVER_OCSP_RESPONSE;
```



## <a name="requirements"></a><span data-ttu-id="3c69c-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3c69c-110">Requirements</span></span>



| <span data-ttu-id="3c69c-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="3c69c-111">Requirement</span></span> | <span data-ttu-id="3c69c-112">Valore</span><span class="sxs-lookup"><span data-stu-id="3c69c-112">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3c69c-113">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3c69c-113">Minimum supported client</span></span><br/> | <span data-ttu-id="3c69c-114">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3c69c-114">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3c69c-115">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3c69c-115">Minimum supported server</span></span><br/> | <span data-ttu-id="3c69c-116">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="3c69c-116">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3c69c-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3c69c-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="3c69c-118"><dt>Wincrypt. h</dt></span><span class="sxs-lookup"><span data-stu-id="3c69c-118"><dt>Wincrypt.h</dt></span></span> </dl> |



 

 




