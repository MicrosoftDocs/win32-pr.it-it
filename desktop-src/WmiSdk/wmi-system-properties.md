---
description: Strumentazione gestione Windows (WMI) definisce un set di proprietà di sistema associate a tutte le classi e istanze delle classi.
ms.assetid: e812c0cb-3e08-4cac-8d05-2cd7abc922d1
ms.tgt_platform: multiple
title: Proprietà di sistema WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3ee541d9de0d37c9aa1eae4ded07d3cb70ff1bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226935"
---
# <a name="wmi-system-properties"></a><span data-ttu-id="8e4a9-103">Proprietà di sistema WMI</span><span class="sxs-lookup"><span data-stu-id="8e4a9-103">WMI System Properties</span></span>

<span data-ttu-id="8e4a9-104">Strumentazione gestione Windows (WMI) definisce un set di proprietà di sistema associate a tutte le classi e istanze delle classi.</span><span class="sxs-lookup"><span data-stu-id="8e4a9-104">Windows Management Instrumentation (WMI) defines a set of system properties that are associated with all classes and instances of classes.</span></span> <span data-ttu-id="8e4a9-105">Come per le classi di sistema, i nomi delle proprietà di sistema iniziano con un carattere di sottolineatura doppio, che li distingue dalle proprietà create da applicazioni o provider che non devono iniziare con un carattere di sottolineatura singolo o doppio.</span><span class="sxs-lookup"><span data-stu-id="8e4a9-105">As with system classes, system property names begin with a double underscore, distinguishing them from properties created by applications or providers that must not start with a single or double underscore.</span></span> <span data-ttu-id="8e4a9-106">Un altro modo per identificare una proprietà di sistema consiste nell'usare il metodo [**IWbemClassObject:: Get**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-get) .</span><span class="sxs-lookup"><span data-stu-id="8e4a9-106">Another way to identify a system property is to use the [**IWbemClassObject::Get**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-get) method.</span></span>

<span data-ttu-id="8e4a9-107">Le proprietà di sistema sono disponibili in qualsiasi momento, ma i valori possono essere **null**.</span><span class="sxs-lookup"><span data-stu-id="8e4a9-107">System properties are available at any time, but values might be **NULL**.</span></span> <span data-ttu-id="8e4a9-108">**Null** indica che una proprietà non è applicabile a un oggetto specifico.</span><span class="sxs-lookup"><span data-stu-id="8e4a9-108">**NULL** indicates a property does not apply to a specific object.</span></span> <span data-ttu-id="8e4a9-109">Tuttavia, le proprietà di sistema potrebbero non essere sempre disponibili per tutte le classi o le istanze.</span><span class="sxs-lookup"><span data-stu-id="8e4a9-109">However, system properties might not be available all the time for all classes or instances.</span></span>

## <a name="system-properties"></a><span data-ttu-id="8e4a9-110">Proprietà di sistema</span><span class="sxs-lookup"><span data-stu-id="8e4a9-110">System Properties</span></span>

<span data-ttu-id="8e4a9-111">Nell'elenco seguente vengono descritte le proprietà di sistema WMI.</span><span class="sxs-lookup"><span data-stu-id="8e4a9-111">The following list describes the WMI system properties.</span></span> <span data-ttu-id="8e4a9-112">Gli esempi forniti sono ricavati dalle proprietà di sistema della classe [**Win32 \_ OptionalFeature**](/windows/desktop/CIMWin32Prov/win32-optionalfeature) , descritta nella parte inferiore di questo argomento.</span><span class="sxs-lookup"><span data-stu-id="8e4a9-112">The examples given are taken from the system properties of the [**Win32\_OptionalFeature**](/windows/desktop/CIMWin32Prov/win32-optionalfeature) class, which is described at the bottom of this topic.</span></span>

<dl> <dt>

<span data-ttu-id="8e4a9-113"><span id="__Class"></span><span id="__class"></span><span id="__CLASS"></span>**\_\_Classe**</span><span class="sxs-lookup"><span data-stu-id="8e4a9-113"><span id="__Class"></span><span id="__class"></span><span id="__CLASS"></span>**\_\_Class**</span></span>
</dt> <dd>

<span data-ttu-id="8e4a9-114">Tipo di dati **: \_ stringa CIM**</span><span class="sxs-lookup"><span data-stu-id="8e4a9-114">Data type: **CIM\_STRING**</span></span>

<span data-ttu-id="8e4a9-115">Tipo di accesso: sola lettura per le istanze; lettura/scrittura per le classi</span><span class="sxs-lookup"><span data-stu-id="8e4a9-115">Access type: Read-only for instances; read/write for classes</span></span>

