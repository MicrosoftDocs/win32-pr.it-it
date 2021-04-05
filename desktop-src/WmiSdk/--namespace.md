---
description: Rappresenta uno spazio dei nomi WMI.
ms.assetid: d5f0abc7-32cf-4d85-b5cd-5d60c991bcbc
ms.tgt_platform: multiple
title: Classe __Namespace
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __Namespace
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 9f396b588f372f26a808e97593ffcc30eac9b3ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884781"
---
# <a name="__namespace-class"></a><span data-ttu-id="6addd-103">\_\_Classe Namespace</span><span class="sxs-lookup"><span data-stu-id="6addd-103">\_\_Namespace class</span></span>

<span data-ttu-id="6addd-104">La classe di sistema **\_ \_ namespace** rappresenta uno spazio dei nomi WMI.</span><span class="sxs-lookup"><span data-stu-id="6addd-104">The **\_\_Namespace** system class represents a WMI namespace.</span></span>

<span data-ttu-id="6addd-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="6addd-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="6addd-106">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="6addd-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="6addd-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6addd-107">Syntax</span></span>

``` syntax
class __Namespace : __SystemClass
{
  string Name;
};
```

## <a name="members"></a><span data-ttu-id="6addd-108">Members</span><span class="sxs-lookup"><span data-stu-id="6addd-108">Members</span></span>

<span data-ttu-id="6addd-109">La classe **\_ \_ namespace** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="6addd-109">The **\_\_Namespace** class has these types of members:</span></span>

