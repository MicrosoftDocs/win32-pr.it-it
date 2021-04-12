---
title: Classe MDM_EnterpriseAPN_01
description: La \_ classe MDM EnterpriseAPN \_ 01 viene usata dall'azienda per eseguire il provisioning di un APN per Internet.
ms.assetid: c5fc0a86-98b7-4d0c-aae5-be836e48eee7
keywords:
- Classe MDM_EnterpriseAPN_01
- Classe MDM_EnterpriseAPN_01, descritta
topic_type:
- apiref
api_name:
- MDM_EnterpriseAPN_01
- MDM_EnterpriseAPN_01.InstanceID
- MDM_EnterpriseAPN_01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2bf8b9563b2f681e71e355f4c21aa097eedf64a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104225219"
---
# <a name="mdm_enterpriseapn_01-class"></a><span data-ttu-id="89615-105">\_Classe MDM EnterpriseAPN \_ 01</span><span class="sxs-lookup"><span data-stu-id="89615-105">MDM\_EnterpriseAPN\_01 class</span></span>

<span data-ttu-id="89615-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="89615-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="89615-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="89615-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="89615-108">La classe **MDM \_ EnterpriseAPN \_ 01** viene usata dall'azienda per eseguire il provisioning di un APN per Internet.</span><span class="sxs-lookup"><span data-stu-id="89615-108">The **MDM\_EnterpriseAPN\_01** class is used by the enterprise to provision an APN for the Internet.</span></span>

