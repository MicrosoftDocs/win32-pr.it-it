---
title: Classe MDM_Policy_Result01_Kerberos02
description: La \_ classe Kerberos02 dei criteri MDM \_ Result01 \_ rappresenta i criteri Kerberos.
ms.assetid: a628272d-723f-491a-a6a1-70514e5096ef
keywords:
- Classe MDM_Policy_Result01_Kerberos02
- Classe MDM_Policy_Result01_Kerberos02, descritta
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_Kerberos02
- MDM_Policy_Result01_Kerberos02.InstanceID
- MDM_Policy_Result01_Kerberos02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 713d7747fe45fa72cb7dcf44a02aa57526161c17
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476277"
---
# <a name="mdm_policy_result01_kerberos02-class"></a><span data-ttu-id="70f24-105">\_ \_ Classe Result01 Kerberos02 di criteri \_ MDM</span><span class="sxs-lookup"><span data-stu-id="70f24-105">MDM\_Policy\_Result01\_Kerberos02 class</span></span>

<span data-ttu-id="70f24-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="70f24-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="70f24-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="70f24-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="70f24-108">La \_ classe Kerberos02 dei criteri MDM \_ Result01 \_ rappresenta i criteri Kerberos.</span><span class="sxs-lookup"><span data-stu-id="70f24-108">The MDM\_Policy\_Result01\_Kerberos02 class represents the Kerberos policies.</span></span>

<span data-ttu-id="70f24-109">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="70f24-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="70f24-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="70f24-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_Kerberos02
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

## <a name="members"></a><span data-ttu-id="70f24-111">Members</span><span class="sxs-lookup"><span data-stu-id="70f24-111">Members</span></span>

<span data-ttu-id="70f24-112">La **classe \_ \_ Result01 \_ Kerberos02 dei criteri MDM** ha questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="70f24-112">The **MDM\_Policy\_Result01\_Kerberos02** class has these types of members:</span></span>

-   [<span data-ttu-id="70f24-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="70f24-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="70f24-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="70f24-114">Properties</span></span>

<span data-ttu-id="70f24-115">La **classe \_ \_ \_ Kerberos02 dei criteri MDM Result01** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="70f24-115">The **MDM\_Policy\_Result01\_Kerberos02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="70f24-116">AllowForestSearchOrder</span><span class="sxs-lookup"><span data-stu-id="70f24-116">AllowForestSearchOrder</span></span>](/windows/client-management/mdm/policy-csp-kerberos#kerberos-allowforestsearchorder)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70f24-117">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="70f24-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70f24-118">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="70f24-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="70f24-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="70f24-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70f24-120">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="70f24-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70f24-121">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="70f24-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="70f24-122">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="70f24-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70f24-123">KerberosClientSupportsClaimsCompoundArmor</span><span class="sxs-lookup"><span data-stu-id="70f24-123">KerberosClientSupportsClaimsCompoundArmor</span></span>](/windows/client-management/mdm/policy-csp-kerberos#kerberos-kerberosclientsupportsclaimscompoundarmor)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70f24-124">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="70f24-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70f24-125">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="70f24-125">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="70f24-126">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="70f24-126">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70f24-127">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="70f24-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70f24-128">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="70f24-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="70f24-129">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="70f24-129">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70f24-130">RequireKerberosArmoring</span><span class="sxs-lookup"><span data-stu-id="70f24-130">RequireKerberosArmoring</span></span>](/windows/client-management/mdm/policy-csp-kerberos#kerberos-requirekerberosarmoring)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70f24-131">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="70f24-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70f24-132">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="70f24-132">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70f24-133">RequireStrictKDCValidation</span><span class="sxs-lookup"><span data-stu-id="70f24-133">RequireStrictKDCValidation</span></span>](/windows/client-management/mdm/policy-csp-kerberos#kerberos-requirestrictkdcvalidation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70f24-134">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="70f24-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70f24-135">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="70f24-135">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="70f24-136">SetMaximumContextTokenSize</span><span class="sxs-lookup"><span data-stu-id="70f24-136">SetMaximumContextTokenSize</span></span>](/windows/client-management/mdm/policy-csp-kerberos#kerberos-setmaximumcontexttokensize)
</dt> <dd> <dl> <dt>

<span data-ttu-id="70f24-137">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="70f24-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="70f24-138">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="70f24-138">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="70f24-139">Requisiti</span><span class="sxs-lookup"><span data-stu-id="70f24-139">Requirements</span></span>



| <span data-ttu-id="70f24-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="70f24-140">Requirement</span></span> | <span data-ttu-id="70f24-141">Valore</span><span class="sxs-lookup"><span data-stu-id="70f24-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="70f24-142">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="70f24-142">Minimum supported client</span></span><br/> | <span data-ttu-id="70f24-143">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="70f24-143">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="70f24-144">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="70f24-144">Minimum supported server</span></span><br/> | <span data-ttu-id="70f24-145">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="70f24-145">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="70f24-146">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="70f24-146">Namespace</span></span><br/>                | <span data-ttu-id="70f24-147">\\ \\ Dmmap MDM CIMV2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="70f24-147">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="70f24-148">MOF</span><span class="sxs-lookup"><span data-stu-id="70f24-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="70f24-149"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="70f24-149"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="70f24-150">DLL</span><span class="sxs-lookup"><span data-stu-id="70f24-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="70f24-151"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="70f24-151"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

