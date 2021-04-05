---
title: Classe MDM_VPNv2_RouteList02_01
description: La \_ classe MDM VPNv2 \_ RouteList02 \_ 01 contiene un elenco facoltativo di route da aggiungere alla tabella di routing per l'interfaccia VPN.
ms.assetid: 4271b0c4-9d29-4148-b956-ac9306316c9b
keywords:
- Classe MDM_VPNv2_RouteList02_01
- Classe MDM_VPNv2_RouteList02_01, descritta
topic_type:
- apiref
api_name:
- MDM_VPNv2_RouteList02_01
- MDM_VPNv2_RouteList02_01.InstanceID
- MDM_VPNv2_RouteList02_01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ebc274bb3efd2bc78850dd37c95b25db35c4cbe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048583"
---
# <a name="mdm_vpnv2_routelist02_01-class"></a><span data-ttu-id="f9e73-105">\_Classe MDM VPNv2 \_ RouteList02 \_ 01</span><span class="sxs-lookup"><span data-stu-id="f9e73-105">MDM\_VPNv2\_RouteList02\_01 class</span></span>

<span data-ttu-id="f9e73-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="f9e73-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="f9e73-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="f9e73-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="f9e73-108">La classe **MDM \_ VPNv2 \_ RouteList02 \_ 01** contiene un elenco facoltativo di route da aggiungere alla tabella di routing per l'interfaccia VPN.</span><span class="sxs-lookup"><span data-stu-id="f9e73-108">The **MDM\_VPNv2\_RouteList02\_01** class contains an optional list of routes to be added to the routing table for the VPN interface.</span></span>

<span data-ttu-id="f9e73-109">Questa operazione è necessaria per i casi di split tunneling in cui il sito del server VPN ha più subnet che la subnet predefinita in base all'indirizzo IP assegnato all'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="f9e73-109">This is required for split tunneling case where the VPN server site has more subnets that the default subnet based on the IP assigned to the interface.</span></span>

<span data-ttu-id="f9e73-110">Ogni computer su cui è in esecuzione TCP/IP prende decisioni di routing.</span><span class="sxs-lookup"><span data-stu-id="f9e73-110">Every computer that runs TCP/IP makes routing decisions.</span></span> <span data-ttu-id="f9e73-111">Queste decisioni sono controllate dalla tabella di routing IP.</span><span class="sxs-lookup"><span data-stu-id="f9e73-111">These decisions are controlled by the IP routing table.</span></span> <span data-ttu-id="f9e73-112">L'aggiunta di valori in questo nodo aggiorna la tabella di routing con le route per l'interfaccia VPN post-connessione.</span><span class="sxs-lookup"><span data-stu-id="f9e73-112">Adding values under this node updates the routing table with routes for the VPN interface post connection.</span></span> <span data-ttu-id="f9e73-113">I valori in questo nodo rappresentano il prefisso di destinazione delle route IP.</span><span class="sxs-lookup"><span data-stu-id="f9e73-113">The values under this node represent the destination prefix of IP routes.</span></span> <span data-ttu-id="f9e73-114">Un prefisso di destinazione è costituito da un prefisso di indirizzo IP e da una lunghezza del prefisso.</span><span class="sxs-lookup"><span data-stu-id="f9e73-114">A destination prefix consists of an IP address prefix and a prefix length.</span></span>

<span data-ttu-id="f9e73-115">L'aggiunta di una route consente allo stack di rete di identificare il traffico che deve superare l'interfaccia VPN per la VPN con split tunneling.</span><span class="sxs-lookup"><span data-stu-id="f9e73-115">Adding a route here allows the networking stack to identify the traffic that needs to go over the VPN interface for split tunnel VPN.</span></span> <span data-ttu-id="f9e73-116">Alcuni server VPN possono configurarla durante la negoziazione della connessione e non necessitano di queste informazioni nel profilo VPN.</span><span class="sxs-lookup"><span data-stu-id="f9e73-116">Some VPN servers can configure this during connect negotiation and do not need this information in the VPN Profile.</span></span> <span data-ttu-id="f9e73-117">Rivolgersi all'amministratore del server VPN per determinare se sono necessarie queste informazioni nel profilo VPN.</span><span class="sxs-lookup"><span data-stu-id="f9e73-117">Please check with your VPN server administrator to determine whether you need this information in the VPN profile.</span></span>

