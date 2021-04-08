---
title: Classe MDM_Policy_Result01_WirelessDisplay02
description: La \_ \_ classe Result01 WirelessDisplay02 dei criteri MDM \_ rappresenta i criteri di visualizzazione wireless disponibili.
ms.assetid: fbdfa785-8747-47b4-9802-da1c245ca222
keywords:
- Classe MDM_Policy_Result01_WirelessDisplay02
- Classe MDM_Policy_Result01_WirelessDisplay02, descritta
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_WirelessDisplay02
- MDM_Policy_Result01_WirelessDisplay02.InstanceID
- MDM_Policy_Result01_WirelessDisplay02.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90f4e309d1c54f12d99dfbeaa0b80807249e61fc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104047905"
---
# <a name="mdm_policy_result01_wirelessdisplay02-class"></a><span data-ttu-id="b3a52-105">\_ \_ Classe Result01 WirelessDisplay02 di criteri \_ MDM</span><span class="sxs-lookup"><span data-stu-id="b3a52-105">MDM\_Policy\_Result01\_WirelessDisplay02 class</span></span>

<span data-ttu-id="b3a52-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="b3a52-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="b3a52-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="b3a52-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="b3a52-108">La **classe \_ \_ Result01 \_ WirelessDisplay02 dei criteri MDM** rappresenta i criteri di visualizzazione wireless disponibili.</span><span class="sxs-lookup"><span data-stu-id="b3a52-108">The **MDM\_Policy\_Result01\_WirelessDisplay02** class represents the wireless display policies available.</span></span>

