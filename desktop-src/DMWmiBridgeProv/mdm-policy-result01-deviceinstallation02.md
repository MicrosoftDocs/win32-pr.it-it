---
title: Classe MDM_Policy_Result01_DeviceInstallation02
description: La \_ \_ classe Result01 DeviceInstallation02 dei criteri MDM \_ rappresenta i criteri di installazione del dispositivo disponibili.
ms.assetid: a5c89661-16f1-42e7-a11d-2c3a7945dac3
keywords:
- Classe MDM_Policy_Result01_DeviceInstallation02
- Classe MDM_Policy_Result01_DeviceInstallation02, descritta
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_DeviceInstallation02
- MDM_Policy_Result01_DeviceInstallation02.InstanceID
- MDM_Policy_Result01_DeviceInstallation02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa6ec11cbfc5b0b38aa5e7482507108204b8798d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963928"
---
# <a name="mdm_policy_result01_deviceinstallation02-class"></a><span data-ttu-id="cde3b-105">\_ \_ Classe Result01 DeviceInstallation02 di criteri \_ MDM</span><span class="sxs-lookup"><span data-stu-id="cde3b-105">MDM\_Policy\_Result01\_DeviceInstallation02 class</span></span>

<span data-ttu-id="cde3b-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="cde3b-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="cde3b-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="cde3b-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="cde3b-108">La \_ \_ classe Result01 DeviceInstallation02 dei criteri MDM \_ rappresenta i criteri di installazione del dispositivo disponibili.</span><span class="sxs-lookup"><span data-stu-id="cde3b-108">The MDM\_Policy\_Result01\_DeviceInstallation02 class represents the available device installation policies.</span></span>

<span data-ttu-id="cde3b-109">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="cde3b-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="cde3b-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cde3b-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_DeviceInstallation02
{
  string InstanceID;
  string ParentID;
  string PreventInstallationOfMatchingDeviceIDs;
  string PreventInstallationOfMatchingDeviceSetupClasses;
};
```

## <a name="members"></a><span data-ttu-id="cde3b-111">Members</span><span class="sxs-lookup"><span data-stu-id="cde3b-111">Members</span></span>

<span data-ttu-id="cde3b-112">La **classe \_ \_ Result01 \_ DeviceInstallation02 dei criteri MDM** ha questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="cde3b-112">The **MDM\_Policy\_Result01\_DeviceInstallation02** class has these types of members:</span></span>

-   [<span data-ttu-id="cde3b-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="cde3b-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="cde3b-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="cde3b-114">Properties</span></span>

<span data-ttu-id="cde3b-115">La **classe \_ \_ \_ DeviceInstallation02 dei criteri MDM Result01** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="cde3b-115">The **MDM\_Policy\_Result01\_DeviceInstallation02** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="cde3b-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="cde3b-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cde3b-117">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="cde3b-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cde3b-118">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cde3b-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cde3b-119">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="cde3b-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="cde3b-120">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="cde3b-120">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cde3b-121">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="cde3b-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cde3b-122">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cde3b-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cde3b-123">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="cde3b-123">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="cde3b-124">PreventInstallationOfMatchingDeviceIDs</span><span class="sxs-lookup"><span data-stu-id="cde3b-124">PreventInstallationOfMatchingDeviceIDs</span></span>](/windows/client-management/mdm/policy-csp-deviceinstallation#deviceinstallation-preventinstallationofmatchingdeviceids)
</dt> <dd> <dl> <dt>

<span data-ttu-id="cde3b-125">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="cde3b-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cde3b-126">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="cde3b-126">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="cde3b-127">PreventInstallationOfMatchingDeviceSetupClasses</span><span class="sxs-lookup"><span data-stu-id="cde3b-127">PreventInstallationOfMatchingDeviceSetupClasses</span></span>](/windows/client-management/mdm/policy-csp-deviceinstallation#deviceinstallation-preventinstallationofmatchingdevicesetupclasses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="cde3b-128">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="cde3b-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cde3b-129">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="cde3b-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="cde3b-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cde3b-130">Requirements</span></span>



| <span data-ttu-id="cde3b-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="cde3b-131">Requirement</span></span> | <span data-ttu-id="cde3b-132">Valore</span><span class="sxs-lookup"><span data-stu-id="cde3b-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cde3b-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cde3b-133">Minimum supported client</span></span><br/> | <span data-ttu-id="cde3b-134">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="cde3b-134">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="cde3b-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cde3b-135">Minimum supported server</span></span><br/> | <span data-ttu-id="cde3b-136">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="cde3b-136">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="cde3b-137">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="cde3b-137">Namespace</span></span><br/>                | <span data-ttu-id="cde3b-138">\\ \\ Dmmap MDM CIMV2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="cde3b-138">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="cde3b-139">MOF</span><span class="sxs-lookup"><span data-stu-id="cde3b-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cde3b-140"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cde3b-140"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="cde3b-141">DLL</span><span class="sxs-lookup"><span data-stu-id="cde3b-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cde3b-142"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cde3b-142"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

