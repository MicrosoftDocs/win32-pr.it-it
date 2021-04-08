---
description: Esperienza di ducking predefinita
ms.assetid: 2ad9482f-1888-4f19-bc41-9d47a8e0ed15
title: Esperienza di ducking predefinita
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d81aa22254ab33ee7396fd4a22d83cc7f5a58041
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748530"
---
# <a name="default-ducking-experience"></a><span data-ttu-id="5fe1a-103">Esperienza di ducking predefinita</span><span class="sxs-lookup"><span data-stu-id="5fe1a-103">Default Ducking Experience</span></span>

<span data-ttu-id="5fe1a-104">Si consideri uno scenario in cui un utente riceve una telefonata mentre ascolta la musica del computer.</span><span class="sxs-lookup"><span data-stu-id="5fe1a-104">Consider a scenario where a user receives a phone call while listening to music on the computer.</span></span> <span data-ttu-id="5fe1a-105">Durante la telefonata, l'utente desidera ridurre il livello di volume della musica mentre partecipa alla telefonata e riprendere il volume originale al termine della telefonata.</span><span class="sxs-lookup"><span data-stu-id="5fe1a-105">During the phone call, the user wants to reduce the volume level of the music while attending to the phone call, and resume the original volume after the phone call has ended.</span></span> <span data-ttu-id="5fe1a-106">A seconda delle opzioni specificate dall'utente nel pannello di controllo **Sounds** , il sistema operativo fornisce automaticamente questa funzionalità tramite l' *attenuazione del flusso* o l' *abbassamento* di flusso, riducendo l'intensità di un flusso audio.</span><span class="sxs-lookup"><span data-stu-id="5fe1a-106">Depending on the options specified by the user in the **Sounds** control panel, the operating system automatically provides this functionality through *ducking* or *stream attenuation*—reduction in the intensity of an audio stream.</span></span>

<span data-ttu-id="5fe1a-107">L'esperienza di attenuazione predefinita dipende dalle preferenze dell'utente, come specificato nell'opzione **Sound** del pannello di controllo.</span><span class="sxs-lookup"><span data-stu-id="5fe1a-107">The default attenuation experience depends on the user's preference, as specified in the control panel's **Sound** option.</span></span> <span data-ttu-id="5fe1a-108">Nella scheda **comunicazioni** l'utente può scegliere un livello di attenuazione (il valore predefinito è 80%), disattivare tutti i flussi non di comunicazione o disabilitare l'esperienza di attenuazione del flusso predefinita.</span><span class="sxs-lookup"><span data-stu-id="5fe1a-108">On the **Communications** tab, the user can choose an attenuation level (default value is 80%), mute all non-communication streams, or disable the default stream attenuation experience.</span></span> <span data-ttu-id="5fe1a-109">Il sistema consente l'apertura di nuovi flussi non di comunicazione (ad eccezione dei nuovi suoni di sistema) durante la sessione di comunicazione, ma i nuovi flussi non vengono attenuati automaticamente.</span><span class="sxs-lookup"><span data-stu-id="5fe1a-109">The system allows new non-communication streams (except for new system sounds) to be opened during the communication session but the new streams are not automatically attenuated.</span></span> <span data-ttu-id="5fe1a-110">Quando tutti i flussi di comunicazione vengono chiusi, il sistema termina la sessione di comunicazione e ripristina il volume dei flussi che sono stati attenuati durante la sessione di comunicazione.</span><span class="sxs-lookup"><span data-stu-id="5fe1a-110">When all of the communication streams are closed, the system ends the communication session and restores the volume of the streams that were attenuated during the communication session.</span></span>

<span data-ttu-id="5fe1a-111">Per indicare visivamente l'attenuazione del flusso, il sistema modifica le impostazioni del mixer del volume a seconda delle preferenze dell'utente.</span><span class="sxs-lookup"><span data-stu-id="5fe1a-111">To indicate stream attenuation visually, the system changes the volume mixer settings depending on the user's preference.</span></span> <span data-ttu-id="5fe1a-112">Ad esempio, se l'utente specifica un livello di attenuazione, il mixer del volume abbassa il dispositivo di scorrimento, Visualizza il nuovo volume attenuato e visualizza il livello del volume originale.</span><span class="sxs-lookup"><span data-stu-id="5fe1a-112">For example, if the user specifies an attenuation level, the volume mixer lowers the slider, displays the new attenuated volume, and displays the original volume level.</span></span> <span data-ttu-id="5fe1a-113">Questo processo è illustrato nella figura seguente.</span><span class="sxs-lookup"><span data-stu-id="5fe1a-113">The following image illustrates this process.</span></span>

![diagramma del comportamento di attenuazione del flusso predefinito disponibile in Windows 7](images/stream-aatenuation.jpg)

<span data-ttu-id="5fe1a-115">Un'applicazione può eseguire l'override dell'attenuazione del flusso e implementare un'esperienza di ducking personalizzata se sa quando inizia e termina la sessione di comunicazione.</span><span class="sxs-lookup"><span data-stu-id="5fe1a-115">An application can override stream attenuation and implement a custom ducking experience if it knows when the communication session starts and ends.</span></span> <span data-ttu-id="5fe1a-116">Per altre informazioni, vedere [fornire un comportamento di ducking personalizzato](providing-a-custom-ducking-experience.md).</span><span class="sxs-lookup"><span data-stu-id="5fe1a-116">For more information, see [Providing a Custom Ducking Behavior](providing-a-custom-ducking-experience.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="5fe1a-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5fe1a-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5fe1a-118">Uso di un dispositivo di comunicazione</span><span class="sxs-lookup"><span data-stu-id="5fe1a-118">Using a Communication Device</span></span>](using-the-communication-device.md)
</dt> <dt>

[<span data-ttu-id="5fe1a-119">Disabilitazione dell'esperienza di ducking predefinita</span><span class="sxs-lookup"><span data-stu-id="5fe1a-119">Disabling the Default Ducking Experience</span></span>](disabling-the-ducking-experience.md)
</dt> <dt>

[<span data-ttu-id="5fe1a-120">Fornire un comportamento di ducking personalizzato</span><span class="sxs-lookup"><span data-stu-id="5fe1a-120">Providing a Custom Ducking Behavior</span></span>](providing-a-custom-ducking-experience.md)
</dt> <dt>

[<span data-ttu-id="5fe1a-121">Considerazioni sull'implementazione per le notifiche di ducking</span><span class="sxs-lookup"><span data-stu-id="5fe1a-121">Implementation Considerations for Ducking Notifications</span></span>](handling-audio-ducking-events-from-communication-devices.md)
</dt> <dt>

[<span data-ttu-id="5fe1a-122">Recupero di eventi ducking</span><span class="sxs-lookup"><span data-stu-id="5fe1a-122">Getting Ducking Events</span></span>](getting-ducking-events-from-a-communication-device.md)
</dt> </dl>

 

 



