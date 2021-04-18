---
title: Classe Win32_SessionBrokerServiceProperties
description: Definisce la query per un servizio di gestore sessioni.
ms.assetid: fe7a0317-8b52-4685-9d0d-2f81058b4561
ms.tgt_platform: multiple
keywords:
- Classe Win32_SessionBrokerServiceProperties Servizi Desktop remoto
- Classe Win32_SessionBrokerServiceProperties Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- Win32_SessionBrokerServiceProperties
- Win32_SessionBrokerServiceProperties.SBNetworkName
- Win32_SessionBrokerServiceProperties.SBDbConnectionString
- Win32_SessionBrokerServiceProperties.SBDbSecondaryConnectionString
api_location:
- TssdWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 507c4211b9506e0635966e9541167d24495735ef
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518981"
---
# <a name="win32_sessionbrokerserviceproperties-class"></a><span data-ttu-id="50d61-105">Win32 \_ SessionBrokerServiceProperties (classe)</span><span class="sxs-lookup"><span data-stu-id="50d61-105">Win32\_SessionBrokerServiceProperties class</span></span>

<span data-ttu-id="50d61-106">Definisce la query per un servizio di gestore sessioni.</span><span class="sxs-lookup"><span data-stu-id="50d61-106">Defines the query for a session broker service.</span></span>

<span data-ttu-id="50d61-107">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="50d61-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="50d61-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="50d61-108">Syntax</span></span>

``` syntax
[dynamic, singleton, provider("Win32_WIN32_SESSIONBROKERSERVICEPROPERTIES_Prov"), AMENDMENT]
class Win32_SessionBrokerServiceProperties
{
  string SBNetworkName;
  string SBDbConnectionString;
  string SBDbSecondaryConnectionString;
};
```

## <a name="members"></a><span data-ttu-id="50d61-109">Members</span><span class="sxs-lookup"><span data-stu-id="50d61-109">Members</span></span>

<span data-ttu-id="50d61-110">La classe **Win32 \_ SessionBrokerServiceProperties** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="50d61-110">The **Win32\_SessionBrokerServiceProperties** class has these types of members:</span></span>

-   [<span data-ttu-id="50d61-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="50d61-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="50d61-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="50d61-112">Properties</span></span>](/windows)

### <a name="methods"></a><span data-ttu-id="50d61-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="50d61-113">Methods</span></span>

<span data-ttu-id="50d61-114">La classe **Win32 \_ SessionBrokerServiceProperties** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="50d61-114">The **Win32\_SessionBrokerServiceProperties** class has these methods.</span></span>



| <span data-ttu-id="50d61-115">Metodo</span><span class="sxs-lookup"><span data-stu-id="50d61-115">Method</span></span>                                                                                                | <span data-ttu-id="50d61-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="50d61-116">Description</span></span>                                                                                                                                                                                                                          |
|:------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="50d61-117">**DeleteSBDbConnectionString**</span><span class="sxs-lookup"><span data-stu-id="50d61-117">**DeleteSBDbConnectionString**</span></span>](win32-sessionbrokerserviceproperties-deletesbdbconnectionstring.md) | <span data-ttu-id="50d61-118">Elimina le stringhe di connessione del database (primaria e secondaria) dal registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="50d61-118">Deletes DB connection strings (primary and secondary) from the registry.</span></span><br/> <span data-ttu-id="50d61-119">**Windows server 2012 R2, Windows server 2012 e Windows server 2008 R2:** Questo metodo non è disponibile prima di Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="50d61-119">**Windows Server 2012 R2, Windows Server 2012 and Windows Server 2008 R2:** This method is not available prior to Windows Server 2016</span></span><br/> |
| [<span data-ttu-id="50d61-120">**InstallBrokerDatabase**</span><span class="sxs-lookup"><span data-stu-id="50d61-120">**InstallBrokerDatabase**</span></span>](win32-sessionbrokerserviceproperties-installbrokerdatabase.md)           | <span data-ttu-id="50d61-121">Installa il database gestore connessione Desktop remoto nella SQL Server centrale</span><span class="sxs-lookup"><span data-stu-id="50d61-121">Installs RD Connection Broker DB on central SQL Server</span></span><br/>                                                                                                                                                                    |
| [<span data-ttu-id="50d61-122">**IsDbReachable**</span><span class="sxs-lookup"><span data-stu-id="50d61-122">**IsDbReachable**</span></span>](win32-sessionbrokerserviceproperties-isdbreachable.md)                           | <span data-ttu-id="50d61-123">Controlla se il database è raggiungibile</span><span class="sxs-lookup"><span data-stu-id="50d61-123">Checks if DB is reachable</span></span><br/>                                                                                                                                                                                                 |
| [<span data-ttu-id="50d61-124">**SetBrokerHAMode**</span><span class="sxs-lookup"><span data-stu-id="50d61-124">**SetBrokerHAMode**</span></span>](win32-sessionbrokerserviceproperties-setbrokerhamode.md)                       | <span data-ttu-id="50d61-125">Esegue la migrazione dei dati dal database WID locale al nuovo database basato su SQL Server.</span><span class="sxs-lookup"><span data-stu-id="50d61-125">Migrates data from local WID DB to the new SQL Server based DB.</span></span> <span data-ttu-id="50d61-126">Configura inoltre il server Broker per l'utilizzo della SQL Server centrale</span><span class="sxs-lookup"><span data-stu-id="50d61-126">It also configures the broker server to use the central SQL Server</span></span><br/>                                                                                        |
| [<span data-ttu-id="50d61-127">**SetBrokerNonHAMode**</span><span class="sxs-lookup"><span data-stu-id="50d61-127">**SetBrokerNonHAMode**</span></span>](win32-sessionbrokerserviceproperties-setbrokernonhamode.md)                 | <span data-ttu-id="50d61-128">Esegue la migrazione dei dati dal SQL Server centrale al database locale.</span><span class="sxs-lookup"><span data-stu-id="50d61-128">Migrates data from central SQL Server to local DB.</span></span> <span data-ttu-id="50d61-129">Configura inoltre il server Broker per l'utilizzo del database locale.</span><span class="sxs-lookup"><span data-stu-id="50d61-129">It also configures the broker server to use the local DB.</span></span><br/>                                                                                                              |
| [<span data-ttu-id="50d61-130">**SetSBDbConnectionStrings**</span><span class="sxs-lookup"><span data-stu-id="50d61-130">**SetSBDbConnectionStrings**</span></span>](win32-sessionbrokerserviceproperties-setsbdbconnectionstrings.md)     | <span data-ttu-id="50d61-131">Salva le stringhe di connessione del database (primaria e secondaria) nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="50d61-131">Saves DB connection strings (primary and secondary) in the registry.</span></span><br/> <span data-ttu-id="50d61-132">**Windows server 2012 R2, Windows server 2012 e Windows server 2008 R2:** Questo metodo non è disponibile prima di Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="50d61-132">**Windows Server 2012 R2, Windows Server 2012 and Windows Server 2008 R2:** This method is not available prior to Windows Server 2016</span></span><br/>     |



 

