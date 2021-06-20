---
title: Registrazione della dipendenza dell'applicazione (Windows Media Format 11 SDK)
description: Informazioni su come registrare l'applicazione con i componenti di runtime delle API fornite da Windows Media Format 11 SDK.
ms.assetid: 09f63519-5c65-4784-9ea4-4fbecfa6d4aa
keywords:
- Windows Media Format SDK, registrazione delle dipendenze dell'applicazione
- registrazione delle dipendenze dell'applicazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1cd546ee9b162652f00a131e87561a7e34f7e3a2
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406164"
---
# <a name="registering-application-dependency-windows-media-format-11-sdk"></a><span data-ttu-id="ff922-105">Registrazione della dipendenza dell'applicazione (Windows Media Format 11 SDK)</span><span class="sxs-lookup"><span data-stu-id="ff922-105">Registering Application Dependency (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="ff922-106">Le applicazioni che usano le API fornite da Windows Media Format SDK o Windows Media Player SDK dipendono dai componenti di run-time di tali tecnologie.</span><span class="sxs-lookup"><span data-stu-id="ff922-106">Applications that use APIs provided by the Windows Media Format SDK or Windows Media Player SDK are dependent upon the run-time components of those technologies.</span></span> <span data-ttu-id="ff922-107">È possibile registrare l'applicazione come dipendente da tali componenti come parte della configurazione dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="ff922-107">You can register your application as being dependent on those components as part of your application setup.</span></span>

<span data-ttu-id="ff922-108">Quando si registra l'applicazione, è possibile scegliere uno dei due livelli di dipendenza: blocco o dipendente.</span><span class="sxs-lookup"><span data-stu-id="ff922-108">When you register your application, you can choose one of two levels of dependency: blocking, or dependent.</span></span> <span data-ttu-id="ff922-109">Quando una o più applicazioni vengono registrate con una dipendenza di blocco da uno dei componenti di run-time, al componente verrà impedito il rollback a una versione precedente.</span><span class="sxs-lookup"><span data-stu-id="ff922-109">When one or more applications are registered with a blocking dependency on one of the run-time components, the component will be blocked from a rollback to a previous version.</span></span> <span data-ttu-id="ff922-110">Le applicazioni dipendenti non registrate come bloccante non bloccano il rollback.</span><span class="sxs-lookup"><span data-stu-id="ff922-110">Dependent applications that are not registered as blocking, do not block rollback.</span></span> <span data-ttu-id="ff922-111">Al contrario, prima dell'esecuzione del rollback, all'utente viene visualizzato un messaggio che informa che le applicazioni dipendono dal componente.</span><span class="sxs-lookup"><span data-stu-id="ff922-111">Instead, before the rollback is performed, the user is prompted with a message stating that applications are dependent on the component.</span></span>

<span data-ttu-id="ff922-112">Per registrare l'applicazione, è necessario impostare un valore nel Registro di sistema che identifica l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="ff922-112">To register your application, you must set a value in the registry that identifies your application.</span></span> <span data-ttu-id="ff922-113">Il valore del Registro di sistema da impostare dipende dal componente da cui dipende l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="ff922-113">The registry value to set depends on the component on which your application is dependent.</span></span> <span data-ttu-id="ff922-114">È anche possibile impostare due valori aggiuntivi per ogni dipendenza per fornire informazioni aggiuntive sull'applicazione.</span><span class="sxs-lookup"><span data-stu-id="ff922-114">You can also set two additional values per dependency to provide extra information about your application.</span></span>

<span data-ttu-id="ff922-115">I valori del Registro di sistema seguenti vengono usati per registrare la dipendenza dal runtime di Windows Media Format SDK:</span><span class="sxs-lookup"><span data-stu-id="ff922-115">The following registry values are used to register dependence on the Windows Media Format SDK runtime:</span></span>

