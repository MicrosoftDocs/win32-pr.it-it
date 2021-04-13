---
title: Metodo DeleteServers della classe Win32_TSGatewayLoadBalancer
description: Elimina i server dalla proprietà Servers.
ms.assetid: 5ef44725-82b6-464a-abab-a68cc8799669
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo DeleteServers
- Metodo DeleteServers Servizi Desktop remoto, classe Win32_TSGatewayLoadBalancer
- Classe Win32_TSGatewayLoadBalancer Servizi Desktop remoto, metodo DeleteServers
topic_type:
- apiref
api_name:
- Win32_TSGatewayLoadBalancer.DeleteServers
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b889f37b783853fbca0b9cb399a83959e2522d0e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400328"
---
# <a name="deleteservers-method-of-the-win32_tsgatewayloadbalancer-class"></a><span data-ttu-id="4d7dc-106">Metodo DeleteServers della \_ classe TSGatewayLoadBalancer Win32</span><span class="sxs-lookup"><span data-stu-id="4d7dc-106">DeleteServers method of the Win32\_TSGatewayLoadBalancer class</span></span>

<span data-ttu-id="4d7dc-107">Elimina i server dalla proprietà **Servers** .</span><span class="sxs-lookup"><span data-stu-id="4d7dc-107">Deletes servers from the **Servers** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d7dc-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4d7dc-108">Syntax</span></span>


```mof
uint32 DeleteServers(
  [in] string Servers
);
```



## <a name="parameters"></a><span data-ttu-id="4d7dc-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="4d7dc-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4d7dc-110">*Server* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="4d7dc-110">*Servers* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4d7dc-111">Elenco delimitato da punti e virgola dei server di bilanciamento del carico di Gateway Desktop remoto da eliminare dalla proprietà **Server** .</span><span class="sxs-lookup"><span data-stu-id="4d7dc-111">Semicolon-separated list of RD Gateway load-balancing servers to delete from the **Servers** property.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4d7dc-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4d7dc-112">Return value</span></span>

<span data-ttu-id="4d7dc-113">Se il metodo ha esito positivo, restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="4d7dc-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="4d7dc-114">Se il metodo ha esito negativo, restituisce un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="4d7dc-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="4d7dc-115">Per un elenco di codici di errore, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="4d7dc-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="4d7dc-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="4d7dc-116">Remarks</span></span>

<span data-ttu-id="4d7dc-117">Se più server si trovano nel parametro *Server* e uno dei server non può essere elaborato, nessuno dei server verrà elaborato.</span><span class="sxs-lookup"><span data-stu-id="4d7dc-117">If multiple servers are in the *Servers* parameter and one of the servers cannot be processed, none of the servers will be processed.</span></span>

<span data-ttu-id="4d7dc-118">Per chiamare questo metodo, è necessario essere membri del gruppo Administrators.</span><span class="sxs-lookup"><span data-stu-id="4d7dc-118">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="4d7dc-119">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="4d7dc-119">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="4d7dc-120">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="4d7dc-120">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="4d7dc-121">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="4d7dc-121">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="4d7dc-122">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="4d7dc-122">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="4d7dc-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4d7dc-123">Requirements</span></span>



| <span data-ttu-id="4d7dc-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="4d7dc-124">Requirement</span></span> | <span data-ttu-id="4d7dc-125">Valore</span><span class="sxs-lookup"><span data-stu-id="4d7dc-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="4d7dc-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4d7dc-126">Minimum supported client</span></span><br/> | <span data-ttu-id="4d7dc-127">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="4d7dc-127">None supported</span></span><br/>                                                                |
| <span data-ttu-id="4d7dc-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4d7dc-128">Minimum supported server</span></span><br/> | <span data-ttu-id="4d7dc-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4d7dc-129">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="4d7dc-130">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="4d7dc-130">Namespace</span></span><br/>                | <span data-ttu-id="4d7dc-131">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="4d7dc-131">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="4d7dc-132">MOF</span><span class="sxs-lookup"><span data-stu-id="4d7dc-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4d7dc-133"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4d7dc-133"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="4d7dc-134">DLL</span><span class="sxs-lookup"><span data-stu-id="4d7dc-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4d7dc-135"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4d7dc-135"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="4d7dc-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4d7dc-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d7dc-137">**\_TSGatewayLoadBalancer Win32**</span><span class="sxs-lookup"><span data-stu-id="4d7dc-137">**Win32\_TSGatewayLoadBalancer**</span></span>](win32-tsgatewayloadbalancer.md)
</dt> </dl>

 

