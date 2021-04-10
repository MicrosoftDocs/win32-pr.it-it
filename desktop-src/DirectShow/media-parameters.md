---
description: Parametri dei supporti
ms.assetid: 48b2bc2e-897d-4aa9-8a50-c2855a17dca5
title: Parametri dei supporti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce9276a3d38b9176458299bfd1a47057cac6236e
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "103885964"
---
# <a name="media-parameters"></a><span data-ttu-id="0dfde-103">Parametri dei supporti</span><span class="sxs-lookup"><span data-stu-id="0dfde-103">Media Parameters</span></span>

<span data-ttu-id="0dfde-104">I parametri multimediali consentono a un'applicazione di configurare le proprietà di un oggetto in modo che cambino nel tempo in modo matematico.</span><span class="sxs-lookup"><span data-stu-id="0dfde-104">Media parameters enable an application to configure an object's properties so that they change over time in a mathematically deterministic way.</span></span>

<span data-ttu-id="0dfde-105">Si supponga, ad esempio, che un ingegnere del suono stia combinando un nastro master digitale e voglia applicare un lieve ritardo a una sezione vocale per compilare il suono.</span><span class="sxs-lookup"><span data-stu-id="0dfde-105">For example, suppose that a sound engineer is mixing a digital master tape and wants to apply a slight delay to a vocal section, to fill out the sound.</span></span> <span data-ttu-id="0dfde-106">L'effetto sarà stridente se il ritardo si interrompe bruscamente.</span><span class="sxs-lookup"><span data-stu-id="0dfde-106">The effect will be jarring if the delay cuts in abruptly.</span></span> <span data-ttu-id="0dfde-107">Al contrario, l'effetto dovrebbe iniziare il 100% a secco (nessun ritardo) e la combinazione Wet/Dry dovrebbe aumentare gradualmente fino a raggiungere il livello desiderato.</span><span class="sxs-lookup"><span data-stu-id="0dfde-107">Instead, the effect should begin 100 percent dry (no delay), and the wet/dry mix should increase gradually until it reaches the desired level.</span></span> <span data-ttu-id="0dfde-108">Questa transizione dovrebbe inoltre seguire una curva uniforme o una progressione lineare.</span><span class="sxs-lookup"><span data-stu-id="0dfde-108">Moreover, this transition should follow a smooth curve or linear progression.</span></span> <span data-ttu-id="0dfde-109">Per supportare questo scenario, un DMO può esporre le interfacce seguenti:</span><span class="sxs-lookup"><span data-stu-id="0dfde-109">To support this scenario, a DMO can expose the following interfaces:</span></span>

-   <span data-ttu-id="0dfde-110">[**IMediaParamInfo**](/previous-versions/windows/desktop/api/Medparam/nn-medparam-imediaparaminfo) contiene metodi per l'individuazione delle informazioni sulle proprietà supportate.</span><span class="sxs-lookup"><span data-stu-id="0dfde-110">[**IMediaParamInfo**](/previous-versions/windows/desktop/api/Medparam/nn-medparam-imediaparaminfo) contains methods for discovering information about the supported properties.</span></span> <span data-ttu-id="0dfde-111">In genere, il client chiamerà questi metodi prima di iniziare a trasmettere i dati.</span><span class="sxs-lookup"><span data-stu-id="0dfde-111">Typically, the client will call these methods before it begins to stream data.</span></span>
-   <span data-ttu-id="0dfde-112">[**IMediaParams**](/previous-versions/windows/desktop/api/Medparam/nn-medparam-imediaparams) contengono metodi per l'impostazione delle curve che seguiranno un parametro durante il flusso.</span><span class="sxs-lookup"><span data-stu-id="0dfde-112">[**IMediaParams**](/previous-versions/windows/desktop/api/Medparam/nn-medparam-imediaparams) contain methods for setting the curves that a parameter will follow during streaming.</span></span>

<span data-ttu-id="0dfde-113">Queste interfacce sono progettate principalmente per DMOs, ma qualsiasi oggetto può supportarle.</span><span class="sxs-lookup"><span data-stu-id="0dfde-113">These interfaces are designed primarily for DMOs, but any object can support them.</span></span> <span data-ttu-id="0dfde-114">In questa sezione il termine *parametro* si riferisce a qualsiasi proprietà che supporta queste due interfacce.</span><span class="sxs-lookup"><span data-stu-id="0dfde-114">Within this section, the term *parameter* refers to any property that supports these two interfaces.</span></span>

<span data-ttu-id="0dfde-115">Questa sezione contiene i seguenti argomenti:</span><span class="sxs-lookup"><span data-stu-id="0dfde-115">This section contains the following topics:</span></span>

-   [<span data-ttu-id="0dfde-116">Curve parametro</span><span class="sxs-lookup"><span data-stu-id="0dfde-116">Parameter Curves</span></span>](parameter-curves.md)
-   [<span data-ttu-id="0dfde-117">Informazioni sui parametri</span><span class="sxs-lookup"><span data-stu-id="0dfde-117">Parameter Information</span></span>](parameter-information.md)
-   [<span data-ttu-id="0dfde-118">Segmenti busta</span><span class="sxs-lookup"><span data-stu-id="0dfde-118">Envelope Segments</span></span>](envelope-segments.md)
-   [<span data-ttu-id="0dfde-119">Calcolo dei valori dei parametri</span><span class="sxs-lookup"><span data-stu-id="0dfde-119">Calculating Parameter Values</span></span>](calculating-parameter-values.md)

## <a name="related-topics"></a><span data-ttu-id="0dfde-120">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0dfde-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0dfde-121">Oggetti multimediali DirectX</span><span class="sxs-lookup"><span data-stu-id="0dfde-121">DirectX Media Objects</span></span>](directx-media-objects.md)
</dt> </dl>

 

 



