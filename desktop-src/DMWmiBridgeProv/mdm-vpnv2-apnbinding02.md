---
title: Classe MDM_VPNv2_APNBinding02
description: Riservato per usi futuri. | Classe MDM_VPNv2_APNBinding02
ms.assetid: ef530e79-b9cc-4bee-8d7b-45227ed55dbe
keywords:
- Classe MDM_VPNv2_APNBinding02
- Classe MDM_VPNv2_APNBinding02, descritta
topic_type:
- apiref
api_name:
- MDM_VPNv2_APNBinding02
- MDM_VPNv2_APNBinding02.InstanceID
- MDM_VPNv2_APNBinding02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d4447d1403903c9633523466504817338db969f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104352401"
---
# <a name="mdm_vpnv2_apnbinding02-class"></a><span data-ttu-id="d151c-106">\_Classe MDM VPNv2 \_ APNBinding02</span><span class="sxs-lookup"><span data-stu-id="d151c-106">MDM\_VPNv2\_APNBinding02 class</span></span>

<span data-ttu-id="d151c-107">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="d151c-107">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="d151c-108">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="d151c-108">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="d151c-109">Riservato per utilizzi futuri</span><span class="sxs-lookup"><span data-stu-id="d151c-109">Reserved for Future Use</span></span>

<span data-ttu-id="d151c-110">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="d151c-110">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="d151c-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d151c-111">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_VPNv2_APNBinding02
{
  string  InstanceID;
  string  ParentID;
  string  ProviderId;
  string  AccessPointName;
  string  UserName;
  string  Password;
  boolean IsCompressionEnabled;
  string  AuthenticationType;
};
```

## <a name="members"></a><span data-ttu-id="d151c-112">Members</span><span class="sxs-lookup"><span data-stu-id="d151c-112">Members</span></span>

<span data-ttu-id="d151c-113">La classe **MDM \_ VPNv2 \_ APNBinding02** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="d151c-113">The **MDM\_VPNv2\_APNBinding02** class has these types of members:</span></span>

-   [<span data-ttu-id="d151c-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="d151c-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d151c-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="d151c-115">Properties</span></span>

<span data-ttu-id="d151c-116">La classe **MDM \_ VPNv2 \_ APNBinding02** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="d151c-116">The **MDM\_VPNv2\_APNBinding02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="d151c-117">AccessPointName</span><span class="sxs-lookup"><span data-stu-id="d151c-117">AccessPointName</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-apnbinding-accesspointname)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d151c-118">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d151c-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d151c-119">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="d151c-119">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d151c-120">AuthenticationType</span><span class="sxs-lookup"><span data-stu-id="d151c-120">AuthenticationType</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-apnbinding-authenticationtype)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d151c-121">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d151c-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d151c-122">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="d151c-122">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="d151c-123">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="d151c-123">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d151c-124">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d151c-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d151c-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d151c-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d151c-126">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="d151c-126">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="d151c-127">Riservato per utilizzi futuri.</span><span class="sxs-lookup"><span data-stu-id="d151c-127">Reserved for future use.</span></span>

</dd> <dt>

[<span data-ttu-id="d151c-128">IsCompressionEnabled</span><span class="sxs-lookup"><span data-stu-id="d151c-128">IsCompressionEnabled</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-apnbinding-iscompressionenabled)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d151c-129">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="d151c-129">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d151c-130">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="d151c-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="d151c-131">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="d151c-131">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d151c-132">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d151c-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d151c-133">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d151c-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d151c-134">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="d151c-134">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="d151c-135">Riservato per utilizzi futuri.</span><span class="sxs-lookup"><span data-stu-id="d151c-135">Reserved for future use.</span></span>

</dd> <dt>

[<span data-ttu-id="d151c-136">Password</span><span class="sxs-lookup"><span data-stu-id="d151c-136">Password</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-apnbinding-password)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d151c-137">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d151c-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d151c-138">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="d151c-138">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d151c-139">ProviderId</span><span class="sxs-lookup"><span data-stu-id="d151c-139">ProviderId</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-apnbinding-providerid)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d151c-140">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d151c-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d151c-141">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="d151c-141">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d151c-142">UserName</span><span class="sxs-lookup"><span data-stu-id="d151c-142">UserName</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-apnbinding-username)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d151c-143">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d151c-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d151c-144">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="d151c-144">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d151c-145">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d151c-145">Requirements</span></span>



| <span data-ttu-id="d151c-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="d151c-146">Requirement</span></span> | <span data-ttu-id="d151c-147">Valore</span><span class="sxs-lookup"><span data-stu-id="d151c-147">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d151c-148">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d151c-148">Minimum supported client</span></span><br/> | <span data-ttu-id="d151c-149">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="d151c-149">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d151c-150">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d151c-150">Minimum supported server</span></span><br/> | <span data-ttu-id="d151c-151">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="d151c-151">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="d151c-152">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="d151c-152">Namespace</span></span><br/>                | <span data-ttu-id="d151c-153">\\ \\ Dmmap MDM CIMV2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="d151c-153">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="d151c-154">MOF</span><span class="sxs-lookup"><span data-stu-id="d151c-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d151c-155"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d151c-155"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="d151c-156">DLL</span><span class="sxs-lookup"><span data-stu-id="d151c-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d151c-157"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d151c-157"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d151c-158">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d151c-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d151c-159">Utilizzo di script di PowerShell con il provider del Bridge WMI</span><span class="sxs-lookup"><span data-stu-id="d151c-159">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

