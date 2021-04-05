---
title: Classe MDM_Policy_User_Config01_EnterpriseCloudPrint02
description: La \_ classe del criterio MDM \_ utente \_ Config01 \_ EnterpriseCloudPrint02 rappresenta i criteri di stampa cloud disponibili.
ms.assetid: cc885184-1197-48c4-ba48-a2944a416534
keywords:
- Classe MDM_Policy_User_Config01_EnterpriseCloudPrint02
- Classe MDM_Policy_User_Config01_EnterpriseCloudPrint02, descritta
topic_type:
- apiref
api_name:
- MDM_Policy_User_Config01_EnterpriseCloudPrint02
- MDM_Policy_User_Config01_EnterpriseCloudPrint02.InstanceID
- MDM_Policy_User_Config01_EnterpriseCloudPrint02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2b9d42afbab4d3f17d91b6db630ef67faf6ccc7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873861"
---
# <a name="mdm_policy_user_config01_enterprisecloudprint02-class"></a><span data-ttu-id="bb89a-105">\_Utente criteri \_ MDM \_ Config01 \_ classe EnterpriseCloudPrint02</span><span class="sxs-lookup"><span data-stu-id="bb89a-105">MDM\_Policy\_User\_Config01\_EnterpriseCloudPrint02 class</span></span>

<span data-ttu-id="bb89a-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="bb89a-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="bb89a-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="bb89a-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="bb89a-108">La \_ classe del criterio MDM \_ utente \_ Config01 \_ EnterpriseCloudPrint02 rappresenta i criteri di stampa cloud disponibili.</span><span class="sxs-lookup"><span data-stu-id="bb89a-108">The MDM\_Policy\_User\_Config01\_EnterpriseCloudPrint02 class represents the available cloud print policies.</span></span>

<span data-ttu-id="bb89a-109">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="bb89a-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb89a-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bb89a-110">Syntax</span></span>

``` syntax
[InPartition("local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_User_Config01_EnterpriseCloudPrint02
{
  string InstanceID;
  string ParentID;
  string CloudPrinterDiscoveryEndPoint;
  string CloudPrintOAuthAuthority;
  string CloudPrintOAuthClientId;
  string CloudPrintResourceId;
  sint32 DiscoveryMaxPrinterLimit;
  string MopriaDiscoveryResourceId;
};
```

## <a name="members"></a><span data-ttu-id="bb89a-111">Members</span><span class="sxs-lookup"><span data-stu-id="bb89a-111">Members</span></span>

<span data-ttu-id="bb89a-112">La **classe \_ \_ \_ Config01 \_ EnterpriseCloudPrint02 dell'utente dei criteri MDM** ha questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="bb89a-112">The **MDM\_Policy\_User\_Config01\_EnterpriseCloudPrint02** class has these types of members:</span></span>

-   [<span data-ttu-id="bb89a-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="bb89a-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="bb89a-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="bb89a-114">Properties</span></span>

<span data-ttu-id="bb89a-115">La **classe \_ \_ \_ Config01 \_ EnterpriseCloudPrint02 dell'utente dei criteri MDM** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="bb89a-115">The **MDM\_Policy\_User\_Config01\_EnterpriseCloudPrint02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="bb89a-116">CloudPrinterDiscoveryEndPoint</span><span class="sxs-lookup"><span data-stu-id="bb89a-116">CloudPrinterDiscoveryEndPoint</span></span>](/windows/client-management/mdm/policy-csp-enterprisecloudprint#enterprisecloudprint-cloudprinterdiscoveryendpoint)
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb89a-117">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="bb89a-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bb89a-118">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="bb89a-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="bb89a-119">CloudPrintOAuthAuthority</span><span class="sxs-lookup"><span data-stu-id="bb89a-119">CloudPrintOAuthAuthority</span></span>](/windows/client-management/mdm/policy-csp-enterprisecloudprint#enterprisecloudprint-cloudprintoauthauthority)
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb89a-120">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="bb89a-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bb89a-121">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="bb89a-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="bb89a-122">CloudPrintOAuthClientId</span><span class="sxs-lookup"><span data-stu-id="bb89a-122">CloudPrintOAuthClientId</span></span>](/windows/client-management/mdm/policy-csp-enterprisecloudprint#enterprisecloudprint-cloudprintoauthclientid)
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb89a-123">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="bb89a-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bb89a-124">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="bb89a-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="bb89a-125">CloudPrintResourceId</span><span class="sxs-lookup"><span data-stu-id="bb89a-125">CloudPrintResourceId</span></span>](/windows/client-management/mdm/policy-csp-enterprisecloudprint#enterprisecloudprint-cloudprintresourceid)
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb89a-126">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="bb89a-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bb89a-127">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="bb89a-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="bb89a-128">DiscoveryMaxPrinterLimit</span><span class="sxs-lookup"><span data-stu-id="bb89a-128">DiscoveryMaxPrinterLimit</span></span>](/windows/client-management/mdm/policy-csp-enterprisecloudprint#enterprisecloudprint-discoverymaxprinterlimit)
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb89a-129">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="bb89a-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="bb89a-130">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="bb89a-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="bb89a-131">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="bb89a-131">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb89a-132">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="bb89a-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bb89a-133">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bb89a-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bb89a-134">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="bb89a-134">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="bb89a-135">MopriaDiscoveryResourceId</span><span class="sxs-lookup"><span data-stu-id="bb89a-135">MopriaDiscoveryResourceId</span></span>](/windows/client-management/mdm/policy-csp-enterprisecloudprint#enterprisecloudprint-mopriadiscoveryresourceid)
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb89a-136">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="bb89a-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bb89a-137">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="bb89a-137">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="bb89a-138">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="bb89a-138">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb89a-139">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="bb89a-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bb89a-140">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bb89a-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bb89a-141">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="bb89a-141">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bb89a-142">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bb89a-142">Requirements</span></span>



| <span data-ttu-id="bb89a-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="bb89a-143">Requirement</span></span> | <span data-ttu-id="bb89a-144">Valore</span><span class="sxs-lookup"><span data-stu-id="bb89a-144">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bb89a-145">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bb89a-145">Minimum supported client</span></span><br/> | <span data-ttu-id="bb89a-146">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="bb89a-146">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="bb89a-147">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bb89a-147">Minimum supported server</span></span><br/> | <span data-ttu-id="bb89a-148">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="bb89a-148">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="bb89a-149">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="bb89a-149">Namespace</span></span><br/>                | <span data-ttu-id="bb89a-150">\\ \\ Dmmap MDM CIMV2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="bb89a-150">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="bb89a-151">MOF</span><span class="sxs-lookup"><span data-stu-id="bb89a-151">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bb89a-152"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bb89a-152"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="bb89a-153">DLL</span><span class="sxs-lookup"><span data-stu-id="bb89a-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bb89a-154"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bb89a-154"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

