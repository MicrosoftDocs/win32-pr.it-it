---
description: Una classe di visualizzazione di associazione consente di utilizzare gli ASSOCIATOri di query sulle classi che risiedono in spazi dei nomi diversi.
ms.assetid: 4af4fe1b-2b19-472e-8261-798b374ae57e
ms.tgt_platform: multiple
title: Associazione di istanze tra gli spazi dei nomi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8347d3a35f06f72d3344f5c12606d82709a1370
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346226"
---
# <a name="associating-instances-between-namespaces"></a>Associazione di istanze tra gli spazi dei nomi

Una classe di visualizzazione di associazione consente di utilizzare gli [associatori di](associators-of-statement.md) query sulle classi che risiedono in spazi dei nomi diversi.

Nella procedura seguente viene descritto come associare le istanze tra gli spazi dei nomi.

**Per associare istanze tra gli spazi dei nomi**

1.  Iniziare la definizione della classe con il qualificatore della stringa di [**associazione**](meta-qualifiers.md) .

    I qualificatori **JoinOn**, [**Association**](meta-qualifiers.md)e **Union** si escludono a vicenda.

2.  Creare le query che definiscono le istanze di origine utilizzate nella classe di visualizzazione con il qualificatore [**ViewSources**](viewsources-qualifier.md) .
3.  Definire i nomi e il percorso degli spazi dei nomi in cui si trovano le istanze di origine con il qualificatore [**ViewSpaces**](viewspaces-qualifier.md) .
4.  Definire le proprietà desiderate nella classe di visualizzazione dell'associazione con il qualificatore [**PropertySources**](propertysources-qualifier.md) .

    Se necessario, è possibile contrassegnare qualsiasi proprietà come appartenente a una classe di origine utilizzando il qualificatore [**HiddenDefault**](qualifiers-specific-to-the-view-provider.md) .

5.  Contrassegnare tutte le proprietà rilevanti con il qualificatore **diretto** .

    Il qualificatore **diretto** impedisce al provider di visualizzazione di eseguire il mapping del riferimento di associazione con tag a un riferimento alla visualizzazione.

Negli esempi di codice seguenti viene illustrato come creare classi di visualizzazione delle associazioni.

``` syntax
[union,
ViewSources {"SELECT * FROM Win32_OperatingSystem"},
    ViewSpaces {"\\\\.\\root\\cimv2"},
    dynamic, provider("MS_VIEW_INSTANCE_PROVIDER")
]
class Union_OS_For_AssociationExample
{
    [key, PropertySources{"Name"}]
    string Name;

    [PropertySources{"Version"}]
    string Version;

    [PropertySources{"BuildNumber"}]
    string BuildNumber;
};

[
Association,
ViewSources {"SELECT * FROM Win32_SystemOperatingSystem"}, 
ViewSpaces {"\\\\.\\root\\cimv2"},
dynamic, provider("MS_VIEW_INSTANCE_PROVIDER")
]
class Association_SystemViewOperatingSystem
{
    [Direct, key, PropertySources{"GroupComponent"}]
    Win32_ComputerSystem ref Computer;
    
    [key, PropertySources{"PartComponent"}]
    Union_OS_For_AssociationExample ref OperatingSystem;
};
```

 

 



