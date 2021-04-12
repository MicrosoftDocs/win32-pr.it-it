---
title: Identificatori di contesto del provider predefiniti (Fwpmu. h)
description: I contesti provider predefiniti identificano i criteri predefiniti da usare con i socket protetti.
ms.assetid: 439a5abc-08ac-4514-a126-d738e5311003
topic_type:
- apiref
api_name:
- FWPM_PROVIDER_CONTEXT_SECURE_SOCKET_AUTHIP
- FWPM_PROVIDER_CONTEXT_SECURE_SOCKET_IPSEC
api_location:
- fwpmu.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 942ed1d21d2acd46f0dc6b303049e0936e3cf63d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475106"
---
# <a name="built-in-provider-context-identifiers"></a><span data-ttu-id="7ddf4-103">Identificatori di contesto del provider predefiniti</span><span class="sxs-lookup"><span data-stu-id="7ddf4-103">Built-in Provider Context Identifiers</span></span>

<span data-ttu-id="7ddf4-104">Gli identificatori per i contesti del provider incorporati in Windows Filtering Platform (WFP) sono rappresentati da un GUID.</span><span class="sxs-lookup"><span data-stu-id="7ddf4-104">The identifiers for the provider contexts that are built in to the Windows Filtering Platform (WFP) are each represented by a GUID.</span></span> <span data-ttu-id="7ddf4-105">Questi contesti provider predefiniti identificano i criteri predefiniti da usare con i socket protetti.</span><span class="sxs-lookup"><span data-stu-id="7ddf4-105">These built-in provider contexts identify the default policies to use with secure sockets.</span></span>

<span data-ttu-id="7ddf4-106">Questi identificatori sono definiti nel modo seguente.</span><span class="sxs-lookup"><span data-stu-id="7ddf4-106">These identifiers are defined as follows.</span></span>

<dl> <dt>

<span data-ttu-id="7ddf4-107"><span id="FWPM_PROVIDER_CONTEXT_SECURE_SOCKET_AUTHIP"></span><span id="fwpm_provider_context_secure_socket_authip"></span>**\_ \_ \_ \_ AUTHIP socket sicuro del contesto del provider FWPM \_**</span><span class="sxs-lookup"><span data-stu-id="7ddf4-107"><span id="FWPM_PROVIDER_CONTEXT_SECURE_SOCKET_AUTHIP"></span><span id="fwpm_provider_context_secure_socket_authip"></span>**FWPM\_PROVIDER\_CONTEXT\_SECURE\_SOCKET\_AUTHIP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7ddf4-108">Authenticated Internet Protocol (AuthIP) criterio predefinito della modalità principale per i socket protetti.</span><span class="sxs-lookup"><span data-stu-id="7ddf4-108">Authenticated Internet Protocol (AuthIP) main mode default policy for secure sockets.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7ddf4-109"><span id="FWPM_PROVIDER_CONTEXT_SECURE_SOCKET_IPSEC"></span><span id="fwpm_provider_context_secure_socket_ipsec"></span>**\_ \_ \_ \_ IPSec socket sicuro del contesto del provider FWPM \_**</span><span class="sxs-lookup"><span data-stu-id="7ddf4-109"><span id="FWPM_PROVIDER_CONTEXT_SECURE_SOCKET_IPSEC"></span><span id="fwpm_provider_context_secure_socket_ipsec"></span>**FWPM\_PROVIDER\_CONTEXT\_SECURE\_SOCKET\_IPSEC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7ddf4-110">Criteri predefiniti della modalità rapida IPsec (Internet Protocol Security) per i socket protetti.</span><span class="sxs-lookup"><span data-stu-id="7ddf4-110">Internet Protocol Security (IPsec) quick mode default policy for secure sockets.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7ddf4-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7ddf4-111">Requirements</span></span>



| <span data-ttu-id="7ddf4-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="7ddf4-112">Requirement</span></span> | <span data-ttu-id="7ddf4-113">Valore</span><span class="sxs-lookup"><span data-stu-id="7ddf4-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7ddf4-114">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7ddf4-114">Minimum supported client</span></span><br/> | <span data-ttu-id="7ddf4-115">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7ddf4-115">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="7ddf4-116">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7ddf4-116">Minimum supported server</span></span><br/> | <span data-ttu-id="7ddf4-117">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="7ddf4-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="7ddf4-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7ddf4-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="7ddf4-119"><dt>Fwpmu. h</dt></span><span class="sxs-lookup"><span data-stu-id="7ddf4-119"><dt>Fwpmu.h</dt></span></span> </dl> |



 

 