-   <span data-ttu-id="ff922-116">HKEY \_ CLASSES ROOT Software Microsoft \_ \\ \\ \\ WindowsMedia Setup REF \\ \\ *\_ TYPE* \\ App, "*APP*", "*APP \_ STRING*"</span><span class="sxs-lookup"><span data-stu-id="ff922-116">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\WindowsMedia\\Setup\\*REF\_TYPE*\\App, "*APP*", "*APP\_STRING*"</span></span>
-   <span data-ttu-id="ff922-117">HKEY \_ CLASSES ROOT Software Microsoft \_ \\ \\ \\ WindowsMedia Setup REF \\ \\ *\_ TYPE* \\ Descriptor, "*APP*", "*REF \_ DESCRIPTOR*"</span><span class="sxs-lookup"><span data-stu-id="ff922-117">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\WindowsMedia\\Setup\\*REF\_TYPE*\\Descriptor, "*APP*", "*REF\_DESCRIPTOR*"</span></span>
-   <span data-ttu-id="ff922-118">HKEY \_ CLASSES ROOT Software Microsoft \_ \\ \\ \\ WindowsMedia Setup REF \\ \\ *\_ TYPE* \\ Version, "*APP*", "*WMF \_ VERSION*"</span><span class="sxs-lookup"><span data-stu-id="ff922-118">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\WindowsMedia\\Setup\\*REF\_TYPE*\\Version, "*APP*", "*WMF\_VERSION*"</span></span>

<span data-ttu-id="ff922-119">Il valore del Registro di sistema seguente viene usato per registrare la dipendenza Windows Media Player runtime sdk:</span><span class="sxs-lookup"><span data-stu-id="ff922-119">The following registry value are used to register dependence on Windows Media Player SDK runtime:</span></span>

-   <span data-ttu-id="ff922-120">HKEY \_ CLASSES ROOT Software Microsoft \_ \\ \\ \\ MediaPlayer \\ Setup REF \\ *\_ TYPE* \\ App, "*APP*", "*APP \_ STRING*"</span><span class="sxs-lookup"><span data-stu-id="ff922-120">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\MediaPlayer\\Setup\\*REF\_TYPE*\\App, "*APP*", "*APP\_STRING*"</span></span>
-   <span data-ttu-id="ff922-121">HKEY \_ CLASSES ROOT Software Microsoft \_ \\ \\ \\ MediaPlayer \\ Setup REF \\ *\_ TYPE* \\ Descriptor, "*APP*", "*REF \_ DESCRIPTOR*"</span><span class="sxs-lookup"><span data-stu-id="ff922-121">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\MediaPlayer\\Setup\\*REF\_TYPE*\\Descriptor, "*APP*", "*REF\_DESCRIPTOR*"</span></span>
-   <span data-ttu-id="ff922-122">HKEY \_ CLASSES ROOT Software Microsoft \_ \\ \\ \\ MediaPlayer \\ Setup REF \\ *\_ TYPE* \\ Version, "*APP*", "*WMP \_ VERSION*"</span><span class="sxs-lookup"><span data-stu-id="ff922-122">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\MediaPlayer\\Setup\\*REF\_TYPE*\\Version, "*APP*", "*WMP\_VERSION*"</span></span>

<span data-ttu-id="ff922-123">Nei valori del Registro di sistema elencati in precedenza vengono usate le variabili seguenti:</span><span class="sxs-lookup"><span data-stu-id="ff922-123">The following variables are used in the registry values listed above:</span></span>

<span data-ttu-id="ff922-124">*REF \_ TYPE*</span><span class="sxs-lookup"><span data-stu-id="ff922-124">*REF\_TYPE*</span></span>

<span data-ttu-id="ff922-125">Sostituire con BlockingRefCounts per bloccare la dipendenza o con DependentRefCounts per la dipendenza non bloccante.</span><span class="sxs-lookup"><span data-stu-id="ff922-125">Replace with BlockingRefCounts for blocking dependency, or with DependentRefCounts for non-blocking dependency.</span></span>

<span data-ttu-id="ff922-126">*APP*</span><span class="sxs-lookup"><span data-stu-id="ff922-126">*APP*</span></span>

<span data-ttu-id="ff922-127">Nome o descrittore breve dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="ff922-127">Name or short descriptor of your application.</span></span> <span data-ttu-id="ff922-128">Questa stringa non verrà usata nei messaggi visualizzati per l'utente.</span><span class="sxs-lookup"><span data-stu-id="ff922-128">This string will not be used in messages displayed for the user.</span></span> <span data-ttu-id="ff922-129">Questo valore è l'identificatore utilizzato in tutti e tre i valori del Registro di sistema associati a ognuno dei componenti di run-time.</span><span class="sxs-lookup"><span data-stu-id="ff922-129">This value is the identifier used in all three registry values associated with each of the run-time components.</span></span>

