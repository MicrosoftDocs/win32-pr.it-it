---
title: Registrazione delle dipendenze dell'applicazione (Windows Media Format 11 SDK)
description: Registrazione delle dipendenze dell'applicazione
ms.assetid: 09f63519-5c65-4784-9ea4-4fbecfa6d4aa
keywords:
- Windows Media Format SDK, registrazione delle dipendenze dell'applicazione
- registrazione delle dipendenze dell'applicazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 090cf61d32597800b52e2bc112d2bee1cc1b7cd7
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104047670"
---
# <a name="registering-application-dependency-windows-media-format-11-sdk"></a><span data-ttu-id="069a0-105">Registrazione delle dipendenze dell'applicazione (Windows Media Format 11 SDK)</span><span class="sxs-lookup"><span data-stu-id="069a0-105">Registering Application Dependency (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="069a0-106">Le applicazioni che usano le API fornite da Windows Media Format SDK o Windows Media Player SDK dipendono dai componenti di runtime di tali tecnologie.</span><span class="sxs-lookup"><span data-stu-id="069a0-106">Applications that use APIs provided by the Windows Media Format SDK or Windows Media Player SDK are dependent upon the run-time components of those technologies.</span></span> <span data-ttu-id="069a0-107">È possibile registrare l'applicazione come dipendente da tali componenti come parte della configurazione dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="069a0-107">You can register your application as being dependent on those components as part of your application setup.</span></span>

<span data-ttu-id="069a0-108">Quando si registra l'applicazione, è possibile scegliere uno dei due livelli di dipendenza: blocco o dipendente.</span><span class="sxs-lookup"><span data-stu-id="069a0-108">When you register your application, you can choose one of two levels of dependency: blocking, or dependent.</span></span> <span data-ttu-id="069a0-109">Quando una o più applicazioni vengono registrate con una dipendenza di blocco da uno dei componenti di runtime, il componente verrà bloccato da un rollback a una versione precedente.</span><span class="sxs-lookup"><span data-stu-id="069a0-109">When one or more applications are registered with a blocking dependency on one of the run-time components, the component will be blocked from a rollback to a previous version.</span></span> <span data-ttu-id="069a0-110">Le applicazioni dipendenti che non sono registrate come bloccanti non bloccano il rollback.</span><span class="sxs-lookup"><span data-stu-id="069a0-110">Dependent applications that are not registered as blocking, do not block rollback.</span></span> <span data-ttu-id="069a0-111">Al contrario, prima che venga eseguito il rollback, all'utente viene richiesto di specificare un messaggio che informa che le applicazioni dipendono dal componente.</span><span class="sxs-lookup"><span data-stu-id="069a0-111">Instead, before the rollback is performed, the user is prompted with a message stating that applications are dependent on the component.</span></span>

<span data-ttu-id="069a0-112">Per registrare l'applicazione, è necessario impostare un valore nel registro di sistema che identifichi l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="069a0-112">To register your application, you must set a value in the registry that identifies your application.</span></span> <span data-ttu-id="069a0-113">Il valore del registro di sistema da impostare dipende dal componente da cui dipende l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="069a0-113">The registry value to set depends on the component on which your application is dependent.</span></span> <span data-ttu-id="069a0-114">È anche possibile impostare due valori aggiuntivi per dipendenza per fornire informazioni aggiuntive sull'applicazione.</span><span class="sxs-lookup"><span data-stu-id="069a0-114">You can also set two additional values per dependency to provide extra information about your application.</span></span>

<span data-ttu-id="069a0-115">I valori del registro di sistema seguenti vengono usati per registrare la dipendenza dal runtime di Windows Media Format SDK:</span><span class="sxs-lookup"><span data-stu-id="069a0-115">The following registry values are used to register dependence on the Windows Media Format SDK runtime:</span></span>

