---
description: WMI implementa una tecnica che consente l'archiviazione nel repository di più versioni localizzate della stessa classe.
ms.assetid: 01e1cee5-d882-45b6-ac93-68533c2c6c9d
ms.tgt_platform: multiple
title: Localizzazione delle informazioni sulla classe WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa9f1a7e34c3ba230655ebba4c070981a8dab901
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348396"
---
# <a name="localizing-wmi-class-information"></a><span data-ttu-id="f293b-103">Localizzazione delle informazioni sulla classe WMI</span><span class="sxs-lookup"><span data-stu-id="f293b-103">Localizing WMI Class Information</span></span>

<span data-ttu-id="f293b-104">WMI implementa una tecnica che consente l'archiviazione nel repository di più versioni localizzate della stessa classe.</span><span class="sxs-lookup"><span data-stu-id="f293b-104">WMI implements a technique that allows multiple localized versions of the same class to be stored in the repository.</span></span>

<span data-ttu-id="f293b-105">La definizione della classe è suddivisa nelle versioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="f293b-105">The class definition is separated into the following versions:</span></span>

-   <span data-ttu-id="f293b-106">Versione indipendente dalla lingua che contiene solo una definizione di classe di base.</span><span class="sxs-lookup"><span data-stu-id="f293b-106">A language-neutral version that contains only a basic class definition.</span></span>
-   <span data-ttu-id="f293b-107">Versione specifica del linguaggio che contiene informazioni localizzate, ad esempio descrizioni delle proprietà specifiche delle impostazioni locali.</span><span class="sxs-lookup"><span data-stu-id="f293b-107">A language-specific version that contains localized information, such as property descriptions that are specific to a locale.</span></span>

<span data-ttu-id="f293b-108">Le definizioni delle classi specifiche del linguaggio vengono archiviate in uno spazio dei nomi figlio sotto lo spazio dei nomi che contiene una definizione di classe Basic indipendente dal linguaggio.</span><span class="sxs-lookup"><span data-stu-id="f293b-108">The language-specific class definitions are stored in a child namespace beneath the namespace that contains a language-neutral basic class definition.</span></span>

<span data-ttu-id="f293b-109">Quando si richiede una definizione di classe localizzata per le impostazioni locali specifiche, WMI combina la definizione della classe di base e le informazioni sulla classe localizzata per formare una classe localizzata completa.</span><span class="sxs-lookup"><span data-stu-id="f293b-109">When you request a localized class definition for a specific locale, WMI combines the basic class definition and the localized class information to form a complete localized class.</span></span> <span data-ttu-id="f293b-110">Per ottenere una versione localizzata di una classe WMI, è possibile specificare le impostazioni locali quando ci si connette a WMI e si imposta un flag che indica che si desiderano le informazioni localizzate.</span><span class="sxs-lookup"><span data-stu-id="f293b-110">You can get a localized version of a WMI class by specifying a locale when you connect to WMI and setting a flag that indicates that you want localized information.</span></span> <span data-ttu-id="f293b-111">WMI quindi unisce le informazioni dalle versioni indipendenti dalla lingua e dalle versioni specifiche del linguaggio della definizione della classe per formare una classe localizzata.</span><span class="sxs-lookup"><span data-stu-id="f293b-111">WMI then merges the information from the language-neutral and the language-specific versions of the class definition to form a localized class.</span></span>

<span data-ttu-id="f293b-112">Le classi WMI che contengono informazioni localizzate sono contrassegnate con il qualificatore della **modifica** e sono denominate classi modificate. una classe supporta le informazioni localizzate se dispone di questo qualificatore.</span><span class="sxs-lookup"><span data-stu-id="f293b-112">WMI classes that contain localized information are marked with the **Amendment** qualifier and are called amended classes; a class supports localized information if it has this qualifier.</span></span> <span data-ttu-id="f293b-113">È possibile determinare per quali impostazioni locali è stata localizzata la classe verificando la presenza di un altro qualificatore denominato [**impostazioni locali**](swbemobjectpath-locale.md).</span><span class="sxs-lookup"><span data-stu-id="f293b-113">You can determine which locale the class has been localized for by checking for another qualifier called [**Locale**](swbemobjectpath-locale.md).</span></span> <span data-ttu-id="f293b-114">Il qualificatore delle impostazioni locali contiene un identificatore di localizzazione (LCID di Windows) che identifica le impostazioni locali.</span><span class="sxs-lookup"><span data-stu-id="f293b-114">The locale qualifier contains a localization identifier (Windows LCID) that identifies a locale.</span></span> <span data-ttu-id="f293b-115">Ad esempio, le impostazioni locali per l'inglese americano sono 0x409.</span><span class="sxs-lookup"><span data-stu-id="f293b-115">For example, the locale for American English is 0x409.</span></span> <span data-ttu-id="f293b-116">Se un qualificatore di una classe modificata contiene informazioni localizzate, contiene la versione del qualificatore **modificata** .</span><span class="sxs-lookup"><span data-stu-id="f293b-116">If a qualifier in an amended class contains localized information, it contains the **amended** qualifier flavor.</span></span>

<span data-ttu-id="f293b-117">La localizzazione WMI include le attività seguenti:</span><span class="sxs-lookup"><span data-stu-id="f293b-117">WMI localization includes the following tasks:</span></span>

-   [<span data-ttu-id="f293b-118">Creazione di definizioni di classi localizzate</span><span class="sxs-lookup"><span data-stu-id="f293b-118">Creating localized class definitions</span></span>](creating-localized-class-definitions.md)
-   [<span data-ttu-id="f293b-119">Compilazione di file MOF localizzati</span><span class="sxs-lookup"><span data-stu-id="f293b-119">Compiling localized MOF files</span></span>](compiling-localized-mof-files.md)
-   [<span data-ttu-id="f293b-120">Localizzazione dei valori delle proprietà</span><span class="sxs-lookup"><span data-stu-id="f293b-120">Localizing property values</span></span>](localizing-property-values.md)
-   [<span data-ttu-id="f293b-121">Recupero di classi modificate</span><span class="sxs-lookup"><span data-stu-id="f293b-121">Retrieving amended classes</span></span>](retrieving-amended-classes.md)

<span data-ttu-id="f293b-122">Per altre informazioni, vedere [considerazioni sulle classi modificate](amended-class-considerations.md).</span><span class="sxs-lookup"><span data-stu-id="f293b-122">For more information, see [Amended Class Considerations](amended-class-considerations.md).</span></span>

 

 



