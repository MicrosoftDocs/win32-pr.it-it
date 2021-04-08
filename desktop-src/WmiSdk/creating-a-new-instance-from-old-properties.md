---
description: Una classe di visualizzazione join contiene le proprietà delle istanze della classe di origine connesse da un valore di proprietà comune, ad esempio Class1. Prop1 = Class2. Prop2. Ogni istanza in una classe di visualizzazione join è costituita da parti di istanze di classi diverse.
ms.assetid: 4d35474d-0b80-4b00-9724-47a193bfd0fc
ms.tgt_platform: multiple
title: Creazione di una nuova istanza da proprietà precedenti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 552d05b9e8c96620ce41579eb14cc234eca675eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968367"
---
# <a name="creating-a-new-instance-from-old-properties"></a><span data-ttu-id="f645e-104">Creazione di una nuova istanza da proprietà precedenti</span><span class="sxs-lookup"><span data-stu-id="f645e-104">Creating a New Instance from Old Properties</span></span>

<span data-ttu-id="f645e-105">Una classe di visualizzazione join contiene le proprietà delle istanze della classe di origine connesse da un valore di proprietà comune, ad esempio **Class1. Prop1**  =  **Class2. prop2**.</span><span class="sxs-lookup"><span data-stu-id="f645e-105">A join view class contains properties from source class instances that are connected by a common property value, such as **Class1.Prop1** = **Class2.Prop2**.</span></span> <span data-ttu-id="f645e-106">Ogni istanza in una classe di visualizzazione join è costituita da parti di istanze di classi diverse.</span><span class="sxs-lookup"><span data-stu-id="f645e-106">Each instance in a join view class consists of parts of different class instances.</span></span>

<span data-ttu-id="f645e-107">È possibile basare una classe di visualizzazione join sulla disuguaglianza dei valori delle proprietà, ad esempio **Class1. Prop1**  <>  **Class2. prop2** , dove **Prop1** e **prop2** non sono mappati alla stessa proprietà nella classe di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="f645e-107">You can base a join view class on inequality of property values, such as **Class1.Prop1** <> **Class2.Prop2** where **Prop1** and **Prop2** are not mapped to the same property in the view class.</span></span>

<span data-ttu-id="f645e-108">Una classe di visualizzazione join è utile quando le informazioni che si stanno cercando sono contenute in classi separate ma correlate.</span><span class="sxs-lookup"><span data-stu-id="f645e-108">A join view class is helpful when the information you are looking for is contained in separate but related classes.</span></span> <span data-ttu-id="f645e-109">Se ad esempio si desiderano informazioni su una stampante e sulla configurazione della stampante, è possibile creare una classe di visualizzazione join contenente alcune delle proprietà della classe [**\_ Printer Win32**](/windows/desktop/CIMWin32Prov/win32-printer) e alcune delle proprietà della classe [**Win32 \_ PrinterConfiguration**](/windows/desktop/CIMWin32Prov/win32-printerconfiguration) .</span><span class="sxs-lookup"><span data-stu-id="f645e-109">For example, if you want information about a printer and about the printer configuration, you can create a join view class that contains some of the properties of the [**Win32\_Printer**](/windows/desktop/CIMWin32Prov/win32-printer) class and some of the properties of the [**Win32\_PrinterConfiguration**](/windows/desktop/CIMWin32Prov/win32-printerconfiguration) class.</span></span> <span data-ttu-id="f645e-110">Senza il provider di visualizzazione, è necessario recuperare e unire le proprietà delle istanze separate per ottenere le informazioni necessarie.</span><span class="sxs-lookup"><span data-stu-id="f645e-110">Without the View Provider, you must retrieve and merge the properties of the separate instances to get the information you need.</span></span>

<span data-ttu-id="f645e-111">Nella procedura riportata di seguito viene descritto come creare una classe di visualizzazione join.</span><span class="sxs-lookup"><span data-stu-id="f645e-111">The following procedure describes how to create a join view class.</span></span>

<span data-ttu-id="f645e-112">**Per creare una classe di visualizzazione join**</span><span class="sxs-lookup"><span data-stu-id="f645e-112">**To create a join view class**</span></span>

1.  <span data-ttu-id="f645e-113">Inizia una definizione di classe con il qualificatore della stringa [**JoinOn**](qualifiers-specific-to-the-view-provider.md) .</span><span class="sxs-lookup"><span data-stu-id="f645e-113">Begin a class definition with the [**JoinOn**](qualifiers-specific-to-the-view-provider.md) string qualifier.</span></span>

    <span data-ttu-id="f645e-114">I qualificatori [**JoinOn**](qualifiers-specific-to-the-view-provider.md), **Association** e **Union** si escludono a vicenda.</span><span class="sxs-lookup"><span data-stu-id="f645e-114">The [**JoinOn**](qualifiers-specific-to-the-view-provider.md), **Association**, and **Union** qualifiers are mutually exclusive.</span></span>

2.  <span data-ttu-id="f645e-115">Se necessario, filtrare le istanze desiderate nella classe join applicando il qualificatore [**PostJoinFilter**](postjoinfilter-qualifier.md) .</span><span class="sxs-lookup"><span data-stu-id="f645e-115">If necessary, filter the instances that you want in the join class by applying the [**PostJoinFilter**](postjoinfilter-qualifier.md) qualifier.</span></span>

    <span data-ttu-id="f645e-116">Il provider [**PostJoinFilter**](postjoinfilter-qualifier.md) consente di limitare le istanze di una classe di visualizzazione alle istanze che soddisfano determinate condizioni.</span><span class="sxs-lookup"><span data-stu-id="f645e-116">The [**PostJoinFilter**](postjoinfilter-qualifier.md) provider allows you to restrict the instances of a view class to instances that meet specific conditions.</span></span>

