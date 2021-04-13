---
title: Registrazione delle dipendenze dell'applicazione (Windows Media Player SDK)
description: Registrazione delle dipendenze dell'applicazione
ms.assetid: 966683d6-e082-448d-8473-baae2311c082
keywords:
- Windows Media Player, impostazioni del registro di sistema di dipendenza dell'applicazione
- Windows Media Player, impostazioni del registro di sistema delle dipendenze
- Windows Media Player, registro di sistema
- Registro di sistema, impostazioni delle dipendenze dell'applicazione
- Registro di sistema, impostazioni di dipendenza
- Registro di sistema, impostazioni per Windows Media Player
- impostazioni del registro di sistema delle dipendenze
- impostazioni del registro di sistema delle dipendenze applicazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67aac78417f5ec8e4347b97a5c2b5f37db20183e
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104474986"
---
# <a name="registering-application-dependency-windows-media-player-sdk"></a><span data-ttu-id="bba68-111">Registrazione delle dipendenze dell'applicazione (Windows Media Player SDK)</span><span class="sxs-lookup"><span data-stu-id="bba68-111">Registering Application Dependency (Windows Media Player SDK)</span></span>

<span data-ttu-id="bba68-112">Le applicazioni che usano le API fornite da Windows Media Player SDK o Windows Media Format SDK dipendono dai componenti di runtime di tali tecnologie.</span><span class="sxs-lookup"><span data-stu-id="bba68-112">Applications that use APIs provided by the Windows Media Player SDK or Windows Media Format SDK are dependent upon the runtime components of those technologies.</span></span> <span data-ttu-id="bba68-113">È possibile registrare l'applicazione come dipendente da tali componenti come parte della configurazione dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="bba68-113">You can register your application as being dependent on those components as part of your application setup.</span></span>

<span data-ttu-id="bba68-114">Quando si registra l'applicazione, è possibile scegliere uno dei due livelli di dipendenza: blocco o dipendente.</span><span class="sxs-lookup"><span data-stu-id="bba68-114">When you register your application, you can choose one of two levels of dependency: blocking or dependent.</span></span> <span data-ttu-id="bba68-115">Quando una o più applicazioni vengono registrate con una dipendenza di blocco su uno dei componenti di runtime, il componente verrà bloccato da un rollback a una versione precedente.</span><span class="sxs-lookup"><span data-stu-id="bba68-115">When one or more application is registered with a blocking dependency on one of the runtime components, the component will be blocked from a rollback to a previous version.</span></span> <span data-ttu-id="bba68-116">Le applicazioni dipendenti non registrate come bloccanti non bloccano il rollback.</span><span class="sxs-lookup"><span data-stu-id="bba68-116">Dependent applications that are not registered as blocking do not block rollback.</span></span> <span data-ttu-id="bba68-117">Prima di eseguire il rollback, viene invece visualizzato un messaggio che informa che le applicazioni dipendono dal componente.</span><span class="sxs-lookup"><span data-stu-id="bba68-117">Instead, before the rollback is performed, the user is displayed a message stating that applications are dependent on the component.</span></span>

<span data-ttu-id="bba68-118">Per registrare l'applicazione, è necessario impostare un valore nel registro di sistema che identifichi l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="bba68-118">To register your application, you must set a value in the registry that identifies your application.</span></span> <span data-ttu-id="bba68-119">Il valore del registro di sistema da impostare dipende dal componente da cui dipende l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="bba68-119">The registry value to set depends on the component on which your application is dependent.</span></span> <span data-ttu-id="bba68-120">È anche possibile impostare due valori aggiuntivi per dipendenza per fornire informazioni aggiuntive sull'applicazione.</span><span class="sxs-lookup"><span data-stu-id="bba68-120">You can also set two additional values per dependency to provide extra information about your application.</span></span>

<span data-ttu-id="bba68-121">I valori del registro di sistema seguenti vengono utilizzati per registrare la dipendenza dal runtime di Windows Media Player SDK:</span><span class="sxs-lookup"><span data-stu-id="bba68-121">The following registry values are used to register dependence on Windows Media Player SDK runtime:</span></span>

