---
title: Classe MDM_RemoteFind_Location01
description: La \_ classe MDM RemoteFind \_ Location01 recupera le informazioni sulla posizione per un determinato dispositivo.
ms.assetid: 0c26bb3c-99b4-43ed-99ce-d976d48c4445
keywords:
- Classe MDM_RemoteFind_Location01
- Classe MDM_RemoteFind_Location01, descritta
topic_type:
- apiref
api_name:
- MDM_RemoteFind_Location01
- MDM_RemoteFind_Location01.InstanceID
- MDM_RemoteFind_Location01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56e1b46a7b4a0c3439f78f38a5fb6cd5b865275c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475287"
---
# <a name="mdm_remotefind_location01-class"></a><span data-ttu-id="13c55-105">\_Classe MDM RemoteFind \_ Location01</span><span class="sxs-lookup"><span data-stu-id="13c55-105">MDM\_RemoteFind\_Location01 class</span></span>

<span data-ttu-id="13c55-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="13c55-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="13c55-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="13c55-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="13c55-108">La classe **MDM \_ RemoteFind \_ Location01** recupera le informazioni sulla posizione per un determinato dispositivo.</span><span class="sxs-lookup"><span data-stu-id="13c55-108">The **MDM\_RemoteFind\_Location01** class retrieves the location information for a particular device.</span></span>

<span data-ttu-id="13c55-109">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="13c55-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="13c55-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="13c55-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_RemoteFind_Location01
{
  string   InstanceID;
  string   ParentID;
  real32   Latitude;
  real32   Longitude;
  real32   Altitude;
  sint32   Accuracy;
  sint32   AltitudeAccuracy;
  datetime Age;
};
```

## <a name="members"></a><span data-ttu-id="13c55-111">Members</span><span class="sxs-lookup"><span data-stu-id="13c55-111">Members</span></span>

<span data-ttu-id="13c55-112">La classe **MDM \_ RemoteFind \_ Location01** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="13c55-112">The **MDM\_RemoteFind\_Location01** class has these types of members:</span></span>

-   [<span data-ttu-id="13c55-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="13c55-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="13c55-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="13c55-114">Properties</span></span>

<span data-ttu-id="13c55-115">La classe **MDM \_ RemoteFind \_ Location01** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="13c55-115">The **MDM\_RemoteFind\_Location01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="13c55-116">Accuratezza</span><span class="sxs-lookup"><span data-stu-id="13c55-116">Accuracy</span></span>](/windows/client-management/mdm/remotefind-csp#accuracy)
</dt> <dd> <dl> <dt>

<span data-ttu-id="13c55-117">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="13c55-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="13c55-118">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="13c55-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="13c55-119">Age</span><span class="sxs-lookup"><span data-stu-id="13c55-119">Age</span></span>](/windows/client-management/mdm/remotefind-csp#age)
</dt> <dd> <dl> <dt>

<span data-ttu-id="13c55-120">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="13c55-120">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="13c55-121">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="13c55-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="13c55-122">Altitudine</span><span class="sxs-lookup"><span data-stu-id="13c55-122">Altitude</span></span>](/windows/client-management/mdm/remotefind-csp#altitude)
</dt> <dd> <dl> <dt>

<span data-ttu-id="13c55-123">Tipo di dati: **real32**</span><span class="sxs-lookup"><span data-stu-id="13c55-123">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="13c55-124">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="13c55-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="13c55-125">AltitudeAccuracy</span><span class="sxs-lookup"><span data-stu-id="13c55-125">AltitudeAccuracy</span></span>](/windows/client-management/mdm/remotefind-csp#altitudeaccuracy)
</dt> <dd> <dl> <dt>

<span data-ttu-id="13c55-126">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="13c55-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="13c55-127">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="13c55-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="13c55-128">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="13c55-128">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13c55-129">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="13c55-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="13c55-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="13c55-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="13c55-131">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="13c55-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="13c55-132">Identifica il nome del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="13c55-132">Identifies the name of the parent node.</span></span> <span data-ttu-id="13c55-133">Per questa classe la stringa è "location".</span><span class="sxs-lookup"><span data-stu-id="13c55-133">For this class, the string is "Location".</span></span>

</dd> <dt>

[<span data-ttu-id="13c55-134">Latitudine</span><span class="sxs-lookup"><span data-stu-id="13c55-134">Latitude</span></span>](/windows/client-management/mdm/remotefind-csp#latitude)
</dt> <dd> <dl> <dt>

<span data-ttu-id="13c55-135">Tipo di dati: **real32**</span><span class="sxs-lookup"><span data-stu-id="13c55-135">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="13c55-136">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="13c55-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="13c55-137">Longitudine</span><span class="sxs-lookup"><span data-stu-id="13c55-137">Longitude</span></span>](/windows/client-management/mdm/remotefind-csp#longitude)
</dt> <dd> <dl> <dt>

<span data-ttu-id="13c55-138">Tipo di dati: **real32**</span><span class="sxs-lookup"><span data-stu-id="13c55-138">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="13c55-139">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="13c55-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="13c55-140">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="13c55-140">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13c55-141">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="13c55-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="13c55-142">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="13c55-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="13c55-143">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="13c55-143">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="13c55-144">Descrive il percorso completo del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="13c55-144">Describes the full path to the parent node.</span></span> <span data-ttu-id="13c55-145">Per questa classe la stringa è "./Vendor/MSFT/RemoteFind"</span><span class="sxs-lookup"><span data-stu-id="13c55-145">For this class, the string is "./Vendor/MSFT/RemoteFind"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="13c55-146">Requisiti</span><span class="sxs-lookup"><span data-stu-id="13c55-146">Requirements</span></span>



| <span data-ttu-id="13c55-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="13c55-147">Requirement</span></span> | <span data-ttu-id="13c55-148">Valore</span><span class="sxs-lookup"><span data-stu-id="13c55-148">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="13c55-149">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="13c55-149">Minimum supported client</span></span><br/> | <span data-ttu-id="13c55-150">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="13c55-150">Windows 10 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="13c55-151">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="13c55-151">Minimum supported server</span></span><br/> | <span data-ttu-id="13c55-152">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="13c55-152">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="13c55-153">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="13c55-153">Namespace</span></span><br/>                | <span data-ttu-id="13c55-154">\\ \\ Dmmap MDM CIMV2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="13c55-154">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                              |
| <span data-ttu-id="13c55-155">MOF</span><span class="sxs-lookup"><span data-stu-id="13c55-155">MOF</span></span><br/>                      | <dl> <span data-ttu-id="13c55-156"><dt>DMWmiBridgeProv1. mof</dt></span><span class="sxs-lookup"><span data-stu-id="13c55-156"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl> |
| <span data-ttu-id="13c55-157">DLL</span><span class="sxs-lookup"><span data-stu-id="13c55-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="13c55-158"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="13c55-158"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="13c55-159">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="13c55-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13c55-160">Utilizzo di script di PowerShell con il provider del Bridge WMI</span><span class="sxs-lookup"><span data-stu-id="13c55-160">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

