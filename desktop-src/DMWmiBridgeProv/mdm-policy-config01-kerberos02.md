---
title: Classe MDM_Policy_Config01_Kerberos02
description: La \_ \_ classe Config01 Kerberos02 dei criteri MDM \_ Configura i criteri Kerberos.
ms.assetid: d34ccc8a-0c0c-4b7a-88c2-35360ebd0b8e
keywords:
- Classe MDM_Policy_Config01_Kerberos02
- Classe MDM_Policy_Config01_Kerberos02, descritta
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_Kerberos02
- MDM_Policy_Config01_Kerberos02.InstanceID
- MDM_Policy_Config01_Kerberos02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c173c892985487ed1ac061ea720e3485ecb355ef
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873782"
---
# <a name="mdm_policy_config01_kerberos02-class"></a><span data-ttu-id="965d6-105">\_ \_ Classe Config01 Kerberos02 di criteri \_ MDM</span><span class="sxs-lookup"><span data-stu-id="965d6-105">MDM\_Policy\_Config01\_Kerberos02 class</span></span>

<span data-ttu-id="965d6-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="965d6-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="965d6-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="965d6-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="965d6-108">La \_ \_ classe Config01 Kerberos02 dei criteri MDM \_ Configura i criteri Kerberos.</span><span class="sxs-lookup"><span data-stu-id="965d6-108">The MDM\_Policy\_Config01\_Kerberos02 class configures the Kerberos policies.</span></span>

<span data-ttu-id="965d6-109">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="965d6-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="965d6-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="965d6-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_Kerberos02
{
  string InstanceID;
  string ParentID;
  string AllowForestSearchOrder;
  string KerberosClientSupportsClaimsCompoundArmor;
  string RequireKerberosArmoring;
  string RequireStrictKDCValidation;
  string SetMaximumContextTokenSize;
};
```

## <a name="members"></a><span data-ttu-id="965d6-111">Members</span><span class="sxs-lookup"><span data-stu-id="965d6-111">Members</span></span>

<span data-ttu-id="965d6-112">La **classe \_ \_ Config01 \_ Kerberos02 dei criteri MDM** ha questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="965d6-112">The **MDM\_Policy\_Config01\_Kerberos02** class has these types of members:</span></span>

-   [<span data-ttu-id="965d6-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="965d6-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="965d6-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="965d6-114">Properties</span></span>

<span data-ttu-id="965d6-115">La **classe \_ \_ \_ Kerberos02 dei criteri MDM Config01** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="965d6-115">The **MDM\_Policy\_Config01\_Kerberos02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="965d6-116">AllowForestSearchOrder</span><span class="sxs-lookup"><span data-stu-id="965d6-116">AllowForestSearchOrder</span></span>](/windows/client-management/mdm/policy-csp-kerberos#kerberos-allowforestsearchorder)
</dt> <dd> <dl> <dt>

<span data-ttu-id="965d6-117">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="965d6-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="965d6-118">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="965d6-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="965d6-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="965d6-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="965d6-120">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="965d6-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="965d6-121">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="965d6-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="965d6-122">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="965d6-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="965d6-123">KerberosClientSupportsClaimsCompoundArmor</span><span class="sxs-lookup"><span data-stu-id="965d6-123">KerberosClientSupportsClaimsCompoundArmor</span></span>](/windows/client-management/mdm/policy-csp-kerberos#kerberos-kerberosclientsupportsclaimscompoundarmor)
</dt> <dd> <dl> <dt>

<span data-ttu-id="965d6-124">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="965d6-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="965d6-125">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="965d6-125">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="965d6-126">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="965d6-126">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="965d6-127">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="965d6-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="965d6-128">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="965d6-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="965d6-129">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="965d6-129">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="965d6-130">RequireKerberosArmoring</span><span class="sxs-lookup"><span data-stu-id="965d6-130">RequireKerberosArmoring</span></span>](/windows/client-management/mdm/policy-csp-kerberos#kerberos-requirekerberosarmoring)
</dt> <dd> <dl> <dt>

<span data-ttu-id="965d6-131">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="965d6-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="965d6-132">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="965d6-132">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="965d6-133">RequireStrictKDCValidation</span><span class="sxs-lookup"><span data-stu-id="965d6-133">RequireStrictKDCValidation</span></span>](/windows/client-management/mdm/policy-csp-kerberos#kerberos-requirestrictkdcvalidation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="965d6-134">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="965d6-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="965d6-135">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="965d6-135">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="965d6-136">SetMaximumContextTokenSize</span><span class="sxs-lookup"><span data-stu-id="965d6-136">SetMaximumContextTokenSize</span></span>](/windows/client-management/mdm/policy-csp-kerberos#kerberos-setmaximumcontexttokensize)
</dt> <dd> <dl> <dt>

<span data-ttu-id="965d6-137">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="965d6-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="965d6-138">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="965d6-138">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="965d6-139">Requisiti</span><span class="sxs-lookup"><span data-stu-id="965d6-139">Requirements</span></span>



| <span data-ttu-id="965d6-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="965d6-140">Requirement</span></span> | <span data-ttu-id="965d6-141">Valore</span><span class="sxs-lookup"><span data-stu-id="965d6-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="965d6-142">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="965d6-142">Minimum supported client</span></span><br/> | <span data-ttu-id="965d6-143">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="965d6-143">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="965d6-144">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="965d6-144">Minimum supported server</span></span><br/> | <span data-ttu-id="965d6-145">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="965d6-145">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="965d6-146">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="965d6-146">Namespace</span></span><br/>                | <span data-ttu-id="965d6-147">\\ \\ Dmmap MDM CIMV2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="965d6-147">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="965d6-148">MOF</span><span class="sxs-lookup"><span data-stu-id="965d6-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="965d6-149"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="965d6-149"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="965d6-150">DLL</span><span class="sxs-lookup"><span data-stu-id="965d6-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="965d6-151"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="965d6-151"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