-   <span data-ttu-id="bba68-122">HKEY \_ classi \_ radice \\ software \\ Microsoft \\ MediaPlayer \\ installazione \\ *ref \_ Type* \\ app, "*app*", "*\_ stringa app*"</span><span class="sxs-lookup"><span data-stu-id="bba68-122">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\MediaPlayer\\Setup\\ *REF\_TYPE* \\App, "*APP*", "*APP\_STRING*"</span></span>
-   <span data-ttu-id="bba68-123">HKEY \_ Classes \_ root \\ software \\ Microsoft \\ MediaPlayer \\ Setup \\ *ref \_ Type* \\ descrittor, "*app*", "*ref \_ descrittor*"</span><span class="sxs-lookup"><span data-stu-id="bba68-123">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\MediaPlayer\\Setup\\ *REF\_TYPE* \\Descriptor, "*APP*", "*REF\_DESCRIPTOR*"</span></span>
-   <span data-ttu-id="bba68-124">HKEY \_ classi \_ radice \\ software \\ Microsoft \\ MediaPlayer \\ configurazione \\ *\_ tipo di riferimento* \\ versione, "*app*",*" \_ versione WMP*"</span><span class="sxs-lookup"><span data-stu-id="bba68-124">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\MediaPlayer\\Setup\\ *REF\_TYPE* \\Version, "*APP*", "*WMP\_VERSION*"</span></span>

<span data-ttu-id="bba68-125">I valori del registro di sistema seguenti vengono usati per registrare la dipendenza dal runtime di Windows Media Format SDK:</span><span class="sxs-lookup"><span data-stu-id="bba68-125">The following registry values are used to register dependence on the Windows Media Format SDK runtime:</span></span>

-   <span data-ttu-id="bba68-126">HKEY \_ classi \_ radice \\ software \\ Microsoft \\ WindowsMedia \\ installazione \\ *ref \_ Type* \\ app, "*app*", "*\_ stringa app*"</span><span class="sxs-lookup"><span data-stu-id="bba68-126">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\WindowsMedia\\Setup\\ *REF\_TYPE* \\App, "*APP*", "*APP\_STRING*"</span></span>
-   <span data-ttu-id="bba68-127">HKEY \_ classi \_ radice \\ software \\ Microsoft \\ WindowsMedia \\ Setup \\ *ref \_ Type* \\ descriptor, "*app*", "*ref \_ descrittor*"</span><span class="sxs-lookup"><span data-stu-id="bba68-127">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\WindowsMedia\\Setup\\ *REF\_TYPE* \\Descriptor, "*APP*", "*REF\_DESCRIPTOR*"</span></span>
-   <span data-ttu-id="bba68-128">HKEY \_ Classes \_ root \\ software \\ Microsoft \\ WindowsMedia \\ Setup \\ *ref \_ Type* \\ Version, "*app*", "*WMF \_ Version*"</span><span class="sxs-lookup"><span data-stu-id="bba68-128">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\WindowsMedia\\Setup\\ *REF\_TYPE* \\Version, "*APP*", "*WMF\_VERSION*"</span></span>

<span data-ttu-id="bba68-129">Nei valori del registro di sistema elencati sopra vengono usate le variabili seguenti:</span><span class="sxs-lookup"><span data-stu-id="bba68-129">The following variables are used in the registry values listed above:</span></span>

<span data-ttu-id="bba68-130">*tipo di riferimento \_*</span><span class="sxs-lookup"><span data-stu-id="bba68-130">*REF\_TYPE*</span></span>

<span data-ttu-id="bba68-131">Sostituire con BlockingRefCounts per la dipendenza di blocco o con DependentRefCounts per la dipendenza non bloccante.</span><span class="sxs-lookup"><span data-stu-id="bba68-131">Replace with BlockingRefCounts for blocking dependency, or with DependentRefCounts for non-blocking dependency.</span></span>

<span data-ttu-id="bba68-132">*APP*</span><span class="sxs-lookup"><span data-stu-id="bba68-132">*APP*</span></span>

<span data-ttu-id="bba68-133">Nome o breve descrittore dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="bba68-133">Name or short descriptor of your application.</span></span> <span data-ttu-id="bba68-134">Questa stringa non verrà utilizzata nei messaggi visualizzati per l'utente.</span><span class="sxs-lookup"><span data-stu-id="bba68-134">This string will not be used in messages displayed for the user.</span></span> <span data-ttu-id="bba68-135">Questo valore è l'identificatore utilizzato in tutti e tre i valori del registro di sistema associati a ognuno dei componenti Runtime.</span><span class="sxs-lookup"><span data-stu-id="bba68-135">This value is the identifier used in all three registry values associated with each of the runtime components.</span></span>

