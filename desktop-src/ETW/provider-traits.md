---
description: I tratti del provider sono un metodo per il fissaggio di più dati a una registrazione del singolo provider.
ms.assetid: 97755D64-BF57-4C0D-8ED4-040FC375C4AF
title: Tratti del provider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c67b25857070edb6419be9a2898d2667f3a179d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980394"
---
# <a name="provider-traits"></a><span data-ttu-id="7808a-103">Tratti del provider</span><span class="sxs-lookup"><span data-stu-id="7808a-103">Provider Traits</span></span>

<span data-ttu-id="7808a-104">I tratti del provider sono un metodo per il fissaggio di più dati a una registrazione del singolo provider.</span><span class="sxs-lookup"><span data-stu-id="7808a-104">Provider Traits are a method of attaching more data to an individual provider registration.</span></span> <span data-ttu-id="7808a-105">Possono essere usati per provider TraceLogging o basati su manifesto.</span><span class="sxs-lookup"><span data-stu-id="7808a-105">They can be used for manifest-based or TraceLogging providers.</span></span> <span data-ttu-id="7808a-106">Questo include attualmente il supporto per l'aggiunta di un nome di provider e/o di un gruppo di provider a una registrazione del singolo provider.</span><span class="sxs-lookup"><span data-stu-id="7808a-106">This currently includes support for adding a Provider Name and/or Provider Group to an individual provider registration.</span></span> <span data-ttu-id="7808a-107">È probabile che più tipi di tratto vengano aggiunti in futuro.</span><span class="sxs-lookup"><span data-stu-id="7808a-107">More trait types are likely to be added in the future.</span></span> <span data-ttu-id="7808a-108">Queste informazioni vengono archiviate nel kernel come BLOB binario di un formato set.</span><span class="sxs-lookup"><span data-stu-id="7808a-108">This information is stored in the kernel as a binary blob of a set format.</span></span>

<span data-ttu-id="7808a-109">I tratti possono essere impostati una sola volta per una registrazione.</span><span class="sxs-lookup"><span data-stu-id="7808a-109">Traits can only be set once for a registration.</span></span> <span data-ttu-id="7808a-110">Eventuali ulteriori tentativi di impostare i tratti della registrazione avranno esito negativo.</span><span class="sxs-lookup"><span data-stu-id="7808a-110">Any further attempts to set the traits on that registration will fail.</span></span>

<span data-ttu-id="7808a-111">Per impostare i tratti del provider in un provider basato su manifesto, chiamare la funzione [**EventSetInformation**](/windows/desktop/api/Evntprov/nf-evntprov-eventsetinformation) con la classe di informazioni EventProviderSetTraits.</span><span class="sxs-lookup"><span data-stu-id="7808a-111">To set Provider Traits on a manifest-based provider, call the [**EventSetInformation**](/windows/desktop/api/Evntprov/nf-evntprov-eventsetinformation) function with the EventProviderSetTraits information class.</span></span> <span data-ttu-id="7808a-112">Il buffer EventInformation deve contenere un BLOB binario nel formato seguente:</span><span class="sxs-lookup"><span data-stu-id="7808a-112">The EventInformation buffer should contain a binary blob of the following format:</span></span>

``` syntax
{
   UINT16 TraitsSize   // Total size of the traits including this field
   CHAR[] ProviderName // Null terminated utf-8 provider name
   TRAIT[] Traits      // Zero or more individual traits
}
```

<span data-ttu-id="7808a-113">I singoli tratti devono avere il formato seguente:</span><span class="sxs-lookup"><span data-stu-id="7808a-113">Individual traits should be in the following format:</span></span>

``` syntax
TRAIT {
      UINT16 TraitSize // Size of this individual trait including this field
      UINT8 Type       // ETW_PROVIDER_TRAIT_TYPE
      BYTE[] Data
      }
```

<span data-ttu-id="7808a-114">Dal tratto singolo, il \_ tipo di tratto del provider ETW \_ \_ è definito come segue:</span><span class="sxs-lookup"><span data-stu-id="7808a-114">From the individual trait, ETW\_PROVIDER\_TRAIT\_TYPE is defined as:</span></span>

