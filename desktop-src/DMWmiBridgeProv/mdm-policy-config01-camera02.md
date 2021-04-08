---
title: Classe MDM_Policy_Config01_Camera02
description: La \_ \_ classe Config01 Camera02 dei criteri MDM \_ rappresenta i criteri della fotocamera disponibili.
ms.assetid: dd17c2bc-8c96-4f5e-a4d2-cf1d27a92eb7
keywords:
- Classe MDM_Policy_Config01_Camera02
- Classe MDM_Policy_Config01_Camera02, descritta
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_Camera02
- MDM_Policy_Config01_Camera02.InstanceID
- MDM_Policy_Config01_Camera02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 377a9eb695560d7bf93fd6a5d761b1e95202bf20
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740970"
---
# <a name="mdm_policy_config01_camera02-class"></a><span data-ttu-id="5f50c-105">\_ \_ Classe Config01 Camera02 di criteri \_ MDM</span><span class="sxs-lookup"><span data-stu-id="5f50c-105">MDM\_Policy\_Config01\_Camera02 class</span></span>

<span data-ttu-id="5f50c-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="5f50c-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="5f50c-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="5f50c-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="5f50c-108">La **classe \_ \_ Config01 \_ Camera02 dei criteri MDM** rappresenta i criteri della fotocamera disponibili.</span><span class="sxs-lookup"><span data-stu-id="5f50c-108">The **MDM\_Policy\_Config01\_Camera02** class represents the camera policies available.</span></span>

<span data-ttu-id="5f50c-109">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="5f50c-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f50c-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5f50c-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_Camera02
{
  string InstanceID;
  string ParentID;
  sint32 AllowCamera;
};
```

## <a name="members"></a><span data-ttu-id="5f50c-111">Members</span><span class="sxs-lookup"><span data-stu-id="5f50c-111">Members</span></span>

<span data-ttu-id="5f50c-112">La **classe \_ \_ Config01 \_ Camera02 dei criteri MDM** ha questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="5f50c-112">The **MDM\_Policy\_Config01\_Camera02** class has these types of members:</span></span>

-   [<span data-ttu-id="5f50c-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="5f50c-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5f50c-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="5f50c-114">Properties</span></span>

<span data-ttu-id="5f50c-115">La **classe \_ \_ \_ Camera02 dei criteri MDM Config01** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="5f50c-115">The **MDM\_Policy\_Config01\_Camera02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="5f50c-116">AllowCamera</span><span class="sxs-lookup"><span data-stu-id="5f50c-116">AllowCamera</span></span>](/windows/client-management/mdm/policy-csp-camera#camera-allowcamera)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f50c-117">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="5f50c-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5f50c-118">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5f50c-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="5f50c-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="5f50c-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f50c-120">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5f50c-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5f50c-121">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5f50c-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5f50c-122">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="5f50c-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="5f50c-123">Identifica il nome del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="5f50c-123">Identifies the name of the parent node.</span></span> <span data-ttu-id="5f50c-124">Per questa classe la stringa è "camera".</span><span class="sxs-lookup"><span data-stu-id="5f50c-124">For this class, the string is "Camera".</span></span>

</dd> <dt>

<span data-ttu-id="5f50c-125">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="5f50c-125">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f50c-126">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5f50c-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5f50c-127">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5f50c-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5f50c-128">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="5f50c-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="5f50c-129">Descrive il percorso completo del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="5f50c-129">Describes the full path to the parent node.</span></span> <span data-ttu-id="5f50c-130">Per questa classe la stringa è "./Vendor/MSFT/Policy/Config"</span><span class="sxs-lookup"><span data-stu-id="5f50c-130">For this class, the string is "./Vendor/MSFT/Policy/Config"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5f50c-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5f50c-131">Requirements</span></span>



| <span data-ttu-id="5f50c-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="5f50c-132">Requirement</span></span> | <span data-ttu-id="5f50c-133">Valore</span><span class="sxs-lookup"><span data-stu-id="5f50c-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5f50c-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5f50c-134">Minimum supported client</span></span><br/> | <span data-ttu-id="5f50c-135">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="5f50c-135">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="5f50c-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5f50c-136">Minimum supported server</span></span><br/> | <span data-ttu-id="5f50c-137">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="5f50c-137">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="5f50c-138">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="5f50c-138">Namespace</span></span><br/>                | <span data-ttu-id="5f50c-139">\\ \\ DMMap MDM CIMv2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="5f50c-139">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="5f50c-140">MOF</span><span class="sxs-lookup"><span data-stu-id="5f50c-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5f50c-141"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5f50c-141"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="5f50c-142">DLL</span><span class="sxs-lookup"><span data-stu-id="5f50c-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5f50c-143"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5f50c-143"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5f50c-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5f50c-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f50c-145">Utilizzo di script di PowerShell con il provider del Bridge WMI</span><span class="sxs-lookup"><span data-stu-id="5f50c-145">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