3.  <span data-ttu-id="f645e-117">Creare le query che definiscono le istanze di origine della classe di visualizzazione con il qualificatore [**ViewSources**](viewsources-qualifier.md) .</span><span class="sxs-lookup"><span data-stu-id="f645e-117">Create the queries that define source instances of the view class with the [**ViewSources**](viewsources-qualifier.md) qualifier.</span></span>
4.  <span data-ttu-id="f645e-118">Definire i nomi e i percorsi degli spazi dei nomi in cui si trovano le istanze di origine con il qualificatore [**ViewSpaces**](viewspaces-qualifier.md) .</span><span class="sxs-lookup"><span data-stu-id="f645e-118">Define the names and locations of the namespaces where the source instances are located with the [**ViewSpaces**](viewspaces-qualifier.md) qualifier.</span></span>
5.  <span data-ttu-id="f645e-119">Definire le proprietà desiderate in una classe di visualizzazione join con il qualificatore [**PropertySources**](propertysources-qualifier.md) .</span><span class="sxs-lookup"><span data-stu-id="f645e-119">Define the properties that you want in a join view class with the [**PropertySources**](propertysources-qualifier.md) qualifier.</span></span>

    <span data-ttu-id="f645e-120">Quando le proprietà vengono aggiunte alla visualizzazione join in base all'uguaglianza, è necessario eseguire il mapping delle due proprietà di origine in un qualificatore [**PropertySources**](propertysources-qualifier.md) .</span><span class="sxs-lookup"><span data-stu-id="f645e-120">When properties are added to the join view based on equality, the two source properties must be mapped in one [**PropertySources**](propertysources-qualifier.md) qualifier.</span></span>

    <span data-ttu-id="f645e-121">Nell'esempio di codice seguente vengono illustrate due proprietà mappate in un qualificatore **PropertySources** .</span><span class="sxs-lookup"><span data-stu-id="f645e-121">The following code example shows two properties that are mapped in one **PropertySources** qualifier.</span></span>

    ``` syntax
    [PropertySources{"IDProcess", "IDProcess"}] Uint32 ProcessID;
    ```

    <span data-ttu-id="f645e-122">Utilizzando il qualificatore [**HiddenDefault**](qualifiers-specific-to-the-view-provider.md) , è possibile contrassegnare le proprietà che appartengono a una classe di origine.</span><span class="sxs-lookup"><span data-stu-id="f645e-122">By using the [**HiddenDefault**](qualifiers-specific-to-the-view-provider.md) qualifier, you can tag the properties that belong to a source class.</span></span>

<span data-ttu-id="f645e-123">Nell'esempio di codice riportato di seguito viene illustrata una classe di visualizzazione join creata dalle classi del provider di Performance Monitor [**Win32 \_ PerfRawData \_ PerfProc \_ Process**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) e [**Win32 \_ PerfRawData \_ PerfProc \_ thread**](/previous-versions//aa394325(v=vs.85)) con proprietà di entrambe le classi unite dalla proprietà **ProcessID** .</span><span class="sxs-lookup"><span data-stu-id="f645e-123">The following code example shows a join view class created from the Performance Monitor provider classes [**Win32\_PerfRawData\_PerfProc\_Process**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) and [**Win32\_PerfRawData\_PerfProc\_Thread**](/previous-versions//aa394325(v=vs.85)) with properties of both classes joined by the **ProcessID** property.</span></span>

``` syntax
#pragma namespace("\\\\.\\root\\cimv2")

instance of __Win32Provider as $DataProv
{
    Name = "MS_VIEW_INSTANCE_PROVIDER";
    ClsId = "{AA70DDF4-E11C-11D1-ABB0-00C04FD9159E}";
    ImpersonationLevel = 1;
    PerUserInitialization = "True";
    
};

instance of __InstanceProviderRegistration
{
    Provider = $DataProv;
    SupportsPut = True;
    SupportsGet = True;
    SupportsDelete = True;
    SupportsEnumeration = True;
    QuerySupportLevels = {"WQL:UnarySelect"};
};

[JoinOn("Win32_PerfRawData_PerfProc_Process.IDProcess = 
    Win32_PerfRawData_PerfProc_Thread.IDProcess"), 
ViewSources{"SELECT Name, IDProcess, PriorityBase 
    FROM Win32_PerfRawData_PerfProc_Process", 
    "SELECT Name, IDProcess, ThreadState, 
    PriorityCurrent FROM Win32_PerfRawData_PerfProc_Thread"},
ViewSpaces{"\\\\.\\root\\cimv2", "\\\\.\\root\\cimv2"},
dynamic: ToInstance, provider("MS_VIEW_INSTANCE_PROVIDER")]

class JoinedProcessThread
{
    [PropertySources{"IDProcess", "IDProcess"}] 
        Uint32 ProcessID;
    [PropertySources{"Name", ""}] 
        String PName;
    [PropertySources{"", "Name"}, key]   
        String TName;
    [PropertySources{"", "ThreadState"}] 
        Uint32 State;
    [PropertySources{"PriorityBase", ""}] 
        Uint32 BasePriority;
    [PropertySources{"", "PriorityCurrent"}] 
        Uint32 CurrentPriority;    
};
```

 

 
