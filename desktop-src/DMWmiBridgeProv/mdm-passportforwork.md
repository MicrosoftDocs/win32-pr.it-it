---
title: Classe MDM_PassportForWork
description: Il \_ PASSPORTFORWORK MDM viene usato per eseguire il provisioning di Windows Hello for business.
ms.assetid: 49bba780-e26f-463d-97ae-e095ea16be87
keywords:
- Classe MDM_PassportForWork
- Classe MDM_PassportForWork, descritta
topic_type:
- apiref
api_name:
- MDM_PassportForWork
- MDM_PassportForWork.InstanceID
- MDM_PassportForWork.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7df7f061c0ab8f0405e8f0e6a6d43d8d896c62f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048179"
---
# <a name="mdm_passportforwork-class"></a><span data-ttu-id="d7dd6-105">MDM \_ PassportForWork (classe)</span><span class="sxs-lookup"><span data-stu-id="d7dd6-105">MDM\_PassportForWork class</span></span>

<span data-ttu-id="d7dd6-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="d7dd6-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="d7dd6-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="d7dd6-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="d7dd6-108">Il **\_ PassportForWork MDM** viene usato per eseguire il provisioning di Windows Hello for business.</span><span class="sxs-lookup"><span data-stu-id="d7dd6-108">The **MDM\_PassportForWork** is used to provision Windows Hello for Business.</span></span>

<span data-ttu-id="d7dd6-109">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="d7dd6-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7dd6-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d7dd6-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_PassportForWork
{
  string  InstanceID;
  string  ParentID;
  boolean UseBiometrics;
};
```

## <a name="members"></a><span data-ttu-id="d7dd6-111">Members</span><span class="sxs-lookup"><span data-stu-id="d7dd6-111">Members</span></span>

<span data-ttu-id="d7dd6-112">La classe **MDM \_ PassportForWork** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="d7dd6-112">The **MDM\_PassportForWork** class has these types of members:</span></span>

-   [<span data-ttu-id="d7dd6-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="d7dd6-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d7dd6-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="d7dd6-114">Properties</span></span>

<span data-ttu-id="d7dd6-115">La classe **MDM \_ PassportForWork** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="d7dd6-115">The **MDM\_PassportForWork** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d7dd6-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="d7dd6-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d7dd6-117">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d7dd6-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d7dd6-118">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d7dd6-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d7dd6-119">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="d7dd6-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="d7dd6-120">Specifica l'ID tenant nel formato di un identificatore univoco globale (GUID) senza parentesi graffe ({,}), che verrà usato come parte del provisioning e della gestione di Windows Hello for business.</span><span class="sxs-lookup"><span data-stu-id="d7dd6-120">Specifies the Tenant ID in the format of a Globally Unique Identifier (GUID) without curly braces ( { , } ), which will be used as part of Windows Hello for Business provisioning and management.</span></span>

</dd> <dt>

<span data-ttu-id="d7dd6-121">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="d7dd6-121">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d7dd6-122">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d7dd6-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d7dd6-123">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d7dd6-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d7dd6-124">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="d7dd6-124">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="d7dd6-125">Descrive il percorso completo del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="d7dd6-125">Describes the full path to the parent node.</span></span> <span data-ttu-id="d7dd6-126">Per questa classe la stringa è "./Vendor/MSFT/PassPortForWork/"</span><span class="sxs-lookup"><span data-stu-id="d7dd6-126">For this class, the string is "./Vendor/MSFT/PassPortForWork/"</span></span>

</dd> <dt>

[<span data-ttu-id="d7dd6-127">UseBiometrics</span><span class="sxs-lookup"><span data-stu-id="d7dd6-127">UseBiometrics</span></span>](/windows/client-management/mdm/passportforwork-csp#usebiometrics)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d7dd6-128">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="d7dd6-128">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d7dd6-129">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="d7dd6-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d7dd6-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d7dd6-130">Requirements</span></span>



| <span data-ttu-id="d7dd6-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="d7dd6-131">Requirement</span></span> | <span data-ttu-id="d7dd6-132">Valore</span><span class="sxs-lookup"><span data-stu-id="d7dd6-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d7dd6-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d7dd6-133">Minimum supported client</span></span><br/> | <span data-ttu-id="d7dd6-134">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="d7dd6-134">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d7dd6-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d7dd6-135">Minimum supported server</span></span><br/> | <span data-ttu-id="d7dd6-136">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="d7dd6-136">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="d7dd6-137">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="d7dd6-137">Namespace</span></span><br/>                | <span data-ttu-id="d7dd6-138">\\ \\ Dmmap MDM CIMV2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="d7dd6-138">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="d7dd6-139">MOF</span><span class="sxs-lookup"><span data-stu-id="d7dd6-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d7dd6-140"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d7dd6-140"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="d7dd6-141">DLL</span><span class="sxs-lookup"><span data-stu-id="d7dd6-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d7dd6-142"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d7dd6-142"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d7dd6-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d7dd6-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7dd6-144">Utilizzo di script di PowerShell con il provider del Bridge WMI</span><span class="sxs-lookup"><span data-stu-id="d7dd6-144">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

