---
title: Classe MDM_Policy_Result01_Power02
description: La \_ classe Power02 dei criteri MDM \_ Result01 \_ rappresenta i criteri di risparmio energia.
ms.assetid: 1458228f-f442-4fd4-b402-e0a4c06ecaa5
keywords:
- Classe MDM_Policy_Result01_Power02
- Classe MDM_Policy_Result01_Power02, descritta
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_Power02
- MDM_Policy_Result01_Power02.InstanceID
- MDM_Policy_Result01_Power02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91635811e876500cb4d3df792067b1eba3d861b1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963883"
---
# <a name="mdm_policy_result01_power02-class"></a><span data-ttu-id="991ce-105">\_ \_ Classe Result01 Power02 di criteri \_ MDM</span><span class="sxs-lookup"><span data-stu-id="991ce-105">MDM\_Policy\_Result01\_Power02 class</span></span>

<span data-ttu-id="991ce-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="991ce-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="991ce-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="991ce-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="991ce-108">La \_ classe Power02 dei criteri MDM \_ Result01 \_ rappresenta i criteri di risparmio energia.</span><span class="sxs-lookup"><span data-stu-id="991ce-108">The MDM\_Policy\_Result01\_Power02 class represents the power policies.</span></span>

<span data-ttu-id="991ce-109">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="991ce-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="991ce-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="991ce-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_Power02
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

## <a name="members"></a><span data-ttu-id="991ce-111">Members</span><span class="sxs-lookup"><span data-stu-id="991ce-111">Members</span></span>

<span data-ttu-id="991ce-112">La **classe \_ \_ Result01 \_ Power02 dei criteri MDM** ha questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="991ce-112">The **MDM\_Policy\_Result01\_Power02** class has these types of members:</span></span>

-   [<span data-ttu-id="991ce-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="991ce-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="991ce-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="991ce-114">Properties</span></span>

<span data-ttu-id="991ce-115">La **classe \_ \_ \_ Power02 dei criteri MDM Result01** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="991ce-115">The **MDM\_Policy\_Result01\_Power02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="991ce-116">AllowStandbyWhenSleepingPluggedIn</span><span class="sxs-lookup"><span data-stu-id="991ce-116">AllowStandbyWhenSleepingPluggedIn</span></span>](/windows/client-management/mdm/policy-csp-power#power-allowstandbywhensleepingpluggedin)
</dt> <dd> <dl> <dt>

<span data-ttu-id="991ce-117">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="991ce-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="991ce-118">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="991ce-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="991ce-119">DisplayOffTimeoutOnBattery</span><span class="sxs-lookup"><span data-stu-id="991ce-119">DisplayOffTimeoutOnBattery</span></span>](/windows/client-management/mdm/policy-csp-power#power-displayofftimeoutonbattery)
</dt> <dd> <dl> <dt>

<span data-ttu-id="991ce-120">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="991ce-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="991ce-121">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="991ce-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="991ce-122">DisplayOffTimeoutPluggedIn</span><span class="sxs-lookup"><span data-stu-id="991ce-122">DisplayOffTimeoutPluggedIn</span></span>](/windows/client-management/mdm/policy-csp-power#power-displayofftimeoutpluggedin)
</dt> <dd> <dl> <dt>

<span data-ttu-id="991ce-123">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="991ce-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="991ce-124">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="991ce-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="991ce-125">HibernateTimeoutOnBattery</span><span class="sxs-lookup"><span data-stu-id="991ce-125">HibernateTimeoutOnBattery</span></span>](/windows/client-management/mdm/policy-csp-power#power-hibernatetimeoutonbattery)
</dt> <dd> <dl> <dt>

<span data-ttu-id="991ce-126">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="991ce-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="991ce-127">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="991ce-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="991ce-128">HibernateTimeoutPluggedIn</span><span class="sxs-lookup"><span data-stu-id="991ce-128">HibernateTimeoutPluggedIn</span></span>](/windows/client-management/mdm/policy-csp-power#power-hibernatetimeoutpluggedin)
</dt> <dd> <dl> <dt>

<span data-ttu-id="991ce-129">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="991ce-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="991ce-130">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="991ce-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="991ce-131">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="991ce-131">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="991ce-132">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="991ce-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="991ce-133">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="991ce-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="991ce-134">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="991ce-134">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="991ce-135">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="991ce-135">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="991ce-136">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="991ce-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="991ce-137">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="991ce-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="991ce-138">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="991ce-138">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="991ce-139">RequirePasswordWhenComputerWakesOnBattery</span><span class="sxs-lookup"><span data-stu-id="991ce-139">RequirePasswordWhenComputerWakesOnBattery</span></span>](/windows/client-management/mdm/policy-csp-power#power-requirepasswordwhencomputerwakesonbattery)
</dt> <dd> <dl> <dt>

<span data-ttu-id="991ce-140">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="991ce-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="991ce-141">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="991ce-141">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="991ce-142">RequirePasswordWhenComputerWakesPluggedIn</span><span class="sxs-lookup"><span data-stu-id="991ce-142">RequirePasswordWhenComputerWakesPluggedIn</span></span>](/windows/client-management/mdm/policy-csp-power#power-requirepasswordwhencomputerwakespluggedin)
</dt> <dd> <dl> <dt>

<span data-ttu-id="991ce-143">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="991ce-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="991ce-144">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="991ce-144">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="991ce-145">StandbyTimeoutOnBattery</span><span class="sxs-lookup"><span data-stu-id="991ce-145">StandbyTimeoutOnBattery</span></span>](/windows/client-management/mdm/policy-csp-power#power-standbytimeoutonbattery)
</dt> <dd> <dl> <dt>

<span data-ttu-id="991ce-146">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="991ce-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="991ce-147">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="991ce-147">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="991ce-148">StandbyTimeoutPluggedIn</span><span class="sxs-lookup"><span data-stu-id="991ce-148">StandbyTimeoutPluggedIn</span></span>](/windows/client-management/mdm/policy-csp-power#power-standbytimeoutpluggedin)
</dt> <dd> <dl> <dt>

<span data-ttu-id="991ce-149">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="991ce-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="991ce-150">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="991ce-150">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="991ce-151">Requisiti</span><span class="sxs-lookup"><span data-stu-id="991ce-151">Requirements</span></span>



| <span data-ttu-id="991ce-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="991ce-152">Requirement</span></span> | <span data-ttu-id="991ce-153">Valore</span><span class="sxs-lookup"><span data-stu-id="991ce-153">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="991ce-154">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="991ce-154">Minimum supported client</span></span><br/> | <span data-ttu-id="991ce-155">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="991ce-155">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="991ce-156">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="991ce-156">Minimum supported server</span></span><br/> | <span data-ttu-id="991ce-157">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="991ce-157">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="991ce-158">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="991ce-158">Namespace</span></span><br/>                | <span data-ttu-id="991ce-159">\\ \\ Dmmap MDM CIMV2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="991ce-159">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="991ce-160">MOF</span><span class="sxs-lookup"><span data-stu-id="991ce-160">MOF</span></span><br/>                      | <dl> <span data-ttu-id="991ce-161"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="991ce-161"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="991ce-162">DLL</span><span class="sxs-lookup"><span data-stu-id="991ce-162">DLL</span></span><br/>                      | <dl> <span data-ttu-id="991ce-163"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="991ce-163"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

