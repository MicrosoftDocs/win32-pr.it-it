---
title: Classe MDM_DevDetail_Microsoft02
description: La \_ classe MDM DEVDETAIL \_ Microsoft02 gestisce l'oggetto di gestione che fornisce parametri specifici del dispositivo al server DM OMA.
ms.assetid: 22a8ba26-d215-4bc5-a51b-6933d5473da3
keywords:
- Classe MDM_DevDetail_Microsoft02
- Classe MDM_DevDetail_Microsoft02, descritta
topic_type:
- apiref
api_name:
- MDM_DevDetail_Microsoft02
- MDM_DevDetail_Microsoft02.InstanceID
- MDM_DevDetail_Microsoft02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b384f9a24e30ca739ff9290efc83730b6d467e4a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964622"
---
# <a name="mdm_devdetail_microsoft02-class"></a><span data-ttu-id="6870b-105">\_Classe MDM DEVDETAIL \_ Microsoft02</span><span class="sxs-lookup"><span data-stu-id="6870b-105">MDM\_DevDetail\_Microsoft02 class</span></span>

<span data-ttu-id="6870b-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="6870b-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="6870b-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="6870b-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="6870b-108">La classe **MDM \_ DEVDETAIL \_ Microsoft02** gestisce l'oggetto di gestione che fornisce parametri specifici del dispositivo al server DM OMA.</span><span class="sxs-lookup"><span data-stu-id="6870b-108">The **MDM\_DevDetail\_Microsoft02** class handles the management object which provides device-specific parameters to the OMA DM server.</span></span> <span data-ttu-id="6870b-109">Questi parametri del dispositivo non vengono inviati automaticamente dal client al server, ma possono essere sottoposti a query dai server che usano i comandi del DM OMA.</span><span class="sxs-lookup"><span data-stu-id="6870b-109">These device parameters are not sent from the client to the server automatically, but can be queried by servers using OMA DM commands.</span></span>

