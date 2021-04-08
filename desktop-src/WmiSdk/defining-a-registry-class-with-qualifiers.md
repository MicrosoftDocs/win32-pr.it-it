---
description: Le classi utilizzate per conservare i dati del registro di sistema sono definite con diversi qualificatori standard.
ms.assetid: d4786880-6c50-4e36-9a16-47de430e77a9
ms.tgt_platform: multiple
title: Definizione di una classe Registry con qualificatori
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f45fdff611814eadbf57eabedf7444d098666918
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880670"
---
# <a name="defining-a-registry-class-with-qualifiers"></a><span data-ttu-id="993fa-103">Definizione di una classe Registry con qualificatori</span><span class="sxs-lookup"><span data-stu-id="993fa-103">Defining a Registry Class With Qualifiers</span></span>

<span data-ttu-id="993fa-104">Le classi utilizzate per conservare i dati del registro di sistema sono definite con diversi qualificatori standard.</span><span class="sxs-lookup"><span data-stu-id="993fa-104">The classes used to hold registry data are defined with several standard qualifiers.</span></span>

<span data-ttu-id="993fa-105">Di seguito è riportato un elenco dei qualificatori standard:</span><span class="sxs-lookup"><span data-stu-id="993fa-105">The following is a list of the standard qualifiers:</span></span>

-   <span data-ttu-id="993fa-106">[Dynamic](standard-wmi-qualifiers.md) e [ **provider**](/windows/desktop/api/Provider/nl-provider-provider)</span><span class="sxs-lookup"><span data-stu-id="993fa-106">[Dynamic](standard-wmi-qualifiers.md) and [**Provider**](/windows/desktop/api/Provider/nl-provider-provider)</span></span>

    <span data-ttu-id="993fa-107">Il qualificatore **dinamico** può essere collegato a una classe o a un'istanza.</span><span class="sxs-lookup"><span data-stu-id="993fa-107">You can attach the **Dynamic** qualifier to either a class or an instance.</span></span> <span data-ttu-id="993fa-108">Il qualificatore **dinamico** contrassegna la classe o l'istanza come gestita in modo dinamico da un provider.</span><span class="sxs-lookup"><span data-stu-id="993fa-108">The **Dynamic** qualifier marks the class or instance as managed dynamically by a provider.</span></span> <span data-ttu-id="993fa-109">Quando viene visualizzato **Dynamic** in una classe o in un'istanza, è necessario che venga visualizzato anche il qualificatore del [**provider**](/windows/desktop/api/Provider/nl-provider-provider) .</span><span class="sxs-lookup"><span data-stu-id="993fa-109">When **Dynamic** appears on a class or instance, the [**Provider**](/windows/desktop/api/Provider/nl-provider-provider) qualifier must also appear.</span></span> <span data-ttu-id="993fa-110">Il qualificatore del **provider** identifica il provider specifico che deve gestire la classe o l'istanza dinamica.</span><span class="sxs-lookup"><span data-stu-id="993fa-110">The **Provider** qualifier identifies the particular provider that must manage the dynamic class or instance.</span></span>

-   [<span data-ttu-id="993fa-111">ClassContext</span><span class="sxs-lookup"><span data-stu-id="993fa-111">ClassContext</span></span>](standard-wmi-qualifiers.md)

    <span data-ttu-id="993fa-112">Il qualificatore **ClassContext** è associato a una classe.</span><span class="sxs-lookup"><span data-stu-id="993fa-112">The **ClassContext** qualifier is attached to a class.</span></span> <span data-ttu-id="993fa-113">Specifica il percorso della chiave del registro di sistema che contiene le informazioni rappresentate dalla classe.</span><span class="sxs-lookup"><span data-stu-id="993fa-113">It specifies the path to the registry key that contains the information the class represents.</span></span>

    <span data-ttu-id="993fa-114">Il qualificatore **ClassContext** ha il formato seguente.</span><span class="sxs-lookup"><span data-stu-id="993fa-114">The **ClassContext** qualifier has the following format.</span></span>

    ``` syntax
    MACHINE_NAME|Subtree\\KeyPath
    ```

    <span data-ttu-id="993fa-115">Il valore per il percorso della chiave può essere Long se include chiavi con sottochiavi.</span><span class="sxs-lookup"><span data-stu-id="993fa-115">The value for KeyPath can be long if it includes keys with subkeys.</span></span>

    <span data-ttu-id="993fa-116">Nell'esempio seguente viene illustrato il qualificatore **ClassContext** che contiene il percorso di un dispositivo di trasporto del computer specifico.</span><span class="sxs-lookup"><span data-stu-id="993fa-116">The following example shows the **ClassContext** qualifier that contains the path to a particular computer transport device.</span></span>

    ``` syntax
    Machine_Name|HKEY_LOCAL_MACHINE\\SOFTWARE\\MICROSOFT\\WBEM\\TRANSPORTS
    ```

<span data-ttu-id="993fa-117">Il modello seguente per una definizione di classe illustra l'uso dei qualificatori **dinamici**, [**provider**](/windows/desktop/api/Provider/nl-provider-provider)e **ClassContext** .</span><span class="sxs-lookup"><span data-stu-id="993fa-117">The following template for a class definition illustrates the use of the **Dynamic**, [**Provider**](/windows/desktop/api/Provider/nl-provider-provider), and **ClassContext** qualifiers.</span></span> <span data-ttu-id="993fa-118">Il provider denominato dal qualificatore del **provider** è il provider del registro di sistema dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="993fa-118">The provider named by the **Provider** qualifier is the instance System Registry provider.</span></span> <span data-ttu-id="993fa-119">Tenere presente che i percorsi del registro di sistema non fanno distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="993fa-119">Be aware that registry paths are case-insensitive, as are qualifier names.</span></span>

``` syntax
[dynamic, provider("RegProv"), 
    ClassContext("local|hkey_local_machine\\software\\microsoft
    \\WBEM\\transports\\Network Transport Modules")]

class RegTrans
{
  [key] string  TransportsGUID;
  [PropertyContext("Name")] string Name;
  [PropertyContext("Independent")] uint32 Enabled;
};
```

<span data-ttu-id="993fa-120">Le applicazioni di gestione possono inoltre utilizzare il provider del registro di sistema per recuperare e modificare i dati del registro di sistema per una chiave specifica.</span><span class="sxs-lookup"><span data-stu-id="993fa-120">Management applications can also use the System Registry provider to retrieve and modify registry data for a particular key.</span></span>

 

 



