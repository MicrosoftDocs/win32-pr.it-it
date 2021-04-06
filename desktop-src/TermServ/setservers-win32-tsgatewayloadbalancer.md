---
title: Metodo seservers della classe Win32_TSGatewayLoadBalancer
description: Imposta la proprietà Servers con l'elenco dei server di bilanciamento del carico di Desktop remoto Gateway (Gateway Desktop remoto).
ms.assetid: c82de8e2-301b-465d-b375-038b8a480cde
ms.tgt_platform: multiple
keywords:
- Metodo seservers Servizi Desktop remoto
- Metodo seservers Servizi Desktop remoto, classe Win32_TSGatewayLoadBalancer
- Classe Win32_TSGatewayLoadBalancer Servizi Desktop remoto, metodo seservers
topic_type:
- apiref
api_name:
- Win32_TSGatewayLoadBalancer.SetServers
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b28d1123ce82844fb501f3562014b93337502b51
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742370"
---
# <a name="setservers-method-of-the-win32_tsgatewayloadbalancer-class"></a><span data-ttu-id="ea918-106">Metodo seservers della classe Win32 \_ TSGatewayLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ea918-106">SetServers method of the Win32\_TSGatewayLoadBalancer class</span></span>

<span data-ttu-id="ea918-107">Imposta la proprietà **Servers** con l'elenco dei server di bilanciamento del carico di desktop remoto Gateway (Gateway Desktop remoto).</span><span class="sxs-lookup"><span data-stu-id="ea918-107">Sets the **Servers** property with the list of Remote Desktop Gateway (RD Gateway) load-balancing servers.</span></span>

## <a name="syntax"></a><span data-ttu-id="ea918-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ea918-108">Syntax</span></span>


```mof
uint32 SetServers(
  [in] string Servers
);
```



## <a name="parameters"></a><span data-ttu-id="ea918-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="ea918-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ea918-110">*Server* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="ea918-110">*Servers* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ea918-111">Elenco delimitato da punti e virgola di server di bilanciamento del carico di Gateway Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="ea918-111">Semicolon-separated list of RD Gateway load-balancing servers.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ea918-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ea918-112">Return value</span></span>

<span data-ttu-id="ea918-113">Se il metodo ha esito positivo, restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="ea918-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="ea918-114">Se il metodo ha esito negativo, restituisce un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="ea918-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="ea918-115">Per un elenco di codici di errore, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="ea918-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="ea918-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="ea918-116">Remarks</span></span>

<span data-ttu-id="ea918-117">Se più server si trovano nel parametro *Server* e uno dei server non può essere elaborato, nessuno dei server verrà elaborato.</span><span class="sxs-lookup"><span data-stu-id="ea918-117">If multiple servers are in the *Servers* parameter and one of the servers cannot be processed, none of the servers will be processed.</span></span>

<span data-ttu-id="ea918-118">Per chiamare questo metodo, è necessario essere membri del gruppo Administrators.</span><span class="sxs-lookup"><span data-stu-id="ea918-118">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="ea918-119">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="ea918-119">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="ea918-120">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="ea918-120">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="ea918-121">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="ea918-121">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="ea918-122">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="ea918-122">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="ea918-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ea918-123">Requirements</span></span>



| <span data-ttu-id="ea918-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="ea918-124">Requirement</span></span> | <span data-ttu-id="ea918-125">Valore</span><span class="sxs-lookup"><span data-stu-id="ea918-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea918-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ea918-126">Minimum supported client</span></span><br/> | <span data-ttu-id="ea918-127">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="ea918-127">None supported</span></span><br/>                                                                |
| <span data-ttu-id="ea918-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ea918-128">Minimum supported server</span></span><br/> | <span data-ttu-id="ea918-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ea918-129">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="ea918-130">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="ea918-130">Namespace</span></span><br/>                | <span data-ttu-id="ea918-131">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="ea918-131">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="ea918-132">MOF</span><span class="sxs-lookup"><span data-stu-id="ea918-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ea918-133"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ea918-133"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="ea918-134">DLL</span><span class="sxs-lookup"><span data-stu-id="ea918-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ea918-135"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ea918-135"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="ea918-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ea918-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea918-137">**\_TSGatewayLoadBalancer Win32**</span><span class="sxs-lookup"><span data-stu-id="ea918-137">**Win32\_TSGatewayLoadBalancer**</span></span>](win32-tsgatewayloadbalancer.md)
</dt> </dl>

 