-   <span data-ttu-id="069a0-116">HKEY \_ classi \_ radice \\ software \\ Microsoft \\ WindowsMedia \\ installazione \\ *ref \_ Type* \\ app, "*app*", "*\_ stringa app*"</span><span class="sxs-lookup"><span data-stu-id="069a0-116">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\WindowsMedia\\Setup\\*REF\_TYPE*\\App, "*APP*", "*APP\_STRING*"</span></span>
-   <span data-ttu-id="069a0-117">HKEY \_ classi \_ radice \\ software \\ Microsoft \\ WindowsMedia \\ Setup \\ *ref \_ Type* \\ descriptor, "*app*", "*ref \_ descrittor*"</span><span class="sxs-lookup"><span data-stu-id="069a0-117">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\WindowsMedia\\Setup\\*REF\_TYPE*\\Descriptor, "*APP*", "*REF\_DESCRIPTOR*"</span></span>
-   <span data-ttu-id="069a0-118">HKEY \_ Classes \_ root \\ software \\ Microsoft \\ WindowsMedia \\ Setup \\ *ref \_ Type* \\ Version, "*app*", "*WMF \_ Version*"</span><span class="sxs-lookup"><span data-stu-id="069a0-118">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\WindowsMedia\\Setup\\*REF\_TYPE*\\Version, "*APP*", "*WMF\_VERSION*"</span></span>

<span data-ttu-id="069a0-119">Il valore del registro di sistema seguente viene usato per registrare la dipendenza dal runtime di Windows Media Player SDK:</span><span class="sxs-lookup"><span data-stu-id="069a0-119">The following registry value are used to register dependence on Windows Media Player SDK runtime:</span></span>

-   <span data-ttu-id="069a0-120">HKEY \_ classi \_ radice \\ software \\ Microsoft \\ MediaPlayer \\ installazione \\ *ref \_ Type* \\ app, "*app*", "*\_ stringa app*"</span><span class="sxs-lookup"><span data-stu-id="069a0-120">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\MediaPlayer\\Setup\\*REF\_TYPE*\\App, "*APP*", "*APP\_STRING*"</span></span>
-   <span data-ttu-id="069a0-121">HKEY \_ Classes \_ root \\ software \\ Microsoft \\ MediaPlayer \\ Setup \\ *ref \_ Type* \\ descrittor, "*app*", "*ref \_ descrittor*"</span><span class="sxs-lookup"><span data-stu-id="069a0-121">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\MediaPlayer\\Setup\\*REF\_TYPE*\\Descriptor, "*APP*", "*REF\_DESCRIPTOR*"</span></span>
-   <span data-ttu-id="069a0-122">HKEY \_ classi \_ radice \\ software \\ Microsoft \\ MediaPlayer \\ configurazione \\ *\_ tipo di riferimento* \\ versione, "*app*",*" \_ versione WMP*"</span><span class="sxs-lookup"><span data-stu-id="069a0-122">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\MediaPlayer\\Setup\\*REF\_TYPE*\\Version, "*APP*", "*WMP\_VERSION*"</span></span>

<span data-ttu-id="069a0-123">Nei valori del registro di sistema elencati sopra vengono usate le variabili seguenti:</span><span class="sxs-lookup"><span data-stu-id="069a0-123">The following variables are used in the registry values listed above:</span></span>

<span data-ttu-id="069a0-124">*tipo di riferimento \_*</span><span class="sxs-lookup"><span data-stu-id="069a0-124">*REF\_TYPE*</span></span>

<span data-ttu-id="069a0-125">Sostituire con BlockingRefCounts per la dipendenza di blocco o con DependentRefCounts per la dipendenza non bloccante.</span><span class="sxs-lookup"><span data-stu-id="069a0-125">Replace with BlockingRefCounts for blocking dependency, or with DependentRefCounts for non-blocking dependency.</span></span>

<span data-ttu-id="069a0-126">*APP*</span><span class="sxs-lookup"><span data-stu-id="069a0-126">*APP*</span></span>

<span data-ttu-id="069a0-127">Nome o breve descrittore dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="069a0-127">Name or short descriptor of your application.</span></span> <span data-ttu-id="069a0-128">Questa stringa non verrà utilizzata nei messaggi visualizzati per l'utente.</span><span class="sxs-lookup"><span data-stu-id="069a0-128">This string will not be used in messages displayed for the user.</span></span> <span data-ttu-id="069a0-129">Questo valore è l'identificatore utilizzato in tutti e tre i valori del registro di sistema associati a ognuno dei componenti di run-time.</span><span class="sxs-lookup"><span data-stu-id="069a0-129">This value is the identifier used in all three registry values associated with each of the run-time components.</span></span>

