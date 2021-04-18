---
title: Comunicazione con i dispositivi MCI
description: Comunicazione con i dispositivi MCI
ms.assetid: 2408f8e4-d040-40f5-a880-1ecb8025656c
keywords:
- MCIWndSendString (macro)
- mciSendString (funzione)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f7f5458cff0ef4c5c5f84e565fae06ade8796c4
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "106299600"
---
# <a name="communicating-with-mci-devices"></a><span data-ttu-id="14d57-105">Comunicazione con i dispositivi MCI</span><span class="sxs-lookup"><span data-stu-id="14d57-105">Communicating with MCI Devices</span></span>

<span data-ttu-id="14d57-106">Il driver di ogni dispositivo MCI gestisce un elenco delle impostazioni e delle funzionalità correnti, quindi può emettere una risposta accurata quando viene eseguita una query per ottenere informazioni.</span><span class="sxs-lookup"><span data-stu-id="14d57-106">The driver of each MCI device maintains a list of its current settings and capabilities, so it can issue an accurate response when it is queried for information.</span></span>

<span data-ttu-id="14d57-107">Quando si vuole comunicare con un dispositivo MCI, è possibile usare le macro e le funzioni di MCIWnd.</span><span class="sxs-lookup"><span data-stu-id="14d57-107">When you want to communicate with an MCI device, you can use MCIWnd macros and functions.</span></span> <span data-ttu-id="14d57-108">Molti dei comandi e delle query MCI più comuni sono definiti come macro.</span><span class="sxs-lookup"><span data-stu-id="14d57-108">Many of the most common MCI commands and queries are defined as macros.</span></span> <span data-ttu-id="14d57-109">Tuttavia, se l'attività che si desidera eseguire non è disponibile come funzione o macro, è possibile inviare i comandi MCI direttamente al driver di dispositivo utilizzando la macro [**MCIWndSendString**](/windows/desktop/api/Vfw/nf-vfw-mciwndsendstring) o il form del messaggio o il formato stringa dei comandi MCI.</span><span class="sxs-lookup"><span data-stu-id="14d57-109">However, if the task you want to perform is unavailable as a function or macro, you can send MCI commands directly to the device driver by using the [**MCIWndSendString**](/windows/desktop/api/Vfw/nf-vfw-mciwndsendstring) macro or by using either the message form or string form of the MCI commands.</span></span> <span data-ttu-id="14d57-110">L'uso della macro **MCIWndSendString** equivale all'uso della funzione [**mciSendString**](/previous-versions//dd757161(v=vs.85)) come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="14d57-110">Using the **MCIWndSendString** macro is equivalent to using the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function as follows:</span></span>


```C++
mciSendString(sz, Null, 0, Null) 
```



<span data-ttu-id="14d57-111">I parametri di [**MCIWndSendString**](/windows/desktop/api/Vfw/nf-vfw-mciwndsendstring) includono solo l'handle di finestra e il formato stringa del comando.</span><span class="sxs-lookup"><span data-stu-id="14d57-111">The parameters of [**MCIWndSendString**](/windows/desktop/api/Vfw/nf-vfw-mciwndsendstring) include only the window handle and the string form of the command.</span></span> <span data-ttu-id="14d57-112">Per recuperare le informazioni restituite da un comando stringa, usare la macro [**MCIWndReturnString**](/windows/desktop/api/Vfw/nf-vfw-mciwndreturnstring) .</span><span class="sxs-lookup"><span data-stu-id="14d57-112">To retrieve the information returned by a string command, use the [**MCIWndReturnString**](/windows/desktop/api/Vfw/nf-vfw-mciwndreturnstring) macro.</span></span>

<span data-ttu-id="14d57-113">Per ulteriori informazioni su MCI, vedere [MCI](mci.md).</span><span class="sxs-lookup"><span data-stu-id="14d57-113">For more information about MCI, see [MCI](mci.md).</span></span>

> [!Note]  
> <span data-ttu-id="14d57-114">È necessario escludere l'alias del dispositivo dal comando MCI quando si usa **MCIWndSendString**.</span><span class="sxs-lookup"><span data-stu-id="14d57-114">You must exclude the device alias from the MCI command when you use **MCIWndSendString**.</span></span> <span data-ttu-id="14d57-115">La libreria MCIWnd aggiunge questo alias quando invia il comando al dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="14d57-115">The MCIWnd library adds this alias when it sends the command to the MCI device.</span></span>

 

 

 