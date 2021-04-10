---
title: Classe Win32_SessionBrokerTarget
description: Definisce la query per una destinazione di Service Broker di sessione.
ms.assetid: 35de25da-cb89-4836-be14-9544b1264248
ms.tgt_platform: multiple
keywords:
- Classe Win32_SessionBrokerTarget Servizi Desktop remoto
- Classe Win32_SessionBrokerTarget Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- Win32_SessionBrokerTarget
- Win32_SessionBrokerTarget.PluginName
- Win32_SessionBrokerTarget.TargetName
- Win32_SessionBrokerTarget.FarmName
- Win32_SessionBrokerTarget.Guid
- Win32_SessionBrokerTarget.Environment
api_location:
- TssdWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16ceca0df64eeb9cd285737fee7c6ca6fa3a2e63
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874530"
---
# <a name="win32_sessionbrokertarget-class"></a><span data-ttu-id="9b1ea-105">Win32 \_ SessionBrokerTarget (classe)</span><span class="sxs-lookup"><span data-stu-id="9b1ea-105">Win32\_SessionBrokerTarget class</span></span>

<span data-ttu-id="9b1ea-106">Definisce la query per una destinazione di Service Broker di sessione.</span><span class="sxs-lookup"><span data-stu-id="9b1ea-106">Defines the query for a session broker target.</span></span>

<span data-ttu-id="9b1ea-107">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="9b1ea-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b1ea-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9b1ea-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_WIN32_SESSIONBROKERTARGET_Prov"), AMENDMENT]
class Win32_SessionBrokerTarget
{
  string PluginName;
  string TargetName;
  string FarmName;
  string Guid;
  string Environment;
};
```

## <a name="members"></a><span data-ttu-id="9b1ea-109">Members</span><span class="sxs-lookup"><span data-stu-id="9b1ea-109">Members</span></span>

<span data-ttu-id="9b1ea-110">La classe **Win32 \_ SessionBrokerTarget** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="9b1ea-110">The **Win32\_SessionBrokerTarget** class has these types of members:</span></span>

-   [<span data-ttu-id="9b1ea-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="9b1ea-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9b1ea-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="9b1ea-112">Properties</span></span>

<span data-ttu-id="9b1ea-113">La classe **Win32 \_ SessionBrokerTarget** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="9b1ea-113">The **Win32\_SessionBrokerTarget** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9b1ea-114">**Environment**</span><span class="sxs-lookup"><span data-stu-id="9b1ea-114">**Environment**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b1ea-115">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="9b1ea-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9b1ea-116">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9b1ea-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9b1ea-117">Nome dell'ambiente.</span><span class="sxs-lookup"><span data-stu-id="9b1ea-117">The environment name.</span></span> <span data-ttu-id="9b1ea-118">Nel caso di una macchina virtuale (VM) destinazione, potrebbe essere il nome host della VM.</span><span class="sxs-lookup"><span data-stu-id="9b1ea-118">In the case of a virtual machine (VM) target, this could be the VM host name.</span></span>

</dd> <dt>

<span data-ttu-id="9b1ea-119">**Farmname**</span><span class="sxs-lookup"><span data-stu-id="9b1ea-119">**FarmName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b1ea-120">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="9b1ea-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9b1ea-121">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9b1ea-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9b1ea-122">Nome della farm a cui appartiene la destinazione.</span><span class="sxs-lookup"><span data-stu-id="9b1ea-122">The name of the farm the target belongs to.</span></span>

</dd> <dt>

<span data-ttu-id="9b1ea-123">**GUID**</span><span class="sxs-lookup"><span data-stu-id="9b1ea-123">**Guid**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b1ea-124">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="9b1ea-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9b1ea-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9b1ea-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b1ea-126">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="9b1ea-126">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="9b1ea-127">Il GUID (se presente) della destinazione.</span><span class="sxs-lookup"><span data-stu-id="9b1ea-127">The GUID (if any) of the target.</span></span>

</dd> <dt>

<span data-ttu-id="9b1ea-128">**PluginName**</span><span class="sxs-lookup"><span data-stu-id="9b1ea-128">**PluginName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b1ea-129">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="9b1ea-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9b1ea-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9b1ea-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b1ea-131">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="9b1ea-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="9b1ea-132">Nome del plug-in.</span><span class="sxs-lookup"><span data-stu-id="9b1ea-132">The name of the plug-in.</span></span>

</dd> <dt>

<span data-ttu-id="9b1ea-133">**TargetName**</span><span class="sxs-lookup"><span data-stu-id="9b1ea-133">**TargetName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b1ea-134">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="9b1ea-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9b1ea-135">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9b1ea-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9b1ea-136">Nome della destinazione.</span><span class="sxs-lookup"><span data-stu-id="9b1ea-136">The name of the target.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="9b1ea-137">Esempio</span><span class="sxs-lookup"><span data-stu-id="9b1ea-137">Examples</span></span>

<span data-ttu-id="9b1ea-138">Nella stringa di query seguente viene illustrato il modo in cui la \_ classe Win32 SessionBrokerTarget viene utilizzata in una query.</span><span class="sxs-lookup"><span data-stu-id="9b1ea-138">The following query string demonstrates how the Win32\_SessionBrokerTarget class is used in a query.</span></span>


```CSharp
queryString = string.Format("SELECT * FROM Win32_SessionBrokerTarget WHERE PluginName = '{0}'", pluginName);
```



## <a name="requirements"></a><span data-ttu-id="9b1ea-139">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9b1ea-139">Requirements</span></span>



| <span data-ttu-id="9b1ea-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="9b1ea-140">Requirement</span></span> | <span data-ttu-id="9b1ea-141">Valore</span><span class="sxs-lookup"><span data-stu-id="9b1ea-141">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9b1ea-142">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9b1ea-142">Minimum supported client</span></span><br/> | <span data-ttu-id="9b1ea-143">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="9b1ea-143">None supported</span></span><br/>                                                              |
| <span data-ttu-id="9b1ea-144">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9b1ea-144">Minimum supported server</span></span><br/> | <span data-ttu-id="9b1ea-145">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="9b1ea-145">Windows Server 2008 R2</span></span><br/>                                                      |
| <span data-ttu-id="9b1ea-146">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="9b1ea-146">Namespace</span></span><br/>                | <span data-ttu-id="9b1ea-147">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="9b1ea-147">Root\\CIMv2\\TerminalServices</span></span><br/>                                               |
| <span data-ttu-id="9b1ea-148">MOF</span><span class="sxs-lookup"><span data-stu-id="9b1ea-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9b1ea-149"><dt>TssdWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9b1ea-149"><dt>TssdWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="9b1ea-150">DLL</span><span class="sxs-lookup"><span data-stu-id="9b1ea-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9b1ea-151"><dt>TssdWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9b1ea-151"><dt>TssdWmi.dll</dt></span></span> </dl> |



 

