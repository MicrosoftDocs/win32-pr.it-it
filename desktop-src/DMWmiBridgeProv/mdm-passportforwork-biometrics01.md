---
title: Classe MDM_PassportForWork_Biometrics01
description: La \_ classe MDM PassportForWork \_ Biometrics01 definisce le impostazioni biometriche.
ms.assetid: 64012526-eac6-4f01-8665-2bd460bc1b93
keywords:
- Classe MDM_PassportForWork_Biometrics01
- Classe MDM_PassportForWork_Biometrics01, descritta
topic_type:
- apiref
api_name:
- MDM_PassportForWork_Biometrics01
- MDM_PassportForWork_Biometrics01.InstanceID
- MDM_PassportForWork_Biometrics01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 132351f17b6f242e39d6e6d6680aa756d5f7b5f8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119435"
---
# <a name="mdm_passportforwork_biometrics01-class"></a><span data-ttu-id="6d6b7-105">\_Classe MDM PassportForWork \_ Biometrics01</span><span class="sxs-lookup"><span data-stu-id="6d6b7-105">MDM\_PassportForWork\_Biometrics01 class</span></span>

<span data-ttu-id="6d6b7-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="6d6b7-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="6d6b7-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="6d6b7-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="6d6b7-108">La classe **MDM \_ PassportForWork \_ Biometrics01** definisce le impostazioni biometriche.</span><span class="sxs-lookup"><span data-stu-id="6d6b7-108">The **MDM\_PassportForWork\_Biometrics01** class defines biometric settings.</span></span>

<span data-ttu-id="6d6b7-109">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="6d6b7-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d6b7-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6d6b7-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_PassportForWork_Biometrics01
{
  string  InstanceID;
  string  ParentID;
  boolean UseBiometrics;
  boolean FacialFeaturesUseEnhancedAntiSpoofing;
};
```

## <a name="members"></a><span data-ttu-id="6d6b7-111">Members</span><span class="sxs-lookup"><span data-stu-id="6d6b7-111">Members</span></span>

<span data-ttu-id="6d6b7-112">La classe **MDM \_ PassportForWork \_ Biometrics01** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="6d6b7-112">The **MDM\_PassportForWork\_Biometrics01** class has these types of members:</span></span>

-   [<span data-ttu-id="6d6b7-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="6d6b7-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6d6b7-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="6d6b7-114">Properties</span></span>

<span data-ttu-id="6d6b7-115">La classe **MDM \_ PassportForWork \_ Biometrics01** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="6d6b7-115">The **MDM\_PassportForWork\_Biometrics01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="6d6b7-116">FacialFeaturesUseEnhancedAntiSpoofing</span><span class="sxs-lookup"><span data-stu-id="6d6b7-116">FacialFeaturesUseEnhancedAntiSpoofing</span></span>](/windows/client-management/mdm/passportforwork-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d6b7-117">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="6d6b7-117">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6d6b7-118">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="6d6b7-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="6d6b7-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="6d6b7-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d6b7-120">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="6d6b7-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6d6b7-121">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6d6b7-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6d6b7-122">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="6d6b7-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="6d6b7-123">Identifica il nome del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="6d6b7-123">Identifies the name of the parent node.</span></span>

</dd> <dt>

<span data-ttu-id="6d6b7-124">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="6d6b7-124">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d6b7-125">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="6d6b7-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6d6b7-126">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6d6b7-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6d6b7-127">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="6d6b7-127">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="6d6b7-128">Descrive il percorso completo del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="6d6b7-128">Describes the full path to the parent node.</span></span> <span data-ttu-id="6d6b7-129">Per questa classe la stringa è "./Vendor/MSFT/PassportForWork/"</span><span class="sxs-lookup"><span data-stu-id="6d6b7-129">For this class, the string is "./Vendor/MSFT/PassportForWork/"</span></span>

</dd> <dt>

[<span data-ttu-id="6d6b7-130">UseBiometrics</span><span class="sxs-lookup"><span data-stu-id="6d6b7-130">UseBiometrics</span></span>](/windows/client-management/mdm/passportforwork-csp#usebiometrics)
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d6b7-131">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="6d6b7-131">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6d6b7-132">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="6d6b7-132">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6d6b7-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6d6b7-133">Requirements</span></span>



| <span data-ttu-id="6d6b7-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="6d6b7-134">Requirement</span></span> | <span data-ttu-id="6d6b7-135">Valore</span><span class="sxs-lookup"><span data-stu-id="6d6b7-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6d6b7-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6d6b7-136">Minimum supported client</span></span><br/> | <span data-ttu-id="6d6b7-137">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="6d6b7-137">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6d6b7-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6d6b7-138">Minimum supported server</span></span><br/> | <span data-ttu-id="6d6b7-139">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="6d6b7-139">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="6d6b7-140">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="6d6b7-140">Namespace</span></span><br/>                | <span data-ttu-id="6d6b7-141">\\ \\ Dmmap MDM CIMV2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="6d6b7-141">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="6d6b7-142">MOF</span><span class="sxs-lookup"><span data-stu-id="6d6b7-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6d6b7-143"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6d6b7-143"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="6d6b7-144">DLL</span><span class="sxs-lookup"><span data-stu-id="6d6b7-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6d6b7-145"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6d6b7-145"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6d6b7-146">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6d6b7-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d6b7-147">Utilizzo di script di PowerShell con il provider del Bridge WMI</span><span class="sxs-lookup"><span data-stu-id="6d6b7-147">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

