---
title: Classe MDM_VPNv2_Manual03
description: MDM \_ VPNv2 \_ Manual03class è un nodo facoltativo contenente le impostazioni manuali del server.
ms.assetid: c294c5a2-35e2-46ca-b7d8-9c63f9d3cdd6
keywords:
- Classe MDM_VPNv2_Manual03
- Classe MDM_VPNv2_Manual03, descritta
topic_type:
- apiref
api_name:
- MDM_VPNv2_Manual03
- MDM_VPNv2_Manual03.InstanceID
- MDM_VPNv2_Manual03.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 561e36d9a048e3a5a523770b9a3987a346fe2283
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964783"
---
# <a name="mdm_vpnv2_manual03-class"></a><span data-ttu-id="44439-105">\_Classe MDM VPNv2 \_ Manual03</span><span class="sxs-lookup"><span data-stu-id="44439-105">MDM\_VPNv2\_Manual03 class</span></span>

<span data-ttu-id="44439-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="44439-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="44439-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="44439-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="44439-108">La classe **MDM \_ VPNv2 \_ Manual03** è un nodo facoltativo contenente le impostazioni manuali del server.</span><span class="sxs-lookup"><span data-stu-id="44439-108">The **MDM\_VPNv2\_Manual03** class is an optional node containing the manual server settings.</span></span>

<span data-ttu-id="44439-109">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="44439-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="44439-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="44439-110">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_VPNv2_Manual03
{
  string InstanceID;
  string ParentID;
  string Server;
};
```

## <a name="members"></a><span data-ttu-id="44439-111">Members</span><span class="sxs-lookup"><span data-stu-id="44439-111">Members</span></span>

<span data-ttu-id="44439-112">La classe **MDM \_ VPNv2 \_ Manual03** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="44439-112">The **MDM\_VPNv2\_Manual03** class has these types of members:</span></span>

-   [<span data-ttu-id="44439-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="44439-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="44439-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="44439-114">Properties</span></span>

<span data-ttu-id="44439-115">La classe **MDM \_ VPNv2 \_ Manual03** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="44439-115">The **MDM\_VPNv2\_Manual03** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="44439-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="44439-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44439-117">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="44439-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="44439-118">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="44439-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="44439-119">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="44439-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="44439-120">Identifica il nome del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="44439-120">Identifies the name of the parent node.</span></span>

</dd> <dt>

<span data-ttu-id="44439-121">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="44439-121">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44439-122">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="44439-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="44439-123">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="44439-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="44439-124">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="44439-124">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="44439-125">Descrive il percorso completo del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="44439-125">Describes the full path to the parent node.</span></span> <span data-ttu-id="44439-126">Per questa classe la stringa è "./Vendor/MSFT/VPNv2/*ProfileName*/proxy/"</span><span class="sxs-lookup"><span data-stu-id="44439-126">For this class, the string is "./Vendor/MSFT/VPNv2/*ProfileName*/Proxy/"</span></span>

</dd> <dt>

[<span data-ttu-id="44439-127">Server</span><span class="sxs-lookup"><span data-stu-id="44439-127">Server</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-proxy-manual-server)
</dt> <dd> <dl> <dt>

<span data-ttu-id="44439-128">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="44439-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="44439-129">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="44439-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="44439-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="44439-130">Requirements</span></span>



| <span data-ttu-id="44439-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="44439-131">Requirement</span></span> | <span data-ttu-id="44439-132">Valore</span><span class="sxs-lookup"><span data-stu-id="44439-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="44439-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="44439-133">Minimum supported client</span></span><br/> | <span data-ttu-id="44439-134">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="44439-134">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="44439-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="44439-135">Minimum supported server</span></span><br/> | <span data-ttu-id="44439-136">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="44439-136">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="44439-137">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="44439-137">Namespace</span></span><br/>                | <span data-ttu-id="44439-138">\\ \\ Dmmap MDM CIMV2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="44439-138">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="44439-139">MOF</span><span class="sxs-lookup"><span data-stu-id="44439-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="44439-140"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="44439-140"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="44439-141">DLL</span><span class="sxs-lookup"><span data-stu-id="44439-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="44439-142"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="44439-142"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="44439-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="44439-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44439-144">Utilizzo di script di PowerShell con il provider del Bridge WMI</span><span class="sxs-lookup"><span data-stu-id="44439-144">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