<span data-ttu-id="f9e73-118">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="f9e73-118">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9e73-119">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f9e73-119">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_VPNv2_RouteList02_01
{
  string InstanceID;
  string ParentID;
  string Address;
  sint32 PrefixSize;
};
```

## <a name="members"></a><span data-ttu-id="f9e73-120">Members</span><span class="sxs-lookup"><span data-stu-id="f9e73-120">Members</span></span>

<span data-ttu-id="f9e73-121">La classe **MDM \_ VPNv2 \_ RouteList02 \_ 01** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="f9e73-121">The **MDM\_VPNv2\_RouteList02\_01** class has these types of members:</span></span>

-   [<span data-ttu-id="f9e73-122">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f9e73-122">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f9e73-123">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f9e73-123">Properties</span></span>

<span data-ttu-id="f9e73-124">La classe **MDM \_ VPNv2 \_ RouteList02 \_ 01** presenta queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="f9e73-124">The **MDM\_VPNv2\_RouteList02\_01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="f9e73-125">Indirizzo</span><span class="sxs-lookup"><span data-stu-id="f9e73-125">Address</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-routelist-routerowid-address)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9e73-126">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f9e73-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f9e73-127">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="f9e73-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f9e73-128">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="f9e73-128">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9e73-129">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f9e73-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f9e73-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f9e73-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f9e73-131">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="f9e73-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="f9e73-132">Identifica il nome del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="f9e73-132">Identifies the name of the parent node.</span></span>

</dd> <dt>

<span data-ttu-id="f9e73-133">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="f9e73-133">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9e73-134">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f9e73-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f9e73-135">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f9e73-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f9e73-136">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="f9e73-136">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="f9e73-137">Descrive il percorso completo del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="f9e73-137">Describes the full path to the parent node.</span></span> <span data-ttu-id="f9e73-138">Per questa classe la stringa è "./Vendor/MSFT/VPNv2/*ProfileName*/RouteList"</span><span class="sxs-lookup"><span data-stu-id="f9e73-138">For this class, the string is "./Vendor/MSFT/VPNv2/*ProfileName*/RouteList"</span></span>

</dd> <dt>

[<span data-ttu-id="f9e73-139">PrefixSize</span><span class="sxs-lookup"><span data-stu-id="f9e73-139">PrefixSize</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-routelist-routerowid-prefixsize)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9e73-140">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="f9e73-140">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f9e73-141">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="f9e73-141">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f9e73-142">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f9e73-142">Requirements</span></span>



| <span data-ttu-id="f9e73-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="f9e73-143">Requirement</span></span> | <span data-ttu-id="f9e73-144">Valore</span><span class="sxs-lookup"><span data-stu-id="f9e73-144">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f9e73-145">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f9e73-145">Minimum supported client</span></span><br/> | <span data-ttu-id="f9e73-146">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="f9e73-146">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f9e73-147">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f9e73-147">Minimum supported server</span></span><br/> | <span data-ttu-id="f9e73-148">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="f9e73-148">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="f9e73-149">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="f9e73-149">Namespace</span></span><br/>                | <span data-ttu-id="f9e73-150">\\ \\ Dmmap MDM CIMV2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="f9e73-150">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="f9e73-151">MOF</span><span class="sxs-lookup"><span data-stu-id="f9e73-151">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f9e73-152"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f9e73-152"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="f9e73-153">DLL</span><span class="sxs-lookup"><span data-stu-id="f9e73-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f9e73-154"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f9e73-154"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f9e73-155">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f9e73-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9e73-156">Utilizzo di script di PowerShell con il provider del Bridge WMI</span><span class="sxs-lookup"><span data-stu-id="f9e73-156">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

