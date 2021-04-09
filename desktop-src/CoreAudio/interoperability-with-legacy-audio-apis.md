---
description: Interoperabilità con le API audio legacy
ms.assetid: 34939f6d-a6e4-4f7a-afa3-b1fed52b471f
title: Interoperabilità con le API audio legacy
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a6b9a80b55695ffcfd3ac54e871f00ea27744d8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966257"
---
# <a name="interoperability-with-legacy-audio-apis"></a><span data-ttu-id="72888-103">Interoperabilità con le API audio legacy</span><span class="sxs-lookup"><span data-stu-id="72888-103">Interoperability with Legacy Audio APIs</span></span>

<span data-ttu-id="72888-104">Molte applicazioni esistenti usano API audio legacy, ad esempio DirectSound, DirectShow e le funzioni multimediali di Windows.</span><span class="sxs-lookup"><span data-stu-id="72888-104">Many existing applications use legacy audio APIs such as DirectSound, DirectShow, and the Windows multimedia functions.</span></span> <span data-ttu-id="72888-105">Con le sole modifiche minime, queste applicazioni possono essere ampliate per usare i [ruoli del dispositivo](device-roles.md), i controlli del volume di [sessione](session-volume-controls.md)e altre funzionalità delle API di base per audio in Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="72888-105">With only minor modifications, these applications can be augmented to make use of [device roles](device-roles.md), [session volume controls](session-volume-controls.md), and other features of the core audio APIs in Windows Vista.</span></span>

<span data-ttu-id="72888-106">Come descritto in [componenti audio in modalità utente](user-mode-audio-components.md), le API di base dell'audio vengono usate come base per la compilazione di API audio di livello superiore.</span><span class="sxs-lookup"><span data-stu-id="72888-106">As discussed in [User-Mode Audio Components](user-mode-audio-components.md), the core audio APIs serve as the foundation on which higher-level audio APIs are built.</span></span> <span data-ttu-id="72888-107">In Windows Vista, i dispositivi audio che accedono alle applicazioni tramite API audio legacy, ad esempio DirectSound e le funzioni Windows Media **waveOutXxx** e **waveInXxx** , sono in effetti [dispositivi di endpoint audio](audio-endpoint-devices.md) implementati dalle API di base audio.</span><span class="sxs-lookup"><span data-stu-id="72888-107">In Windows Vista, the audio devices that applications access through legacy audio APIs such as DirectSound and the Windows media **waveOutXxx** and **waveInXxx** functions are, in fact, [audio endpoint devices](audio-endpoint-devices.md) that are implemented by the core audio APIs.</span></span> <span data-ttu-id="72888-108">A causa delle limitazioni intrinseche nelle interfacce delle API audio legacy, un'applicazione può accedere ad alcune delle funzionalità dei dispositivi dell'endpoint audio tramite queste interfacce, ma non tutte.</span><span class="sxs-lookup"><span data-stu-id="72888-108">Because of inherent limitations in the interfaces of legacy audio APIs, an application can access some but not all of the capabilities of audio endpoint devices through these interfaces.</span></span> <span data-ttu-id="72888-109">Le sezioni seguenti descrivono le tecniche per migliorare le applicazioni esistenti accedendo a funzionalità aggiuntive dei dispositivi dell'endpoint audio direttamente tramite le API di base di audio.</span><span class="sxs-lookup"><span data-stu-id="72888-109">The following sections describe techniques for enhancing existing applications by accessing additional capabilities of audio endpoint devices directly through the core audio APIs.</span></span> <span data-ttu-id="72888-110">Questi miglioramenti richiedono in genere solo modifiche minime al codice dell'applicazione esistente.</span><span class="sxs-lookup"><span data-stu-id="72888-110">These enhancements typically require only minor changes to the existing application code.</span></span>

<span data-ttu-id="72888-111">Le sezioni seguenti descrivono come incorporare le funzionalità delle API audio di base in applicazioni esistenti che usano le API audio legacy:</span><span class="sxs-lookup"><span data-stu-id="72888-111">The following sections describe how to incorporate features of the core audio APIs into existing applications that use legacy audio APIs:</span></span>

-   [<span data-ttu-id="72888-112">Ruoli del dispositivo per le applicazioni DirectSound</span><span class="sxs-lookup"><span data-stu-id="72888-112">Device Roles for DirectSound Applications</span></span>](device-roles-for-directsound-applications.md)
-   [<span data-ttu-id="72888-113">Ruoli del dispositivo per le applicazioni DirectShow</span><span class="sxs-lookup"><span data-stu-id="72888-113">Device Roles for DirectShow Applications</span></span>](device-roles-for-directshow-applications.md)
-   [<span data-ttu-id="72888-114">Ruoli del dispositivo per applicazioni multimediali Windows legacy</span><span class="sxs-lookup"><span data-stu-id="72888-114">Device Roles for Legacy Windows Multimedia Applications</span></span>](device-roles-for-legacy-windows-multimedia-applications.md)
-   [<span data-ttu-id="72888-115">Eventi audio per applicazioni audio legacy</span><span class="sxs-lookup"><span data-stu-id="72888-115">Audio Events for Legacy Audio Applications</span></span>](audio-events-for-legacy-audio-applications.md)
-   [<span data-ttu-id="72888-116">Suoni di notifica per le applicazioni audio legacy</span><span class="sxs-lookup"><span data-stu-id="72888-116">Notification Sounds for Legacy Audio Applications</span></span>](notification-sounds-for-legacy-audio-applications.md)

## <a name="related-topics"></a><span data-ttu-id="72888-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="72888-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="72888-118">Ruoli del dispositivo</span><span class="sxs-lookup"><span data-stu-id="72888-118">Device Roles</span></span>](device-roles.md)
</dt> </dl>

 

 