### <a name="properties"></a><span data-ttu-id="50d61-133">Proprietà</span><span class="sxs-lookup"><span data-stu-id="50d61-133">Properties</span></span>

<span data-ttu-id="50d61-134">La classe **Win32 \_ SessionBrokerServiceProperties** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="50d61-134">The **Win32\_SessionBrokerServiceProperties** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="50d61-135">**SBDbConnectionString**</span><span class="sxs-lookup"><span data-stu-id="50d61-135">**SBDbConnectionString**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="50d61-136">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="50d61-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="50d61-137">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="50d61-137">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="50d61-138">Stringa di connessione del database utilizzata dal servizio Gestore sessioni.</span><span class="sxs-lookup"><span data-stu-id="50d61-138">Database connection string used by Session Broker service.</span></span>

<span data-ttu-id="50d61-139">**Windows Server 2008 R2:** Questa proprietà non è disponibile prima di Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="50d61-139">**Windows Server 2008 R2:** This property is not available prior to Windows Server 2012</span></span>

</dd> <dt>

<span data-ttu-id="50d61-140">**SBDbSecondaryConnectionString**</span><span class="sxs-lookup"><span data-stu-id="50d61-140">**SBDbSecondaryConnectionString**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="50d61-141">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="50d61-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="50d61-142">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="50d61-142">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="50d61-143">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="50d61-143">Optional.</span></span> <span data-ttu-id="50d61-144">Stringa di connessione al database secondario, usata dal servizio Broker di sessione per supportare la scadenza della password.</span><span class="sxs-lookup"><span data-stu-id="50d61-144">Secondary database connection string, used by Session Broker service to support password expiration.</span></span>

<span data-ttu-id="50d61-145">**Windows server 2012 R2, Windows server 2012 e Windows server 2008 R2:** Questa proprietà non è disponibile prima di Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="50d61-145">**Windows Server 2012 R2, Windows Server 2012 and Windows Server 2008 R2:** This property is not available prior to Windows Server 2016</span></span>

</dd> <dt>

<span data-ttu-id="50d61-146">**SBNetworkName**</span><span class="sxs-lookup"><span data-stu-id="50d61-146">**SBNetworkName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="50d61-147">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="50d61-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="50d61-148">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="50d61-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="50d61-149">Nome di rete utilizzato dal servizio Broker di sessione.</span><span class="sxs-lookup"><span data-stu-id="50d61-149">The network name used by the session broker service.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="50d61-150">Requisiti</span><span class="sxs-lookup"><span data-stu-id="50d61-150">Requirements</span></span>



| <span data-ttu-id="50d61-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="50d61-151">Requirement</span></span> | <span data-ttu-id="50d61-152">Valore</span><span class="sxs-lookup"><span data-stu-id="50d61-152">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="50d61-153">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="50d61-153">Minimum supported client</span></span><br/> | <span data-ttu-id="50d61-154">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="50d61-154">None supported</span></span><br/>                                                              |
| <span data-ttu-id="50d61-155">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="50d61-155">Minimum supported server</span></span><br/> | <span data-ttu-id="50d61-156">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="50d61-156">Windows Server 2008 R2</span></span><br/>                                                      |
| <span data-ttu-id="50d61-157">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="50d61-157">Namespace</span></span><br/>                | <span data-ttu-id="50d61-158">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="50d61-158">Root\\CIMv2\\TerminalServices</span></span><br/>                                               |
| <span data-ttu-id="50d61-159">MOF</span><span class="sxs-lookup"><span data-stu-id="50d61-159">MOF</span></span><br/>                      | <dl> <span data-ttu-id="50d61-160"><dt>TssdWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="50d61-160"><dt>TssdWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="50d61-161">DLL</span><span class="sxs-lookup"><span data-stu-id="50d61-161">DLL</span></span><br/>                      | <dl> <span data-ttu-id="50d61-162"><dt>TssdWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="50d61-162"><dt>TssdWmi.dll</dt></span></span> </dl> |



 

