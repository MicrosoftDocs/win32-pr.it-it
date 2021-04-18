---
title: Metodo IsLoadBalancingServer della classe Win32_TSGatewayLoadBalancer
description: Determina se il server Gateway Desktop remoto (Gateway Desktop remoto) può eseguire il bilanciamento del carico.
ms.assetid: ae1a91c1-0b8b-4bd0-83f9-41c973247f27
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo IsLoadBalancingServer
- Metodo IsLoadBalancingServer Servizi Desktop remoto, classe Win32_TSGatewayLoadBalancer
- Classe Win32_TSGatewayLoadBalancer Servizi Desktop remoto, metodo IsLoadBalancingServer
topic_type:
- apiref
api_name:
- Win32_TSGatewayLoadBalancer.IsLoadBalancingServer
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6eae909df4074c8129a1b49eb0d5c3b336fed5d2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301963"
---
# <a name="isloadbalancingserver-method-of-the-win32_tsgatewayloadbalancer-class"></a><span data-ttu-id="cd453-106">Metodo IsLoadBalancingServer della \_ classe TSGatewayLoadBalancer Win32</span><span class="sxs-lookup"><span data-stu-id="cd453-106">IsLoadBalancingServer method of the Win32\_TSGatewayLoadBalancer class</span></span>

<span data-ttu-id="cd453-107">Determina se il server Gateway Desktop remoto (Gateway Desktop remoto) può eseguire il bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="cd453-107">Determines whether the Remote Desktop Gateway (RD Gateway) server can perform load balancing.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd453-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cd453-108">Syntax</span></span>


```mof
uint32 IsLoadBalancingServer(
  [out] boolean LoadBalancing
);
```



## <a name="parameters"></a><span data-ttu-id="cd453-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="cd453-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cd453-110">*Loadbalancing* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="cd453-110">*LoadBalancing* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cd453-111">**True** se il server è in grado di eseguire il bilanciamento del carico e **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="cd453-111">**TRUE** if the server can perform load balancing, and **FALSE** otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cd453-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="cd453-112">Return value</span></span>

<span data-ttu-id="cd453-113">Se il metodo ha esito positivo, restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="cd453-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="cd453-114">Se il metodo ha esito negativo, restituisce un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="cd453-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="cd453-115">Per un elenco di codici di errore, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="cd453-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="cd453-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="cd453-116">Remarks</span></span>

<span data-ttu-id="cd453-117">Per chiamare questo metodo, è necessario essere membri del gruppo Administrators.</span><span class="sxs-lookup"><span data-stu-id="cd453-117">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="cd453-118">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="cd453-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="cd453-119">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="cd453-119">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="cd453-120">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="cd453-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="cd453-121">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="cd453-121">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="cd453-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cd453-122">Requirements</span></span>



| <span data-ttu-id="cd453-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="cd453-123">Requirement</span></span> | <span data-ttu-id="cd453-124">Valore</span><span class="sxs-lookup"><span data-stu-id="cd453-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="cd453-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cd453-125">Minimum supported client</span></span><br/> | <span data-ttu-id="cd453-126">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="cd453-126">None supported</span></span><br/>                                                                |
| <span data-ttu-id="cd453-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cd453-127">Minimum supported server</span></span><br/> | <span data-ttu-id="cd453-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cd453-128">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="cd453-129">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="cd453-129">Namespace</span></span><br/>                | <span data-ttu-id="cd453-130">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="cd453-130">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="cd453-131">MOF</span><span class="sxs-lookup"><span data-stu-id="cd453-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cd453-132"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cd453-132"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="cd453-133">DLL</span><span class="sxs-lookup"><span data-stu-id="cd453-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cd453-134"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cd453-134"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="cd453-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cd453-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd453-136">**\_TSGatewayLoadBalancer Win32**</span><span class="sxs-lookup"><span data-stu-id="cd453-136">**Win32\_TSGatewayLoadBalancer**</span></span>](win32-tsgatewayloadbalancer.md)
</dt> </dl>

 

