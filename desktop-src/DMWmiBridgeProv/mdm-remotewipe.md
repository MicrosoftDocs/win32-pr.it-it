---
title: Classe MDM_RemoteWipe
description: La \_ classe MDM RemoteWipe consente la cancellazione remota di un dispositivo.
ms.assetid: 8c7c8705-8694-4ce3-ba21-ca610fe1f547
keywords:
- Classe MDM_RemoteWipe
- Classe MDM_RemoteWipe, descritta
topic_type:
- apiref
api_name:
- MDM_RemoteWipe
- MDM_RemoteWipe.InstanceID
- MDM_RemoteWipe.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ece626fca573e34cf938105f5e59b61e0585fd3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104047897"
---
# <a name="mdm_remotewipe-class"></a><span data-ttu-id="e6c8d-105">MDM \_ RemoteWipe (classe)</span><span class="sxs-lookup"><span data-stu-id="e6c8d-105">MDM\_RemoteWipe class</span></span>

<span data-ttu-id="e6c8d-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="e6c8d-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="e6c8d-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="e6c8d-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="e6c8d-108">La classe **MDM \_ RemoteWipe** consente la cancellazione remota di un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e6c8d-108">The **MDM\_RemoteWipe** class allows a remote wipe of a device.</span></span>

<span data-ttu-id="e6c8d-109">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="e6c8d-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6c8d-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e6c8d-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_RemoteWipe
{
  string InstanceID;
  string ParentID;
};
```

## <a name="members"></a><span data-ttu-id="e6c8d-111">Members</span><span class="sxs-lookup"><span data-stu-id="e6c8d-111">Members</span></span>

<span data-ttu-id="e6c8d-112">La classe **MDM \_ RemoteWipe** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="e6c8d-112">The **MDM\_RemoteWipe** class has these types of members:</span></span>

-   [<span data-ttu-id="e6c8d-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="e6c8d-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="e6c8d-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="e6c8d-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="e6c8d-115">Metodi</span><span class="sxs-lookup"><span data-stu-id="e6c8d-115">Methods</span></span>

<span data-ttu-id="e6c8d-116">La classe **MDM \_ RemoteWipe** ha questi metodi.</span><span class="sxs-lookup"><span data-stu-id="e6c8d-116">The **MDM\_RemoteWipe** class has these methods.</span></span>



| <span data-ttu-id="e6c8d-117">Metodo</span><span class="sxs-lookup"><span data-stu-id="e6c8d-117">Method</span></span>                                              | <span data-ttu-id="e6c8d-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e6c8d-118">Description</span></span>                                              |
|:----------------------------------------------------|:---------------------------------------------------------|
| [<span data-ttu-id="e6c8d-119">**doWipeMethod**</span><span class="sxs-lookup"><span data-stu-id="e6c8d-119">**doWipeMethod**</span></span>](mdm-remotewipe-dowipemethod.md) | <span data-ttu-id="e6c8d-120">Attiva il dispositivo per avviare la cancellazione remota.</span><span class="sxs-lookup"><span data-stu-id="e6c8d-120">Triggers the device to start the remote wipe.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="e6c8d-121">Proprietà</span><span class="sxs-lookup"><span data-stu-id="e6c8d-121">Properties</span></span>

<span data-ttu-id="e6c8d-122">La classe **MDM \_ RemoteWipe** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="e6c8d-122">The **MDM\_RemoteWipe** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e6c8d-123">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="e6c8d-123">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6c8d-124">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e6c8d-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e6c8d-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e6c8d-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e6c8d-126">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="e6c8d-126">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="e6c8d-127">Identifica il nome del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="e6c8d-127">Identifies the name of the parent node.</span></span> <span data-ttu-id="e6c8d-128">Per questa classe la stringa è "RemoteWipe".</span><span class="sxs-lookup"><span data-stu-id="e6c8d-128">For this class, the string is "RemoteWipe".</span></span>

</dd> <dt>

<span data-ttu-id="e6c8d-129">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="e6c8d-129">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e6c8d-130">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e6c8d-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e6c8d-131">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e6c8d-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e6c8d-132">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="e6c8d-132">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="e6c8d-133">Descrive il percorso completo del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="e6c8d-133">Describes the full path to the parent node.</span></span> <span data-ttu-id="e6c8d-134">Per questa classe la stringa è "./Vendor/MSFT/"</span><span class="sxs-lookup"><span data-stu-id="e6c8d-134">For this class, the string is "./Vendor/MSFT/"</span></span>

</dd> </dl>

## <a name="example"></a><span data-ttu-id="e6c8d-135">Esempio</span><span class="sxs-lookup"><span data-stu-id="e6c8d-135">Example</span></span>

<span data-ttu-id="e6c8d-136">Nell'esempio seguente viene illustrato come utilizzare RemoteWipe e richiamare doWipeMethod.</span><span class="sxs-lookup"><span data-stu-id="e6c8d-136">The following example demonstrates how to use the RemoteWipe and invoke the doWipeMethod.</span></span>

> [!Note]  
> <span data-ttu-id="e6c8d-137">Questo esempio deve essere eseguito con l'utente di sistema locale.</span><span class="sxs-lookup"><span data-stu-id="e6c8d-137">This example must be executed under local system user.</span></span> <span data-ttu-id="e6c8d-138">A tale scopo, scaricare lo strumento PsExec da <https://technet.microsoft.com/sysinternals/bb897553.aspx> ed eseguire `psexec.exe -i -s cmd.exe` da un prompt dei comandi di amministrazione con privilegi elevati.</span><span class="sxs-lookup"><span data-stu-id="e6c8d-138">To do that, download the psexec tool from <https://technet.microsoft.com/sysinternals/bb897553.aspx> and run `psexec.exe -i -s cmd.exe` from an elevated admin command prompt.</span></span>

 

``` syntax
$namespaceName = "root\cimv2\mdm\dmmap"
$className = "MDM_RemoteWipe"
$methodName = "doWipeMethod"

