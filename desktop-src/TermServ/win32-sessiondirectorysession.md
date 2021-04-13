---
title: Classe Win32_SessionDirectorySession
description: Fornisce le proprietà per la visualizzazione delle proprietà di una sessione di gestore connessione Desktop remoto (Connessione Desktop remoto Broker).
ms.assetid: 34b5a898-3952-493c-ba62-dd0d298b0600
ms.tgt_platform: multiple
keywords:
- Classe Win32_SessionDirectorySession Servizi Desktop remoto
- Classe Win32_SessionDirectorySession Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- Win32_SessionDirectorySession
- Win32_SessionDirectorySession.ServerName
- Win32_SessionDirectorySession.SessionID
- Win32_SessionDirectorySession.UserName
- Win32_SessionDirectorySession.DomainName
- Win32_SessionDirectorySession.ServerIPAddress
- Win32_SessionDirectorySession.TSProtocol
- Win32_SessionDirectorySession.ApplicationType
- Win32_SessionDirectorySession.ResolutionWidth
- Win32_SessionDirectorySession.ResolutionHeight
- Win32_SessionDirectorySession.ColorDepth
- Win32_SessionDirectorySession.CreateTime
- Win32_SessionDirectorySession.DisconnectTime
- Win32_SessionDirectorySession.SessionState
api_location:
- TssdWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fba8fdbdffc764c3bdcc1a8f5bc53aa479f318d4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400369"
---
# <a name="win32_sessiondirectorysession-class"></a><span data-ttu-id="ec72d-105">Win32 \_ SessionDirectorySession (classe)</span><span class="sxs-lookup"><span data-stu-id="ec72d-105">Win32\_SessionDirectorySession class</span></span>

<span data-ttu-id="ec72d-106">Fornisce le proprietà per la visualizzazione delle proprietà di una sessione di gestore connessione Desktop remoto (Connessione Desktop remoto Broker).</span><span class="sxs-lookup"><span data-stu-id="ec72d-106">Provides properties for viewing the properties of a Remote Desktop Connection Broker (RD Connection Broker) session.</span></span>

