---
description: Una classe di visualizzazione associazione consente di usare query ASSOCIATORS OF su classi che risiedono in spazi dei nomi diversi.
ms.assetid: 4af4fe1b-2b19-472e-8261-798b374ae57e
ms.tgt_platform: multiple
title: Associazione di istanze tra spazi dei nomi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d743b835d28af4fe0a8dd5d09858b2ba6ff0abacd0f35219c3dd90d39d0810d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118557019"
---
# <a name="associating-instances-between-namespaces"></a>Associazione di istanze tra spazi dei nomi

Una classe di visualizzazione associazione consente di usare query [ASSOCIATORS OF](associators-of-statement.md) su classi che risiedono in spazi dei nomi diversi.

La procedura seguente descrive come associare istanze tra spazi dei nomi.

**Per associare istanze tra spazi dei nomi**

1.  Iniziare la definizione della classe con il [**qualificatore di**](meta-qualifiers.md) stringa association.

    I **qualificatori JoinOn**, [**Association**](meta-qualifiers.md)e **Union** si escludono a vicenda.

2.  Creare le query che definiscono le istanze di origine usate nella classe di visualizzazione con il [**qualificatore ViewSources.**](viewsources-qualifier.md)
3.  Definire i nomi e il percorso degli spazi dei nomi in cui si trovano le istanze di origine con il [**qualificatore ViewSpaces.**](viewspaces-qualifier.md)
4.  Definire le proprietà desiderate nella classe di visualizzazione di associazione con il qualificatore [**PropertySources.**](propertysources-qualifier.md)

    Se necessario, è possibile contrassegnare le proprietà come appartenenti a una classe di origine usando il [**qualificatore HiddenDefault.**](qualifiers-specific-to-the-view-provider.md)

5.  Contrassegnare le proprietà rilevanti con il **qualificatore Direct.**

    Il **qualificatore Direct** impedisce al provider di visualizzazione di eseguire il mapping del riferimento all'associazione con tag a un riferimento di vista.

Gli esempi di codice seguenti illustrano come creare classi di visualizzazione di associazione.

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

 

 