$session = New-CimSession

$params = New-Object Microsoft.Management.Infrastructure.CimMethodParametersCollection
$param = [Microsoft.Management.Infrastructure.CimMethodParameter]::Create("param", "", "String", "In")
$params.Add($param)

try
{
    $instance = Get-CimInstance -Namespace $namespaceName -ClassName $className -Filter "ParentID='./Vendor/MSFT' and InstanceID='RemoteWipe'"
    $session.InvokeMethod($namespaceName, $instance, $methodName, $params)
}
catch [Exception]
{
    write-host $_ | out-string
}
```

## <a name="requirements"></a><span data-ttu-id="e6c8d-139">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e6c8d-139">Requirements</span></span>



| <span data-ttu-id="e6c8d-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="e6c8d-140">Requirement</span></span> | <span data-ttu-id="e6c8d-141">Valore</span><span class="sxs-lookup"><span data-stu-id="e6c8d-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6c8d-142">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e6c8d-142">Minimum supported client</span></span><br/> | <span data-ttu-id="e6c8d-143">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="e6c8d-143">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e6c8d-144">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e6c8d-144">Minimum supported server</span></span><br/> | <span data-ttu-id="e6c8d-145">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="e6c8d-145">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="e6c8d-146">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="e6c8d-146">Namespace</span></span><br/>                | <span data-ttu-id="e6c8d-147">\\ \\ DMMap MDM CIMv2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="e6c8d-147">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="e6c8d-148">MOF</span><span class="sxs-lookup"><span data-stu-id="e6c8d-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e6c8d-149"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e6c8d-149"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="e6c8d-150">DLL</span><span class="sxs-lookup"><span data-stu-id="e6c8d-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e6c8d-151"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e6c8d-151"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e6c8d-152">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e6c8d-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6c8d-153">Utilizzo di script di PowerShell con il provider del Bridge WMI</span><span class="sxs-lookup"><span data-stu-id="e6c8d-153">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