> [!Note]  
> <span data-ttu-id="ec72d-107">In Windows Server 2008 R2 il nome di gestore sessioni Servizi terminal è stato modificato in Gestore connessione Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="ec72d-107">In Windows Server 2008 R2, the name of Terminal Services Session Broker (TS Session Broker) was changed to RD Connection Broker.</span></span> <span data-ttu-id="ec72d-108">Queste proprietà si applicano a tutti i sistemi operativi supportati se non diversamente specificato.</span><span class="sxs-lookup"><span data-stu-id="ec72d-108">These properties apply to all supported operating systems unless otherwise noted.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="ec72d-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ec72d-109">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_WIN32_SESSIONDIRECTORYSESSION_Prov"), AMENDMENT]
class Win32_SessionDirectorySession
{
  string   ServerName;
  uint32   SessionID;
  string   UserName;
  string   DomainName;
  string   ServerIPAddress;
  uint32   TSProtocol;
  string   ApplicationType;
  uint32   ResolutionWidth;
  uint32   ResolutionHeight;
  uint32   ColorDepth;
  DateTime CreateTime;
  DateTime DisconnectTime;
  uint32   SessionState;
};
```

## <a name="members"></a><span data-ttu-id="ec72d-110">Members</span><span class="sxs-lookup"><span data-stu-id="ec72d-110">Members</span></span>

<span data-ttu-id="ec72d-111">La classe **Win32 \_ SessionDirectorySession** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="ec72d-111">The **Win32\_SessionDirectorySession** class has these types of members:</span></span>

-   [<span data-ttu-id="ec72d-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ec72d-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ec72d-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ec72d-113">Properties</span></span>

<span data-ttu-id="ec72d-114">La classe **Win32 \_ SessionDirectorySession** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="ec72d-114">The **Win32\_SessionDirectorySession** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ec72d-115">**ApplicationType**</span><span class="sxs-lookup"><span data-stu-id="ec72d-115">**ApplicationType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec72d-116">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ec72d-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ec72d-117">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ec72d-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ec72d-118">Applicazione avviata con questa sessione.</span><span class="sxs-lookup"><span data-stu-id="ec72d-118">Application started with this session.</span></span> <span data-ttu-id="ec72d-119">Corrisponde alla proprietà **StartProgram** di [**IMsTscSecuredSettings**](imstscsecuredsettings-interface.md).</span><span class="sxs-lookup"><span data-stu-id="ec72d-119">This is the same as the **StartProgram** property of [**IMsTscSecuredSettings**](imstscsecuredsettings-interface.md).</span></span>

</dd> <dt>

<span data-ttu-id="ec72d-120">**ColorDepth**</span><span class="sxs-lookup"><span data-stu-id="ec72d-120">**ColorDepth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec72d-121">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ec72d-121">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ec72d-122">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ec72d-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ec72d-123">Profondità di colore della sessione, misurata in bit per pixel.</span><span class="sxs-lookup"><span data-stu-id="ec72d-123">Color depth of the session, measured in bits per pixel.</span></span>

</dd> <dt>

<span data-ttu-id="ec72d-124">**CreateTime**</span><span class="sxs-lookup"><span data-stu-id="ec72d-124">**CreateTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec72d-125">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="ec72d-125">Data type: **DateTime**</span></span>
</dt> <dt>

<span data-ttu-id="ec72d-126">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ec72d-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ec72d-127">Data e ora di creazione della sessione.</span><span class="sxs-lookup"><span data-stu-id="ec72d-127">Date and time the session was created.</span></span> <span data-ttu-id="ec72d-128">Questo valore non viene reimpostato quando una sessione viene disconnessa e riconnessa.</span><span class="sxs-lookup"><span data-stu-id="ec72d-128">This value is not reset when a session is disconnected and reconnected.</span></span>

</dd> <dt>

<span data-ttu-id="ec72d-129">**DisconnectTime**</span><span class="sxs-lookup"><span data-stu-id="ec72d-129">**DisconnectTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec72d-130">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="ec72d-130">Data type: **DateTime**</span></span>
</dt> <dt>

<span data-ttu-id="ec72d-131">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ec72d-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ec72d-132">Data e ora in cui la sessione è stata disconnessa (se applicabile).</span><span class="sxs-lookup"><span data-stu-id="ec72d-132">Date and time the session was disconnected (if applicable).</span></span>

</dd> <dt>

<span data-ttu-id="ec72d-133">**NomeDominio**</span><span class="sxs-lookup"><span data-stu-id="ec72d-133">**DomainName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec72d-134">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ec72d-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ec72d-135">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ec72d-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ec72d-136">Nome di dominio dell'utente connesso a questa sessione.</span><span class="sxs-lookup"><span data-stu-id="ec72d-136">Domain name of the user logged on to this session.</span></span>

</dd> <dt>

<span data-ttu-id="ec72d-137">**ResolutionHeight**</span><span class="sxs-lookup"><span data-stu-id="ec72d-137">**ResolutionHeight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec72d-138">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ec72d-138">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ec72d-139">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ec72d-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ec72d-140">Altezza della sessione, in pixel, per questa sessione.</span><span class="sxs-lookup"><span data-stu-id="ec72d-140">Height of the session, in pixels, for this session.</span></span>

</dd> <dt>

<span data-ttu-id="ec72d-141">**ResolutionWidth**</span><span class="sxs-lookup"><span data-stu-id="ec72d-141">**ResolutionWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec72d-142">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ec72d-142">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ec72d-143">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ec72d-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ec72d-144">Larghezza della sessione, in pixel, per questa sessione.</span><span class="sxs-lookup"><span data-stu-id="ec72d-144">Width of the session, in pixels, for this session.</span></span>

</dd> <dt>

<span data-ttu-id="ec72d-145">**ServerIPAddress**</span><span class="sxs-lookup"><span data-stu-id="ec72d-145">**ServerIPAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec72d-146">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ec72d-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ec72d-147">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ec72d-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ec72d-148">Indirizzo IP del server Gestore connessione Desktop remoto per questa sessione.</span><span class="sxs-lookup"><span data-stu-id="ec72d-148">IP address of the RD Connection Broker server for this session.</span></span>

</dd> <dt>

<span data-ttu-id="ec72d-149">**ServerName**</span><span class="sxs-lookup"><span data-stu-id="ec72d-149">**ServerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec72d-150">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ec72d-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ec72d-151">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ec72d-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ec72d-152">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="ec72d-152">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="ec72d-153">Nome del server Gestore connessione Desktop remoto per la sessione.</span><span class="sxs-lookup"><span data-stu-id="ec72d-153">Name of the RD Connection Broker server for this session.</span></span>

</dd> <dt>

<span data-ttu-id="ec72d-154">**SessionID**</span><span class="sxs-lookup"><span data-stu-id="ec72d-154">**SessionID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec72d-155">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ec72d-155">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ec72d-156">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ec72d-156">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ec72d-157">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="ec72d-157">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="ec72d-158">ID sessione per questa sessione.</span><span class="sxs-lookup"><span data-stu-id="ec72d-158">Session ID for this session.</span></span>

</dd> <dt>

<span data-ttu-id="ec72d-159">**SessionState**</span><span class="sxs-lookup"><span data-stu-id="ec72d-159">**SessionState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec72d-160">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ec72d-160">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ec72d-161">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ec72d-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ec72d-162">Stato della sessione.</span><span class="sxs-lookup"><span data-stu-id="ec72d-162">State of this session.</span></span>

<dt>

<span data-ttu-id="ec72d-163">0</span><span class="sxs-lookup"><span data-stu-id="ec72d-163">0</span></span>
</dt> <dd>

<span data-ttu-id="ec72d-164">La sessione è attiva.</span><span class="sxs-lookup"><span data-stu-id="ec72d-164">The session is active.</span></span>

</dd> <dt>

<span data-ttu-id="ec72d-165">1</span><span class="sxs-lookup"><span data-stu-id="ec72d-165">1</span></span>
</dt> <dd>

<span data-ttu-id="ec72d-166">La sessione è disconnessa.</span><span class="sxs-lookup"><span data-stu-id="ec72d-166">The session is disconnected.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ec72d-167">**TSProtocol**</span><span class="sxs-lookup"><span data-stu-id="ec72d-167">**TSProtocol**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec72d-168">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ec72d-168">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ec72d-169">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ec72d-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ec72d-170">Protocollo per questa sessione.</span><span class="sxs-lookup"><span data-stu-id="ec72d-170">Protocol for this session.</span></span>

<dt>

<span data-ttu-id="ec72d-171">0</span><span class="sxs-lookup"><span data-stu-id="ec72d-171">0</span></span>
</dt> <dd>

<span data-ttu-id="ec72d-172">Questa sessione è in esecuzione su una console fisica.</span><span class="sxs-lookup"><span data-stu-id="ec72d-172">This session is running on a physical console.</span></span>

</dd> <dt>

<span data-ttu-id="ec72d-173">1</span><span class="sxs-lookup"><span data-stu-id="ec72d-173">1</span></span>
</dt> <dd>

<span data-ttu-id="ec72d-174">Per questa sessione viene usato un protocollo di terze parti proprietario.</span><span class="sxs-lookup"><span data-stu-id="ec72d-174">A proprietary third-party protocol is used for this session.</span></span>

</dd> <dt>

<span data-ttu-id="ec72d-175">2</span><span class="sxs-lookup"><span data-stu-id="ec72d-175">2</span></span>
</dt> <dd>

<span data-ttu-id="ec72d-176">Per questa sessione viene usato Remote Desktop Protocol (RDP).</span><span class="sxs-lookup"><span data-stu-id="ec72d-176">Remote Desktop Protocol (RDP) is used for this session.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ec72d-177">**UserName**</span><span class="sxs-lookup"><span data-stu-id="ec72d-177">**UserName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec72d-178">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ec72d-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ec72d-179">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ec72d-179">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ec72d-180">Nome utente dell'utente che ha effettuato l'accesso a questa sessione.</span><span class="sxs-lookup"><span data-stu-id="ec72d-180">User name of the user logged on to this session.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ec72d-181">Commenti</span><span class="sxs-lookup"><span data-stu-id="ec72d-181">Remarks</span></span>

<span data-ttu-id="ec72d-182">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="ec72d-182">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="ec72d-183">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="ec72d-183">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="ec72d-184">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="ec72d-184">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="ec72d-185">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="ec72d-185">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="ec72d-186">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ec72d-186">Requirements</span></span>



| <span data-ttu-id="ec72d-187">Requisito</span><span class="sxs-lookup"><span data-stu-id="ec72d-187">Requirement</span></span> | <span data-ttu-id="ec72d-188">Valore</span><span class="sxs-lookup"><span data-stu-id="ec72d-188">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ec72d-189">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ec72d-189">Minimum supported client</span></span><br/> | <span data-ttu-id="ec72d-190">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="ec72d-190">None supported</span></span><br/>                                                              |
| <span data-ttu-id="ec72d-191">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ec72d-191">Minimum supported server</span></span><br/> | <span data-ttu-id="ec72d-192">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ec72d-192">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="ec72d-193">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="ec72d-193">Namespace</span></span><br/>                | <span data-ttu-id="ec72d-194">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="ec72d-194">Root\\CIMv2</span></span><br/>                                                                 |
| <span data-ttu-id="ec72d-195">MOF</span><span class="sxs-lookup"><span data-stu-id="ec72d-195">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ec72d-196"><dt>TssdWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ec72d-196"><dt>TssdWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="ec72d-197">DLL</span><span class="sxs-lookup"><span data-stu-id="ec72d-197">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ec72d-198"><dt>TssdWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ec72d-198"><dt>TssdWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ec72d-199">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ec72d-199">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec72d-200">**\_SessionDirectoryCluster Win32**</span><span class="sxs-lookup"><span data-stu-id="ec72d-200">**Win32\_SessionDirectoryCluster**</span></span>](win32-sessiondirectorycluster.md)
</dt> <dt>

[<span data-ttu-id="ec72d-201">**\_SessionDirectoryServer Win32**</span><span class="sxs-lookup"><span data-stu-id="ec72d-201">**Win32\_SessionDirectoryServer**</span></span>](win32-sessiondirectoryserver.md)
</dt> </dl>

 

