---
title: Classe MDM_Policy_Config01_Power02
description: La \_ \_ classe Config01 Power02 dei criteri MDM \_ Configura i criteri di risparmio energia.
ms.assetid: 8913c38c-0d8d-456f-a412-d47c2ccd5d13
keywords:
- Classe MDM_Policy_Config01_Power02
- Classe MDM_Policy_Config01_Power02, descritta
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_Power02
- MDM_Policy_Config01_Power02.InstanceID
- MDM_Policy_Config01_Power02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c9bdda57bbd85100e8bccb87990d928f448a972
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119722"
---
# <a name="mdm_policy_config01_power02-class"></a><span data-ttu-id="46094-105">\_ \_ Classe Config01 Power02 di criteri \_ MDM</span><span class="sxs-lookup"><span data-stu-id="46094-105">MDM\_Policy\_Config01\_Power02 class</span></span>

<span data-ttu-id="46094-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="46094-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="46094-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="46094-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="46094-108">La \_ \_ classe Config01 Power02 dei criteri MDM \_ Configura i criteri di risparmio energia.</span><span class="sxs-lookup"><span data-stu-id="46094-108">The MDM\_Policy\_Config01\_Power02 class configures the power policies.</span></span>

<span data-ttu-id="46094-109">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="46094-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="46094-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="46094-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_Power02
{
  string InstanceID;
  string ParentID;
  string AllowStandbyWhenSleepingPluggedIn;
  string HibernateTimeoutPluggedIn;
  string HibernateTimeoutOnBattery;
  string DisplayOffTimeoutPluggedIn;
  string DisplayOffTimeoutOnBattery;
  string RequirePasswordWhenComputerWakesOnBattery;
  string RequirePasswordWhenComputerWakesPluggedIn;
  string StandbyTimeoutPluggedIn;
  string StandbyTimeoutOnBattery;
};
```

## <a name="members"></a><span data-ttu-id="46094-111">Members</span><span class="sxs-lookup"><span data-stu-id="46094-111">Members</span></span>

<span data-ttu-id="46094-112">La **classe \_ \_ Config01 \_ Power02 dei criteri MDM** ha questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="46094-112">The **MDM\_Policy\_Config01\_Power02** class has these types of members:</span></span>

-   [<span data-ttu-id="46094-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="46094-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="46094-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="46094-114">Properties</span></span>

<span data-ttu-id="46094-115">La **classe \_ \_ \_ Power02 dei criteri MDM Config01** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="46094-115">The **MDM\_Policy\_Config01\_Power02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="46094-116">AllowStandbyWhenSleepingPluggedIn</span><span class="sxs-lookup"><span data-stu-id="46094-116">AllowStandbyWhenSleepingPluggedIn</span></span>](/windows/client-management/mdm/policy-csp-power#power-allowstandbywhensleepingpluggedin)
</dt> <dd> <dl> <dt>

<span data-ttu-id="46094-117">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="46094-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="46094-118">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="46094-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="46094-119">DisplayOffTimeoutOnBattery</span><span class="sxs-lookup"><span data-stu-id="46094-119">DisplayOffTimeoutOnBattery</span></span>](/windows/client-management/mdm/policy-csp-power#power-displayofftimeoutonbattery)
</dt> <dd> <dl> <dt>

<span data-ttu-id="46094-120">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="46094-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="46094-121">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="46094-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="46094-122">DisplayOffTimeoutPluggedIn</span><span class="sxs-lookup"><span data-stu-id="46094-122">DisplayOffTimeoutPluggedIn</span></span>](/windows/client-management/mdm/policy-csp-power#power-displayofftimeoutpluggedin)
</dt> <dd> <dl> <dt>

<span data-ttu-id="46094-123">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="46094-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="46094-124">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="46094-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="46094-125">HibernateTimeoutOnBattery</span><span class="sxs-lookup"><span data-stu-id="46094-125">HibernateTimeoutOnBattery</span></span>](/windows/client-management/mdm/policy-csp-power#power-hibernatetimeoutonbattery)
</dt> <dd> <dl> <dt>

<span data-ttu-id="46094-126">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="46094-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="46094-127">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="46094-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="46094-128">HibernateTimeoutPluggedIn</span><span class="sxs-lookup"><span data-stu-id="46094-128">HibernateTimeoutPluggedIn</span></span>](/windows/client-management/mdm/policy-csp-power#power-hibernatetimeoutpluggedin)
</dt> <dd> <dl> <dt>

<span data-ttu-id="46094-129">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="46094-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="46094-130">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="46094-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="46094-131">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="46094-131">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46094-132">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="46094-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="46094-133">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="46094-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="46094-134">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="46094-134">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="46094-135">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="46094-135">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46094-136">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="46094-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="46094-137">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="46094-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="46094-138">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="46094-138">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="46094-139">RequirePasswordWhenComputerWakesOnBattery</span><span class="sxs-lookup"><span data-stu-id="46094-139">RequirePasswordWhenComputerWakesOnBattery</span></span>](/windows/client-management/mdm/policy-csp-power#power-requirepasswordwhencomputerwakesonbattery)
</dt> <dd> <dl> <dt>

<span data-ttu-id="46094-140">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="46094-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="46094-141">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="46094-141">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="46094-142">RequirePasswordWhenComputerWakesPluggedIn</span><span class="sxs-lookup"><span data-stu-id="46094-142">RequirePasswordWhenComputerWakesPluggedIn</span></span>](/windows/client-management/mdm/policy-csp-power#power-requirepasswordwhencomputerwakespluggedin)
</dt> <dd> <dl> <dt>

<span data-ttu-id="46094-143">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="46094-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="46094-144">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="46094-144">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="46094-145">StandbyTimeoutOnBattery</span><span class="sxs-lookup"><span data-stu-id="46094-145">StandbyTimeoutOnBattery</span></span>](/windows/client-management/mdm/policy-csp-power#power-standbytimeoutonbattery)
</dt> <dd> <dl> <dt>

<span data-ttu-id="46094-146">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="46094-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="46094-147">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="46094-147">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="46094-148">StandbyTimeoutPluggedIn</span><span class="sxs-lookup"><span data-stu-id="46094-148">StandbyTimeoutPluggedIn</span></span>](/windows/client-management/mdm/policy-csp-power#power-standbytimeoutpluggedin)
</dt> <dd> <dl> <dt>

<span data-ttu-id="46094-149">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="46094-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="46094-150">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="46094-150">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="46094-151">Requisiti</span><span class="sxs-lookup"><span data-stu-id="46094-151">Requirements</span></span>



| <span data-ttu-id="46094-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="46094-152">Requirement</span></span> | <span data-ttu-id="46094-153">Valore</span><span class="sxs-lookup"><span data-stu-id="46094-153">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="46094-154">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="46094-154">Minimum supported client</span></span><br/> | <span data-ttu-id="46094-155">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="46094-155">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="46094-156">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="46094-156">Minimum supported server</span></span><br/> | <span data-ttu-id="46094-157">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="46094-157">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="46094-158">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="46094-158">Namespace</span></span><br/>                | <span data-ttu-id="46094-159">\\ \\ Dmmap MDM CIMV2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="46094-159">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="46094-160">MOF</span><span class="sxs-lookup"><span data-stu-id="46094-160">MOF</span></span><br/>                      | <dl> <span data-ttu-id="46094-161"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="46094-161"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="46094-162">DLL</span><span class="sxs-lookup"><span data-stu-id="46094-162">DLL</span></span><br/>                      | <dl> <span data-ttu-id="46094-163"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="46094-163"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

