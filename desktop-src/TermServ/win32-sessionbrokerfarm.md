---
title: Classe Win32_SessionBrokerFarm
description: Definisce la query per una farm di Service Broker di sessione.
ms.assetid: 55a2a7ea-e891-4723-b919-ee3c908eaffb
ms.tgt_platform: multiple
keywords:
- Classe Win32_SessionBrokerFarm Servizi Desktop remoto
- Classe Win32_SessionBrokerFarm Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- Win32_SessionBrokerFarm
- Win32_SessionBrokerFarm.PluginName
- Win32_SessionBrokerFarm.FarmName
api_location:
- TssdWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e6a3ccbb5e1e08a036fb9973d552db73ee1607c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476696"
---
# <a name="win32_sessionbrokerfarm-class"></a><span data-ttu-id="d83e5-105">Win32 \_ SessionBrokerFarm (classe)</span><span class="sxs-lookup"><span data-stu-id="d83e5-105">Win32\_SessionBrokerFarm class</span></span>

<span data-ttu-id="d83e5-106">Definisce la query per una farm di Service Broker di sessione.</span><span class="sxs-lookup"><span data-stu-id="d83e5-106">Defines the query for a session broker farm.</span></span>

<span data-ttu-id="d83e5-107">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="d83e5-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="d83e5-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d83e5-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_WIN32_SESSIONBROKERFARM_Prov"), AMENDMENT]
class Win32_SessionBrokerFarm
{
  string PluginName;
  string FarmName;
};
```

## <a name="members"></a><span data-ttu-id="d83e5-109">Members</span><span class="sxs-lookup"><span data-stu-id="d83e5-109">Members</span></span>

<span data-ttu-id="d83e5-110">La classe **Win32 \_ SessionBrokerFarm** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="d83e5-110">The **Win32\_SessionBrokerFarm** class has these types of members:</span></span>

-   [<span data-ttu-id="d83e5-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="d83e5-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d83e5-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="d83e5-112">Properties</span></span>

<span data-ttu-id="d83e5-113">La classe **Win32 \_ SessionBrokerFarm** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="d83e5-113">The **Win32\_SessionBrokerFarm** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d83e5-114">**Farmname**</span><span class="sxs-lookup"><span data-stu-id="d83e5-114">**FarmName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d83e5-115">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d83e5-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d83e5-116">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d83e5-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d83e5-117">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="d83e5-117">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="d83e5-118">Nome della farm di broker di sessione su cui è necessario eseguire una query.</span><span class="sxs-lookup"><span data-stu-id="d83e5-118">The name of the session broker farm that needs to be queried.</span></span>

</dd> <dt>

<span data-ttu-id="d83e5-119">**PluginName**</span><span class="sxs-lookup"><span data-stu-id="d83e5-119">**PluginName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d83e5-120">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d83e5-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d83e5-121">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d83e5-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d83e5-122">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="d83e5-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="d83e5-123">Nome del plug-in.</span><span class="sxs-lookup"><span data-stu-id="d83e5-123">The name of the plug-in.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="d83e5-124">Esempio</span><span class="sxs-lookup"><span data-stu-id="d83e5-124">Examples</span></span>

<span data-ttu-id="d83e5-125">Nella stringa di query seguente viene illustrato il modo in cui la classe **Win32 \_ SessionBrokerFarm** viene utilizzata in una query.</span><span class="sxs-lookup"><span data-stu-id="d83e5-125">The following query string demonstrates how the **Win32\_SessionBrokerFarm** class is used in a query.</span></span>


```CSharp
queryString = string.Format("SELECT * FROM Win32_SessionBrokerFarm WHERE PluginName = '{0}'", pluginName);
```



## <a name="requirements"></a><span data-ttu-id="d83e5-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d83e5-126">Requirements</span></span>



| <span data-ttu-id="d83e5-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="d83e5-127">Requirement</span></span> | <span data-ttu-id="d83e5-128">Valore</span><span class="sxs-lookup"><span data-stu-id="d83e5-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d83e5-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d83e5-129">Minimum supported client</span></span><br/> | <span data-ttu-id="d83e5-130">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="d83e5-130">None supported</span></span><br/>                                                              |
| <span data-ttu-id="d83e5-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d83e5-131">Minimum supported server</span></span><br/> | <span data-ttu-id="d83e5-132">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="d83e5-132">Windows Server 2008 R2</span></span><br/>                                                      |
| <span data-ttu-id="d83e5-133">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="d83e5-133">Namespace</span></span><br/>                | <span data-ttu-id="d83e5-134">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="d83e5-134">Root\\CIMv2\\TerminalServices</span></span><br/>                                               |
| <span data-ttu-id="d83e5-135">MOF</span><span class="sxs-lookup"><span data-stu-id="d83e5-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d83e5-136"><dt>TssdWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d83e5-136"><dt>TssdWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="d83e5-137">DLL</span><span class="sxs-lookup"><span data-stu-id="d83e5-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d83e5-138"><dt>TssdWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d83e5-138"><dt>TssdWmi.dll</dt></span></span> </dl> |



 

