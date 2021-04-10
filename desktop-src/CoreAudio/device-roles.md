---
description: Ruoli del dispositivo
ms.assetid: aa787004-0d3e-448b-80dd-92055f841aee
title: Ruoli del dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b7182e3af6bf76af500588546a1b7c0db9eea97
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126902"
---
# <a name="device-roles"></a><span data-ttu-id="b2e34-103">Ruoli del dispositivo</span><span class="sxs-lookup"><span data-stu-id="b2e34-103">Device Roles</span></span>

<span data-ttu-id="b2e34-104">Se un sistema contiene due o più dispositivi endpoint per il rendering audio, un dispositivo potrebbe essere più adatto per la riproduzione di un tipo di contenuto audio e un altro dispositivo potrebbe essere migliore per la riproduzione di un altro tipo di contenuto.</span><span class="sxs-lookup"><span data-stu-id="b2e34-104">If a system contains two or more audio-rendering endpoint devices, then one device might be best for playing one type of audio content, and another device might be best for playing another type of content.</span></span> <span data-ttu-id="b2e34-105">Ad esempio, se un sistema dispone di due dispositivi di rendering, l'utente potrebbe scegliere di riprodurre musica in un dispositivo e di riprodurre suoni di notifica di sistema sull'altro.</span><span class="sxs-lookup"><span data-stu-id="b2e34-105">For example, if a system has two rendering devices, the user might choose to play music on one device and to play system notification sounds on the other.</span></span>

<span data-ttu-id="b2e34-106">Analogamente, se un sistema contiene due o più dispositivi endpoint di acquisizione audio, un dispositivo potrebbe essere più adatto per l'acquisizione di un tipo di contenuto audio e un altro dispositivo potrebbe essere migliore per l'acquisizione di un altro tipo di contenuto.</span><span class="sxs-lookup"><span data-stu-id="b2e34-106">Similarly, if a system contains two or more audio-capture endpoint devices, then one device might be best for capturing one type of audio content, and another device might be best for capturing another type of content.</span></span> <span data-ttu-id="b2e34-107">Ad esempio, se un sistema dispone di due dispositivi di acquisizione, l'utente può scegliere di registrare musica in tempo reale in un dispositivo e di usare l'altro dispositivo per i comandi vocali.</span><span class="sxs-lookup"><span data-stu-id="b2e34-107">For example, if a system has two capture devices, the user might choose to record live music on one device and to use the other device for voice commands.</span></span>

<span data-ttu-id="b2e34-108">I dispositivi possono avere tre ruoli: console, comunicazioni e multimedia. nella tabella seguente vengono descritti i ruoli del dispositivo identificati dalle tre costanti, ovvero eConsole, comunicazioni elettroniche e eMultimedia, nell'enumerazione [**ERole**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-erole) .</span><span class="sxs-lookup"><span data-stu-id="b2e34-108">Devices can have three roles: Console, Communications, and Multimedia.The following table describes the device roles identified by the three constants—eConsole, eCommunications, and eMultimedia—in the [**ERole**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-erole) enumeration.</span></span>



| <span data-ttu-id="b2e34-109">Costante ERole</span><span class="sxs-lookup"><span data-stu-id="b2e34-109">ERole constant</span></span>  | <span data-ttu-id="b2e34-110">Ruolo del dispositivo</span><span class="sxs-lookup"><span data-stu-id="b2e34-110">Device role</span></span>                              | <span data-ttu-id="b2e34-111">Esempi di rendering</span><span class="sxs-lookup"><span data-stu-id="b2e34-111">Rendering examples</span></span>             | <span data-ttu-id="b2e34-112">Esempi di acquisizione</span><span class="sxs-lookup"><span data-stu-id="b2e34-112">Capture examples</span></span>                   |
|-----------------|------------------------------------------|--------------------------------|------------------------------------|
| <span data-ttu-id="b2e34-113">eConsole</span><span class="sxs-lookup"><span data-stu-id="b2e34-113">eConsole</span></span>        | <span data-ttu-id="b2e34-114">Interazione con il computer</span><span class="sxs-lookup"><span data-stu-id="b2e34-114">Interaction with the computer</span></span>            | <span data-ttu-id="b2e34-115">Giochi e notifiche di sistema</span><span class="sxs-lookup"><span data-stu-id="b2e34-115">Games and system notifications</span></span> | <span data-ttu-id="b2e34-116">Comandi vocali</span><span class="sxs-lookup"><span data-stu-id="b2e34-116">Voice commands</span></span>                     |
| <span data-ttu-id="b2e34-117">Comunicazioni elettroniche</span><span class="sxs-lookup"><span data-stu-id="b2e34-117">eCommunications</span></span> | <span data-ttu-id="b2e34-118">Comunicazioni vocali con un'altra persona</span><span class="sxs-lookup"><span data-stu-id="b2e34-118">Voice communications with another person</span></span> | <span data-ttu-id="b2e34-119">Chat e VoIP</span><span class="sxs-lookup"><span data-stu-id="b2e34-119">Chat and VoIP</span></span>                  | <span data-ttu-id="b2e34-120">Chat e VoIP</span><span class="sxs-lookup"><span data-stu-id="b2e34-120">Chat and VoIP</span></span>                      |
| <span data-ttu-id="b2e34-121">eMultimedia</span><span class="sxs-lookup"><span data-stu-id="b2e34-121">eMultimedia</span></span>     | <span data-ttu-id="b2e34-122">Riproduzione o registrazione di contenuto audio</span><span class="sxs-lookup"><span data-stu-id="b2e34-122">Playing or recording audio content</span></span>       | <span data-ttu-id="b2e34-123">Musica e film</span><span class="sxs-lookup"><span data-stu-id="b2e34-123">Music and movies</span></span>               | <span data-ttu-id="b2e34-124">Registrazione e musica in diretta</span><span class="sxs-lookup"><span data-stu-id="b2e34-124">Narration and live music recording</span></span> |



 

