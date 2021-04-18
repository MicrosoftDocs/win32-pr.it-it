---
title: Proprietà GatewayDomain di IMsRdpClientTransportSettings2
description: Specifica o Recupera il nome di dominio di un utente fornito al server gateway di Desktop remoto (Gateway Desktop remoto).
ms.assetid: 792ff7c6-afeb-4a2a-86b4-7722513a08e0
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà GatewayDomain
- Servizi Desktop remoto proprietà GatewayDomain, interfaccia IMsRdpClientTransportSettings2
- Interfaccia IMsRdpClientTransportSettings2 Servizi Desktop remoto, proprietà GatewayDomain
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings2.GatewayDomain
- IMsRdpClientTransportSettings2.get_GatewayDomain
- IMsRdpClientTransportSettings2.put_GatewayDomain
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5088780fbbaa4ab86fc416a3e9aa353920cc25e9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400378"
---
# <a name="imsrdpclienttransportsettings2gatewaydomain-property"></a><span data-ttu-id="8f568-106">Proprietà IMsRdpClientTransportSettings2:: GatewayDomain</span><span class="sxs-lookup"><span data-stu-id="8f568-106">IMsRdpClientTransportSettings2::GatewayDomain property</span></span>

<span data-ttu-id="8f568-107">Specifica o Recupera il nome di dominio di un utente fornito al server gateway di Desktop remoto (Gateway Desktop remoto).</span><span class="sxs-lookup"><span data-stu-id="8f568-107">Specifies or retrieves the domain name of a user that is provided to the Remote Desktop Gateway (RD Gateway) server.</span></span>

<span data-ttu-id="8f568-108">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="8f568-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="8f568-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8f568-109">Syntax</span></span>


```C++
HRESULT put_GatewayDomain(
  [in]  BSTR proxyDomain
);

HRESULT get_GatewayDomain(
  [out] BSTR *pProxyDomain
);
```



## <a name="property-value"></a><span data-ttu-id="8f568-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="8f568-110">Property value</span></span>

<span data-ttu-id="8f568-111">Nome di dominio fornito per la connessione al server Gateway Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="8f568-111">The domain name that is provided to connect to the RD Gateway server.</span></span>

## <a name="error-codes"></a><span data-ttu-id="8f568-112">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="8f568-112">Error codes</span></span>

<span data-ttu-id="8f568-113">Restituisce **\_ OK** se ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="8f568-113">Returns **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="8f568-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8f568-114">Requirements</span></span>



| <span data-ttu-id="8f568-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="8f568-115">Requirement</span></span> | <span data-ttu-id="8f568-116">Valore</span><span class="sxs-lookup"><span data-stu-id="8f568-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8f568-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8f568-117">Minimum supported client</span></span><br/> | <span data-ttu-id="8f568-118">Windows Vista con SP1</span><span class="sxs-lookup"><span data-stu-id="8f568-118">Windows Vista with SP1</span></span><br/>                                                                 |
| <span data-ttu-id="8f568-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8f568-119">Minimum supported server</span></span><br/> | <span data-ttu-id="8f568-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8f568-120">Windows Server 2008</span></span><br/>                                                                    |
| <span data-ttu-id="8f568-121">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="8f568-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="8f568-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8f568-122"><dt>MsTscAx.dll</dt></span></span> </dl>            |
| <span data-ttu-id="8f568-123">DLL</span><span class="sxs-lookup"><span data-stu-id="8f568-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8f568-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8f568-124"><dt>MsTscAx.dll</dt></span></span> </dl>            |
| <span data-ttu-id="8f568-125">IID</span><span class="sxs-lookup"><span data-stu-id="8f568-125">IID</span></span><br/>                      | <span data-ttu-id="8f568-126">IID \_ IMsRdpClientTransportSettings2 è definito come 67341688-D606-4C73-A5D2-2E0489009319</span><span class="sxs-lookup"><span data-stu-id="8f568-126">IID\_IMsRdpClientTransportSettings2 is defined as 67341688-D606-4c73-A5D2-2E0489009319</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8f568-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8f568-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f568-128">**IMsRdpClientTransportSettings**</span><span class="sxs-lookup"><span data-stu-id="8f568-128">**IMsRdpClientTransportSettings**</span></span>](imsrdpclienttransportsettings.md)
</dt> <dt>

[<span data-ttu-id="8f568-129">**IMsRdpClientTransportSettings2**</span><span class="sxs-lookup"><span data-stu-id="8f568-129">**IMsRdpClientTransportSettings2**</span></span>](imsrdpclienttransportsettings2.md)
</dt> </dl>

 

 