``` syntax
typedef enum {
    EtwProviderTraitTypeGroup = 1,
    EtwProviderTraitTypeMax
} ETW_PROVIDER_TRAIT_TYPE;
```

<span data-ttu-id="7808a-115">I provider TraceLogging impostano automaticamente i tratti del provider quando viene chiamata la funzione [**TraceLoggingRegister**](/windows/win32/api/traceloggingprovider/nf-traceloggingprovider-traceloggingregister) .</span><span class="sxs-lookup"><span data-stu-id="7808a-115">TraceLogging providers automatically set the Provider Traits when the [**TraceLoggingRegister**](/windows/win32/api/traceloggingprovider/nf-traceloggingprovider-traceloggingregister) function is called.</span></span> <span data-ttu-id="7808a-116">Il nome del provider TraceLogging sarà sempre incluso nei relativi tratti.</span><span class="sxs-lookup"><span data-stu-id="7808a-116">The TraceLogging provider's name will always be included in its traits.</span></span> <span data-ttu-id="7808a-117">Un gruppo può essere impostato su un provider TraceLogging usando la macro [**TraceLoggingOptionGroup**](/windows/win32/api/traceloggingprovider/nf-traceloggingprovider-traceloggingoptiongroup) nella definizione del provider.</span><span class="sxs-lookup"><span data-stu-id="7808a-117">A group can be set on a TraceLogging provider using the [**TraceLoggingOptionGroup**](/windows/win32/api/traceloggingprovider/nf-traceloggingprovider-traceloggingoptiongroup) macro in the provider definition.</span></span>

## <a name="custom-traits"></a><span data-ttu-id="7808a-118">Tratti personalizzati</span><span class="sxs-lookup"><span data-stu-id="7808a-118">Custom Traits</span></span>

<span data-ttu-id="7808a-119">Sebbene la maggior parte dei 255 tipi di tratti possibili non siano ancora definiti, i tipi di tratto 1-127 sono riservati per la definizione da parte di Microsoft.</span><span class="sxs-lookup"><span data-stu-id="7808a-119">Although most of the 255 possible trait types are not yet defined, trait types 1-127 are reserved for definition by Microsoft.</span></span> <span data-ttu-id="7808a-120">I valori di tipo indicizzato più elevati rimanenti possono essere utilizzati dagli sviluppatori esterni nel modo in cui si adattano.</span><span class="sxs-lookup"><span data-stu-id="7808a-120">The remaining higher indexed type values can be used by external developers as they see fit.</span></span> <span data-ttu-id="7808a-121">Chiunque stia valutando di aggiungere i propri tratti personalizzati al provider deve provare a mantenerne le dimensioni totali in 256 byte per i motivi seguenti:</span><span class="sxs-lookup"><span data-stu-id="7808a-121">Anyone considering adding their own custom traits to their provider should try to keep their total trait size under 256 bytes for the following reasons:</span></span>

-   <span data-ttu-id="7808a-122">I tratti sono inclusi in ogni evento scritto per il provider.</span><span class="sxs-lookup"><span data-stu-id="7808a-122">The traits are included in every event written for the provider.</span></span> <span data-ttu-id="7808a-123">I tratti di grandi dimensioni potrebbero causare file di log di dimensioni molto elevate.</span><span class="sxs-lookup"><span data-stu-id="7808a-123">Large traits could lead to very large log files.</span></span>
-   <span data-ttu-id="7808a-124">I tratti vengono archiviati nel pool di kernel non di paging per la durata del provider.</span><span class="sxs-lookup"><span data-stu-id="7808a-124">The traits are stored in nonpaged kernel pool for the lifetime of the provider.</span></span>

## <a name="provider-groups"></a><span data-ttu-id="7808a-125">Gruppi di provider</span><span class="sxs-lookup"><span data-stu-id="7808a-125">Provider Groups</span></span>

