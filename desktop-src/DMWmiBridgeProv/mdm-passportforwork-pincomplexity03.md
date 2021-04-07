---
title: Classe MDM_PassportForWork_PINComplexity03
description: La \_ classe MDM PassportForWork \_ PINComplexity03 definisce la complessità del PIN per le credenziali di accesso per Windows Hello for business.
ms.assetid: 83dcf859-03da-4508-b809-bafd24dc8bd4
keywords:
- Classe MDM_PassportForWork_PINComplexity03
- Classe MDM_PassportForWork_PINComplexity03, descritta
topic_type:
- apiref
api_name:
- MDM_PassportForWork_PINComplexity03
- MDM_PassportForWork_PINComplexity03.InstanceID
- MDM_PassportForWork_PINComplexity03.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a9d01cd152935a1daa0a9b0721ea27129e21934
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964027"
---
# <a name="mdm_passportforwork_pincomplexity03-class"></a><span data-ttu-id="5686d-105">\_Classe MDM PassportForWork \_ PINComplexity03</span><span class="sxs-lookup"><span data-stu-id="5686d-105">MDM\_PassportForWork\_PINComplexity03 class</span></span>

<span data-ttu-id="5686d-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="5686d-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="5686d-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="5686d-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="5686d-108">La classe **MDM \_ PassportForWork \_ PINComplexity03** definisce la complessità del PIN per le credenziali di accesso per Windows Hello for business.</span><span class="sxs-lookup"><span data-stu-id="5686d-108">The **MDM\_PassportForWork\_PINComplexity03** class defines the PIN complexity for the logon credentials for Windows Hello for Business.</span></span>

<span data-ttu-id="5686d-109">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="5686d-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="5686d-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5686d-110">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_PassportForWork_PINComplexity03
{
  string InstanceID;
  string ParentID;
  sint32 MinimumPINLength;
  sint32 MaximumPINLength;
  sint32 UppercaseLetters;
  sint32 LowercaseLetters;
  sint32 SpecialCharacters;
  sint32 Digits;
  sint32 History;
  sint32 Expiration;
};
```

## <a name="members"></a><span data-ttu-id="5686d-111">Members</span><span class="sxs-lookup"><span data-stu-id="5686d-111">Members</span></span>

<span data-ttu-id="5686d-112">La classe **MDM \_ PassportForWork \_ PINComplexity03** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="5686d-112">The **MDM\_PassportForWork\_PINComplexity03** class has these types of members:</span></span>

-   [<span data-ttu-id="5686d-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="5686d-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5686d-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="5686d-114">Properties</span></span>

<span data-ttu-id="5686d-115">La classe **MDM \_ PassportForWork \_ PINComplexity03** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="5686d-115">The **MDM\_PassportForWork\_PINComplexity03** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="5686d-116">Cifre</span><span class="sxs-lookup"><span data-stu-id="5686d-116">Digits</span></span>](/windows/client-management/mdm/passportforwork-csp#tenantid-policies-pincomplexity-digits)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5686d-117">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="5686d-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5686d-118">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5686d-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5686d-119">Scadenza</span><span class="sxs-lookup"><span data-stu-id="5686d-119">Expiration</span></span>](/windows/client-management/mdm/passportforwork-csp#tenantid-policies-pincomplexity-expiration)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5686d-120">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="5686d-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5686d-121">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5686d-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5686d-122">History</span><span class="sxs-lookup"><span data-stu-id="5686d-122">History</span></span>](/windows/client-management/mdm/passportforwork-csp#tenantid-policies-pincomplexity-history)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5686d-123">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="5686d-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5686d-124">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5686d-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="5686d-125">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="5686d-125">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5686d-126">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5686d-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5686d-127">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5686d-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5686d-128">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="5686d-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="5686d-129">Nodo radice per i criteri PIN.</span><span class="sxs-lookup"><span data-stu-id="5686d-129">Root node for PIN policies.</span></span>

</dd> <dt>

[<span data-ttu-id="5686d-130">LowercaseLetters</span><span class="sxs-lookup"><span data-stu-id="5686d-130">LowercaseLetters</span></span>](/windows/client-management/mdm/passportforwork-csp#tenantid-policies-pincomplexity-lowercaseletters)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5686d-131">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="5686d-131">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5686d-132">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5686d-132">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5686d-133">MaximumPINLength</span><span class="sxs-lookup"><span data-stu-id="5686d-133">MaximumPINLength</span></span>](/windows/client-management/mdm/passportforwork-csp#tenantid-policies-pincomplexity-maximumpinlength)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5686d-134">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="5686d-134">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5686d-135">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5686d-135">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5686d-136">MinimumPINLength</span><span class="sxs-lookup"><span data-stu-id="5686d-136">MinimumPINLength</span></span>](/windows/client-management/mdm/passportforwork-csp#tenantid-policies-pincomplexity-minimumpinlength)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5686d-137">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="5686d-137">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5686d-138">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5686d-138">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="5686d-139">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="5686d-139">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5686d-140">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5686d-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5686d-141">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5686d-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5686d-142">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="5686d-142">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="5686d-143">Descrive il percorso completo del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="5686d-143">Describes the full path to the parent node.</span></span> <span data-ttu-id="5686d-144">Per questa classe la stringa è "./Vendor/MSFT/PassPortForWork/*TenantId*/Policies"</span><span class="sxs-lookup"><span data-stu-id="5686d-144">For this class, the string is "./Vendor/MSFT/PassPortForWork/*TenantID*/Policies"</span></span>

</dd> <dt>

[<span data-ttu-id="5686d-145">SpecialCharacters</span><span class="sxs-lookup"><span data-stu-id="5686d-145">SpecialCharacters</span></span>](/windows/client-management/mdm/passportforwork-csp#tenantid-policies-pincomplexity-specialcharacters)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5686d-146">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="5686d-146">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5686d-147">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5686d-147">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5686d-148">UppercaseLetters</span><span class="sxs-lookup"><span data-stu-id="5686d-148">UppercaseLetters</span></span>](/windows/client-management/mdm/passportforwork-csp#tenantid-policies-pincomplexity-uppercaseletters)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5686d-149">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="5686d-149">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5686d-150">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5686d-150">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5686d-151">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5686d-151">Requirements</span></span>



| <span data-ttu-id="5686d-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="5686d-152">Requirement</span></span> | <span data-ttu-id="5686d-153">Valore</span><span class="sxs-lookup"><span data-stu-id="5686d-153">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5686d-154">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5686d-154">Minimum supported client</span></span><br/> | <span data-ttu-id="5686d-155">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="5686d-155">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="5686d-156">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5686d-156">Minimum supported server</span></span><br/> | <span data-ttu-id="5686d-157">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="5686d-157">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="5686d-158">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="5686d-158">Namespace</span></span><br/>                | <span data-ttu-id="5686d-159">\\ \\ Dmmap MDM CIMV2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="5686d-159">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="5686d-160">MOF</span><span class="sxs-lookup"><span data-stu-id="5686d-160">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5686d-161"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5686d-161"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="5686d-162">DLL</span><span class="sxs-lookup"><span data-stu-id="5686d-162">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5686d-163"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5686d-163"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5686d-164">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5686d-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5686d-165">Utilizzo di script di PowerShell con il provider del Bridge WMI</span><span class="sxs-lookup"><span data-stu-id="5686d-165">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

