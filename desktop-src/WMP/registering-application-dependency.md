---
title: Registrazione della dipendenza dell'applicazione (Windows Media Player SDK)
description: Informazioni su come registrare l'applicazione con i componenti di runtime delle API fornite da Windows Media Player SDK.
ms.assetid: 966683d6-e082-448d-8473-baae2311c082
keywords:
- Windows Media Player,impostazioni del Registro di sistema delle dipendenze dell'applicazione
- Windows Media Player,impostazioni del Registro di sistema delle dipendenze
- Windows Media Player,registro
- registro, impostazioni delle dipendenze dell'applicazione
- registro, impostazioni delle dipendenze
- registro, impostazioni per Windows Media Player
- impostazioni del Registro di sistema delle dipendenze
- impostazioni del Registro di sistema delle dipendenze dell'applicazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb4b1692c6a4e1a8274472bbe9d718721c1ab4f1
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407364"
---
# <a name="registering-application-dependency-windows-media-player-sdk"></a><span data-ttu-id="d2f49-111">Registrazione della dipendenza dell'applicazione (Windows Media Player SDK)</span><span class="sxs-lookup"><span data-stu-id="d2f49-111">Registering Application Dependency (Windows Media Player SDK)</span></span>

<span data-ttu-id="d2f49-112">Le applicazioni che usano API fornite da Windows Media Player SDK o Windows Media Format SDK dipendono dai componenti di runtime di tali tecnologie.</span><span class="sxs-lookup"><span data-stu-id="d2f49-112">Applications that use APIs provided by the Windows Media Player SDK or Windows Media Format SDK are dependent upon the runtime components of those technologies.</span></span> <span data-ttu-id="d2f49-113">È possibile registrare l'applicazione come dipendente da tali componenti come parte della configurazione dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="d2f49-113">You can register your application as being dependent on those components as part of your application setup.</span></span>

<span data-ttu-id="d2f49-114">Quando si registra l'applicazione, è possibile scegliere uno dei due livelli di dipendenza: blocco o dipendente.</span><span class="sxs-lookup"><span data-stu-id="d2f49-114">When you register your application, you can choose one of two levels of dependency: blocking or dependent.</span></span> <span data-ttu-id="d2f49-115">Quando una o più applicazioni vengono registrate con una dipendenza di blocco da uno dei componenti di runtime, il componente verrà bloccato da un rollback a una versione precedente.</span><span class="sxs-lookup"><span data-stu-id="d2f49-115">When one or more application is registered with a blocking dependency on one of the runtime components, the component will be blocked from a rollback to a previous version.</span></span> <span data-ttu-id="d2f49-116">Le applicazioni dipendenti non registrate come bloccante non bloccano il rollback.</span><span class="sxs-lookup"><span data-stu-id="d2f49-116">Dependent applications that are not registered as blocking do not block rollback.</span></span> <span data-ttu-id="d2f49-117">Al contrario, prima che venga eseguito il rollback, all'utente viene visualizzato un messaggio che indica che le applicazioni dipendono dal componente.</span><span class="sxs-lookup"><span data-stu-id="d2f49-117">Instead, before the rollback is performed, the user is displayed a message stating that applications are dependent on the component.</span></span>

<span data-ttu-id="d2f49-118">Per registrare l'applicazione, è necessario impostare un valore nel Registro di sistema che identifica l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="d2f49-118">To register your application, you must set a value in the registry that identifies your application.</span></span> <span data-ttu-id="d2f49-119">Il valore del Registro di sistema da impostare dipende dal componente da cui dipende l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="d2f49-119">The registry value to set depends on the component on which your application is dependent.</span></span> <span data-ttu-id="d2f49-120">È anche possibile impostare due valori aggiuntivi per ogni dipendenza per fornire informazioni aggiuntive sull'applicazione.</span><span class="sxs-lookup"><span data-stu-id="d2f49-120">You can also set two additional values per dependency to provide extra information about your application.</span></span>

<span data-ttu-id="d2f49-121">I valori del Registro di sistema seguenti vengono usati per registrare la dipendenza dal runtime Windows Media Player SDK:</span><span class="sxs-lookup"><span data-stu-id="d2f49-121">The following registry values are used to register dependence on Windows Media Player SDK runtime:</span></span>