-   [<span data-ttu-id="6addd-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="6addd-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6addd-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="6addd-111">Properties</span></span>

<span data-ttu-id="6addd-112">La classe **\_ \_ namespace** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="6addd-112">The **\_\_Namespace** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6addd-113">**Nome**</span><span class="sxs-lookup"><span data-stu-id="6addd-113">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6addd-114">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="6addd-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6addd-115">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="6addd-115">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="6addd-116">Qualificatori: [ **chiave**](standard-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="6addd-116">Qualifiers: [**Key**](standard-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="6addd-117">Nome spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="6addd-117">Namespace name.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6addd-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="6addd-118">Remarks</span></span>

<span data-ttu-id="6addd-119">La classe **\_ \_ dello spazio dei nomi** è derivata da [**\_ \_ SystemClass**](--systemclass.md), che non dispone di proprietà.</span><span class="sxs-lookup"><span data-stu-id="6addd-119">The **\_\_Namespace** class is derived from [**\_\_SystemClass**](--systemclass.md), which has no properties.</span></span>

<span data-ttu-id="6addd-120">È possibile utilizzare lo **\_ \_ spazio dei nomi** per identificare, creare ed eliminare gli spazi dei nomi figlio nello spazio dei nomi funzionante corrente per il quale si dispone di un oggetto [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) .</span><span class="sxs-lookup"><span data-stu-id="6addd-120">You can use **\_\_Namespace** to identify, create, and delete child namespaces within the current working namespace for which you have an [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) object.</span></span> <span data-ttu-id="6addd-121">La creazione di una nuova istanza dello **\_ \_ spazio dei** nomi in qualsiasi spazio dei nomi funzionante crea uno spazio dei nomi figlio nello spazio dei nomi funzionante.</span><span class="sxs-lookup"><span data-stu-id="6addd-121">Creating a new instance of **\_\_Namespace** within any working namespace creates a child namespace within the working namespace.</span></span> <span data-ttu-id="6addd-122">Viceversa, l'eliminazione di un'istanza dello **\_ \_ spazio dei nomi** consente di rimuovere lo spazio dei nomi figlio dallo spazio dei nomi funzionante.</span><span class="sxs-lookup"><span data-stu-id="6addd-122">Conversely, deleting an instance of **\_\_Namespace** removes the child namespace from the working namespace.</span></span> <span data-ttu-id="6addd-123">Si noti che l'eliminazione di uno spazio dei nomi figlio elimina anche tutte le relative classi e istanze.</span><span class="sxs-lookup"><span data-stu-id="6addd-123">Note that deleting a child namespace also deletes all of its classes and instances.</span></span>

<span data-ttu-id="6addd-124">L'enumerazione delle istanze di questa classe in qualsiasi spazio dei nomi funzionante fornisce gli spazi dei nomi figlio disponibili.</span><span class="sxs-lookup"><span data-stu-id="6addd-124">Enumerating instances of this class within any working namespace gives the available child namespaces.</span></span>

<span data-ttu-id="6addd-125">Ad esempio, all'interno dello \\ spazio dei nomi radice si trovano due istanze dello **\_ \_ spazio dei nomi**.</span><span class="sxs-lookup"><span data-stu-id="6addd-125">For example, within the \\root namespace are two instances of **\_\_Namespace**.</span></span> <span data-ttu-id="6addd-126">Una ha la proprietà **Name** impostata su "default", l'altra ha il **nome** impostato su "Cimv2".</span><span class="sxs-lookup"><span data-stu-id="6addd-126">One has its **Name** property set to "Default," the other has **Name** set to "Cimv2."</span></span> <span data-ttu-id="6addd-127">Queste istanze rappresentano \\ rispettivamente gli \\ \\ \\ spazi dei nomi predefiniti radice e CIMV2 radice.</span><span class="sxs-lookup"><span data-stu-id="6addd-127">These instances represent the \\root\\default, and \\root\\cimv2 namespaces, respectively.</span></span>

## <a name="examples"></a><span data-ttu-id="6addd-128">Esempio</span><span class="sxs-lookup"><span data-stu-id="6addd-128">Examples</span></span>

<span data-ttu-id="6addd-129">Nell'esempio relativo all' [elenco di tutti gli spazi dei nomi WMI](https://Gallery.TechNet.Microsoft.Com/4a8e84f1-4b52-452c-ae4f-e4e00e266257) della raccolta TechNet viene utilizzata una chiamata ricorsiva per elencare tutte le istanze della \_ \_ classe dello spazio dei nomi in un sistema.</span><span class="sxs-lookup"><span data-stu-id="6addd-129">The [List All WMI Namespaces](https://Gallery.TechNet.Microsoft.Com/4a8e84f1-4b52-452c-ae4f-e4e00e266257) VBScript example on the TechNet Gallery uses a recursive call to list all instances of the \_\_Namespace class on a system.</span></span>

<span data-ttu-id="6addd-130">Nell'esempio di codice seguente vengono recuperati tutti gli spazi dei nomi in PowerShell.</span><span class="sxs-lookup"><span data-stu-id="6addd-130">The following code sample retrieves all namespaces in PowerShell.</span></span>


```PowerShell
get-wmiobject __namespace -namespace 'root' -list -recurse | format-table __namespace
```



<span data-ttu-id="6addd-131">Nell'esempio di codice seguente viene migliorato l'esempio precedente e vengono aggiunte altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="6addd-131">The following code sample improves on the previous sample, and adds in additional information.</span></span>


```PowerShell
# Set computer name 
$comp = "." 
 
# Get the name spaces on the local computer, and the local computer name 
$Namespace = get-wmiobject __namespace -namespace 'root' -list -recurse -computer $comp  
$hotsname = hostname 
 
# Display number of and names of the namespaces 
"{0} Namespaces on: {1}" -f $namespace.count, $hostname 
$NameSpace| sort __namespace  | Format-Table @{Expression = "__Namespace"; Label = "Namespace"}
```



## <a name="requirements"></a><span data-ttu-id="6addd-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6addd-132">Requirements</span></span>



| <span data-ttu-id="6addd-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="6addd-133">Requirement</span></span> | <span data-ttu-id="6addd-134">Valore</span><span class="sxs-lookup"><span data-stu-id="6addd-134">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="6addd-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6addd-135">Minimum supported client</span></span><br/> | <span data-ttu-id="6addd-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6addd-136">Windows Vista</span></span><br/>       |
| <span data-ttu-id="6addd-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6addd-137">Minimum supported server</span></span><br/> | <span data-ttu-id="6addd-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6addd-138">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="6addd-139">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="6addd-139">Namespace</span></span><br/>                | <span data-ttu-id="6addd-140">Tutti gli spazi dei nomi WMI</span><span class="sxs-lookup"><span data-stu-id="6addd-140">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="6addd-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6addd-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6addd-142">**\_\_SystemClass**</span><span class="sxs-lookup"><span data-stu-id="6addd-142">**\_\_SystemClass**</span></span>](--systemclass.md)
</dt> <dt>

[<span data-ttu-id="6addd-143">Classi di sistema WMI</span><span class="sxs-lookup"><span data-stu-id="6addd-143">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

 




