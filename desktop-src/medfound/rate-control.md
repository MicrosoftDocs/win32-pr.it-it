---
description: Controllo della frequenza
ms.assetid: 6529859f-cfb6-4983-a489-bcc2f04e721f
title: Controllo della frequenza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f484a0469d96578ca1bb7e1d661d7e2319bd8bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309022"
---
# <a name="rate-control"></a><span data-ttu-id="f3350-103">Controllo della frequenza</span><span class="sxs-lookup"><span data-stu-id="f3350-103">Rate Control</span></span>

<span data-ttu-id="f3350-104">La [sessione multimediale](media-session.md) supporta la modifica della velocità di riproduzione, che può essere usata da un'applicazione per implementare funzionalità di riproduzione, ad esempio l'avanzamento rapido e il riavvolgimento.</span><span class="sxs-lookup"><span data-stu-id="f3350-104">The [Media Session](media-session.md) supports changing the playback rate, which an application can use to implement playback features such as fast-forward and rewind.</span></span> <span data-ttu-id="f3350-105">In questa sezione viene descritto in che modo le applicazioni possono modificare la velocità di riproduzione durante l'utilizzo della sessione multimediale.</span><span class="sxs-lookup"><span data-stu-id="f3350-105">This section describes how applications can change the playback rate while using the Media Session.</span></span>

<span data-ttu-id="f3350-106">Per informazioni sul controllo della velocità di supporto nei componenti della pipeline, vedere [implementazione del controllo della frequenza](implementing-rate-control.md).</span><span class="sxs-lookup"><span data-stu-id="f3350-106">For information about supporting rate control in your own pipeline components, see [Implementing Rate Control](implementing-rate-control.md).</span></span>

<span data-ttu-id="f3350-107">In questa sezione vengono trattati gli argomenti seguenti.</span><span class="sxs-lookup"><span data-stu-id="f3350-107">This section contains the following topics.</span></span>



| <span data-ttu-id="f3350-108">Argomento</span><span class="sxs-lookup"><span data-stu-id="f3350-108">Topic</span></span>                                                                                                      | <span data-ttu-id="f3350-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f3350-109">Description</span></span>                                                            |
|------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [<span data-ttu-id="f3350-110">Informazioni sul controllo della frequenza</span><span class="sxs-lookup"><span data-stu-id="f3350-110">About Rate Control</span></span>](about-rate-control.md)                                                               | <span data-ttu-id="f3350-111">Fornisce una panoramica generale del controllo della frequenza.</span><span class="sxs-lookup"><span data-stu-id="f3350-111">Gives a general overview of rate control.</span></span>                              |
| [<span data-ttu-id="f3350-112">Come determinare le tariffe supportate</span><span class="sxs-lookup"><span data-stu-id="f3350-112">How to Determine Supported Rates</span></span>](how-to-determine-supported-rates.md)                                   | <span data-ttu-id="f3350-113">Come trovare la velocità di riproduzione supportata più veloce e più lenta.</span><span class="sxs-lookup"><span data-stu-id="f3350-113">How to find the fastest and slowest supported playback rates.</span></span>          |
| [<span data-ttu-id="f3350-114">Come impostare la velocità di riproduzione nella sessione multimediale</span><span class="sxs-lookup"><span data-stu-id="f3350-114">How to Set the Playback Rate on the Media Session</span></span>](how-to-set-the-playback-rate-on-the-media-session.md) | <span data-ttu-id="f3350-115">Come modificare la velocità di riproduzione.</span><span class="sxs-lookup"><span data-stu-id="f3350-115">How to change the playback rate.</span></span>                                       |
| [<span data-ttu-id="f3350-116">Come eseguire lo scrubbing</span><span class="sxs-lookup"><span data-stu-id="f3350-116">How to Perform Scrubbing</span></span>](how-to-perform-scrubbing.md)                                                   | <span data-ttu-id="f3350-117">Come eseguire un passaggio di un frame video alla volta.</span><span class="sxs-lookup"><span data-stu-id="f3350-117">How to step one video frame at a time.</span></span>                                 |
| [<span data-ttu-id="f3350-118">Implementazione del controllo della frequenza</span><span class="sxs-lookup"><span data-stu-id="f3350-118">Implementing Rate Control</span></span>](implementing-rate-control.md)                                                 | <span data-ttu-id="f3350-119">Come supportare frequenze di riproduzione variabili in un componente della pipeline personalizzato.</span><span class="sxs-lookup"><span data-stu-id="f3350-119">How to support variable playback rates in a custom pipeline component.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="f3350-120">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f3350-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f3350-121">Sessione multimediale</span><span class="sxs-lookup"><span data-stu-id="f3350-121">Media Session</span></span>](media-session.md)
</dt> <dt>

[<span data-ttu-id="f3350-122">Ricerca, avanzamento rapido e riproduzione inversa</span><span class="sxs-lookup"><span data-stu-id="f3350-122">Seeking, Fast Forward, and Reverse Play</span></span>](seeking--fast-forward--and-reverse-play.md)
</dt> </dl>

 

 