<span data-ttu-id="89615-109">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="89615-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="89615-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="89615-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_EnterpriseAPN_01
{
  string  InstanceID;
  string  ParentID;
  string  APNName;
  string  IPType;
  boolean IsAttachAPN;
  string  ClassId;
  string  AuthType;
  string  UserName;
  string  Password;
  string  IccId;
  boolean AlwaysOn;
  boolean Enabled;
  string  Roaming;
};
```

## <a name="members"></a><span data-ttu-id="89615-111">Members</span><span class="sxs-lookup"><span data-stu-id="89615-111">Members</span></span>

<span data-ttu-id="89615-112">La classe **MDM \_ EnterpriseAPN \_ 01** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="89615-112">The **MDM\_EnterpriseAPN\_01** class has these types of members:</span></span>

-   [<span data-ttu-id="89615-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="89615-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="89615-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="89615-114">Properties</span></span>

<span data-ttu-id="89615-115">La classe **MDM \_ EnterpriseAPN \_ 01** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="89615-115">The **MDM\_EnterpriseAPN\_01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="89615-116">AlwaysOn</span><span class="sxs-lookup"><span data-stu-id="89615-116">AlwaysOn</span></span>](/windows/client-management/mdm/enterpriseapn-csp#enterpriseapn-connectionname-alwayson)
</dt> <dd> <dl> <dt>

<span data-ttu-id="89615-117">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="89615-117">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="89615-118">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="89615-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="89615-119">APNName</span><span class="sxs-lookup"><span data-stu-id="89615-119">APNName</span></span>](/windows/client-management/mdm/enterpriseapn-csp#enterpriseapn-connectionname-apnname)
</dt> <dd> <dl> <dt>

<span data-ttu-id="89615-120">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="89615-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="89615-121">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="89615-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="89615-122">AuthType</span><span class="sxs-lookup"><span data-stu-id="89615-122">AuthType</span></span>](/windows/client-management/mdm/enterpriseapn-csp#enterpriseapn-connectionname-authtype)
</dt> <dd> <dl> <dt>

<span data-ttu-id="89615-123">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="89615-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="89615-124">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="89615-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="89615-125">ClassId</span><span class="sxs-lookup"><span data-stu-id="89615-125">ClassId</span></span>](/windows/client-management/mdm/enterpriseapn-csp#enterpriseapn-connectionname-classid)
</dt> <dd> <dl> <dt>

<span data-ttu-id="89615-126">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="89615-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="89615-127">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="89615-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="89615-128">Enabled</span><span class="sxs-lookup"><span data-stu-id="89615-128">Enabled</span></span>](/windows/client-management/mdm/enterpriseapn-csp#enterpriseapn-connectionname-enabled)
</dt> <dd> <dl> <dt>

<span data-ttu-id="89615-129">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="89615-129">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="89615-130">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="89615-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="89615-131">IccId</span><span class="sxs-lookup"><span data-stu-id="89615-131">IccId</span></span>](/windows/client-management/mdm/enterpriseapn-csp#enterpriseapn-connectionname-iccid)
</dt> <dd> <dl> <dt>

<span data-ttu-id="89615-132">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="89615-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="89615-133">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="89615-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="89615-134">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="89615-134">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89615-135">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="89615-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="89615-136">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="89615-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="89615-137">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="89615-137">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="89615-138">Nome della connessione visualizzato da gestione connessione Windows.</span><span class="sxs-lookup"><span data-stu-id="89615-138">Name of the connection as seen by Windows Connection Manager.</span></span>

</dd> <dt>

[<span data-ttu-id="89615-139">IPType</span><span class="sxs-lookup"><span data-stu-id="89615-139">IPType</span></span>](/windows/client-management/mdm/enterpriseapn-csp#enterpriseapn-connectionname-iptype)
</dt> <dd> <dl> <dt>

<span data-ttu-id="89615-140">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="89615-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="89615-141">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="89615-141">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="89615-142">IsAttachAPN</span><span class="sxs-lookup"><span data-stu-id="89615-142">IsAttachAPN</span></span>](/windows/client-management/mdm/enterpriseapn-csp#enterpriseapn-connectionname-isattachapn)
</dt> <dd> <dl> <dt>

<span data-ttu-id="89615-143">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="89615-143">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="89615-144">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="89615-144">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="89615-145">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="89615-145">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89615-146">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="89615-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="89615-147">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="89615-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="89615-148">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="89615-148">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="89615-149">Descrive il percorso completo del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="89615-149">Describes the full path to the parent node.</span></span> <span data-ttu-id="89615-150">Per questa classe la stringa è "./Vendor/MSFT/EnterpriseAPN"</span><span class="sxs-lookup"><span data-stu-id="89615-150">For this class, the string is "./Vendor/MSFT/EnterpriseAPN"</span></span>

</dd> <dt>

[<span data-ttu-id="89615-151">Password</span><span class="sxs-lookup"><span data-stu-id="89615-151">Password</span></span>](/windows/client-management/mdm/enterpriseapn-csp#enterpriseapn-connectionname-password)
</dt> <dd> <dl> <dt>

<span data-ttu-id="89615-152">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="89615-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="89615-153">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="89615-153">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="89615-154">Roaming</span><span class="sxs-lookup"><span data-stu-id="89615-154">Roaming</span></span>](/windows/client-management/mdm/enterpriseapn-csp#enterpriseapn-connectionname-roaming)
</dt> <dd> <dl> <dt>

<span data-ttu-id="89615-155">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="89615-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="89615-156">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="89615-156">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="89615-157">UserName</span><span class="sxs-lookup"><span data-stu-id="89615-157">UserName</span></span>](/windows/client-management/mdm/enterpriseapn-csp#enterpriseapn-connectionname-username)
</dt> <dd> <dl> <dt>

<span data-ttu-id="89615-158">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="89615-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="89615-159">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="89615-159">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="89615-160">Requisiti</span><span class="sxs-lookup"><span data-stu-id="89615-160">Requirements</span></span>



| <span data-ttu-id="89615-161">Requisito</span><span class="sxs-lookup"><span data-stu-id="89615-161">Requirement</span></span> | <span data-ttu-id="89615-162">Valore</span><span class="sxs-lookup"><span data-stu-id="89615-162">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="89615-163">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="89615-163">Minimum supported client</span></span><br/> | <span data-ttu-id="89615-164">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="89615-164">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="89615-165">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="89615-165">Minimum supported server</span></span><br/> | <span data-ttu-id="89615-166">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="89615-166">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="89615-167">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="89615-167">Namespace</span></span><br/>                | <span data-ttu-id="89615-168">\\ \\ Dmmap MDM CIMV2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="89615-168">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="89615-169">MOF</span><span class="sxs-lookup"><span data-stu-id="89615-169">MOF</span></span><br/>                      | <dl> <span data-ttu-id="89615-170"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="89615-170"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="89615-171">DLL</span><span class="sxs-lookup"><span data-stu-id="89615-171">DLL</span></span><br/>                      | <dl> <span data-ttu-id="89615-172"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="89615-172"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="89615-173">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="89615-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89615-174">Utilizzo di script di PowerShell con il provider del Bridge WMI</span><span class="sxs-lookup"><span data-stu-id="89615-174">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

