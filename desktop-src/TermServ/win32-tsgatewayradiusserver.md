---
title: Classe Win32_TSGatewayRADIUSServer
description: Descrive un server Remote Authentication Dial-In User Service (RADIUS), che dispone di un set di criteri di autorizzazione della connessione Servizi Desktop remoto (RD \ 160; CAPs).
ms.assetid: 40254354-f446-4e17-b7ec-649c98dd94f9
ms.tgt_platform: multiple
keywords:
- Classe Win32_TSGatewayRADIUSServer Servizi Desktop remoto
- Classe Win32_TSGatewayRADIUSServer Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- Win32_TSGatewayRADIUSServer
- Win32_TSGatewayRADIUSServer.Name
- Win32_TSGatewayRADIUSServer.Priority
- Win32_TSGatewayRADIUSServer.SharedSecret
api_location:
- AagWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4157d89dc942a1c2f8ff7d778f9f8048971902ba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476385"
---
# <a name="win32_tsgatewayradiusserver-class"></a><span data-ttu-id="b2181-105">Win32 \_ TSGatewayRADIUSServer (classe)</span><span class="sxs-lookup"><span data-stu-id="b2181-105">Win32\_TSGatewayRADIUSServer class</span></span>

<span data-ttu-id="b2181-106">Viene descritto un server Remote Authentication Dial-In User Service (RADIUS), che dispone di un set di criteri di autorizzazione della connessione Servizi Desktop remoto (RD CAPs).</span><span class="sxs-lookup"><span data-stu-id="b2181-106">Describes a Remote Authentication Dial-In User Service (RADIUS) server, which has a set of Remote Desktop Services connection authorization policies (RD CAPs).</span></span>

<span data-ttu-id="b2181-107">RADIUS è un protocollo standard del settore utilizzato per trasmettere le informazioni di autenticazione, autorizzazione e configurazione tra un computer server e un server di autenticazione, denominato server RADIUS, con un database in cui sono archiviate le informazioni dell'utente.</span><span class="sxs-lookup"><span data-stu-id="b2181-107">RADIUS is an industry-standard protocol that is used to transmit authentication, authorization, and configuration information between a server computer and an authenticating server, called a RADIUS server, with a database that stores user information.</span></span> <span data-ttu-id="b2181-108">Per ulteriori informazioni, vedere [protocollo RADIUS](/previous-versions/windows/it-pro/windows-server-2003/cc781821(v=ws.10)).</span><span class="sxs-lookup"><span data-stu-id="b2181-108">For more information, see [RADIUS Protocol](/previous-versions/windows/it-pro/windows-server-2003/cc781821(v=ws.10)).</span></span>

## <a name="syntax"></a><span data-ttu-id="b2181-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b2181-109">Syntax</span></span>

``` syntax
[dynamic, provider("AAGProvider"), AMENDMENT]
class Win32_TSGatewayRADIUSServer
{
  string Name;
  uint32 Priority;
  string SharedSecret;
};
```

## <a name="members"></a><span data-ttu-id="b2181-110">Members</span><span class="sxs-lookup"><span data-stu-id="b2181-110">Members</span></span>

<span data-ttu-id="b2181-111">La classe **Win32 \_ TSGatewayRADIUSServer** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="b2181-111">The **Win32\_TSGatewayRADIUSServer** class has these types of members:</span></span>