<span data-ttu-id="bba68-136">*\_stringa app*</span><span class="sxs-lookup"><span data-stu-id="bba68-136">*APP\_STRING*</span></span>

<span data-ttu-id="bba68-137">Descrittore dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="bba68-137">Descriptor of your application.</span></span> <span data-ttu-id="bba68-138">Questa stringa può essere utilizzata nei messaggi visualizzati per l'utente.</span><span class="sxs-lookup"><span data-stu-id="bba68-138">This string may be used in messages displayed for the user.</span></span>

<span data-ttu-id="bba68-139">*\_descrittore Ref*</span><span class="sxs-lookup"><span data-stu-id="bba68-139">*REF\_DESCRIPTOR*</span></span>

<span data-ttu-id="bba68-140">Descrizione della modalità di utilizzo del componente da parte dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="bba68-140">Description of how your application uses the component.</span></span> <span data-ttu-id="bba68-141">Questo valore può includere un massimo di 256 caratteri.</span><span class="sxs-lookup"><span data-stu-id="bba68-141">This value can include a maximum of 256 characters.</span></span>

<span data-ttu-id="bba68-142">*versione di WMP \_*</span><span class="sxs-lookup"><span data-stu-id="bba68-142">*WMP\_VERSION*</span></span>

<span data-ttu-id="bba68-143">Versione di Windows Media Player richiesta dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="bba68-143">Version of Windows Media Player required by your application.</span></span> <span data-ttu-id="bba68-144">Se non viene specificata alcuna versione, viene utilizzato il valore predefinito 9.0.0.0.</span><span class="sxs-lookup"><span data-stu-id="bba68-144">If no version is specified, the default value is assumed to be 9.0.0.0.</span></span>

<span data-ttu-id="bba68-145">*\_versione WMF*</span><span class="sxs-lookup"><span data-stu-id="bba68-145">*WMF\_VERSION*</span></span>

<span data-ttu-id="bba68-146">Versione di Windows Media Format SDK richiesta dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="bba68-146">Version of the Windows Media Format SDK required by your application.</span></span>

<span data-ttu-id="bba68-147">I tre valori di registro di esempio seguenti illustrano come configurare i valori per l'applicazione:</span><span class="sxs-lookup"><span data-stu-id="bba68-147">The following three example registry values demonstrate how to configure the values for your application:</span></span>

-   <span data-ttu-id="bba68-148">HKEY \_ classi \_ radice \\ software \\ Microsoft \\ MediaPlayer \\ Setup \\ DependentRefCounts \\ app, "southridgevideo", "Southridge Video Player"</span><span class="sxs-lookup"><span data-stu-id="bba68-148">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\MediaPlayer\\Setup\\DependentRefCounts\\App, "SouthridgeVideo", "Southridge Video Player"</span></span>
-   <span data-ttu-id="bba68-149">HKEY \_ classi \_ radice \\ software \\ Microsoft \\ MediaPlayer \\ Setup \\ DependentRefCounts \\ descrittore, "southridgevideo", "Southridge Video Player usa Windows Media Format SDK per riprodurre file video".</span><span class="sxs-lookup"><span data-stu-id="bba68-149">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\MediaPlayer\\Setup\\DependentRefCounts\\Descriptor, "SouthridgeVideo", "Southridge Video Player uses the Windows Media Format SDK to play video files."</span></span>
-   <span data-ttu-id="bba68-150">HKEY \_ classi \_ radice \\ software \\ Microsoft \\ MediaPlayer \\ Setup \\ DependentRefCounts \\ Version, "southridgevideo", "9.0.0.2600"</span><span class="sxs-lookup"><span data-stu-id="bba68-150">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\MediaPlayer\\Setup\\DependentRefCounts\\Version, "SouthridgeVideo", "9.0.0.2600"</span></span>

## <a name="related-topics"></a><span data-ttu-id="bba68-151">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="bba68-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bba68-152">**Impostazioni del registro di sistema**</span><span class="sxs-lookup"><span data-stu-id="bba68-152">**Registry Settings**</span></span>](registry-settings.md)
</dt> </dl>

 

 




