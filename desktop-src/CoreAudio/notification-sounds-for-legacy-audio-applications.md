---
description: Suoni di notifica per le applicazioni audio legacy
ms.assetid: c5ad67d9-56fb-4bf0-aea4-5b49b0e5bf95
title: Suoni di notifica per le applicazioni audio legacy
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e9ee2ef1155694e32a21779c55d290da6b3799c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523802"
---
# <a name="notification-sounds-for-legacy-audio-applications"></a><span data-ttu-id="653ff-103">Suoni di notifica per le applicazioni audio legacy</span><span class="sxs-lookup"><span data-stu-id="653ff-103">Notification Sounds for Legacy Audio Applications</span></span>

<span data-ttu-id="653ff-104">In Windows Vista, il sistema operativo assegna tutti i suoni di notifica del sistema a una sessione audio tra processi che riproduce il dispositivo dell'endpoint di rendering che è attualmente assegnato al ruolo del [dispositivo](device-roles.md)eConsole.</span><span class="sxs-lookup"><span data-stu-id="653ff-104">In Windows Vista, the operating system assigns all of its system notification sounds to a cross-process audio session that plays through the rendering endpoint device that is currently assigned to the eConsole [device role](device-roles.md).</span></span> <span data-ttu-id="653ff-105">Il programma di controllo del volume di sistema, sndvol, Visualizza un dispositivo di scorrimento del volume dedicato ai suoni delle notifiche di sistema.</span><span class="sxs-lookup"><span data-stu-id="653ff-105">The system volume-control program, Sndvol, displays a volume slider that is dedicated to system notification sounds.</span></span>

<span data-ttu-id="653ff-106">Alcune applicazioni riprodotno i suoni di notifica.</span><span class="sxs-lookup"><span data-stu-id="653ff-106">Some applications play notification sounds.</span></span> <span data-ttu-id="653ff-107">Anziché richiedere all'utente di gestire le notifiche di un'applicazione tramite un dispositivo di scorrimento del volume separato in sndvol, l'applicazione può assegnare i suoni di notifica alla stessa sessione del suono delle notifiche di sistema.</span><span class="sxs-lookup"><span data-stu-id="653ff-107">Instead of requiring the user to manage an application's notification sounds through a separate volume slider in Sndvol, the application can assign its notification sounds to the same session as the system notification sounds.</span></span> <span data-ttu-id="653ff-108">Il dispositivo di scorrimento del volume sndvol che controlla i suoni della notifica di sistema controlla quindi i suoni di notifica dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="653ff-108">The Sndvol volume slider that controls the system notification sounds then controls the notification sounds from the application.</span></span>

<span data-ttu-id="653ff-109">Per abilitare questo comportamento, Windows Vista definisce un \_ flag di sistema SND per la funzione [**PlaySound**](/previous-versions//dd743680(v=vs.85)) legacy.</span><span class="sxs-lookup"><span data-stu-id="653ff-109">To enable this behavior, Windows Vista defines a SND\_SYSTEM flag for the legacy [**PlaySound**](/previous-versions//dd743680(v=vs.85)) function.</span></span> <span data-ttu-id="653ff-110">Questo flag non è supportato nelle versioni precedenti di Windows, tra cui Windows Server 2003, Windows XP e Windows 2000. Se il chiamante imposta questo flag, la funzione **PlaySound** assegna il suono che riproduce alla sessione tra processi utilizzata dal sistema operativo per i suoni di notifica.</span><span class="sxs-lookup"><span data-stu-id="653ff-110">(This flag is not supported in earlier versions of Windows, including Windows Server 2003, Windows XP, and Windows 2000.) If the caller sets this flag, then the **PlaySound** function assigns the sound that it plays to the cross-process session that the operating system uses for its notification sounds.</span></span> <span data-ttu-id="653ff-111">Se il chiamante non imposta il flag, **PlaySound** assegna il suono che riproduce alla sessione predefinita, ovvero la sessione specifica del processo identificata dal GUID del valore GUID della sessione \_ null.</span><span class="sxs-lookup"><span data-stu-id="653ff-111">If the caller does not set the flag, then **PlaySound** assigns the sound that it plays to the default session—the process-specific session that is identified by the session GUID value GUID\_NULL.</span></span> <span data-ttu-id="653ff-112">\_Il sistema SND è definito nel file di intestazione MMSYSTEM. h.</span><span class="sxs-lookup"><span data-stu-id="653ff-112">SND\_SYSTEM is defined in the header file Mmsystem.h.</span></span> <span data-ttu-id="653ff-113">Per ulteriori informazioni su **PlaySound**, vedere la documentazione Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="653ff-113">For more information about **PlaySound**, see the Windows SDK documentation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="653ff-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="653ff-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="653ff-115">Interoperabilità con le API audio legacy</span><span class="sxs-lookup"><span data-stu-id="653ff-115">Interoperability with Legacy Audio APIs</span></span>](interoperability-with-legacy-audio-apis.md)
</dt> </dl>

 

 
