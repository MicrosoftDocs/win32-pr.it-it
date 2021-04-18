---
description: 'Le costanti RENDBIND sono flag usati dal metodo ITDirectory:: Bind per indicare i tipi di autenticazione forniti.'
ms.assetid: 27bcf36a-1826-4603-9821-22fcc5c1e186
title: Costanti RENDBIND_ (rend. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: badd2a48b2ae0632e317522533c664d4f74a6c77
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330741"
---
# <a name="rendbind_-constants"></a><span data-ttu-id="dac6d-103">\_Costanti RENDBIND</span><span class="sxs-lookup"><span data-stu-id="dac6d-103">RENDBIND\_ Constants</span></span>

<span data-ttu-id="dac6d-104">\[ I controlli e le interfacce per la comunicazione di telefonia IP Rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="dac6d-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="dac6d-105">L'API del client RTC fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="dac6d-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="dac6d-106">Le costanti RENDBIND sono flag usati dal metodo [**ITDirectory:: bind**](/windows/desktop/api/Rend/nf-rend-itdirectory-bind) per indicare i tipi di autenticazione forniti.</span><span class="sxs-lookup"><span data-stu-id="dac6d-106">The RENDBIND constants are flags used by the [**ITDirectory::Bind**](/windows/desktop/api/Rend/nf-rend-itdirectory-bind) method to indicate types of authentication supplied.</span></span>

<dl> <dt>

<span data-ttu-id="dac6d-107"><span id="RENDBIND_AUTHENTICATE"></span><span id="rendbind_authenticate"></span>**\_autenticazione RENDBIND**</span><span class="sxs-lookup"><span data-stu-id="dac6d-107"><span id="RENDBIND_AUTHENTICATE"></span><span id="rendbind_authenticate"></span>**RENDBIND\_AUTHENTICATE**</span></span>
</dt> <dd> <dl> <dt>

 <span data-ttu-id="dac6d-108">0x00000001</span><span class="sxs-lookup"><span data-stu-id="dac6d-108">0x00000001</span></span>
</dt> <dt>



<span data-ttu-id="dac6d-109">Autenticare l'utente.</span><span class="sxs-lookup"><span data-stu-id="dac6d-109">Authenticate user.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="dac6d-110"><span id="RENDBIND_DEFAULTDOMAINNAME"></span><span id="rendbind_defaultdomainname"></span>**\_DEFAULTDOMAINNAME RENDBIND**</span><span class="sxs-lookup"><span data-stu-id="dac6d-110"><span id="RENDBIND_DEFAULTDOMAINNAME"></span><span id="rendbind_defaultdomainname"></span>**RENDBIND\_DEFAULTDOMAINNAME**</span></span>
</dt> <dd> <dl> <dt>

 <span data-ttu-id="dac6d-111">0x00000002</span><span class="sxs-lookup"><span data-stu-id="dac6d-111">0x00000002</span></span>
</dt> <dt>



<span data-ttu-id="dac6d-112">Usare il nome di dominio predefinito.</span><span class="sxs-lookup"><span data-stu-id="dac6d-112">Use default domain name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="dac6d-113"><span id="RENDBIND_DEFAULTUSERNAME"></span><span id="rendbind_defaultusername"></span>**\_DEFAULTUSERNAME RENDBIND**</span><span class="sxs-lookup"><span data-stu-id="dac6d-113"><span id="RENDBIND_DEFAULTUSERNAME"></span><span id="rendbind_defaultusername"></span>**RENDBIND\_DEFAULTUSERNAME**</span></span>
</dt> <dd> <dl> <dt>

 <span data-ttu-id="dac6d-114">0x00000004</span><span class="sxs-lookup"><span data-stu-id="dac6d-114">0x00000004</span></span>
</dt> <dt>



<span data-ttu-id="dac6d-115">Usare il nome utente predefinito.</span><span class="sxs-lookup"><span data-stu-id="dac6d-115">Use default user name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="dac6d-116"><span id="RENDBIND_DEFAULTPASSWORD"></span><span id="rendbind_defaultpassword"></span>**\_DEFAULTPASSWORD RENDBIND**</span><span class="sxs-lookup"><span data-stu-id="dac6d-116"><span id="RENDBIND_DEFAULTPASSWORD"></span><span id="rendbind_defaultpassword"></span>**RENDBIND\_DEFAULTPASSWORD**</span></span>
</dt> <dd> <dl> <dt>

 <span data-ttu-id="dac6d-117">0x00000008</span><span class="sxs-lookup"><span data-stu-id="dac6d-117">0x00000008</span></span>
</dt> <dt>



<span data-ttu-id="dac6d-118">Usa password predefinita.</span><span class="sxs-lookup"><span data-stu-id="dac6d-118">Use default password.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="dac6d-119"><span id="RENDBIND_DEFAULTCREDENTIALS"></span><span id="rendbind_defaultcredentials"></span>**\_DEFAULTCREDENTIALS RENDBIND**</span><span class="sxs-lookup"><span data-stu-id="dac6d-119"><span id="RENDBIND_DEFAULTCREDENTIALS"></span><span id="rendbind_defaultcredentials"></span>**RENDBIND\_DEFAULTCREDENTIALS**</span></span>
</dt> <dd> <dl> <dt>

 <span data-ttu-id="dac6d-120">0x0000000E</span><span class="sxs-lookup"><span data-stu-id="dac6d-120">0x0000000e</span></span>
</dt> <dt>



<span data-ttu-id="dac6d-121">I tre ORed precedenti sono insieme per praticità.</span><span class="sxs-lookup"><span data-stu-id="dac6d-121">The previous three ORed together for convenience.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="dac6d-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dac6d-122">Requirements</span></span>



| <span data-ttu-id="dac6d-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="dac6d-123">Requirement</span></span> | <span data-ttu-id="dac6d-124">Valore</span><span class="sxs-lookup"><span data-stu-id="dac6d-124">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="dac6d-125">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="dac6d-125">TAPI version</span></span><br/> | <span data-ttu-id="dac6d-126">Richiede TAPI 3,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="dac6d-126">Requires TAPI 3.0 or later</span></span><br/>                                             |
| <span data-ttu-id="dac6d-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="dac6d-127">Header</span></span><br/>       | <dl> <span data-ttu-id="dac6d-128"><dt>Rend. h</dt></span><span class="sxs-lookup"><span data-stu-id="dac6d-128"><dt>Rend.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dac6d-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="dac6d-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dac6d-130">**ITDirectory**</span><span class="sxs-lookup"><span data-stu-id="dac6d-130">**ITDirectory**</span></span>](/windows/desktop/api/Rend/nn-rend-itdirectory)
</dt> <dt>

[<span data-ttu-id="dac6d-131">**ITDirectory:: bind**</span><span class="sxs-lookup"><span data-stu-id="dac6d-131">**ITDirectory::Bind**</span></span>](/windows/desktop/api/Rend/nf-rend-itdirectory-bind)
</dt> </dl>

 

 