<span data-ttu-id="7808a-126">Un gruppo di provider è un'entità controllabile definita dal GUID, molto simile a un provider stesso.</span><span class="sxs-lookup"><span data-stu-id="7808a-126">A provider group is a GUID-defined controllable entity much like a provider itself.</span></span> <span data-ttu-id="7808a-127">La differenza principale consiste nel fatto che, mentre un GUID del provider viene utilizzato per controllare le registrazioni del solo provider, un gruppo controllerà tutte le registrazioni dei membri.</span><span class="sxs-lookup"><span data-stu-id="7808a-127">The key difference is that while a provider GUID is used to control registrations of just its provider, a group will control all of its member registrations.</span></span> <span data-ttu-id="7808a-128">Se ad esempio si Abilita un gruppo di provider con una parola chiave e un livello specificati, tutte le registrazioni dei membri dei gruppi vengono abilitate con la parola chiave e il livello specificati.</span><span class="sxs-lookup"><span data-stu-id="7808a-128">For example, enabling a provider group with a given keyword and level will enable all of the groups member registrations with that keyword and level.</span></span>

<span data-ttu-id="7808a-129">L'appartenenza al gruppo può essere limitata da autorizzazioni.</span><span class="sxs-lookup"><span data-stu-id="7808a-129">Group membership may be restricted by permissions.</span></span> <span data-ttu-id="7808a-130">Se il chiamante di [**EventSetInformation**](/windows/desktop/api/Evntprov/nf-evntprov-eventsetinformation) non dispone delle autorizzazioni per l'aggiunta al gruppo specificato, l'appartenenza verrà negata.</span><span class="sxs-lookup"><span data-stu-id="7808a-130">If the caller of [**EventSetInformation**](/windows/desktop/api/Evntprov/nf-evntprov-eventsetinformation) doesn't have permissions to join the specified group, then membership will be denied.</span></span>

<span data-ttu-id="7808a-131">In alcuni casi è possibile che il controller della sessione di traccia desideri escludere alcuni provider dalla relativa abilitazione di un gruppo.</span><span class="sxs-lookup"><span data-stu-id="7808a-131">In some cases the trace session controller may want to exclude a few providers from its enable of a group.</span></span> <span data-ttu-id="7808a-132">Questa operazione può essere eseguita impostando un elenco non consentiti.</span><span class="sxs-lookup"><span data-stu-id="7808a-132">This can be done by setting a disallow list.</span></span> <span data-ttu-id="7808a-133">Un elenco non consentito è un elenco di GUID del provider che non verranno abilitati in base alle impostazioni di gruppo per una singola sessione di registrazione.</span><span class="sxs-lookup"><span data-stu-id="7808a-133">A disallow list is a list of provider GUIDs that will not be enabled based on the group settings for a single logging session.</span></span> <span data-ttu-id="7808a-134">Gli elenchi non consentiti possono essere modificati dinamicamente con [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation) e la classe di informazioni TraceSetDisallowList.</span><span class="sxs-lookup"><span data-stu-id="7808a-134">Disallow lists can be changed dynamically with [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation) and the TraceSetDisallowList information class.</span></span>

<span data-ttu-id="7808a-135">Sebbene la maggior parte delle azioni di abilitazione possa essere eseguita per i gruppi di provider in modo analogo ai singoli provider, esistono alcune eccezioni.</span><span class="sxs-lookup"><span data-stu-id="7808a-135">While most enable actions can be done for Provider Groups in a similar manner to individual providers, there are some exceptions.</span></span> <span data-ttu-id="7808a-136">Le eccezioni sono le seguenti:</span><span class="sxs-lookup"><span data-stu-id="7808a-136">Exceptions include:</span></span>

-   <span data-ttu-id="7808a-137">I gruppi di provider non possono essere controllati da sessioni di traccia private.</span><span class="sxs-lookup"><span data-stu-id="7808a-137">Provider Groups cannot be controlled by private trace sessions.</span></span>
-   <span data-ttu-id="7808a-138">I filtri nome evento, ID evento e payload non sono applicabili ai gruppi di provider perché presuppongono informazioni specifiche di un singolo provider.</span><span class="sxs-lookup"><span data-stu-id="7808a-138">Event Name, Event ID, and Payload filters are not applicable to Provider Groups as they assume specific information of an individual provider.</span></span>

 

 
