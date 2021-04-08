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
# <a name="creating-a-new-instance-from-old-properties"></a>Creazione di una nuova istanza da proprietà precedenti

Una classe di visualizzazione join contiene le proprietà delle istanze della classe di origine connesse da un valore di proprietà comune, ad esempio **Class1. Prop1**  =  **Class2. prop2**. Ogni istanza in una classe di visualizzazione join è costituita da parti di istanze di classi diverse.

È possibile basare una classe di visualizzazione join sulla disuguaglianza dei valori delle proprietà, ad esempio **Class1. Prop1**  <>  **Class2. prop2** , dove **Prop1** e **prop2** non sono mappati alla stessa proprietà nella classe di visualizzazione.

Una classe di visualizzazione join è utile quando le informazioni che si stanno cercando sono contenute in classi separate ma correlate. Se ad esempio si desiderano informazioni su una stampante e sulla configurazione della stampante, è possibile creare una classe di visualizzazione join contenente alcune delle proprietà della classe [**\_ Printer Win32**](/windows/desktop/CIMWin32Prov/win32-printer) e alcune delle proprietà della classe [**Win32 \_ PrinterConfiguration**](/windows/desktop/CIMWin32Prov/win32-printerconfiguration) . Senza il provider di visualizzazione, è necessario recuperare e unire le proprietà delle istanze separate per ottenere le informazioni necessarie.

Nella procedura riportata di seguito viene descritto come creare una classe di visualizzazione join.

**Per creare una classe di visualizzazione join**

1.  Inizia una definizione di classe con il qualificatore della stringa [**JoinOn**](qualifiers-specific-to-the-view-provider.md) .

    I qualificatori [**JoinOn**](qualifiers-specific-to-the-view-provider.md), **Association** e **Union** si escludono a vicenda.

2.  Se necessario, filtrare le istanze desiderate nella classe join applicando il qualificatore [**PostJoinFilter**](postjoinfilter-qualifier.md) .

    Il provider [**PostJoinFilter**](postjoinfilter-qualifier.md) consente di limitare le istanze di una classe di visualizzazione alle istanze che soddisfano determinate condizioni.

3.  Creare le query che definiscono le istanze di origine della classe di visualizzazione con il qualificatore [**ViewSources**](viewsources-qualifier.md) .
4.  Definire i nomi e i percorsi degli spazi dei nomi in cui si trovano le istanze di origine con il qualificatore [**ViewSpaces**](viewspaces-qualifier.md) .
5.  Definire le proprietà desiderate in una classe di visualizzazione join con il qualificatore [**PropertySources**](propertysources-qualifier.md) .

    Quando le proprietà vengono aggiunte alla visualizzazione join in base all'uguaglianza, è necessario eseguire il mapping delle due proprietà di origine in un qualificatore [**PropertySources**](propertysources-qualifier.md) .

    Nell'esempio di codice seguente vengono illustrate due proprietà mappate in un qualificatore **PropertySources** .

    ``` syntax
    [PropertySources{"IDProcess", "IDProcess"}] Uint32 ProcessID;
    ```

    Utilizzando il qualificatore [**HiddenDefault**](qualifiers-specific-to-the-view-provider.md) , è possibile contrassegnare le proprietà che appartengono a una classe di origine.

Nell'esempio di codice riportato di seguito viene illustrata una classe di visualizzazione join creata dalle classi del provider di Performance Monitor [**Win32 \_ PerfRawData \_ PerfProc \_ Process**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) e [**Win32 \_ PerfRawData \_ PerfProc \_ thread**](/previous-versions//aa394325(v=vs.85)) con proprietà di entrambe le classi unite dalla proprietà **ProcessID** .

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

 

 