<span data-ttu-id="8e4a9-116">Nome della classe.</span><span class="sxs-lookup"><span data-stu-id="8e4a9-116">The name of the class.</span></span>

<span data-ttu-id="8e4a9-117">Esempio: Win32 \_ OptionalFeature</span><span class="sxs-lookup"><span data-stu-id="8e4a9-117">Example: Win32\_OptionalFeature</span></span>

</dd> <dt>

<span data-ttu-id="8e4a9-118"><span id="__Derivation"></span><span id="__derivation"></span><span id="__DERIVATION"></span>**\_\_Derivazione**</span><span class="sxs-lookup"><span data-stu-id="8e4a9-118"><span id="__Derivation"></span><span id="__derivation"></span><span id="__DERIVATION"></span>**\_\_Derivation**</span></span>
</dt> <dd>

<span data-ttu-id="8e4a9-119">Tipo di dati: matrice di **\_ stringhe CIM**</span><span class="sxs-lookup"><span data-stu-id="8e4a9-119">Data type: **CIM\_STRING** array</span></span>

<span data-ttu-id="8e4a9-120">Tipo di accesso: sola lettura per istanze e classi</span><span class="sxs-lookup"><span data-stu-id="8e4a9-120">Access type: Read-only for both instances and classes</span></span>

<span data-ttu-id="8e4a9-121">Gerarchia di classi della classe o dell'istanza corrente.</span><span class="sxs-lookup"><span data-stu-id="8e4a9-121">Class hierarchy of the current class or instance.</span></span> <span data-ttu-id="8e4a9-122">Il primo elemento è la classe padre immediata, il successivo è il padre e così via; l'ultimo elemento è la classe base.</span><span class="sxs-lookup"><span data-stu-id="8e4a9-122">The first element is the immediate parent class, the next is its parent, and so on; the last element is the base class.</span></span>

<span data-ttu-id="8e4a9-123">Esempio: {CIM \_ LogicalElement, CIM \_ ManagedSystemElement}</span><span class="sxs-lookup"><span data-stu-id="8e4a9-123">Example: {CIM\_LogicalElement, CIM\_ManagedSystemElement}</span></span>

</dd> <dt>

<span data-ttu-id="8e4a9-124"><span id="__Dynasty"></span><span id="__dynasty"></span><span id="__DYNASTY"></span>**\_\_Dinastia**</span><span class="sxs-lookup"><span data-stu-id="8e4a9-124"><span id="__Dynasty"></span><span id="__dynasty"></span><span id="__DYNASTY"></span>**\_\_Dynasty**</span></span>
</dt> <dd>

<span data-ttu-id="8e4a9-125">Tipo di dati **: \_ stringa CIM**</span><span class="sxs-lookup"><span data-stu-id="8e4a9-125">Data type: **CIM\_STRING**</span></span>

<span data-ttu-id="8e4a9-126">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8e4a9-126">Access type: Read-only</span></span>

<span data-ttu-id="8e4a9-127">Nome della classe di primo livello da cui viene derivata la classe o l'istanza.</span><span class="sxs-lookup"><span data-stu-id="8e4a9-127">Name of the top-level class from which the class or instance is derived.</span></span> <span data-ttu-id="8e4a9-128">Quando questa classe o istanza è la classe di primo livello, i valori di **\_ \_ Dynasty** e **\_ \_ Class** sono gli stessi.</span><span class="sxs-lookup"><span data-stu-id="8e4a9-128">When this class or instance is the top-level class, the values of **\_\_Dynasty** and **\_\_Class** are the same.</span></span>

<span data-ttu-id="8e4a9-129">Esempio: CIM \_ ManagedSystemElement</span><span class="sxs-lookup"><span data-stu-id="8e4a9-129">Example: CIM\_ManagedSystemElement</span></span>

</dd> <dt>

<span data-ttu-id="8e4a9-130"><span id="__Genus"></span><span id="__genus"></span><span id="__GENUS"></span>**\_\_Genere**</span><span class="sxs-lookup"><span data-stu-id="8e4a9-130"><span id="__Genus"></span><span id="__genus"></span><span id="__GENUS"></span>**\_\_Genus**</span></span>
</dt> <dd>

<span data-ttu-id="8e4a9-131">Tipo di dati: **CIM \_ SINT32**</span><span class="sxs-lookup"><span data-stu-id="8e4a9-131">Data type: **CIM\_SINT32**</span></span>

<span data-ttu-id="8e4a9-132">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8e4a9-132">Access type: Read-only</span></span>

