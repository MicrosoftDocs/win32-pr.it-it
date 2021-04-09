---
title: Progettazione dell'animazione
description: Progettazione dell'animazione
ms.assetid: 8812e4cc-9062-4c65-81ef-229bd29534cd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7d6cf86cfe115ec209fb305f0ae017951bd7f41
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955351"
---
# <a name="animation-design"></a><span data-ttu-id="e05e8-103">Progettazione dell'animazione</span><span class="sxs-lookup"><span data-stu-id="e05e8-103">Animation Design</span></span>

<span data-ttu-id="e05e8-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="e05e8-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

### <a name="image-design"></a><span data-ttu-id="e05e8-105">Progettazione immagine</span><span class="sxs-lookup"><span data-stu-id="e05e8-105">Image Design</span></span>

<span data-ttu-id="e05e8-106">Usare la tavolozza Microsoft Office durante la progettazione dei caratteri per ridurre al minimo i potenziali problemi di realizzazione della tavolozza.</span><span class="sxs-lookup"><span data-stu-id="e05e8-106">Use the Microsoft Office Palette when designing your characters to minimize any potential palette realization issues.</span></span> <span data-ttu-id="e05e8-107">Evitare di selezionare un colore di trasparenza simile ai colori usati nel documento.</span><span class="sxs-lookup"><span data-stu-id="e05e8-107">Avoid selecting a transparency color that is similar to the colors that you use in your document.</span></span>

### <a name="sounds"></a><span data-ttu-id="e05e8-108">Suoni</span><span class="sxs-lookup"><span data-stu-id="e05e8-108">Sounds</span></span>

<span data-ttu-id="e05e8-109">Microsoft Agent consente di riprodurre suoni nelle animazioni.</span><span class="sxs-lookup"><span data-stu-id="e05e8-109">Microsoft Agent enables you to play sounds in your animations.</span></span> <span data-ttu-id="e05e8-110">Si consiglia di non includere suoni per le animazioni **inattive** .</span><span class="sxs-lookup"><span data-stu-id="e05e8-110">We recommend you do not include sounds for your **Idle** animations.</span></span> <span data-ttu-id="e05e8-111">In questo modo, se l'agente deve caricare la DLL multimediale di sistema, non si verifica alcun ritardo al centro dell'animazione.</span><span class="sxs-lookup"><span data-stu-id="e05e8-111">This is so there won't be a delay in the middle of the animation, if Agent has to load the system multimedia DLL.</span></span>

### <a name="frame-size"></a><span data-ttu-id="e05e8-112">Dimensioni frame</span><span class="sxs-lookup"><span data-stu-id="e05e8-112">Frame Size</span></span>

<span data-ttu-id="e05e8-113">Gli assistenti di Office tipici sono 123 x 93 pixel.</span><span class="sxs-lookup"><span data-stu-id="e05e8-113">Typical Office Assistants are 123 x 93 pixels.</span></span> <span data-ttu-id="e05e8-114">Sebbene sia possibile creare caratteri di altre dimensioni, questi verranno ridimensionati a 123 x 93 nella raccolta di assistenti.</span><span class="sxs-lookup"><span data-stu-id="e05e8-114">While you can create characters of other sizes, they will be scaled to 123 x 93 in the Assistant Gallery.</span></span>

### <a name="frame-transition"></a><span data-ttu-id="e05e8-115">Transizione del frame</span><span class="sxs-lookup"><span data-stu-id="e05e8-115">Frame Transition</span></span>

<span data-ttu-id="e05e8-116">Tutte le animazioni eccetto **Goodbye**, **Greeting**, **show** e **Hide** devono iniziare e terminare con l'animazione RestPose.</span><span class="sxs-lookup"><span data-stu-id="e05e8-116">All animations except for **Goodbye**, **Greeting**, **Show** and **Hide** should begin and end with the RestPose animation.</span></span> <span data-ttu-id="e05e8-117">Microsoft Office non riproduce animazioni di **restituzione** esplicite, pertanto non è necessario definirle.</span><span class="sxs-lookup"><span data-stu-id="e05e8-117">Microsoft Office does not play explicit **Return** animations, so you should not define them.</span></span> <span data-ttu-id="e05e8-118">Tutte le animazioni devono anche avere una diramazione di uscita.</span><span class="sxs-lookup"><span data-stu-id="e05e8-118">All animations should also have Exit Branching.</span></span> <span data-ttu-id="e05e8-119">Exit Branching consente di affrettare e completare l'animazione corrente prima di chiamare l'animazione successiva.</span><span class="sxs-lookup"><span data-stu-id="e05e8-119">Exit branching enables us to 'hurry up and finish' the current animation before we call the next animation.</span></span> <span data-ttu-id="e05e8-120">Se non si fornisce la diramazione di uscita, la transizione tra le animazioni potrebbe essere Jerky.</span><span class="sxs-lookup"><span data-stu-id="e05e8-120">If you don't supply Exit Branching, the transition between animations may be jerky.</span></span>

