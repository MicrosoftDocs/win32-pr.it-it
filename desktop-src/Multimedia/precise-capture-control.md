---
title: Controllo di acquisizione preciso
description: Controllo di acquisizione preciso
ms.assetid: 497c9d77-f392-4cbb-88f3-8418e1e9fc6b
keywords:
- Funzioni di callback AVICap, controllo di acquisizione preciso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0749d420d7a1999d074546a0cf577fdaceb72483
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104515700"
---
# <a name="precise-capture-control"></a><span data-ttu-id="f7b36-104">Controllo di acquisizione preciso</span><span class="sxs-lookup"><span data-stu-id="f7b36-104">Precise Capture Control</span></span>

<span data-ttu-id="f7b36-105">Una finestra di acquisizione può fornire la funzione di callback Capture-Control con un controllo preciso sui momenti in cui l'acquisizione di flussi inizia e termina.</span><span class="sxs-lookup"><span data-stu-id="f7b36-105">A capture window can provide the capture-control callback function with precise control over the moments that streaming capture begin and end.</span></span> <span data-ttu-id="f7b36-106">Il primo messaggio inviato dal driver di acquisizione alla procedura di callback imposta il parametro *nState* su CONTROLCALLBACK \_ preroll dopo l'allocazione di tutti i buffer e tutte le altre preparazioni di acquisizione sono completate.</span><span class="sxs-lookup"><span data-stu-id="f7b36-106">The first message sent from the capture driver to the callback procedure sets the *nState* parameter to CONTROLCALLBACK\_PREROLL after allocating all buffers and all other capture preparations are complete.</span></span> <span data-ttu-id="f7b36-107">Questo messaggio fornisce all'applicazione la possibilità di preregistrare le origini video.</span><span class="sxs-lookup"><span data-stu-id="f7b36-107">This message gives the application the ability to preroll the video sources.</span></span> <span data-ttu-id="f7b36-108">(La funzione di callback specifica *nState* come secondo parametro). La funzione di callback viene quindi restituita al momento esatto in cui viene avviata la registrazione.</span><span class="sxs-lookup"><span data-stu-id="f7b36-108">(The callback function specifies *nState* as its second parameter.) The callback function then returns at the exact moment recording is to begin.</span></span> <span data-ttu-id="f7b36-109">Un valore restituito **true** dalla funzione di callback continua l'acquisizione.</span><span class="sxs-lookup"><span data-stu-id="f7b36-109">A return value of **TRUE** from the callback function continues capture.</span></span> <span data-ttu-id="f7b36-110">Viene restituito un valore di **false** Aborts Capture.</span><span class="sxs-lookup"><span data-stu-id="f7b36-110">A return value of **FALSE** aborts capture.</span></span> <span data-ttu-id="f7b36-111">Una volta avviata l'acquisizione, la funzione di callback viene chiamata spesso con *nState* impostato sull'acquisizione di CONTROLCALLBACK \_ per consentire all'applicazione di terminare l'acquisizione restituendo **false**.</span><span class="sxs-lookup"><span data-stu-id="f7b36-111">Once capture begins, the callback function is called frequently with *nState* set to CONTROLCALLBACK\_CAPTURING to allow the application to end capture by returning **FALSE**.</span></span>

 

 




