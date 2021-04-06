---
title: Classe Win32_SessionDirectoryVMMPlugin
description: Rappresenta un plug-in Virtual Machine Manager (VMM) registrato con un broker di sessione.
ms.assetid: b5c5deb1-6c1b-4547-a24a-db3ce6654144
ms.tgt_platform: multiple
keywords:
- Classe Win32_SessionDirectoryVMMPlugin Servizi Desktop remoto
- Classe Win32_SessionDirectoryVMMPlugin Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- Win32_SessionDirectoryVMMPlugin
- Win32_SessionDirectoryVMMPlugin.sName
- Win32_SessionDirectoryVMMPlugin.sProvider
- Win32_SessionDirectoryVMMPlugin.sClassID
- Win32_SessionDirectoryVMMPlugin.sServiceLocation
- Win32_SessionDirectoryVMMPlugin.Priority
- Win32_SessionDirectoryVMMPlugin.Enabled
api_location:
- TssdWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c5fc6b899eaa264357527eb107e11ad5a40ad67
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963901"
---
# <a name="win32_sessiondirectoryvmmplugin-class"></a><span data-ttu-id="08e63-105">Win32 \_ SessionDirectoryVMMPlugin (classe)</span><span class="sxs-lookup"><span data-stu-id="08e63-105">Win32\_SessionDirectoryVMMPlugin class</span></span>

<span data-ttu-id="08e63-106">Rappresenta un plug-in Virtual Machine Manager (VMM) registrato con un broker di sessione.</span><span class="sxs-lookup"><span data-stu-id="08e63-106">Represents a virtual machine manager (VMM) plug-in registered with a session broker.</span></span>

