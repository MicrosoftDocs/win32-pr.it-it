---
title: Proprietà GatewayCredsSource di IMsRdpClientTransportSettings
description: Specifica o Recupera il metodo di autenticazione del Gateway Desktop remoto (Gateway Desktop remoto).
ms.assetid: 3b05edcb-f678-4d80-99fd-b76d27c80c68
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà GatewayCredsSource
- Servizi Desktop remoto proprietà GatewayCredsSource, interfaccia IMsRdpClientTransportSettings
- Interfaccia IMsRdpClientTransportSettings Servizi Desktop remoto, proprietà GatewayCredsSource
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings.GatewayCredsSource
- IMsRdpClientTransportSettings.get_GatewayCredsSource
- IMsRdpClientTransportSettings.put_GatewayCredsSource
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2771998ddc7c53d05c5d0db452f34a734a7c3e58
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400382"
---
# <a name="imsrdpclienttransportsettingsgatewaycredssource-property"></a><span data-ttu-id="16f4b-106">Proprietà IMsRdpClientTransportSettings:: GatewayCredsSource</span><span class="sxs-lookup"><span data-stu-id="16f4b-106">IMsRdpClientTransportSettings::GatewayCredsSource property</span></span>

<span data-ttu-id="16f4b-107">Specifica o Recupera il metodo di autenticazione del Gateway Desktop remoto (Gateway Desktop remoto).</span><span class="sxs-lookup"><span data-stu-id="16f4b-107">Specifies or retrieves the Remote Desktop Gateway (RD Gateway) authentication method.</span></span>

<span data-ttu-id="16f4b-108">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="16f4b-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="16f4b-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="16f4b-109">Syntax</span></span>


```C++
HRESULT put_GatewayCredsSource(
  [in]  ULONG ulProxyCredsSource
);

HRESULT get_GatewayCredsSource(
  [out] ULONG *pulProxyCredsSource
);
```



## <a name="property-value"></a><span data-ttu-id="16f4b-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="16f4b-110">Property value</span></span>

<span data-ttu-id="16f4b-111">Variabile **ULONG** che specifica il metodo di autenticazione Gateway Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="16f4b-111">A **ULONG** variable that specifies the RD Gateway authentication method.</span></span> <span data-ttu-id="16f4b-112">Questo parametro può avere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="16f4b-112">This parameter can be one of the following values.</span></span>

<dt>

<span data-ttu-id="16f4b-113">\_Modalità credenziali del proxy TSC \_ \_ \_ USERPASS (0)</span><span class="sxs-lookup"><span data-stu-id="16f4b-113">TSC\_PROXY\_CREDS\_MODE\_USERPASS (0)</span></span>
</dt> <dd>

<span data-ttu-id="16f4b-114">Usare una password (NTLM) come metodo di autenticazione per Gateway Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="16f4b-114">Use a password (NTLM) as the authentication method for RD Gateway.</span></span>

</dd> <dt>

<span data-ttu-id="16f4b-115">\_ \_ Smart Card della modalità credenziali del proxy TSC \_ \_ (1)</span><span class="sxs-lookup"><span data-stu-id="16f4b-115">TSC\_PROXY\_CREDS\_MODE\_SMARTCARD (1)</span></span>
</dt> <dd>

<span data-ttu-id="16f4b-116">Usare una smart card come metodo di autenticazione per Gateway Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="16f4b-116">Use a smart card as the authentication method for RD Gateway.</span></span>

</dd> <dt>

<span data-ttu-id="16f4b-117">\_Modalità credenziali del proxy TSC \_ \_ \_ Any (4)</span><span class="sxs-lookup"><span data-stu-id="16f4b-117">TSC\_PROXY\_CREDS\_MODE\_ANY (4)</span></span>
</dt> <dd>

<span data-ttu-id="16f4b-118">Usare qualsiasi metodo di autenticazione per Gateway Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="16f4b-118">Use any authentication method for RD Gateway.</span></span>

</dd> </dl>

## <a name="error-codes"></a><span data-ttu-id="16f4b-119">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="16f4b-119">Error codes</span></span>

<span data-ttu-id="16f4b-120">Restituisce **\_ OK** se ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="16f4b-120">Returns **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="16f4b-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="16f4b-121">Requirements</span></span>



| <span data-ttu-id="16f4b-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="16f4b-122">Requirement</span></span> | <span data-ttu-id="16f4b-123">Valore</span><span class="sxs-lookup"><span data-stu-id="16f4b-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="16f4b-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="16f4b-124">Minimum supported client</span></span><br/> | <span data-ttu-id="16f4b-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="16f4b-125">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="16f4b-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="16f4b-126">Minimum supported server</span></span><br/> | <span data-ttu-id="16f4b-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="16f4b-127">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="16f4b-128">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="16f4b-128">Type library</span></span><br/>             | <dl> <span data-ttu-id="16f4b-129"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="16f4b-129"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="16f4b-130">DLL</span><span class="sxs-lookup"><span data-stu-id="16f4b-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="16f4b-131"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="16f4b-131"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="16f4b-132">IID</span><span class="sxs-lookup"><span data-stu-id="16f4b-132">IID</span></span><br/>                      | <span data-ttu-id="16f4b-133">IID \_ IMsRdpClientTransportSettings è definito come 720298C0-A099-46f5-9F82-96921BAE4701</span><span class="sxs-lookup"><span data-stu-id="16f4b-133">IID\_IMsRdpClientTransportSettings is defined as 720298C0-A099-46f5-9F82-96921BAE4701</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="16f4b-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="16f4b-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16f4b-135">**IMsRdpClientTransportSettings**</span><span class="sxs-lookup"><span data-stu-id="16f4b-135">**IMsRdpClientTransportSettings**</span></span>](imsrdpclienttransportsettings.md)
</dt> </dl>

 

 





