---
title: Metodo EnableAllowOnlySDRServers della classe Win32_TSGatewayConnectionAuthorizationPolicy
description: Utilizzato per impostare o disabilitare la proprietà AllowOnlySDRServers.
ms.assetid: ec7f22bc-4e80-4ece-9567-5f405207480e
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo EnableAllowOnlySDRServers
- Metodo EnableAllowOnlySDRServers Servizi Desktop remoto, classe Win32_TSGatewayConnectionAuthorizationPolicy
- Classe Win32_TSGatewayConnectionAuthorizationPolicy Servizi Desktop remoto, metodo EnableAllowOnlySDRServers
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.EnableAllowOnlySDRServers
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f031cff46e0fafdce80a995d2d4778875c1d56f7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741255"
---
# <a name="enableallowonlysdrservers-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a><span data-ttu-id="c9cc0-106">Metodo EnableAllowOnlySDRServers della \_ classe TSGatewayConnectionAuthorizationPolicy Win32</span><span class="sxs-lookup"><span data-stu-id="c9cc0-106">EnableAllowOnlySDRServers method of the Win32\_TSGatewayConnectionAuthorizationPolicy class</span></span>

<span data-ttu-id="c9cc0-107">Utilizzato per impostare o disabilitare la proprietà **AllowOnlySDRServers** .</span><span class="sxs-lookup"><span data-stu-id="c9cc0-107">Used to toggle the **AllowOnlySDRServers** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9cc0-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c9cc0-108">Syntax</span></span>


```mof
uint32 EnableAllowOnlySDRServers(
  [in] boolean AllowOnlySDRServers
);
```



## <a name="parameters"></a><span data-ttu-id="c9cc0-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="c9cc0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9cc0-110">*AllowOnlySDRServers* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c9cc0-110">*AllowOnlySDRServers* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9cc0-111">Se è impostato su **true**, le connessioni saranno consentite solo per i server RDS (Secure Device Reindirizzamento).</span><span class="sxs-lookup"><span data-stu-id="c9cc0-111">If set to **True**, connections will be allowed only to secure device redirection (SDR) RDS servers.</span></span> <span data-ttu-id="c9cc0-112">Se impostato su **false**, le connessioni saranno consentite anche ai server RDS meno recenti</span><span class="sxs-lookup"><span data-stu-id="c9cc0-112">If set to **False**, connections will be allowed to older RDS servers also</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c9cc0-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c9cc0-113">Return value</span></span>

<span data-ttu-id="c9cc0-114">Se il metodo ha esito positivo, restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="c9cc0-114">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="c9cc0-115">Se il metodo ha esito negativo, restituisce un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="c9cc0-115">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="c9cc0-116">Per un elenco di codici di errore, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="c9cc0-116">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c9cc0-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c9cc0-117">Requirements</span></span>



| <span data-ttu-id="c9cc0-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="c9cc0-118">Requirement</span></span> | <span data-ttu-id="c9cc0-119">Valore</span><span class="sxs-lookup"><span data-stu-id="c9cc0-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9cc0-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c9cc0-120">Minimum supported client</span></span><br/> | <span data-ttu-id="c9cc0-121">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="c9cc0-121">None supported</span></span><br/>                                                                |
| <span data-ttu-id="c9cc0-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c9cc0-122">Minimum supported server</span></span><br/> | <span data-ttu-id="c9cc0-123">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c9cc0-123">Windows Server 2008 R2</span></span><br/>                                                        |
| <span data-ttu-id="c9cc0-124">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="c9cc0-124">Namespace</span></span><br/>                | <span data-ttu-id="c9cc0-125">RADICE \\ CIMV2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="c9cc0-125">ROOT\\cimv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="c9cc0-126">MOF</span><span class="sxs-lookup"><span data-stu-id="c9cc0-126">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c9cc0-127"><dt>TsGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c9cc0-127"><dt>TsGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="c9cc0-128">DLL</span><span class="sxs-lookup"><span data-stu-id="c9cc0-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c9cc0-129"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c9cc0-129"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="c9cc0-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c9cc0-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9cc0-131">**\_TSGatewayConnectionAuthorizationPolicy Win32**</span><span class="sxs-lookup"><span data-stu-id="c9cc0-131">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 

 