-   [<span data-ttu-id="b2181-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="b2181-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="b2181-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b2181-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="b2181-114">Metodi</span><span class="sxs-lookup"><span data-stu-id="b2181-114">Methods</span></span>

<span data-ttu-id="b2181-115">La classe **Win32 \_ TSGatewayRADIUSServer** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="b2181-115">The **Win32\_TSGatewayRADIUSServer** class has these methods.</span></span>



| <span data-ttu-id="b2181-116">Metodo</span><span class="sxs-lookup"><span data-stu-id="b2181-116">Method</span></span>                                                                 | <span data-ttu-id="b2181-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b2181-117">Description</span></span>                                                                  |
|:-----------------------------------------------------------------------|:-----------------------------------------------------------------------------|
| [<span data-ttu-id="b2181-118">**Aggiungere**</span><span class="sxs-lookup"><span data-stu-id="b2181-118">**Add**</span></span>](win32-tsgatewayradiusserver-add.md)                         | <span data-ttu-id="b2181-119">Aggiunge un nuovo server RADIUS.</span><span class="sxs-lookup"><span data-stu-id="b2181-119">Adds a new RADIUS server.</span></span><br/>                                         |
| [<span data-ttu-id="b2181-120">**MoveDown**</span><span class="sxs-lookup"><span data-stu-id="b2181-120">**MoveDown**</span></span>](movedown-win32-tsgatewayradiusserver.md)               | <span data-ttu-id="b2181-121">Sposta il server RADIUS una posizione verso il basso nell'ordine di priorità.</span><span class="sxs-lookup"><span data-stu-id="b2181-121">Moves this RADIUS server one position down in the priority order.</span></span><br/> |
| [<span data-ttu-id="b2181-122">**MoveUp**</span><span class="sxs-lookup"><span data-stu-id="b2181-122">**MoveUp**</span></span>](moveup-win32-tsgatewayradiusserver.md)                   | <span data-ttu-id="b2181-123">Sposta questo server RADIUS una posizione verso l'alto nell'ordine di priorità.</span><span class="sxs-lookup"><span data-stu-id="b2181-123">Moves this RADIUS server one position up in the priority order.</span></span><br/>   |
| [<span data-ttu-id="b2181-124">**Rimuovi**</span><span class="sxs-lookup"><span data-stu-id="b2181-124">**Remove**</span></span>](win32-tsgatewayradiusserver-remove.md)                   | <span data-ttu-id="b2181-125">Rimuove il server RADIUS corrente.</span><span class="sxs-lookup"><span data-stu-id="b2181-125">Removes the current RADIUS server.</span></span><br/>                                |
| [<span data-ttu-id="b2181-126">**SetName**</span><span class="sxs-lookup"><span data-stu-id="b2181-126">**SetName**</span></span>](setname-win32-tsgatewayradiusserver.md)                 | <span data-ttu-id="b2181-127">Imposta la proprietà **Name** per il server RADIUS.</span><span class="sxs-lookup"><span data-stu-id="b2181-127">Sets the **Name** property for this RADIUS server.</span></span><br/>                |
| [<span data-ttu-id="b2181-128">**SetSharedSecret**</span><span class="sxs-lookup"><span data-stu-id="b2181-128">**SetSharedSecret**</span></span>](setsharedsecret-win32-tsgatewayradiusserver.md) | <span data-ttu-id="b2181-129">Imposta la proprietà **SharedSecret** per questo server RADIUS.</span><span class="sxs-lookup"><span data-stu-id="b2181-129">Sets the **SharedSecret** property for this RADIUS server.</span></span><br/>        |
| [<span data-ttu-id="b2181-130">**Aggiornamento**</span><span class="sxs-lookup"><span data-stu-id="b2181-130">**Update**</span></span>](update-win32-tsgatewayradiusserver.md)                   | <span data-ttu-id="b2181-131">Aggiorna il server RADIUS corrente.</span><span class="sxs-lookup"><span data-stu-id="b2181-131">Updates the current RADIUS server.</span></span><br/>                                |



 

### <a name="properties"></a><span data-ttu-id="b2181-132">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b2181-132">Properties</span></span>

<span data-ttu-id="b2181-133">La classe **Win32 \_ TSGatewayRADIUSServer** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="b2181-133">The **Win32\_TSGatewayRADIUSServer** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b2181-134">**Nome**</span><span class="sxs-lookup"><span data-stu-id="b2181-134">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2181-135">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b2181-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2181-136">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b2181-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b2181-137">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="b2181-137">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="b2181-138">Nome del server RADIUS.</span><span class="sxs-lookup"><span data-stu-id="b2181-138">Name of the RADIUS server.</span></span> <span data-ttu-id="b2181-139">Questa proprietà può essere modificata con il metodo [**Sename**](setname-win32-tsgatewayradiusserver.md) .</span><span class="sxs-lookup"><span data-stu-id="b2181-139">This property can be changed with the [**SetName**](setname-win32-tsgatewayradiusserver.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="b2181-140">**Priorità**</span><span class="sxs-lookup"><span data-stu-id="b2181-140">**Priority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2181-141">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b2181-141">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b2181-142">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b2181-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b2181-143">Priorità del server RADIUS.</span><span class="sxs-lookup"><span data-stu-id="b2181-143">Priority of the RADIUS server.</span></span> <span data-ttu-id="b2181-144">Il server Gateway Desktop remoto cerca i CAPs RD nei server RADIUS in base alla priorità.</span><span class="sxs-lookup"><span data-stu-id="b2181-144">The RD Gateway server looks for RD CAPs on RADIUS servers based on the priority.</span></span> <span data-ttu-id="b2181-145">Questa proprietà può essere modificata con i metodi [**MoveUp**](moveup-win32-tsgatewayradiusserver.md), [**MoveDown**](movedown-win32-tsgatewayradiusserver.md), [**Add**](win32-tsgatewayradiusserver-add.md)e [**Remove**](win32-tsgatewayradiusserver-remove.md) .</span><span class="sxs-lookup"><span data-stu-id="b2181-145">This property can be changed with the [**MoveUp**](moveup-win32-tsgatewayradiusserver.md), [**MoveDown**](movedown-win32-tsgatewayradiusserver.md), [**Add**](win32-tsgatewayradiusserver-add.md), and [**Remove**](win32-tsgatewayradiusserver-remove.md) methods.</span></span>

</dd> <dt>

<span data-ttu-id="b2181-146">**SharedSecret**</span><span class="sxs-lookup"><span data-stu-id="b2181-146">**SharedSecret**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2181-147">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b2181-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2181-148">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b2181-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b2181-149">Segreto condiviso per il server RADIUS.</span><span class="sxs-lookup"><span data-stu-id="b2181-149">Shared secret for the RADIUS server.</span></span> <span data-ttu-id="b2181-150">Questa proprietà può essere modificata con il metodo [**SetSharedSecret**](setsharedsecret-win32-tsgatewayradiusserver.md) .</span><span class="sxs-lookup"><span data-stu-id="b2181-150">This property can be changed with the [**SetSharedSecret**](setsharedsecret-win32-tsgatewayradiusserver.md) method.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b2181-151">Commenti</span><span class="sxs-lookup"><span data-stu-id="b2181-151">Remarks</span></span>

<span data-ttu-id="b2181-152">Per utilizzare questa classe, è necessario essere membri del gruppo Administrators.</span><span class="sxs-lookup"><span data-stu-id="b2181-152">You must be a member of the Administrators group to use this class.</span></span>

<span data-ttu-id="b2181-153">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="b2181-153">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="b2181-154">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="b2181-154">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="b2181-155">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="b2181-155">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="b2181-156">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="b2181-156">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="b2181-157">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b2181-157">Requirements</span></span>



| <span data-ttu-id="b2181-158">Requisito</span><span class="sxs-lookup"><span data-stu-id="b2181-158">Requirement</span></span> | <span data-ttu-id="b2181-159">Valore</span><span class="sxs-lookup"><span data-stu-id="b2181-159">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b2181-160">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b2181-160">Minimum supported client</span></span><br/> | <span data-ttu-id="b2181-161">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="b2181-161">None supported</span></span><br/>                                                                |
| <span data-ttu-id="b2181-162">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b2181-162">Minimum supported server</span></span><br/> | <span data-ttu-id="b2181-163">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b2181-163">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="b2181-164">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="b2181-164">Namespace</span></span><br/>                | <span data-ttu-id="b2181-165">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="b2181-165">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="b2181-166">MOF</span><span class="sxs-lookup"><span data-stu-id="b2181-166">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b2181-167"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b2181-167"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="b2181-168">DLL</span><span class="sxs-lookup"><span data-stu-id="b2181-168">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b2181-169"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b2181-169"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="b2181-170">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b2181-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2181-171">**\_TSGatewayConnection Win32**</span><span class="sxs-lookup"><span data-stu-id="b2181-171">**Win32\_TSGatewayConnection**</span></span>](win32-tsgatewayconnection.md)
</dt> <dt>

[<span data-ttu-id="b2181-172">**\_TSGatewayConnectionAuthorizationPolicy Win32**</span><span class="sxs-lookup"><span data-stu-id="b2181-172">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> <dt>

[<span data-ttu-id="b2181-173">**\_TSGatewayLoadBalancer Win32**</span><span class="sxs-lookup"><span data-stu-id="b2181-173">**Win32\_TSGatewayLoadBalancer**</span></span>](win32-tsgatewayloadbalancer.md)
</dt> <dt>

[<span data-ttu-id="b2181-174">**\_TSGatewayResourceAuthorizationPolicy Win32**</span><span class="sxs-lookup"><span data-stu-id="b2181-174">**Win32\_TSGatewayResourceAuthorizationPolicy**</span></span>](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> <dt>

[<span data-ttu-id="b2181-175">**\_TSGatewayResourceGroup Win32**</span><span class="sxs-lookup"><span data-stu-id="b2181-175">**Win32\_TSGatewayResourceGroup**</span></span>](win32-tsgatewayresourcegroup.md)
</dt> <dt>

[<span data-ttu-id="b2181-176">**\_TSGatewayServerSettings Win32**</span><span class="sxs-lookup"><span data-stu-id="b2181-176">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 