<span data-ttu-id="b3a52-109">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="b3a52-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3a52-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b3a52-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_WirelessDisplay02
{
  string InstanceID;
  string ParentID;
  sint32 AllowMdnsDiscovery;
  sint32 AllowMdnsAdvertisement;
  sint32 AllowProjectionFromPCOverInfrastructure;
  sint32 AllowProjectionFromPC;
  sint32 AllowProjectionToPC;
  sint32 AllowProjectionToPCOverInfrastructure;
  sint32 AllowUserInputFromWirelessDisplayReceiver;
  sint32 RequirePinForPairing;
};
```

## <a name="members"></a><span data-ttu-id="b3a52-111">Members</span><span class="sxs-lookup"><span data-stu-id="b3a52-111">Members</span></span>

<span data-ttu-id="b3a52-112">La **classe \_ \_ Result01 \_ WirelessDisplay02 dei criteri MDM** ha questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="b3a52-112">The **MDM\_Policy\_Result01\_WirelessDisplay02** class has these types of members:</span></span>

-   [<span data-ttu-id="b3a52-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b3a52-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b3a52-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b3a52-114">Properties</span></span>

<span data-ttu-id="b3a52-115">La **classe \_ \_ \_ WirelessDisplay02 dei criteri MDM Result01** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="b3a52-115">The **MDM\_Policy\_Result01\_WirelessDisplay02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="b3a52-116">AllowMdnsAdvertisement</span><span class="sxs-lookup"><span data-stu-id="b3a52-116">AllowMdnsAdvertisement</span></span>](/windows/client-management/mdm/policy-csp-wirelessdisplay#wirelessdisplay-allowmdnsadvertisement)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3a52-117">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b3a52-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b3a52-118">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="b3a52-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3a52-119">AllowMdnsDiscovery</span><span class="sxs-lookup"><span data-stu-id="b3a52-119">AllowMdnsDiscovery</span></span>](/windows/client-management/mdm/policy-csp-wirelessdisplay#wirelessdisplay-allowmdnsdiscovery)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3a52-120">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b3a52-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b3a52-121">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="b3a52-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3a52-122">AllowProjectionFromPC</span><span class="sxs-lookup"><span data-stu-id="b3a52-122">AllowProjectionFromPC</span></span>](/windows/client-management/mdm/policy-csp-wirelessdisplay#wirelessdisplay-allowprojectionfrompc)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3a52-123">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b3a52-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b3a52-124">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="b3a52-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3a52-125">AllowProjectionFromPCOverInfrastructure</span><span class="sxs-lookup"><span data-stu-id="b3a52-125">AllowProjectionFromPCOverInfrastructure</span></span>](/windows/client-management/mdm/policy-csp-wirelessdisplay#wirelessdisplay-allowprojectionfrompcoverinfrastructure)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3a52-126">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b3a52-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b3a52-127">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="b3a52-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3a52-128">AllowProjectionToPC</span><span class="sxs-lookup"><span data-stu-id="b3a52-128">AllowProjectionToPC</span></span>](/windows/client-management/mdm/policy-csp-wirelessdisplay#wirelessdisplay-allowprojectiontopc)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3a52-129">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b3a52-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b3a52-130">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="b3a52-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3a52-131">AllowProjectionToPCOverInfrastructure</span><span class="sxs-lookup"><span data-stu-id="b3a52-131">AllowProjectionToPCOverInfrastructure</span></span>](/windows/client-management/mdm/policy-csp-wirelessdisplay#wirelessdisplay-allowprojectiontopcoverinfrastructure)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3a52-132">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b3a52-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b3a52-133">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="b3a52-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3a52-134">AllowUserInputFromWirelessDisplayReceiver</span><span class="sxs-lookup"><span data-stu-id="b3a52-134">AllowUserInputFromWirelessDisplayReceiver</span></span>](/windows/client-management/mdm/policy-csp-wirelessdisplay#wirelessdisplay-allowuserinputfromwirelessdisplayreceiver)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3a52-135">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b3a52-135">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b3a52-136">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="b3a52-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="b3a52-137">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="b3a52-137">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3a52-138">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b3a52-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3a52-139">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b3a52-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b3a52-140">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="b3a52-140">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="b3a52-141">Identifica il nome del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="b3a52-141">Identifies the name of the parent node.</span></span> <span data-ttu-id="b3a52-142">Per questa classe la stringa è "WirelessDisplay".</span><span class="sxs-lookup"><span data-stu-id="b3a52-142">For this class, the string is "WirelessDisplay".</span></span>

</dd> <dt>

<span data-ttu-id="b3a52-143">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="b3a52-143">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3a52-144">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b3a52-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3a52-145">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b3a52-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b3a52-146">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="b3a52-146">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="b3a52-147">Descrive il percorso completo del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="b3a52-147">Describes the full path to the parent node.</span></span> <span data-ttu-id="b3a52-148">Per questa classe la stringa è "./Vendor/MSFT/Policy/Config"</span><span class="sxs-lookup"><span data-stu-id="b3a52-148">For this class, the string is "./Vendor/MSFT/Policy/Config"</span></span>

</dd> <dt>

[<span data-ttu-id="b3a52-149">RequirePinForPairing</span><span class="sxs-lookup"><span data-stu-id="b3a52-149">RequirePinForPairing</span></span>](/windows/client-management/mdm/policy-csp-wirelessdisplay#wirelessdisplay-requirepinforpairing)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3a52-150">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b3a52-150">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b3a52-151">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="b3a52-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b3a52-152">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b3a52-152">Requirements</span></span>



| <span data-ttu-id="b3a52-153">Requisito</span><span class="sxs-lookup"><span data-stu-id="b3a52-153">Requirement</span></span> | <span data-ttu-id="b3a52-154">Valore</span><span class="sxs-lookup"><span data-stu-id="b3a52-154">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b3a52-155">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b3a52-155">Minimum supported client</span></span><br/> | <span data-ttu-id="b3a52-156">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="b3a52-156">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="b3a52-157">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b3a52-157">Minimum supported server</span></span><br/> | <span data-ttu-id="b3a52-158">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="b3a52-158">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="b3a52-159">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="b3a52-159">Namespace</span></span><br/>                | <span data-ttu-id="b3a52-160">\\ \\ Dmmap MDM CIMV2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="b3a52-160">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="b3a52-161">MOF</span><span class="sxs-lookup"><span data-stu-id="b3a52-161">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b3a52-162"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b3a52-162"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl>       |
| <span data-ttu-id="b3a52-163">DLL</span><span class="sxs-lookup"><span data-stu-id="b3a52-163">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b3a52-164"><dt>\\DMWmiBridgeProv.dllfile MOF</dt></span><span class="sxs-lookup"><span data-stu-id="b3a52-164"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

