---
title: Classe MDM_DevDetail
description: La \_ classe MDM DEVDETAIL gestisce l'oggetto di gestione che fornisce parametri specifici del dispositivo al server DM OMA.
ms.assetid: 1a709051-656a-4900-b354-efbd208b46fc
keywords:
- Classe MDM_DevDetail
- Classe MDM_DevDetail, descritta
topic_type:
- apiref
api_name:
- MDM_DevDetail
- MDM_DevDetail.InstanceID
- MDM_DevDetail.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 751c4e147dd0b60398ed16eeb3eb60a8a768307f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302122"
---
# <a name="mdm_devdetail-class"></a><span data-ttu-id="aa4ce-105">MDM \_ DEVDETAIL (classe)</span><span class="sxs-lookup"><span data-stu-id="aa4ce-105">MDM\_DevDetail class</span></span>

<span data-ttu-id="aa4ce-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="aa4ce-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="aa4ce-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="aa4ce-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="aa4ce-108">La classe **MDM \_ DEVDETAIL** gestisce l'oggetto di gestione che fornisce parametri specifici del dispositivo al server DM OMA.</span><span class="sxs-lookup"><span data-stu-id="aa4ce-108">The **MDM\_DevDetail** class handles the management object which provides device-specific parameters to the OMA DM server.</span></span> <span data-ttu-id="aa4ce-109">Questi parametri del dispositivo non vengono inviati automaticamente dal client al server, ma possono essere sottoposti a query dai server che usano i comandi del DM OMA.</span><span class="sxs-lookup"><span data-stu-id="aa4ce-109">These device parameters are not sent from the client to the server automatically, but can be queried by servers using OMA DM commands.</span></span>

<span data-ttu-id="aa4ce-110">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="aa4ce-110">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa4ce-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="aa4ce-111">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_DevDetail
{
  string  InstanceID;
  string  ParentID;
  string  DevTyp;
  string  OEM;
  string  FwV;
  string  SwV;
  string  HwV;
  boolean LrgObj;
};
```

## <a name="members"></a><span data-ttu-id="aa4ce-112">Members</span><span class="sxs-lookup"><span data-stu-id="aa4ce-112">Members</span></span>

<span data-ttu-id="aa4ce-113">La classe **MDM \_ DEVDETAIL** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="aa4ce-113">The **MDM\_DevDetail** class has these types of members:</span></span>

-   [<span data-ttu-id="aa4ce-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="aa4ce-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="aa4ce-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="aa4ce-115">Properties</span></span>

<span data-ttu-id="aa4ce-116">La classe **MDM \_ DEVDETAIL** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="aa4ce-116">The **MDM\_DevDetail** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="aa4ce-117">DevTyp</span><span class="sxs-lookup"><span data-stu-id="aa4ce-117">DevTyp</span></span>](/windows/client-management/mdm/devdetail-csp#devtyp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa4ce-118">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="aa4ce-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aa4ce-119">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="aa4ce-119">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="aa4ce-120">FwV</span><span class="sxs-lookup"><span data-stu-id="aa4ce-120">FwV</span></span>](/windows/client-management/mdm/devdetail-csp#fwv)
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa4ce-121">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="aa4ce-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aa4ce-122">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="aa4ce-122">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="aa4ce-123">HwV</span><span class="sxs-lookup"><span data-stu-id="aa4ce-123">HwV</span></span>](/windows/client-management/mdm/devdetail-csp#hwv)
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa4ce-124">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="aa4ce-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aa4ce-125">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="aa4ce-125">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="aa4ce-126">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="aa4ce-126">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa4ce-127">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="aa4ce-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aa4ce-128">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="aa4ce-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa4ce-129">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="aa4ce-129">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="aa4ce-130">Identifica il nome del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="aa4ce-130">Identifies the name of the parent node.</span></span> <span data-ttu-id="aa4ce-131">Per questa classe la stringa è "DevDetail"</span><span class="sxs-lookup"><span data-stu-id="aa4ce-131">For this class, the string is "DevDetail"</span></span>

</dd> <dt>

[<span data-ttu-id="aa4ce-132">LrgObj</span><span class="sxs-lookup"><span data-stu-id="aa4ce-132">LrgObj</span></span>](/windows/client-management/mdm/devdetail-csp#lrgobj)
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa4ce-133">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="aa4ce-133">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="aa4ce-134">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="aa4ce-134">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="aa4ce-135">OEM</span><span class="sxs-lookup"><span data-stu-id="aa4ce-135">OEM</span></span>](/windows/client-management/mdm/devdetail-csp#oem)
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa4ce-136">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="aa4ce-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aa4ce-137">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="aa4ce-137">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="aa4ce-138">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="aa4ce-138">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa4ce-139">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="aa4ce-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aa4ce-140">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="aa4ce-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa4ce-141">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="aa4ce-141">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="aa4ce-142">Descrive il percorso completo del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="aa4ce-142">Describes the full path to the parent node.</span></span>

</dd> <dt>

[<span data-ttu-id="aa4ce-143">SwV</span><span class="sxs-lookup"><span data-stu-id="aa4ce-143">SwV</span></span>](/windows/client-management/mdm/devdetail-csp#swv)
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa4ce-144">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="aa4ce-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aa4ce-145">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="aa4ce-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="aa4ce-146">Requisiti</span><span class="sxs-lookup"><span data-stu-id="aa4ce-146">Requirements</span></span>



| <span data-ttu-id="aa4ce-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="aa4ce-147">Requirement</span></span> | <span data-ttu-id="aa4ce-148">Valore</span><span class="sxs-lookup"><span data-stu-id="aa4ce-148">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa4ce-149">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="aa4ce-149">Minimum supported client</span></span><br/> | <span data-ttu-id="aa4ce-150">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="aa4ce-150">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="aa4ce-151">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="aa4ce-151">Minimum supported server</span></span><br/> | <span data-ttu-id="aa4ce-152">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="aa4ce-152">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="aa4ce-153">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="aa4ce-153">Namespace</span></span><br/>                | <span data-ttu-id="aa4ce-154">\\ \\ Dmmap MDM CIMV2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="aa4ce-154">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="aa4ce-155">MOF</span><span class="sxs-lookup"><span data-stu-id="aa4ce-155">MOF</span></span><br/>                      | <dl> <span data-ttu-id="aa4ce-156"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="aa4ce-156"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="aa4ce-157">DLL</span><span class="sxs-lookup"><span data-stu-id="aa4ce-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aa4ce-158"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aa4ce-158"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aa4ce-159">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="aa4ce-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa4ce-160">Utilizzo di script di PowerShell con il provider del Bridge WMI</span><span class="sxs-lookup"><span data-stu-id="aa4ce-160">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