<span data-ttu-id="6870b-110">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="6870b-110">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="6870b-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6870b-111">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_DevDetail_Microsoft02
{
  string InstanceID;
  string ParentID;
  string MobileID;
  string RadioSwV;
  string Resolution;
  string CommercializationOperator;
  sint32 ProcessorArchitecture;
  sint32 ProcessorType;
  string OSPlatform;
  string LocalTime;
  string DeviceName;
};
```

## <a name="members"></a><span data-ttu-id="6870b-112">Members</span><span class="sxs-lookup"><span data-stu-id="6870b-112">Members</span></span>

<span data-ttu-id="6870b-113">La classe **MDM \_ DEVDETAIL \_ Microsoft02** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="6870b-113">The **MDM\_DevDetail\_Microsoft02** class has these types of members:</span></span>

-   [<span data-ttu-id="6870b-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="6870b-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6870b-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="6870b-115">Properties</span></span>

<span data-ttu-id="6870b-116">La classe **MDM \_ DEVDETAIL \_ Microsoft02** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="6870b-116">The **MDM\_DevDetail\_Microsoft02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="6870b-117">CommercializationOperator</span><span class="sxs-lookup"><span data-stu-id="6870b-117">CommercializationOperator</span></span>](/windows/client-management/mdm/devdetail-csp#ext-microsoft-commercializationoperator)
</dt> <dd> <dl> <dt>

<span data-ttu-id="6870b-118">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="6870b-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6870b-119">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="6870b-119">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="6870b-120">DeviceName</span><span class="sxs-lookup"><span data-stu-id="6870b-120">DeviceName</span></span>](/windows/client-management/mdm/devdetail-csp#ext-microsoft-devicename)
</dt> <dd> <dl> <dt>

<span data-ttu-id="6870b-121">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="6870b-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6870b-122">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="6870b-122">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="6870b-123">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="6870b-123">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6870b-124">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="6870b-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6870b-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6870b-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6870b-126">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="6870b-126">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="6870b-127">Identifica il nome del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="6870b-127">Identifies the name of the parent node.</span></span> <span data-ttu-id="6870b-128">Per questa classe la stringa è "Microsoft"</span><span class="sxs-lookup"><span data-stu-id="6870b-128">For this class, the string is "Microsoft"</span></span>

</dd> <dt>

[<span data-ttu-id="6870b-129">LocalTime</span><span class="sxs-lookup"><span data-stu-id="6870b-129">LocalTime</span></span>](/windows/client-management/mdm/devdetail-csp#ext-microsoft-localtime)
</dt> <dd> <dl> <dt>

<span data-ttu-id="6870b-130">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="6870b-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6870b-131">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="6870b-131">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="6870b-132">MobileID</span><span class="sxs-lookup"><span data-stu-id="6870b-132">MobileID</span></span>](/windows/client-management/mdm/devdetail-csp#ext-microsoft-mobileid)
</dt> <dd> <dl> <dt>

<span data-ttu-id="6870b-133">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="6870b-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6870b-134">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="6870b-134">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="6870b-135">OSPlatform</span><span class="sxs-lookup"><span data-stu-id="6870b-135">OSPlatform</span></span>](/windows/client-management/mdm/devdetail-csp#ext-microsoft-osplatform)
</dt> <dd> <dl> <dt>

<span data-ttu-id="6870b-136">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="6870b-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6870b-137">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="6870b-137">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="6870b-138">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="6870b-138">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6870b-139">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="6870b-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6870b-140">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6870b-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6870b-141">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="6870b-141">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="6870b-142">Descrive il percorso completo del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="6870b-142">Describes the full path to the parent node.</span></span> <span data-ttu-id="6870b-143">Per questa classe la stringa è "./DevDetail/Ext"</span><span class="sxs-lookup"><span data-stu-id="6870b-143">For this class, the string is "./DevDetail/Ext"</span></span>

</dd> <dt>

[<span data-ttu-id="6870b-144">ProcessorArchitecture</span><span class="sxs-lookup"><span data-stu-id="6870b-144">ProcessorArchitecture</span></span>](/windows/client-management/mdm/devdetail-csp#ext-microsoft-processorarchitecture)
</dt> <dd> <dl> <dt>

<span data-ttu-id="6870b-145">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="6870b-145">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="6870b-146">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="6870b-146">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="6870b-147">ProcessorType</span><span class="sxs-lookup"><span data-stu-id="6870b-147">ProcessorType</span></span>](/windows/client-management/mdm/devdetail-csp#ext-microsoft-processortype)
</dt> <dd> <dl> <dt>

<span data-ttu-id="6870b-148">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="6870b-148">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="6870b-149">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="6870b-149">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="6870b-150">RadioSwV</span><span class="sxs-lookup"><span data-stu-id="6870b-150">RadioSwV</span></span>](/windows/client-management/mdm/devdetail-csp#ext-microsoft-radioswv)
</dt> <dd> <dl> <dt>

<span data-ttu-id="6870b-151">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="6870b-151">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6870b-152">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="6870b-152">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="6870b-153">Restituisce il numero di versione del software dello stack di radio.</span><span class="sxs-lookup"><span data-stu-id="6870b-153">Returns the radio stack software version number.</span></span>

</dd> <dt>

[<span data-ttu-id="6870b-154">Risoluzione</span><span class="sxs-lookup"><span data-stu-id="6870b-154">Resolution</span></span>](/windows/client-management/mdm/devdetail-csp#ext-microsoft-resolution)
</dt> <dd> <dl> <dt>

<span data-ttu-id="6870b-155">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="6870b-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6870b-156">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="6870b-156">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6870b-157">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6870b-157">Requirements</span></span>



| <span data-ttu-id="6870b-158">Requisito</span><span class="sxs-lookup"><span data-stu-id="6870b-158">Requirement</span></span> | <span data-ttu-id="6870b-159">Valore</span><span class="sxs-lookup"><span data-stu-id="6870b-159">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6870b-160">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6870b-160">Minimum supported client</span></span><br/> | <span data-ttu-id="6870b-161">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="6870b-161">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6870b-162">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6870b-162">Minimum supported server</span></span><br/> | <span data-ttu-id="6870b-163">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="6870b-163">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="6870b-164">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="6870b-164">Namespace</span></span><br/>                | <span data-ttu-id="6870b-165">\\ \\ Dmmap MDM CIMV2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="6870b-165">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="6870b-166">MOF</span><span class="sxs-lookup"><span data-stu-id="6870b-166">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6870b-167"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6870b-167"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="6870b-168">DLL</span><span class="sxs-lookup"><span data-stu-id="6870b-168">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6870b-169"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6870b-169"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6870b-170">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6870b-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6870b-171">Utilizzo di script di PowerShell con il provider del Bridge WMI</span><span class="sxs-lookup"><span data-stu-id="6870b-171">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