<span data-ttu-id="069a0-130">*\_stringa app*</span><span class="sxs-lookup"><span data-stu-id="069a0-130">*APP\_STRING*</span></span>

<span data-ttu-id="069a0-131">Descrittore dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="069a0-131">Descriptor of your application.</span></span> <span data-ttu-id="069a0-132">Questa stringa può essere utilizzata nei messaggi visualizzati per l'utente.</span><span class="sxs-lookup"><span data-stu-id="069a0-132">This string may be used in messages displayed for the user.</span></span>

<span data-ttu-id="069a0-133">*\_descrittore Ref*</span><span class="sxs-lookup"><span data-stu-id="069a0-133">*REF\_DESCRIPTOR*</span></span>

<span data-ttu-id="069a0-134">Descrizione della modalità di utilizzo del componente da parte dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="069a0-134">Description of how your application uses the component.</span></span> <span data-ttu-id="069a0-135">Questo valore può includere un massimo di 256 caratteri.</span><span class="sxs-lookup"><span data-stu-id="069a0-135">This value can include a maximum of 256 characters.</span></span>

<span data-ttu-id="069a0-136">*versione di WMP \_*</span><span class="sxs-lookup"><span data-stu-id="069a0-136">*WMP\_VERSION*</span></span>

<span data-ttu-id="069a0-137">Versione di Windows Media Player richiesta dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="069a0-137">Version of Windows Media Player required by your application.</span></span>

<span data-ttu-id="069a0-138">*\_versione WMF*</span><span class="sxs-lookup"><span data-stu-id="069a0-138">*WMF\_VERSION*</span></span>

<span data-ttu-id="069a0-139">Versione di Windows Media Format SDK richiesta dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="069a0-139">Version of the Windows Media Format SDK required by your application.</span></span>

<span data-ttu-id="069a0-140">I tre valori di registro di esempio seguenti illustrano come configurare i valori per l'applicazione:</span><span class="sxs-lookup"><span data-stu-id="069a0-140">The following three example registry values demonstrate how to configure the values for your application:</span></span>

-   <span data-ttu-id="069a0-141">HKEY \_ classi \_ radice \\ software \\ Microsoft \\ WindowsMedia \\ Setup \\ DependentRefCounts \\ app, "southridgevideo", "Southridge Video Player"</span><span class="sxs-lookup"><span data-stu-id="069a0-141">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\WindowsMedia\\Setup\\DependentRefCounts\\App, "SouthridgeVideo", "Southridge Video Player"</span></span>
-   <span data-ttu-id="069a0-142">HKEY \_ classi \_ radice \\ software \\ Microsoft \\ WindowsMedia \\ Setup \\ DependentRefCounts \\ descrittore, "southridgevideo", "Southridge Video Player usa Windows Media Format SDK per riprodurre file video".</span><span class="sxs-lookup"><span data-stu-id="069a0-142">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\WindowsMedia\\Setup\\DependentRefCounts\\Descriptor, "SouthridgeVideo", "Southridge Video Player uses the Windows Media Format SDK to play video files."</span></span>
-   <span data-ttu-id="069a0-143">HKEY \_ classi \_ radice \\ software \\ Microsoft \\ WindowsMedia \\ Setup \\ DependentRefCounts \\ Version, "southridgevideo", "9.0.0.2600"</span><span class="sxs-lookup"><span data-stu-id="069a0-143">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\WindowsMedia\\Setup\\DependentRefCounts\\Version, "SouthridgeVideo", "9.0.0.2600"</span></span>

## <a name="related-topics"></a><span data-ttu-id="069a0-144">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="069a0-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="069a0-145">**Considerazioni sui progetti**</span><span class="sxs-lookup"><span data-stu-id="069a0-145">**Project Considerations**</span></span>](project-considerations.md)
</dt> </dl>

 

 




