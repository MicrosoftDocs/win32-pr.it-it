---
title: Classe Win32_TSGatewayLoadBalancer
description: Viene descritto un set di server di bilanciamento del carico di Desktop remoto Gateway Desktop remoto. Questi vengono usati per il bilanciamento del carico delle connessioni Gateway Desktop remoto su più server.
ms.assetid: aa7e7b77-7233-4c6a-8f41-cc332fa509d5
ms.tgt_platform: multiple
keywords:
- Classe Win32_TSGatewayLoadBalancer Servizi Desktop remoto
- Classe Win32_TSGatewayLoadBalancer Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- Win32_TSGatewayLoadBalancer
- Win32_TSGatewayLoadBalancer.Servers
api_location:
- AagWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4956ed4dc9536ff6f7e3263071a2a477cb0f515
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741250"
---
# <a name="win32_tsgatewayloadbalancer-class"></a><span data-ttu-id="9f570-106">Win32 \_ TSGatewayLoadBalancer (classe)</span><span class="sxs-lookup"><span data-stu-id="9f570-106">Win32\_TSGatewayLoadBalancer class</span></span>

<span data-ttu-id="9f570-107">Viene descritto un set di server di bilanciamento del carico di Desktop remoto Gateway Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="9f570-107">Describes a set of Remote Desktop Gateway (RD Gateway) load-balancing servers.</span></span> <span data-ttu-id="9f570-108">Questi vengono usati per il bilanciamento del carico delle connessioni Gateway Desktop remoto su più server.</span><span class="sxs-lookup"><span data-stu-id="9f570-108">These are used to load balance RD Gateway connections across multiple servers.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f570-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9f570-109">Syntax</span></span>

``` syntax
[dynamic, provider("AAGProvider"), AMENDMENT]
class Win32_TSGatewayLoadBalancer
{
  string Servers;
};
```

## <a name="members"></a><span data-ttu-id="9f570-110">Members</span><span class="sxs-lookup"><span data-stu-id="9f570-110">Members</span></span>

<span data-ttu-id="9f570-111">La classe **Win32 \_ TSGatewayLoadBalancer** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="9f570-111">The **Win32\_TSGatewayLoadBalancer** class has these types of members:</span></span>

