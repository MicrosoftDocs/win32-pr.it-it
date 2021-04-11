---
title: Classe MDM_VPNv2_DomainNameInformationList02_01
description: La \_ classe MDM VPNv2 \_ DomainNameInformationList02 \_ 01 descrive le regole della tabella dei criteri di risoluzione dei nomi per il profilo VPN.
ms.assetid: ed6863aa-f85e-4f65-9312-ddf60a8c0d5a
keywords:
- Classe MDM_VPNv2_DomainNameInformationList02_01
- Classe MDM_VPNv2_DomainNameInformationList02_01, descritta
topic_type:
- apiref
api_name:
- MDM_VPNv2_DomainNameInformationList02_01
- MDM_VPNv2_DomainNameInformationList02_01.InstanceID
- MDM_VPNv2_DomainNameInformationList02_01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec2fa2b6fd4216256a085caa23333bccc5f386d0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964784"
---
# <a name="mdm_vpnv2_domainnameinformationlist02_01-class"></a><span data-ttu-id="0ac81-105">\_Classe MDM VPNv2 \_ DomainNameInformationList02 \_ 01</span><span class="sxs-lookup"><span data-stu-id="0ac81-105">MDM\_VPNv2\_DomainNameInformationList02\_01 class</span></span>

<span data-ttu-id="0ac81-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="0ac81-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="0ac81-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="0ac81-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="0ac81-108">La classe **MDM \_ VPNv2 \_ DomainNameInformationList02 \_ 01** descrive le regole della tabella dei criteri di risoluzione dei nomi per il profilo VPN.</span><span class="sxs-lookup"><span data-stu-id="0ac81-108">The **MDM\_VPNv2\_DomainNameInformationList02\_01** class describes the Name Resolution Policy Table (NRPT) rules for the VPN profile.</span></span>

<span data-ttu-id="0ac81-109">La tabella dei criteri di risoluzione dei nomi è una tabella di spazi dei nomi e le impostazioni corrispondenti archiviate nel registro di sistema di Windows, che determinano il comportamento del client DNS quando inviano query e elaborano le risposte.</span><span class="sxs-lookup"><span data-stu-id="0ac81-109">The Name Resolution Policy Table (NRPT) is a table of namespaces and corresponding settings stored in the Windows registry that determines the DNS client behavior when issuing queries and processing responses.</span></span> <span data-ttu-id="0ac81-110">Ogni riga della tabella dei criteri di risoluzione dei nomi rappresenta una regola per una parte dello spazio dei nomi per cui il client DNS invia query.</span><span class="sxs-lookup"><span data-stu-id="0ac81-110">Each row in the NRPT represents a rule for a portion of the namespace for which the DNS client issues queries.</span></span> <span data-ttu-id="0ac81-111">Prima di emettere query di risoluzione dei nomi, il client DNS consulta la tabella dei criteri di risoluzione dei nomi per determinare se nella query è necessario impostare eventuali flag aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="0ac81-111">Before issuing name resolution queries, the DNS client consults the NRPT to determine if any additional flags must be set in the query.</span></span> <span data-ttu-id="0ac81-112">Dopo aver ricevuto la risposta, il client consulta di nuovo la tabella dei criteri di risoluzione dei nomi per verificare la presenza di requisiti di elaborazione o criteri specifici.</span><span class="sxs-lookup"><span data-stu-id="0ac81-112">After receiving the response, the client again consults the NRPT to check for any special processing or policy requirements.</span></span> <span data-ttu-id="0ac81-113">In assenza della tabella dei criteri di risoluzione dei nomi, il client opera in base ai server DNS e ai suffissi impostati sull'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="0ac81-113">In the absence of the NRPT, the client operates based on the DNS servers and suffixes set on the interface.</span></span>