<span data-ttu-id="8e4a9-133">Valore utilizzato per distinguere le classi e le istanze.</span><span class="sxs-lookup"><span data-stu-id="8e4a9-133">Value that is used to distinguish between classes and instances.</span></span> <span data-ttu-id="8e4a9-134">Questo valore è **WBEM \_ genre \_ Class** (1) per le classi e **WBEM \_ genre \_ instance** (2) per le istanze e gli eventi.</span><span class="sxs-lookup"><span data-stu-id="8e4a9-134">This value is **WBEM\_GENUS\_CLASS** (1) for classes, and **WBEM\_GENUS\_INSTANCE** (2) for instances and events.</span></span>

<span data-ttu-id="8e4a9-135">Esempio: 2</span><span class="sxs-lookup"><span data-stu-id="8e4a9-135">Example: 2</span></span>

</dd> <dt>

<span data-ttu-id="8e4a9-136"><span id="__Namespace"></span><span id="__namespace"></span><span id="__NAMESPACE"></span>[**\_\_Namespace**](--namespace.md)</span><span class="sxs-lookup"><span data-stu-id="8e4a9-136"><span id="__Namespace"></span><span id="__namespace"></span><span id="__NAMESPACE"></span>[**\_\_Namespace**](--namespace.md)</span></span>
</dt> <dd>

<span data-ttu-id="8e4a9-137">Tipo di dati **: \_ stringa CIM**</span><span class="sxs-lookup"><span data-stu-id="8e4a9-137">Data type: **CIM\_STRING**</span></span>

<span data-ttu-id="8e4a9-138">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8e4a9-138">Access type: Read-only</span></span>

<span data-ttu-id="8e4a9-139">Nome dello [*spazio dei nomi*](gloss-n.md) della classe o dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="8e4a9-139">Name of the [*namespace*](gloss-n.md) of the class or instance.</span></span>

<span data-ttu-id="8e4a9-140">Esempio: radice \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="8e4a9-140">Example: root\\cimv2</span></span>

</dd> <dt>

<span data-ttu-id="8e4a9-141"><span id="__Path"></span><span id="__path"></span><span id="__PATH"></span>**\_\_Percorso**</span><span class="sxs-lookup"><span data-stu-id="8e4a9-141"><span id="__Path"></span><span id="__path"></span><span id="__PATH"></span>**\_\_Path**</span></span>
</dt> <dd>

<span data-ttu-id="8e4a9-142">Tipo di dati **: \_ stringa CIM**</span><span class="sxs-lookup"><span data-stu-id="8e4a9-142">Data type: **CIM\_STRING**</span></span>

<span data-ttu-id="8e4a9-143">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8e4a9-143">Access type: Read-only</span></span>

<span data-ttu-id="8e4a9-144">Percorso completo della classe o dell'istanza, inclusi server e spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="8e4a9-144">Full path to the class or instance—including server and namespace.</span></span>

<span data-ttu-id="8e4a9-145">Esempio: \\ \\ MyServer \\ radice \\ CIMV2: Win32 \_ OptionalFeature. Name = "TelnetClient"</span><span class="sxs-lookup"><span data-stu-id="8e4a9-145">Example: \\\\MyServer\\root\\cimv2:Win32\_OptionalFeature.Name="TelnetClient"</span></span>

</dd> <dt>

<span data-ttu-id="8e4a9-146"><span id="__Property_Count"></span><span id="__property_count"></span><span id="__PROPERTY_COUNT"></span>**\_\_\_Conteggio proprietà**</span><span class="sxs-lookup"><span data-stu-id="8e4a9-146"><span id="__Property_Count"></span><span id="__property_count"></span><span id="__PROPERTY_COUNT"></span>**\_\_Property\_Count**</span></span>
</dt> <dd>

<span data-ttu-id="8e4a9-147">Tipo di dati: **CIM \_ SINT32**</span><span class="sxs-lookup"><span data-stu-id="8e4a9-147">Data type: **CIM\_SINT32**</span></span>

<span data-ttu-id="8e4a9-148">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8e4a9-148">Access type: Read-only</span></span>

<span data-ttu-id="8e4a9-149">Numero di proprietà non di sistema definite per la classe o l'istanza.</span><span class="sxs-lookup"><span data-stu-id="8e4a9-149">Number of nonsystem properties defined for the class or instance.</span></span>

<span data-ttu-id="8e4a9-150">Esempio: 6</span><span class="sxs-lookup"><span data-stu-id="8e4a9-150">Example: 6</span></span>

</dd> <dt>

<span data-ttu-id="8e4a9-151"><span id="__Relpath"></span><span id="__relpath"></span><span id="__RELPATH"></span>**\_\_RelPath**</span><span class="sxs-lookup"><span data-stu-id="8e4a9-151"><span id="__Relpath"></span><span id="__relpath"></span><span id="__RELPATH"></span>**\_\_Relpath**</span></span>
</dt> <dd>