<span data-ttu-id="ff922-130">*STRINGA \_ APP*</span><span class="sxs-lookup"><span data-stu-id="ff922-130">*APP\_STRING*</span></span>

<span data-ttu-id="ff922-131">Descrittore dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="ff922-131">Descriptor of your application.</span></span> <span data-ttu-id="ff922-132">Questa stringa può essere usata nei messaggi visualizzati per l'utente.</span><span class="sxs-lookup"><span data-stu-id="ff922-132">This string may be used in messages displayed for the user.</span></span>

<span data-ttu-id="ff922-133">*REF \_ DESCRIPTOR*</span><span class="sxs-lookup"><span data-stu-id="ff922-133">*REF\_DESCRIPTOR*</span></span>

<span data-ttu-id="ff922-134">Descrizione del modo in cui l'applicazione usa il componente.</span><span class="sxs-lookup"><span data-stu-id="ff922-134">Description of how your application uses the component.</span></span> <span data-ttu-id="ff922-135">Questo valore può includere un massimo di 256 caratteri.</span><span class="sxs-lookup"><span data-stu-id="ff922-135">This value can include a maximum of 256 characters.</span></span>

<span data-ttu-id="ff922-136">*VERSIONE \_ WMP*</span><span class="sxs-lookup"><span data-stu-id="ff922-136">*WMP\_VERSION*</span></span>

<span data-ttu-id="ff922-137">La versione Windows Media Player richiesta dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="ff922-137">Version of Windows Media Player required by your application.</span></span>

<span data-ttu-id="ff922-138">*VERSIONE \_ WMF*</span><span class="sxs-lookup"><span data-stu-id="ff922-138">*WMF\_VERSION*</span></span>

<span data-ttu-id="ff922-139">Versione di Windows Media Format SDK richiesta dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="ff922-139">Version of the Windows Media Format SDK required by your application.</span></span>

<span data-ttu-id="ff922-140">I tre valori del Registro di sistema di esempio seguenti illustrano come configurare i valori per l'applicazione:</span><span class="sxs-lookup"><span data-stu-id="ff922-140">The following three example registry values demonstrate how to configure the values for your application:</span></span>

-   <span data-ttu-id="ff922-141">HKEY \_ CLASSES ROOT Software Microsoft \_ \\ \\ \\ WindowsMedia Setup \\ \\ DependentRefCounts \\ App, "SouthclipVideo", "South southmedia Video Player"</span><span class="sxs-lookup"><span data-stu-id="ff922-141">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\WindowsMedia\\Setup\\DependentRefCounts\\App, "SouthridgeVideo", "Southridge Video Player"</span></span>
-   <span data-ttu-id="ff922-142">HKEY \_ CLASSES ROOT Software Microsoft \_ \\ \\ \\ WindowsMedia Setup \\ \\ DependentRefCounts \\ Descriptor, "SouthclipVideo", "Southclip Video Player uses the Windows Media Format SDK to play video files".</span><span class="sxs-lookup"><span data-stu-id="ff922-142">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\WindowsMedia\\Setup\\DependentRefCounts\\Descriptor, "SouthridgeVideo", "Southridge Video Player uses the Windows Media Format SDK to play video files."</span></span>
-   <span data-ttu-id="ff922-143">HKEY \_ CLASSES ROOT Software Microsoft \_ \\ \\ \\ WindowsMedia Setup \\ \\ DependentRefCounts \\ Version, "South dependentVideo", "9.0.0.2600"</span><span class="sxs-lookup"><span data-stu-id="ff922-143">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\WindowsMedia\\Setup\\DependentRefCounts\\Version, "SouthridgeVideo", "9.0.0.2600"</span></span>

## <a name="related-topics"></a><span data-ttu-id="ff922-144">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ff922-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ff922-145">**Considerazioni sui progetti**</span><span class="sxs-lookup"><span data-stu-id="ff922-145">**Project Considerations**</span></span>](project-considerations.md)
</dt> </dl>

 

 