<span data-ttu-id="0ac81-114">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="0ac81-114">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ac81-115">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0ac81-115">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_VPNv2_DomainNameInformationList02_01
{
  string InstanceID;
  string ParentID;
  string DomainName;
  string DomainNameType;
  string DnsServers;
  string WebProxyServers;
};
```

## <a name="members"></a><span data-ttu-id="0ac81-116">Members</span><span class="sxs-lookup"><span data-stu-id="0ac81-116">Members</span></span>

<span data-ttu-id="0ac81-117">La classe **MDM \_ VPNv2 \_ DomainNameInformationList02 \_ 01** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="0ac81-117">The **MDM\_VPNv2\_DomainNameInformationList02\_01** class has these types of members:</span></span>

-   [<span data-ttu-id="0ac81-118">Proprietà</span><span class="sxs-lookup"><span data-stu-id="0ac81-118">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0ac81-119">Proprietà</span><span class="sxs-lookup"><span data-stu-id="0ac81-119">Properties</span></span>

<span data-ttu-id="0ac81-120">La classe **MDM \_ VPNv2 \_ DomainNameInformationList02 \_ 01** presenta queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="0ac81-120">The **MDM\_VPNv2\_DomainNameInformationList02\_01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="0ac81-121">DnsServers</span><span class="sxs-lookup"><span data-stu-id="0ac81-121">DnsServers</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-domainnameinformationlist-dnirowid-dnsservers)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ac81-122">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0ac81-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ac81-123">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="0ac81-123">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ac81-124">NomeDominio</span><span class="sxs-lookup"><span data-stu-id="0ac81-124">DomainName</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-domainnameinformationlist-dnirowid-domainname)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ac81-125">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0ac81-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ac81-126">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="0ac81-126">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ac81-127">DomainNameType</span><span class="sxs-lookup"><span data-stu-id="0ac81-127">DomainNameType</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-domainnameinformationlist-dnirowid-domainnametype)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ac81-128">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0ac81-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ac81-129">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="0ac81-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="0ac81-130">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="0ac81-130">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ac81-131">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0ac81-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ac81-132">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0ac81-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0ac81-133">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="0ac81-133">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="0ac81-134">Identifica il nome del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="0ac81-134">Identifies the name of the parent node.</span></span>

</dd> <dt>

<span data-ttu-id="0ac81-135">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="0ac81-135">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ac81-136">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0ac81-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ac81-137">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0ac81-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0ac81-138">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="0ac81-138">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="0ac81-139">Descrive il percorso completo del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="0ac81-139">Describes the full path to the parent node.</span></span> <span data-ttu-id="0ac81-140">Per questa classe la stringa è "./Vendor/MSFT/VPNv2/*ProfileName*"</span><span class="sxs-lookup"><span data-stu-id="0ac81-140">For this class, the string is "./Vendor/MSFT/VPNv2/*ProfileName*"</span></span>

</dd> <dt>

[<span data-ttu-id="0ac81-141">WebProxyServers</span><span class="sxs-lookup"><span data-stu-id="0ac81-141">WebProxyServers</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-domainnameinformationlist-dnirowid-webproxyservers)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ac81-142">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0ac81-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ac81-143">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="0ac81-143">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0ac81-144">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0ac81-144">Requirements</span></span>



| <span data-ttu-id="0ac81-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="0ac81-145">Requirement</span></span> | <span data-ttu-id="0ac81-146">Valore</span><span class="sxs-lookup"><span data-stu-id="0ac81-146">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0ac81-147">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0ac81-147">Minimum supported client</span></span><br/> | <span data-ttu-id="0ac81-148">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="0ac81-148">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0ac81-149">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0ac81-149">Minimum supported server</span></span><br/> | <span data-ttu-id="0ac81-150">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="0ac81-150">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="0ac81-151">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="0ac81-151">Namespace</span></span><br/>                | <span data-ttu-id="0ac81-152">\\ \\ Dmmap MDM CIMV2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="0ac81-152">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="0ac81-153">MOF</span><span class="sxs-lookup"><span data-stu-id="0ac81-153">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0ac81-154"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0ac81-154"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="0ac81-155">DLL</span><span class="sxs-lookup"><span data-stu-id="0ac81-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0ac81-156"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0ac81-156"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0ac81-157">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0ac81-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ac81-158">Utilizzo di script di PowerShell con il provider del Bridge WMI</span><span class="sxs-lookup"><span data-stu-id="0ac81-158">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

