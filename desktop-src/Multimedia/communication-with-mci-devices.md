---
title: Comunicazione con i dispositivi MCI
description: Comunicazione con i dispositivi MCI
ms.assetid: a2532c29-553f-4ae3-8ad5-319fd9470e76
keywords:
- Dispositivi MCI, comunicazione
- MCIWndGetDeviceID (macro)
- mciSendCommand (funzione)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1b5bfb7909b94bf8e71745adeeaeda61cae20ae
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104336910"
---
# <a name="communication-with-mci-devices"></a><span data-ttu-id="e984c-106">Comunicazione con i dispositivi MCI</span><span class="sxs-lookup"><span data-stu-id="e984c-106">Communication with MCI Devices</span></span>

<span data-ttu-id="e984c-107">Ogni dispositivo MCI può usare uno o più degli identificatori seguenti:</span><span class="sxs-lookup"><span data-stu-id="e984c-107">It is possible for each MCI device to use one or more of the following as identifiers:</span></span>

-   <span data-ttu-id="e984c-108">identificatore del dispositivo</span><span class="sxs-lookup"><span data-stu-id="e984c-108">a device identifier</span></span>
-   <span data-ttu-id="e984c-109">Nome dispositivo</span><span class="sxs-lookup"><span data-stu-id="e984c-109">a device name</span></span>
-   <span data-ttu-id="e984c-110">un alias</span><span class="sxs-lookup"><span data-stu-id="e984c-110">an alias</span></span>
-   <span data-ttu-id="e984c-111">nome file del contenuto attualmente caricato.</span><span class="sxs-lookup"><span data-stu-id="e984c-111">the filename of the currently loaded content.</span></span>

<span data-ttu-id="e984c-112">MCIWnd fornisce le macro che è possibile usare per recuperare queste informazioni.</span><span class="sxs-lookup"><span data-stu-id="e984c-112">MCIWnd provides macros you can use to retrieve this information.</span></span> <span data-ttu-id="e984c-113">È quindi possibile usare queste informazioni per comunicare tramite MCI direttamente con i dispositivi MCI associati a MCIWnd Windows.</span><span class="sxs-lookup"><span data-stu-id="e984c-113">You can then use this information to communicate through MCI directly with MCI devices associated with MCIWnd windows.</span></span>

<span data-ttu-id="e984c-114">È possibile recuperare l'identificatore del dispositivo MCI corrente usando la macro [**MCIWndGetDeviceID**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetdeviceid) .</span><span class="sxs-lookup"><span data-stu-id="e984c-114">You can retrieve the identifier of the current MCI device by using the [**MCIWndGetDeviceID**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetdeviceid) macro.</span></span> <span data-ttu-id="e984c-115">L'identificatore del dispositivo MCI è un valore numerico che identifica l'istanza del dispositivo MCI usato dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="e984c-115">The MCI device identifier is a numerical value that identifies the instance of the MCI device your application is using.</span></span> <span data-ttu-id="e984c-116">L'applicazione può usare questo identificatore durante la comunicazione con un dispositivo MCI usando la funzione [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="e984c-116">Your application can use this identifier when communicating with an MCI device by using the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function.</span></span>

<span data-ttu-id="e984c-117">Per recuperare il nome del dispositivo MCI corrente, usare la macro [**MCIWndGetDevice**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetdevice) .</span><span class="sxs-lookup"><span data-stu-id="e984c-117">To retrieve the name of the current MCI device, use the [**MCIWndGetDevice**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetdevice) macro.</span></span> <span data-ttu-id="e984c-118">Il nome del dispositivo MCI è una stringa con terminazione null che identifica il tipo di dispositivo associato a una finestra MCIWnd.</span><span class="sxs-lookup"><span data-stu-id="e984c-118">The MCI device name is a null-terminated string that identifies the device type associated with an MCIWnd window.</span></span> <span data-ttu-id="e984c-119">L'applicazione può usare questo nome durante la comunicazione con un dispositivo MCI usando **mciSendCommand**.</span><span class="sxs-lookup"><span data-stu-id="e984c-119">Your application can use this name when communicating with an MCI device by using **mciSendCommand**.</span></span>

<span data-ttu-id="e984c-120">È possibile recuperare l'alias del dispositivo MCI corrente usando la macro [**MCIWndGetAlias**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetalias) .</span><span class="sxs-lookup"><span data-stu-id="e984c-120">You can retrieve the alias of the current MCI device by using the [**MCIWndGetAlias**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetalias) macro.</span></span> <span data-ttu-id="e984c-121">L'applicazione può usare questo alias durante la comunicazione con un dispositivo MCI usando la funzione [**mciSendString**](/previous-versions//dd757161(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="e984c-121">Your application can use this alias when communicating with an MCI device by using the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function.</span></span>

<span data-ttu-id="e984c-122">Infine, è possibile recuperare il nome file usato da un dispositivo MCI usando la macro [**MCIWndGetFileName**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetfilename) .</span><span class="sxs-lookup"><span data-stu-id="e984c-122">Finally, you can retrieve the filename used by an MCI device by using the [**MCIWndGetFileName**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetfilename) macro.</span></span> <span data-ttu-id="e984c-123">Il nome file identifica il contenuto attualmente associato a una finestra MCIWnd.</span><span class="sxs-lookup"><span data-stu-id="e984c-123">The filename identifies the content currently associated with an MCIWnd window.</span></span> <span data-ttu-id="e984c-124">L'applicazione può usare questo nome file durante la comunicazione con un dispositivo MCI usando **mciSendCommand** o **mciSendString**.</span><span class="sxs-lookup"><span data-stu-id="e984c-124">Your application can use this filename when communicating with a MCI device by using **mciSendCommand** or **mciSendString**.</span></span>

 

 