### <a name="character-properties"></a><span data-ttu-id="e05e8-121">Proprietà carattere</span><span class="sxs-lookup"><span data-stu-id="e05e8-121">Character Properties</span></span>

<span data-ttu-id="e05e8-122">Microsoft Agent consente di impostare il [**nome**](name-property.md), la [**Descrizione**](description-property.md) e le proprietà [**dei dati**](extradata-property.md) di tipo carattere.</span><span class="sxs-lookup"><span data-stu-id="e05e8-122">Microsoft Agent enables you to set the character's [**Name**](name-property.md), [**Description**](description-property.md) and [**ExtraData**](extradata-property.md) properties.</span></span> <span data-ttu-id="e05e8-123">Microsoft Office utilizza il campo **dei dati** di prima per conservare una o più frasi introduttive e frasi di promemoria.</span><span class="sxs-lookup"><span data-stu-id="e05e8-123">Microsoft Office uses the **ExtraData** field to hold to one or more Introduction Phrases and Reminder Phrases.</span></span> <span data-ttu-id="e05e8-124">Microsoft Office preleva dalle altre frasi introduttive da inserire nell'aerostato vocale della raccolta di assistenti.</span><span class="sxs-lookup"><span data-stu-id="e05e8-124">Microsoft Office picks from the other Introduction Phrases to put in the speech balloon in the Assistant Gallery.</span></span> <span data-ttu-id="e05e8-125">Le frasi promemoria vengono usate quando si riceve un promemoria da Outlook.</span><span class="sxs-lookup"><span data-stu-id="e05e8-125">We use the Reminder Phrases when you receive a reminder from Outlook.</span></span>

<span data-ttu-id="e05e8-126">Il campo [**dati**](extradata-property.md) non è formattato come segue:</span><span class="sxs-lookup"><span data-stu-id="e05e8-126">The [**ExtraData**](extradata-property.md) field is formatted as follows:</span></span>

<span data-ttu-id="e05e8-127">IntroPhrase1~~IntroPhrase2~~IntroPhrase3 ^ ^ ReminderPhrase1~~ReminderPhrase2~~ReminderPhrase3</span><span class="sxs-lookup"><span data-stu-id="e05e8-127">IntroPhrase1~~IntroPhrase2~~IntroPhrase3^^ReminderPhrase1~~ReminderPhrase2~~ReminderPhrase3</span></span>

<span data-ttu-id="e05e8-128">Le frasi introduttive sono separate da una coppia di caratteri tilde (~), seguite da frasi di promemoria.</span><span class="sxs-lookup"><span data-stu-id="e05e8-128">Intro Phrases are separated by a pair of tilde characters (~), followed by Reminder Phrases.</span></span> <span data-ttu-id="e05e8-129">Queste frasi di promemoria sono separate anche da una coppia di caratteri tilde.</span><span class="sxs-lookup"><span data-stu-id="e05e8-129">These Reminder Phrases are also separated by a pair of tilde characters.</span></span> <span data-ttu-id="e05e8-130">I due set di frasi sono separati da due caratteri di accento (^^).</span><span class="sxs-lookup"><span data-stu-id="e05e8-130">The two sets of phrases are separated by two caret characters (^^).</span></span> <span data-ttu-id="e05e8-131">Non esiste alcun limite al numero di ogni tipo di frase, ad eccezione del fatto che deve essere presente almeno uno di essi.</span><span class="sxs-lookup"><span data-stu-id="e05e8-131">There is no limit to the number of each kind of phrase, except that there must be at least one of each.</span></span>

 

 




