---
title: Modelli di conformità del dispositivo
description: Modelli di conformità del dispositivo
ms.assetid: 5172ab39-819a-4d74-8e6e-b275b43f664c
keywords:
- Windows Media Format SDK, modelli di conformità del dispositivo
- codec, modelli di conformità del dispositivo
- modelli di conformità del dispositivo, informazioni
- modelli, modelli di conformità dei dispositivi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6eccb88b372f9e0eb463d88db83d70102408a7a6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104332327"
---
# <a name="device-conformance-templates"></a><span data-ttu-id="ddb36-107">Modelli di conformità del dispositivo</span><span class="sxs-lookup"><span data-stu-id="ddb36-107">Device Conformance Templates</span></span>

<span data-ttu-id="ddb36-108">I codec della serie Windows Media 9 supportano i modelli di conformità dei dispositivi, che sono intervalli definiti di impostazioni di configurazione del flusso e algoritmi di codec.</span><span class="sxs-lookup"><span data-stu-id="ddb36-108">The Windows Media 9 Series codecs support device conformance templates, which are defined ranges of stream configuration settings and codec algorithms.</span></span> <span data-ttu-id="ddb36-109">Ogni modello definisce gli intervalli di valori appropriati per determinati dispositivi.</span><span class="sxs-lookup"><span data-stu-id="ddb36-109">Each template defines the ranges of values appropriate for certain devices.</span></span>

<span data-ttu-id="ddb36-110">In passato, i produttori di hardware che rendevano i dispositivi in grado di riprodurre file ASF venivano tutti applicati ai propri standard.</span><span class="sxs-lookup"><span data-stu-id="ddb36-110">In the past, the hardware manufacturers that made devices capable of playing ASF files were all working to their own standards.</span></span> <span data-ttu-id="ddb36-111">Ciò ha comportato una gamma molto diversificata di funzionalità su dispositivi simili che continuano a essere attuali.</span><span class="sxs-lookup"><span data-stu-id="ddb36-111">This resulted in the widely disparate range of capabilities on similar devices that continues today.</span></span>

<span data-ttu-id="ddb36-112">Con i modelli di conformità dei dispositivi, i codec Windows Media stabiliscono un terreno comune per dispositivi simili.</span><span class="sxs-lookup"><span data-stu-id="ddb36-112">With device conformance templates, the Windows Media codecs establish common ground for similar devices.</span></span> <span data-ttu-id="ddb36-113">I produttori di hardware possono indicare a quali modelli sono conformi i loro dispositivi, consentendo agli autori di contenuti di indirizzare i file in modo più sicuro alla lettura dei dispositivi.</span><span class="sxs-lookup"><span data-stu-id="ddb36-113">Hardware manufacturers can state which templates their devices conform to, enabling content creators to more confidently target their files to reading devices.</span></span> <span data-ttu-id="ddb36-114">È inoltre più facile per le applicazioni del lettore determinare se un file non è appropriato per il dispositivo prima di provare a riprodurlo.</span><span class="sxs-lookup"><span data-stu-id="ddb36-114">It is also easier for player applications to determine whether a file is inappropriate for the device before attempting to play it.</span></span>

<span data-ttu-id="ddb36-115">Un modello di conformità del dispositivo è identificato da una stringa, archiviata come un attributo di metadati associato al flusso a cui si applica il modello.</span><span class="sxs-lookup"><span data-stu-id="ddb36-115">A device conformance template is identified by a string, which is stored as a metadata attribute associated with the stream to which the template applies.</span></span> <span data-ttu-id="ddb36-116">Per un elenco dei modelli e delle relative stringhe e parametri, vedere [parametri del modello di conformità del dispositivo](device-conformance-template-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="ddb36-116">For a list of the templates and their strings and parameters, see [Device Conformance Template Parameters](device-conformance-template-parameters.md).</span></span>

<span data-ttu-id="ddb36-117">I modelli di conformità dei dispositivi sono supportati per tutti i codec Windows Media 9 e versioni successive, ad eccezione del codec Windows Media Video 9 screen e del codec Windows Media Audio 9 Lossless.</span><span class="sxs-lookup"><span data-stu-id="ddb36-117">Device conformance templates are supported for all of the Windows Media 9 Series and later codecs except the Windows Media Video 9 Screen codec and the Windows Media Audio 9 Lossless codec.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ddb36-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ddb36-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ddb36-119">**Funzionalità di codec**</span><span class="sxs-lookup"><span data-stu-id="ddb36-119">**Codec Features**</span></span>](codec-features.md)
</dt> <dt>

[<span data-ttu-id="ddb36-120">**Uso dei modelli di conformità dei dispositivi**</span><span class="sxs-lookup"><span data-stu-id="ddb36-120">**Working with Device Conformance Templates**</span></span>](working-with-device-conformance-templates.md)
</dt> </dl>

 

 