-   <span data-ttu-id="d2f49-122">HKEY \_ CLASSES ROOT Software Microsoft \_ \\ \\ \\ MediaPlayer \\ Setup REF \\ *\_ TYPE* \\ App, "*APP*", "*APP \_ STRING*"</span><span class="sxs-lookup"><span data-stu-id="d2f49-122">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\MediaPlayer\\Setup\\ *REF\_TYPE* \\App, "*APP*", "*APP\_STRING*"</span></span>
-   <span data-ttu-id="d2f49-123">HKEY \_ CLASSES ROOT Software Microsoft \_ \\ \\ \\ MediaPlayer \\ Setup REF \\ *\_ TYPE* \\ Descriptor, "*APP*", "*REF \_ DESCRIPTOR*"</span><span class="sxs-lookup"><span data-stu-id="d2f49-123">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\MediaPlayer\\Setup\\ *REF\_TYPE* \\Descriptor, "*APP*", "*REF\_DESCRIPTOR*"</span></span>
-   <span data-ttu-id="d2f49-124">HKEY \_ CLASSES ROOT Software Microsoft \_ \\ \\ \\ MediaPlayer \\ Setup REF \\ *\_ TYPE* \\ Version, "*APP*", "*WMP \_ VERSION*"</span><span class="sxs-lookup"><span data-stu-id="d2f49-124">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\MediaPlayer\\Setup\\ *REF\_TYPE* \\Version, "*APP*", "*WMP\_VERSION*"</span></span>

<span data-ttu-id="d2f49-125">I valori del Registro di sistema seguenti vengono usati per registrare la dipendenza dal runtime di Windows Media Format SDK:</span><span class="sxs-lookup"><span data-stu-id="d2f49-125">The following registry values are used to register dependence on the Windows Media Format SDK runtime:</span></span>

-   <span data-ttu-id="d2f49-126">HKEY \_ CLASSES ROOT Software Microsoft \_ \\ \\ \\ WindowsMedia Setup REF \\ \\ *\_ TYPE* \\ App, "*APP*", "*APP \_ STRING*"</span><span class="sxs-lookup"><span data-stu-id="d2f49-126">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\WindowsMedia\\Setup\\ *REF\_TYPE* \\App, "*APP*", "*APP\_STRING*"</span></span>
-   <span data-ttu-id="d2f49-127">HKEY \_ CLASSES ROOT Software Microsoft \_ \\ \\ \\ WindowsMedia Setup REF \\ \\ *\_ TYPE* \\ Descriptor, "*APP*", "*REF \_ DESCRIPTOR*"</span><span class="sxs-lookup"><span data-stu-id="d2f49-127">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\WindowsMedia\\Setup\\ *REF\_TYPE* \\Descriptor, "*APP*", "*REF\_DESCRIPTOR*"</span></span>
-   <span data-ttu-id="d2f49-128">HKEY \_ CLASSES ROOT Software Microsoft \_ \\ \\ \\ WindowsMedia Setup REF \\ \\ *\_ TYPE* \\ Version, "*APP*", "*WMF \_ VERSION*"</span><span class="sxs-lookup"><span data-stu-id="d2f49-128">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\WindowsMedia\\Setup\\ *REF\_TYPE* \\Version, "*APP*", "*WMF\_VERSION*"</span></span>

<span data-ttu-id="d2f49-129">Nei valori del Registro di sistema elencati in precedenza vengono usate le variabili seguenti:</span><span class="sxs-lookup"><span data-stu-id="d2f49-129">The following variables are used in the registry values listed above:</span></span>

<span data-ttu-id="d2f49-130">*TIPO \_ REF*</span><span class="sxs-lookup"><span data-stu-id="d2f49-130">*REF\_TYPE*</span></span>

<span data-ttu-id="d2f49-131">Sostituire con BlockingRefCounts per bloccare la dipendenza o con DependentRefCounts per la dipendenza non bloccante.</span><span class="sxs-lookup"><span data-stu-id="d2f49-131">Replace with BlockingRefCounts for blocking dependency, or with DependentRefCounts for non-blocking dependency.</span></span>

<span data-ttu-id="d2f49-132">*APP*</span><span class="sxs-lookup"><span data-stu-id="d2f49-132">*APP*</span></span>

<span data-ttu-id="d2f49-133">Nome o breve descrittore dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="d2f49-133">Name or short descriptor of your application.</span></span> <span data-ttu-id="d2f49-134">Questa stringa non verrà usata nei messaggi visualizzati per l'utente.</span><span class="sxs-lookup"><span data-stu-id="d2f49-134">This string will not be used in messages displayed for the user.</span></span> <span data-ttu-id="d2f49-135">Questo valore è l'identificatore usato in tutti e tre i valori del Registro di sistema associati a ognuno dei componenti di runtime.</span><span class="sxs-lookup"><span data-stu-id="d2f49-135">This value is the identifier used in all three registry values associated with each of the runtime components.</span></span>