<span data-ttu-id="b2e34-125">A un particolare dispositivo di rendering o acquisizione potrebbe essere assegnato nessuno, uno, alcuni o tutti i ruoli nella tabella precedente.</span><span class="sxs-lookup"><span data-stu-id="b2e34-125">A particular rendering or capture device might be assigned none, one, some, or all of the roles in the preceding table.</span></span> <span data-ttu-id="b2e34-126">Ogni ruolo della tabella viene assegnato in qualsiasi momento a uno (e un solo) dispositivo di rendering e a un solo dispositivo di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="b2e34-126">At any time, each role in the table is assigned to one (and only one) rendering device and to one (and only one) capture device.</span></span> <span data-ttu-id="b2e34-127">Ovvero, l'assegnazione dei ruoli ai dispositivi di rendering è indipendente dall'assegnazione dei ruoli per l'acquisizione di dispositivi.</span><span class="sxs-lookup"><span data-stu-id="b2e34-127">That is, the assignment of roles to rendering devices is independent of the assignment of roles to capture devices.</span></span>

<span data-ttu-id="b2e34-128">Un'applicazione può scegliere di riprodurre tutti i flussi di output tramite un singolo dispositivo endpoint di rendering e di registrare tutti i flussi di input da un singolo dispositivo dell'endpoint di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="b2e34-128">An application might choose to play all of its output streams through a single rendering endpoint device, and to record all of its input streams from a single capture endpoint device.</span></span> <span data-ttu-id="b2e34-129">In alternativa, un'applicazione può scegliere di riprodurre alcuni flussi di output tramite un dispositivo di rendering e di riprodurre altri flussi di output tramite un altro dispositivo di rendering.</span><span class="sxs-lookup"><span data-stu-id="b2e34-129">Alternatively, an application might choose to play some of its output streams through one rendering device and to play other output streams through another rendering device.</span></span> <span data-ttu-id="b2e34-130">Analogamente, può scegliere di registrare alcuni dei flussi di input attraverso un dispositivo di acquisizione e di registrare altri flussi di input tramite un altro dispositivo di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="b2e34-130">Similarly, it might choose to record some of its input streams through one capture device and to record other input streams through another capture device.</span></span> <span data-ttu-id="b2e34-131">In tutti i casi, l'applicazione può assegnare ogni flusso al dispositivo il cui ruolo è più appropriato per il flusso.</span><span class="sxs-lookup"><span data-stu-id="b2e34-131">In all cases, the application can assign each stream to the device whose role is most appropriate for that stream.</span></span>

<span data-ttu-id="b2e34-132">Ad esempio, un'applicazione VoIP potrebbe assegnare il flusso di output che contiene la notifica circolare al dispositivo dell'endpoint di rendering con il ruolo eConsole.</span><span class="sxs-lookup"><span data-stu-id="b2e34-132">For example, a VoIP application might assign the output stream that contains the ring-in notification to the rendering endpoint device with the eConsole role.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b2e34-133">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b2e34-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b2e34-134">Dispositivi endpoint audio</span><span class="sxs-lookup"><span data-stu-id="b2e34-134">Audio Endpoint Devices</span></span>](audio-endpoint-devices.md)
</dt> <dt>

[<span data-ttu-id="b2e34-135">Utilizzo dei ruoli del dispositivo</span><span class="sxs-lookup"><span data-stu-id="b2e34-135">Working with Device Roles</span></span>](device-roles-in-windows-vista.md)
</dt> <dt>

[<span data-ttu-id="b2e34-136">Interoperabilità con le API audio legacy</span><span class="sxs-lookup"><span data-stu-id="b2e34-136">Interoperability with Legacy Audio APIs</span></span>](interoperability-with-legacy-audio-apis.md)
</dt> </dl>

 

 



