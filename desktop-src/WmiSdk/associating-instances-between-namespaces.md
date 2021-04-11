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
# <a name="associating-instances-between-namespaces"></a><span data-ttu-id="ca0d2-103">Associazione di istanze tra gli spazi dei nomi</span><span class="sxs-lookup"><span data-stu-id="ca0d2-103">Associating Instances Between Namespaces</span></span>

<span data-ttu-id="ca0d2-104">Una classe di visualizzazione di associazione consente di utilizzare gli [associatori di](associators-of-statement.md) query sulle classi che risiedono in spazi dei nomi diversi.</span><span class="sxs-lookup"><span data-stu-id="ca0d2-104">An association view class allows you to use [ASSOCIATORS OF](associators-of-statement.md) queries on classes that reside in different namespaces.</span></span>

<span data-ttu-id="ca0d2-105">Nella procedura seguente viene descritto come associare le istanze tra gli spazi dei nomi.</span><span class="sxs-lookup"><span data-stu-id="ca0d2-105">The following procedure describes how to associate instances between namespaces.</span></span>

<span data-ttu-id="ca0d2-106">**Per associare istanze tra gli spazi dei nomi**</span><span class="sxs-lookup"><span data-stu-id="ca0d2-106">**To associate instances between namespaces**</span></span>

1.  <span data-ttu-id="ca0d2-107">Iniziare la definizione della classe con il qualificatore della stringa di [**associazione**](meta-qualifiers.md) .</span><span class="sxs-lookup"><span data-stu-id="ca0d2-107">Begin your class definition with the [**Association**](meta-qualifiers.md) string qualifier.</span></span>

    <span data-ttu-id="ca0d2-108">I qualificatori **JoinOn**, [**Association**](meta-qualifiers.md)e **Union** si escludono a vicenda.</span><span class="sxs-lookup"><span data-stu-id="ca0d2-108">The **JoinOn**, [**Association**](meta-qualifiers.md), and **Union** qualifiers are mutually exclusive.</span></span>

2.  <span data-ttu-id="ca0d2-109">Creare le query che definiscono le istanze di origine utilizzate nella classe di visualizzazione con il qualificatore [**ViewSources**](viewsources-qualifier.md) .</span><span class="sxs-lookup"><span data-stu-id="ca0d2-109">Create the queries that define source instances used in the view class with the [**ViewSources**](viewsources-qualifier.md) qualifier.</span></span>
3.  <span data-ttu-id="ca0d2-110">Definire i nomi e il percorso degli spazi dei nomi in cui si trovano le istanze di origine con il qualificatore [**ViewSpaces**](viewspaces-qualifier.md) .</span><span class="sxs-lookup"><span data-stu-id="ca0d2-110">Define the names and location of the namespaces in which the source instances are located with the [**ViewSpaces**](viewspaces-qualifier.md) qualifier.</span></span>
4.  <span data-ttu-id="ca0d2-111">Definire le proprietà desiderate nella classe di visualizzazione dell'associazione con il qualificatore [**PropertySources**](propertysources-qualifier.md) .</span><span class="sxs-lookup"><span data-stu-id="ca0d2-111">Define the properties you want in your association view class with the [**PropertySources**](propertysources-qualifier.md) qualifier.</span></span>

    <span data-ttu-id="ca0d2-112">Se necessario, è possibile contrassegnare qualsiasi proprietà come appartenente a una classe di origine utilizzando il qualificatore [**HiddenDefault**](qualifiers-specific-to-the-view-provider.md) .</span><span class="sxs-lookup"><span data-stu-id="ca0d2-112">If necessary, you can tag any of the properties as belonging to a source class by using the [**HiddenDefault**](qualifiers-specific-to-the-view-provider.md) qualifier.</span></span>

5.  <span data-ttu-id="ca0d2-113">Contrassegnare tutte le proprietà rilevanti con il qualificatore **diretto** .</span><span class="sxs-lookup"><span data-stu-id="ca0d2-113">Tag any relevant properties with the **Direct** qualifier.</span></span>

    <span data-ttu-id="ca0d2-114">Il qualificatore **diretto** impedisce al provider di visualizzazione di eseguire il mapping del riferimento di associazione con tag a un riferimento alla visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="ca0d2-114">The **Direct** qualifier prevents the View Provider from mapping the tagged association reference to a view reference.</span></span>

<span data-ttu-id="ca0d2-115">Negli esempi di codice seguenti viene illustrato come creare classi di visualizzazione delle associazioni.</span><span class="sxs-lookup"><span data-stu-id="ca0d2-115">The following code examples show how to create association view classes.</span></span>

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

 

 