<span data-ttu-id="08e63-107">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="08e63-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="08e63-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="08e63-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_WIN32_SESSIONDIRECTORYVMMPLUGIN_Prov"), AMENDMENT]
class Win32_SessionDirectoryVMMPlugin
{
  string  sName;
  string  sProvider;
  string  sClassID;
  string  sServiceLocation;
  sint32  Priority = 0;
  boolean Enabled = FALSE;
};
```

## <a name="members"></a><span data-ttu-id="08e63-109">Members</span><span class="sxs-lookup"><span data-stu-id="08e63-109">Members</span></span>

<span data-ttu-id="08e63-110">La classe **Win32 \_ SessionDirectoryVMMPlugin** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="08e63-110">The **Win32\_SessionDirectoryVMMPlugin** class has these types of members:</span></span>

-   [<span data-ttu-id="08e63-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="08e63-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="08e63-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="08e63-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="08e63-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="08e63-113">Methods</span></span>

<span data-ttu-id="08e63-114">La classe **Win32 \_ SessionDirectoryVMMPlugin** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="08e63-114">The **Win32\_SessionDirectoryVMMPlugin** class has these methods.</span></span>



| <span data-ttu-id="08e63-115">Metodo</span><span class="sxs-lookup"><span data-stu-id="08e63-115">Method</span></span>                                                                             | <span data-ttu-id="08e63-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="08e63-116">Description</span></span>                                                   |
|:-----------------------------------------------------------------------------------|:--------------------------------------------------------------|
| [<span data-ttu-id="08e63-117">**GetCurrentVMMPlugin**</span><span class="sxs-lookup"><span data-stu-id="08e63-117">**GetCurrentVMMPlugin**</span></span>](getcurrentvmmplugin-win32-sessiondirectoryvmmplugin.md) | <span data-ttu-id="08e63-118">Ottiene il plug-in con priorità più elevata attivato.</span><span class="sxs-lookup"><span data-stu-id="08e63-118">Gets the highest priority plug-in that is enabled.</span></span><br/> |
| [<span data-ttu-id="08e63-119">**RegisterVMMPlugin**</span><span class="sxs-lookup"><span data-stu-id="08e63-119">**RegisterVMMPlugin**</span></span>](registervmmplugin-win32-sessiondirectoryvmmplugin.md)     | <span data-ttu-id="08e63-120">Registra un nuovo plug-in VMM.</span><span class="sxs-lookup"><span data-stu-id="08e63-120">Registers a new VMM plug-in.</span></span><br/>                       |
| [<span data-ttu-id="08e63-121">**SetEnabled**</span><span class="sxs-lookup"><span data-stu-id="08e63-121">**SetEnabled**</span></span>](setenabled-win32-sessiondirectoryvmmplugin.md)                   | <span data-ttu-id="08e63-122">Abilita o Disabilita il plug-in.</span><span class="sxs-lookup"><span data-stu-id="08e63-122">Enables or disables the plug-in.</span></span><br/>                   |
| [<span data-ttu-id="08e63-123">**SetName**</span><span class="sxs-lookup"><span data-stu-id="08e63-123">**SetName**</span></span>](setname-win32-sessiondirectoryvmmplugin.md)                         | <span data-ttu-id="08e63-124">Imposta il nome del plug-in.</span><span class="sxs-lookup"><span data-stu-id="08e63-124">Sets the name of the plug-in.</span></span><br/>                      |
| [<span data-ttu-id="08e63-125">**SetPriority**</span><span class="sxs-lookup"><span data-stu-id="08e63-125">**SetPriority**</span></span>](setpriority-win32-sessiondirectoryvmmplugin.md)                 | <span data-ttu-id="08e63-126">Imposta la priorità del plug-in.</span><span class="sxs-lookup"><span data-stu-id="08e63-126">Sets the priority of the plug-in.</span></span><br/>                  |
| [<span data-ttu-id="08e63-127">**SqlProvider**</span><span class="sxs-lookup"><span data-stu-id="08e63-127">**SetProvider**</span></span>](setprovider-win32-sessiondirectoryvmmplugin.md)                 | <span data-ttu-id="08e63-128">Imposta il nome del provider del plug-in.</span><span class="sxs-lookup"><span data-stu-id="08e63-128">Sets the provider name of the plug-in.</span></span><br/>             |
| [<span data-ttu-id="08e63-129">**SetServiceLocation**</span><span class="sxs-lookup"><span data-stu-id="08e63-129">**SetServiceLocation**</span></span>](setservicelocation-win32-sessiondirectoryvmmplugin.md)   | <span data-ttu-id="08e63-130">Imposta la posizione del servizio del plug-in.</span><span class="sxs-lookup"><span data-stu-id="08e63-130">Sets the service location of the plug-in.</span></span><br/>          |
| [<span data-ttu-id="08e63-131">**UnregisterVMMPlugin**</span><span class="sxs-lookup"><span data-stu-id="08e63-131">**UnregisterVMMPlugin**</span></span>](unregistervmmplugin-win32-sessiondirectoryvmmplugin.md) | <span data-ttu-id="08e63-132">Annulla la registrazione del plug-in.</span><span class="sxs-lookup"><span data-stu-id="08e63-132">Unregisters the plug-in.</span></span><br/>                           |



 

### <a name="properties"></a><span data-ttu-id="08e63-133">Proprietà</span><span class="sxs-lookup"><span data-stu-id="08e63-133">Properties</span></span>

<span data-ttu-id="08e63-134">La classe **Win32 \_ SessionDirectoryVMMPlugin** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="08e63-134">The **Win32\_SessionDirectoryVMMPlugin** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="08e63-135">**Enabled**</span><span class="sxs-lookup"><span data-stu-id="08e63-135">**Enabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08e63-136">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="08e63-136">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="08e63-137">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="08e63-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08e63-138">Indica se il plug-in è abilitato o disabilitato.</span><span class="sxs-lookup"><span data-stu-id="08e63-138">Indicates whether the plug-in is enabled or disabled.</span></span> <span data-ttu-id="08e63-139">**True** se il plug-in è abilitato o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="08e63-139">**True** if the plug-in is enabled or **false** otherwise.</span></span> <span data-ttu-id="08e63-140">Il plug-in è disabilitato per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="08e63-140">The plug-in is disabled by default.</span></span>

</dd> <dt>

<span data-ttu-id="08e63-141">**Priorità**</span><span class="sxs-lookup"><span data-stu-id="08e63-141">**Priority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08e63-142">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="08e63-142">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="08e63-143">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="08e63-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="08e63-144">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="08e63-144">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="08e63-145">Priorità del plug-in.</span><span class="sxs-lookup"><span data-stu-id="08e63-145">The priority of the plug-in.</span></span> <span data-ttu-id="08e63-146">Maggiore è il valore, maggiore è la priorità del plug-in.</span><span class="sxs-lookup"><span data-stu-id="08e63-146">The higher the value, the higher the priority of the plug-in.</span></span> <span data-ttu-id="08e63-147">Per impostazione predefinita, la priorità è zero.</span><span class="sxs-lookup"><span data-stu-id="08e63-147">The priority is zero by default.</span></span>

</dd> <dt>

<span data-ttu-id="08e63-148">**sClassID**</span><span class="sxs-lookup"><span data-stu-id="08e63-148">**sClassID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08e63-149">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="08e63-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="08e63-150">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="08e63-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08e63-151">Identificatore di classe del plug-in.</span><span class="sxs-lookup"><span data-stu-id="08e63-151">The class identifier of the plug-in.</span></span>

</dd> <dt>

<span data-ttu-id="08e63-152">**sName**</span><span class="sxs-lookup"><span data-stu-id="08e63-152">**sName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08e63-153">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="08e63-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="08e63-154">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="08e63-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08e63-155">Nome del plug-in.</span><span class="sxs-lookup"><span data-stu-id="08e63-155">The name of the plug-in.</span></span>

</dd> <dt>

<span data-ttu-id="08e63-156">**sProvider**</span><span class="sxs-lookup"><span data-stu-id="08e63-156">**sProvider**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08e63-157">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="08e63-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="08e63-158">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="08e63-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08e63-159">Nome del provider del plug-in.</span><span class="sxs-lookup"><span data-stu-id="08e63-159">The name of the plug-in provider.</span></span>

</dd> <dt>

<span data-ttu-id="08e63-160">**sServiceLocation**</span><span class="sxs-lookup"><span data-stu-id="08e63-160">**sServiceLocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08e63-161">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="08e63-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="08e63-162">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="08e63-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08e63-163">Posizione del servizio che il plug-in deve contattare.</span><span class="sxs-lookup"><span data-stu-id="08e63-163">The service location that the plug-in should contact.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="08e63-164">Requisiti</span><span class="sxs-lookup"><span data-stu-id="08e63-164">Requirements</span></span>



| <span data-ttu-id="08e63-165">Requisito</span><span class="sxs-lookup"><span data-stu-id="08e63-165">Requirement</span></span> | <span data-ttu-id="08e63-166">Valore</span><span class="sxs-lookup"><span data-stu-id="08e63-166">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="08e63-167">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="08e63-167">Minimum supported client</span></span><br/> | <span data-ttu-id="08e63-168">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="08e63-168">None supported</span></span><br/>                                                              |
| <span data-ttu-id="08e63-169">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="08e63-169">Minimum supported server</span></span><br/> | <span data-ttu-id="08e63-170">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="08e63-170">Windows Server 2008 R2</span></span><br/>                                                      |
| <span data-ttu-id="08e63-171">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="08e63-171">Namespace</span></span><br/>                | <span data-ttu-id="08e63-172">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="08e63-172">Root\\CIMv2\\TerminalServices</span></span><br/>                                               |
| <span data-ttu-id="08e63-173">MOF</span><span class="sxs-lookup"><span data-stu-id="08e63-173">MOF</span></span><br/>                      | <dl> <span data-ttu-id="08e63-174"><dt>TssdWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="08e63-174"><dt>TssdWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="08e63-175">DLL</span><span class="sxs-lookup"><span data-stu-id="08e63-175">DLL</span></span><br/>                      | <dl> <span data-ttu-id="08e63-176"><dt>TssdWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="08e63-176"><dt>TssdWmi.dll</dt></span></span> </dl> |



 