<span data-ttu-id="8e4a9-152">Tipo di dati **: \_ stringa CIM**</span><span class="sxs-lookup"><span data-stu-id="8e4a9-152">Data type: **CIM\_STRING**</span></span>

<span data-ttu-id="8e4a9-153">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8e4a9-153">Access type: Read-only</span></span>

<span data-ttu-id="8e4a9-154">Percorso relativo della classe o dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="8e4a9-154">Relative path to the class or instance.</span></span>

<span data-ttu-id="8e4a9-155">Esempio: Win32 \_ OptionalFeature. Name = "TelnetClient"</span><span class="sxs-lookup"><span data-stu-id="8e4a9-155">Example: Win32\_OptionalFeature.Name="TelnetClient"</span></span>

</dd> <dt>

<span data-ttu-id="8e4a9-156"><span id="__Server"></span><span id="__server"></span><span id="__SERVER"></span>**\_\_Server**</span><span class="sxs-lookup"><span data-stu-id="8e4a9-156"><span id="__Server"></span><span id="__server"></span><span id="__SERVER"></span>**\_\_Server**</span></span>
</dt> <dd>

<span data-ttu-id="8e4a9-157">Tipo di dati **: \_ stringa CIM**</span><span class="sxs-lookup"><span data-stu-id="8e4a9-157">Data type: **CIM\_STRING**</span></span>

<span data-ttu-id="8e4a9-158">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8e4a9-158">Access type: Read-only</span></span>

<span data-ttu-id="8e4a9-159">Nome del server che fornisce la classe o l'istanza.</span><span class="sxs-lookup"><span data-stu-id="8e4a9-159">Name of the server supplying the class or instance.</span></span>

<span data-ttu-id="8e4a9-160">Esempio: myserver</span><span class="sxs-lookup"><span data-stu-id="8e4a9-160">Example: MyServer</span></span>

</dd> <dt>

<span data-ttu-id="8e4a9-161"><span id="__Superclass"></span><span id="__superclass"></span><span id="__SUPERCLASS"></span>**\_\_Superclasse**</span><span class="sxs-lookup"><span data-stu-id="8e4a9-161"><span id="__Superclass"></span><span id="__superclass"></span><span id="__SUPERCLASS"></span>**\_\_Superclass**</span></span>
</dt> <dd>

<span data-ttu-id="8e4a9-162">Tipo di dati **: \_ stringa CIM**</span><span class="sxs-lookup"><span data-stu-id="8e4a9-162">Data type: **CIM\_STRING**</span></span>

<span data-ttu-id="8e4a9-163">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8e4a9-163">Access type: Read-only</span></span>

<span data-ttu-id="8e4a9-164">Nome della classe padre immediata della classe o dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="8e4a9-164">Name of the immediate parent class of the class or instance.</span></span>

<span data-ttu-id="8e4a9-165">Esempio: CIM \_ LogicalElement</span><span class="sxs-lookup"><span data-stu-id="8e4a9-165">Example: CIM\_LogicalElement</span></span>

</dd> </dl>

<span data-ttu-id="8e4a9-166">Il codice di PowerShell seguente consente di recuperare le proprietà della classe [**Win32 \_ OptionalFeature**](/windows/desktop/CIMWin32Prov/win32-optionalfeature) , che include le proprietà di sistema.</span><span class="sxs-lookup"><span data-stu-id="8e4a9-166">The following PowerShell code retrieves the properties of the [**Win32\_OptionalFeature**](/windows/desktop/CIMWin32Prov/win32-optionalfeature) class, which includes the system properties.</span></span>


```PowerShell
Get-WmiObject win32_OptionalFeature | Where-Object {$_.name -eq "TelnetClient"}
```



<span data-ttu-id="8e4a9-167">Nell'esempio di codice precedente vengono restituiti gli elementi seguenti:</span><span class="sxs-lookup"><span data-stu-id="8e4a9-167">The previous code sample returns the following:</span></span>


```PowerShell
__GENUS          : 2
__CLASS          : Win32_OptionalFeature
__SUPERCLASS     : CIM_LogicalElement
__DYNASTY        : CIM_ManagedSystemElement
__RELPATH        : Win32_OptionalFeature.Name="TelnetClient"
__PROPERTY_COUNT : 6
__DERIVATION     : {CIM_LogicalElement, CIM_ManagedSystemElement}
__SERVER         : myServer
__NAMESPACE      : root\cimv2
__PATH           : \\myServer\root\cimv2:Win32_OptionalFeature.Name="TelnetClient"
Caption          : Telnet Client
Description      : 
InstallDate      : 
InstallState     : 2
Name             : TelnetClient
Status           : 
PSComputerName   : myServer
```



 

 
