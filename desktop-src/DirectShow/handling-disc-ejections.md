---
description: Gestione delle espulsioni dei dischi
ms.assetid: c43dd795-749b-4ca7-8510-71d62e0076b3
title: Gestione delle espulsioni dei dischi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8964c8fd18395e932e1536e885bae1814d5952fd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103875929"
---
# <a name="handling-disc-ejections"></a><span data-ttu-id="35e87-103">Gestione delle espulsioni dei dischi</span><span class="sxs-lookup"><span data-stu-id="35e87-103">Handling Disc Ejections</span></span>

<span data-ttu-id="35e87-104">Quando l'utente espelle un DVD dall'unità, il navigatore DVD invia all'applicazione un messaggio di \_ rilascio del disco DVD di EC \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="35e87-104">When the user ejects a DVD from the drive, the DVD Navigator sends your application an EC\_DVD\_DISC\_EJECTED message.</span></span> <span data-ttu-id="35e87-105">L'applicazione può ignorare questo messaggio e consentire al navigatore DVD di gestire lo stato del grafo.</span><span class="sxs-lookup"><span data-stu-id="35e87-105">The application can safely ignore this message and let the DVD Navigator manage the graph's state.</span></span> <span data-ttu-id="35e87-106">Un'applicazione può inoltre gestire il \_ \_ metodo di rimozione del disco DVD EC \_ per implementare un comportamento personalizzato quando viene espulso un disco.</span><span class="sxs-lookup"><span data-stu-id="35e87-106">An application can also handle the EC\_DVD\_DISC\_EJECTED method to implement custom behavior when a disc is ejected.</span></span> <span data-ttu-id="35e87-107">Se si gestisce il messaggio, è necessario impostare il \_ flag DVD ResetOnStop su **true** con il metodo [**SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) , quindi chiamare [**IMediaControl:: Stop**](/windows/desktop/api/Control/nf-control-imediacontrol-stop) prima di chiudere l'applicazione o riprodurre un altro disco.</span><span class="sxs-lookup"><span data-stu-id="35e87-107">If you handle the message, you must set the DVD\_ResetOnStop flag to **TRUE** with the [**SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) method and then call [**IMediaControl::Stop**](/windows/desktop/api/Control/nf-control-imediacontrol-stop) before closing the application or playing another disc.</span></span>

## <a name="related-topics"></a><span data-ttu-id="35e87-108">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="35e87-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="35e87-109">Applicazioni DVD</span><span class="sxs-lookup"><span data-stu-id="35e87-109">DVD Applications</span></span>](dvd-applications.md)
</dt> </dl>

 

 