-   [<span data-ttu-id="9f570-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="9f570-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="9f570-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="9f570-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="9f570-114">Metodi</span><span class="sxs-lookup"><span data-stu-id="9f570-114">Methods</span></span>

<span data-ttu-id="9f570-115">La classe **Win32 \_ TSGatewayLoadBalancer** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="9f570-115">The **Win32\_TSGatewayLoadBalancer** class has these methods.</span></span>



| <span data-ttu-id="9f570-116">Metodo</span><span class="sxs-lookup"><span data-stu-id="9f570-116">Method</span></span>                                                                             | <span data-ttu-id="9f570-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9f570-117">Description</span></span>                                                                                                      |
|:-----------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9f570-118">**AddServers**</span><span class="sxs-lookup"><span data-stu-id="9f570-118">**AddServers**</span></span>](addservers-win32-tsgatewayloadbalancer.md)                       | <span data-ttu-id="9f570-119">Aggiunge server alla proprietà **Servers** .</span><span class="sxs-lookup"><span data-stu-id="9f570-119">Adds servers to the **Servers** property.</span></span><br/>                                                             |
| [<span data-ttu-id="9f570-120">**DeleteAllServers**</span><span class="sxs-lookup"><span data-stu-id="9f570-120">**DeleteAllServers**</span></span>](deleteallservers-win32-tsgatewayloadbalancer.md)           | <span data-ttu-id="9f570-121">Elimina tutti i server di bilanciamento del carico Gateway Desktop remoto che partecipano alla farm di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="9f570-121">Deletes all RD Gateway load-balancing servers participating in the load-balancing farm.</span></span><br/>               |
| [<span data-ttu-id="9f570-122">**DeleteServers**</span><span class="sxs-lookup"><span data-stu-id="9f570-122">**DeleteServers**</span></span>](deleteservers-win32-tsgatewayloadbalancer.md)                 | <span data-ttu-id="9f570-123">Elimina i server dalla proprietà **Servers** .</span><span class="sxs-lookup"><span data-stu-id="9f570-123">Deletes servers from the **Servers** property.</span></span><br/>                                                        |
| [<span data-ttu-id="9f570-124">**IsLoadBalancingServer**</span><span class="sxs-lookup"><span data-stu-id="9f570-124">**IsLoadBalancingServer**</span></span>](win32-tsgatewayloadbalancer-isloadbalancingserver.md) | <span data-ttu-id="9f570-125">Determina se il server è in grado di eseguire il bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="9f570-125">Determines whether the server can perform load balancing.</span></span><br/>                                             |
| [<span data-ttu-id="9f570-126">**Server**</span><span class="sxs-lookup"><span data-stu-id="9f570-126">**SetServers**</span></span>](setservers-win32-tsgatewayloadbalancer.md)                       | <span data-ttu-id="9f570-127">Imposta la proprietà **Servers** con l'elenco delimitato da punti e virgola dei server di bilanciamento del carico di Gateway Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="9f570-127">Sets the **Servers** property with the semicolon-separated list of RD Gateway load-balancing servers.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="9f570-128">Proprietà</span><span class="sxs-lookup"><span data-stu-id="9f570-128">Properties</span></span>

<span data-ttu-id="9f570-129">La classe **Win32 \_ TSGatewayLoadBalancer** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="9f570-129">The **Win32\_TSGatewayLoadBalancer** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9f570-130">**Server**</span><span class="sxs-lookup"><span data-stu-id="9f570-130">**Servers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f570-131">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="9f570-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9f570-132">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9f570-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9f570-133">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="9f570-133">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="9f570-134">Elenco delimitato da punti e virgola di server di bilanciamento del carico di Gateway Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="9f570-134">Semicolon-separated list of RD Gateway load-balancing servers.</span></span> <span data-ttu-id="9f570-135">Questa proprietà può essere modificata con i metodi [**Seservers**](setservers-win32-tsgatewayloadbalancer.md), [**AddServers**](addservers-win32-tsgatewayloadbalancer.md), [**DeleteServers**](deleteservers-win32-tsgatewayloadbalancer.md)e [**DeleteAllServers**](deleteallservers-win32-tsgatewayloadbalancer.md) .</span><span class="sxs-lookup"><span data-stu-id="9f570-135">This property can be changed with the [**SetServers**](setservers-win32-tsgatewayloadbalancer.md), [**AddServers**](addservers-win32-tsgatewayloadbalancer.md), [**DeleteServers**](deleteservers-win32-tsgatewayloadbalancer.md), and [**DeleteAllServers**](deleteallservers-win32-tsgatewayloadbalancer.md) methods.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9f570-136">Commenti</span><span class="sxs-lookup"><span data-stu-id="9f570-136">Remarks</span></span>

<span data-ttu-id="9f570-137">Per utilizzare questa classe, è necessario essere membri del gruppo Administrators.</span><span class="sxs-lookup"><span data-stu-id="9f570-137">You must be a member of the Administrators group to use this class.</span></span>

<span data-ttu-id="9f570-138">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="9f570-138">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="9f570-139">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="9f570-139">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="9f570-140">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="9f570-140">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="9f570-141">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="9f570-141">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="9f570-142">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9f570-142">Requirements</span></span>



| <span data-ttu-id="9f570-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="9f570-143">Requirement</span></span> | <span data-ttu-id="9f570-144">Valore</span><span class="sxs-lookup"><span data-stu-id="9f570-144">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f570-145">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9f570-145">Minimum supported client</span></span><br/> | <span data-ttu-id="9f570-146">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="9f570-146">None supported</span></span><br/>                                                                |
| <span data-ttu-id="9f570-147">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9f570-147">Minimum supported server</span></span><br/> | <span data-ttu-id="9f570-148">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9f570-148">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="9f570-149">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="9f570-149">Namespace</span></span><br/>                | <span data-ttu-id="9f570-150">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="9f570-150">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="9f570-151">MOF</span><span class="sxs-lookup"><span data-stu-id="9f570-151">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9f570-152"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9f570-152"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="9f570-153">DLL</span><span class="sxs-lookup"><span data-stu-id="9f570-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9f570-154"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9f570-154"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="9f570-155">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9f570-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f570-156">**\_TSGatewayConnection Win32**</span><span class="sxs-lookup"><span data-stu-id="9f570-156">**Win32\_TSGatewayConnection**</span></span>](win32-tsgatewayconnection.md)
</dt> <dt>

[<span data-ttu-id="9f570-157">**\_TSGatewayConnectionAuthorizationPolicy Win32**</span><span class="sxs-lookup"><span data-stu-id="9f570-157">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> <dt>

[<span data-ttu-id="9f570-158">**\_TSGatewayRADIUSServer Win32**</span><span class="sxs-lookup"><span data-stu-id="9f570-158">**Win32\_TSGatewayRADIUSServer**</span></span>](win32-tsgatewayradiusserver.md)
</dt> <dt>

[<span data-ttu-id="9f570-159">**\_TSGatewayResourceAuthorizationPolicy Win32**</span><span class="sxs-lookup"><span data-stu-id="9f570-159">**Win32\_TSGatewayResourceAuthorizationPolicy**</span></span>](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> <dt>

[<span data-ttu-id="9f570-160">**\_TSGatewayResourceGroup Win32**</span><span class="sxs-lookup"><span data-stu-id="9f570-160">**Win32\_TSGatewayResourceGroup**</span></span>](win32-tsgatewayresourcegroup.md)
</dt> <dt>

[<span data-ttu-id="9f570-161">**\_TSGatewayServerSettings Win32**</span><span class="sxs-lookup"><span data-stu-id="9f570-161">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 