<span data-ttu-id="d2f49-136">*STRINGA \_ APP*</span><span class="sxs-lookup"><span data-stu-id="d2f49-136">*APP\_STRING*</span></span>

<span data-ttu-id="d2f49-137">Descrittore dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="d2f49-137">Descriptor of your application.</span></span> <span data-ttu-id="d2f49-138">Questa stringa può essere usata nei messaggi visualizzati per l'utente.</span><span class="sxs-lookup"><span data-stu-id="d2f49-138">This string may be used in messages displayed for the user.</span></span>

<span data-ttu-id="d2f49-139">*DESCRITTORE \_ REF*</span><span class="sxs-lookup"><span data-stu-id="d2f49-139">*REF\_DESCRIPTOR*</span></span>

<span data-ttu-id="d2f49-140">Descrizione del modo in cui l'applicazione usa il componente.</span><span class="sxs-lookup"><span data-stu-id="d2f49-140">Description of how your application uses the component.</span></span> <span data-ttu-id="d2f49-141">Questo valore può includere un massimo di 256 caratteri.</span><span class="sxs-lookup"><span data-stu-id="d2f49-141">This value can include a maximum of 256 characters.</span></span>

<span data-ttu-id="d2f49-142">*VERSIONE \_ WMP*</span><span class="sxs-lookup"><span data-stu-id="d2f49-142">*WMP\_VERSION*</span></span>

<span data-ttu-id="d2f49-143">La versione Windows Media Player richiesta dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="d2f49-143">Version of Windows Media Player required by your application.</span></span> <span data-ttu-id="d2f49-144">Se non viene specificata alcuna versione, si presuppone che il valore predefinito sia 9.0.0.0.</span><span class="sxs-lookup"><span data-stu-id="d2f49-144">If no version is specified, the default value is assumed to be 9.0.0.0.</span></span>

<span data-ttu-id="d2f49-145">*VERSIONE DI \_ WMF*</span><span class="sxs-lookup"><span data-stu-id="d2f49-145">*WMF\_VERSION*</span></span>

<span data-ttu-id="d2f49-146">Versione di Windows Media Format SDK richiesta dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="d2f49-146">Version of the Windows Media Format SDK required by your application.</span></span>

<span data-ttu-id="d2f49-147">I tre valori del Registro di sistema di esempio seguenti illustrano come configurare i valori per l'applicazione:</span><span class="sxs-lookup"><span data-stu-id="d2f49-147">The following three example registry values demonstrate how to configure the values for your application:</span></span>

-   <span data-ttu-id="d2f49-148">HKEY \_ CLASSES \_ ROOT \\ Software \\ Microsoft \\ MediaPlayer \\ Setup \\ DependentRefCounts \\ App, "SouthridgeVideo", "Southridge Video Player"</span><span class="sxs-lookup"><span data-stu-id="d2f49-148">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\MediaPlayer\\Setup\\DependentRefCounts\\App, "SouthridgeVideo", "Southridge Video Player"</span></span>
-   <span data-ttu-id="d2f49-149">HKEY \_ CLASSES ROOT Software Microsoft \_ \\ \\ \\ MediaPlayer \\ Setup \\ DependentRefCounts \\ Descriptor, "SouthridgeVideo", "Southridge Video Player uses the Windows Media Format SDK to play video files".</span><span class="sxs-lookup"><span data-stu-id="d2f49-149">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\MediaPlayer\\Setup\\DependentRefCounts\\Descriptor, "SouthridgeVideo", "Southridge Video Player uses the Windows Media Format SDK to play video files."</span></span>
-   <span data-ttu-id="d2f49-150">HKEY \_ CLASSES ROOT Software Microsoft \_ \\ \\ \\ MediaPlayer \\ Setup \\ DependentRefCounts \\ Version, "SouthridgeVideo", "9.0.0.2600"</span><span class="sxs-lookup"><span data-stu-id="d2f49-150">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\MediaPlayer\\Setup\\DependentRefCounts\\Version, "SouthridgeVideo", "9.0.0.2600"</span></span>

## <a name="related-topics"></a><span data-ttu-id="d2f49-151">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d2f49-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d2f49-152">**Impostazioni del Registro di sistema**</span><span class="sxs-lookup"><span data-stu-id="d2f49-152">**Registry Settings**</span></span>](registry-settings.md)
</dt> </dl>

 

 




