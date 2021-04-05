---
title: Connessione di una finestra di acquisizione a un driver di acquisizione
description: Connessione di una finestra di acquisizione a un driver di acquisizione
ms.assetid: 78d4aaf5-6216-4eec-84d4-6727d1822983
keywords:
- Messaggio WM_CAP_DRIVER_CONNECT
- capDriverConnect (macro)
- capGetDriverDescription (funzione)
- Messaggio WM_CAP_DRIVER_GET_NAME
- capDriverGetName (macro)
- Messaggio WM_CAP_DRIVER_GET_VERSION
- capDriverGetVersion (macro)
- Messaggio WM_CAP_DRIVER_DISCONNECT
- capDriverDisconnect (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c189ad3ea5631e269ffbe85f20a143b074486f22
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103710156"
---
# <a name="connecting-a-capture-window-to-a-capture-driver"></a><span data-ttu-id="67b43-112">Connessione di una finestra di acquisizione a un driver di acquisizione</span><span class="sxs-lookup"><span data-stu-id="67b43-112">Connecting a Capture Window to a Capture Driver</span></span>

<span data-ttu-id="67b43-113">È possibile connettere o disconnettere dinamicamente una finestra di acquisizione a un driver di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="67b43-113">You can dynamically connect or disconnect a capture window to a capture driver.</span></span> <span data-ttu-id="67b43-114">È possibile connettere o associare una finestra di acquisizione a un driver di acquisizione usando il messaggio di [**\_ \_ \_ connessione driver WM Cap**](wm-cap-driver-connect.md) (o la macro [**capDriverConnect**](/windows/desktop/api/Vfw/nf-vfw-capdriverconnect) ).</span><span class="sxs-lookup"><span data-stu-id="67b43-114">You can connect or associate a capture window with a capture driver by using the [**WM\_CAP\_DRIVER\_CONNECT**](wm-cap-driver-connect.md) message (or the [**capDriverConnect**](/windows/desktop/api/Vfw/nf-vfw-capdriverconnect) macro).</span></span> <span data-ttu-id="67b43-115">Dopo la connessione di una finestra di acquisizione e di un driver di acquisizione, è possibile inviare messaggi specifici del dispositivo al driver di acquisizione associato a una finestra di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="67b43-115">After a capture window and capture driver are connected, you can send device-specific messages to the capture driver associated with a capture window.</span></span>

<span data-ttu-id="67b43-116">Se si dispone di più di un dispositivo di acquisizione installato in un sistema, è possibile connettere una finestra di acquisizione a un driver di dispositivo di acquisizione video specifico specificando un numero intero per il parametro *wParam* del \_ messaggio di \_ connessione driver WM Cap \_ .</span><span class="sxs-lookup"><span data-stu-id="67b43-116">If you have more than one capture device installed on a system, you can connect a capture window to a particular video capture device driver by specifying an integer for the *wParam* parameter of the WM\_CAP\_DRIVER\_CONNECT message.</span></span> <span data-ttu-id="67b43-117">Il valore integer è un indice che identifica un driver di acquisizione video elencato nel registro di sistema o nella \[ \] sezione driver del file SYSTEM.INI.</span><span class="sxs-lookup"><span data-stu-id="67b43-117">The integer is an index that identifies a video capture driver listed in the registry or in the \[drivers\] section of the SYSTEM.INI file.</span></span> <span data-ttu-id="67b43-118">Usare zero per la prima voce di indice.</span><span class="sxs-lookup"><span data-stu-id="67b43-118">Use zero for the first index entry.</span></span>

<span data-ttu-id="67b43-119">È possibile recuperare il nome e la versione di un driver di acquisizione installato utilizzando la funzione [**capGetDriverDescription**](/windows/desktop/api/Vfw/nf-vfw-capgetdriverdescriptiona) .</span><span class="sxs-lookup"><span data-stu-id="67b43-119">You can retrieve the name and version of an installed capture driver by using the [**capGetDriverDescription**](/windows/desktop/api/Vfw/nf-vfw-capgetdriverdescriptiona) function.</span></span> <span data-ttu-id="67b43-120">L'applicazione può usare questa funzione per enumerare i driver e i dispositivi di acquisizione installati, in modo che l'utente possa selezionare un dispositivo di acquisizione per connettersi a una finestra di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="67b43-120">Your application can use this function to enumerate the installed capture devices and drivers, so the user can select a capture device to connect to a capture window.</span></span>

<span data-ttu-id="67b43-121">È possibile recuperare il nome del driver di dispositivo di acquisizione connesso a una finestra di acquisizione usando [**il \_ driver di WM Cap \_ \_ get \_ Name**](wm-cap-driver-get-name.md) Message (o la macro [**capDriverGetName**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetname) ).</span><span class="sxs-lookup"><span data-stu-id="67b43-121">You can retrieve the name of the capture device driver connected to a capture window by using the [**WM\_CAP\_DRIVER\_GET\_NAME**](wm-cap-driver-get-name.md) message (or the [**capDriverGetName**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetname) macro).</span></span> <span data-ttu-id="67b43-122">Per recuperare la versione di un driver di acquisizione installato, usare il messaggio [**WM \_ Cap \_ driver \_ get \_ Version**](wm-cap-driver-get-version.md) (o la macro [**capDriverGetVersion**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetversion) ).</span><span class="sxs-lookup"><span data-stu-id="67b43-122">To retrieve the version of an installed capture driver, use the [**WM\_CAP\_DRIVER\_GET\_VERSION**](wm-cap-driver-get-version.md) message (or the [**capDriverGetVersion**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetversion) macro).</span></span>

<span data-ttu-id="67b43-123">È possibile disconnettere una finestra di acquisizione da un driver di acquisizione usando il messaggio di [**\_ \_ \_ disconnessione del driver WM Cap**](wm-cap-driver-disconnect.md) (o la macro [**capDriverDisconnect**](/windows/desktop/api/Vfw/nf-vfw-capdriverdisconnect) ).</span><span class="sxs-lookup"><span data-stu-id="67b43-123">You can disconnect a capture window from a capture driver by using the [**WM\_CAP\_DRIVER\_DISCONNECT**](wm-cap-driver-disconnect.md) message (or the [**capDriverDisconnect**](/windows/desktop/api/Vfw/nf-vfw-capdriverdisconnect) macro).</span></span>

<span data-ttu-id="67b43-124">Quando viene eliminata definitivamente una finestra di acquisizione, i driver di dispositivo di acquisizione video connessi vengono automaticamente disconnessi.</span><span class="sxs-lookup"><span data-stu-id="67b43-124">When an capture window is destroyed, any connected video capture device drivers are automatically disconnected.</span></span>

 

 




