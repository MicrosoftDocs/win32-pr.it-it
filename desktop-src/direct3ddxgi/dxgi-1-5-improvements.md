---
description: Le funzionalità seguenti sono state aggiunte a Microsoft DirectX Graphics Infrastructure (DXGI) 1,5, per supportare la specifica e la duplicazione più flessibili dei formati di output.
ms.assetid: DD7401E1-9991-48D8-AD23-4D34238EA4AF
title: Miglioramenti di DXGI 1,5
ms.topic: article
ms.date: 03/05/2021
ms.openlocfilehash: 58df3ef78781437ee033530a2ed2179bb9a132d8
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/06/2021
ms.locfileid: "104351926"
---
# <a name="dxgi-15-improvements"></a><span data-ttu-id="4da0a-103">Miglioramenti di DXGI 1,5</span><span class="sxs-lookup"><span data-stu-id="4da0a-103">DXGI 1.5 Improvements</span></span>

<span data-ttu-id="4da0a-104">Le funzionalità seguenti sono state aggiunte a Microsoft DirectX Graphics Infrastructure (DXGI) 1,5, per supportare la specifica e la duplicazione più flessibili dei formati di output.</span><span class="sxs-lookup"><span data-stu-id="4da0a-104">The following functionality has been added to Microsoft DirectX Graphics Infrastructure (DXGI) 1.5, to support more flexible specifying and duplication of output formats.</span></span>

## <a name="high-dynamic-range-and-wide-color-gamut"></a><span data-ttu-id="4da0a-105">Gamma dinamica elevata e gamma di colori ampia</span><span class="sxs-lookup"><span data-stu-id="4da0a-105">High Dynamic Range and Wide Color Gamut</span></span>

<span data-ttu-id="4da0a-106">Vedere [uso di DirectX con schermi con intervallo dinamico elevato e colori avanzati](../direct3darticles/high-dynamic-range.md).</span><span class="sxs-lookup"><span data-stu-id="4da0a-106">Refer to [Using DirectX with high dynamic range displays and advanced color](../direct3darticles/high-dynamic-range.md).</span></span>

## <a name="variable-refresh-rate-displays"></a><span data-ttu-id="4da0a-107">Visualizzazione frequenza di aggiornamento variabili</span><span class="sxs-lookup"><span data-stu-id="4da0a-107">Variable refresh rate displays</span></span>

<span data-ttu-id="4da0a-108">Vedere [frequenza di aggiornamento variabili](variable-refresh-rate-displays.md).</span><span class="sxs-lookup"><span data-stu-id="4da0a-108">Refer to [Variable refresh rate displays](variable-refresh-rate-displays.md).</span></span>

## <a name="duplicating-output"></a><span data-ttu-id="4da0a-109">Duplicazione dell'output</span><span class="sxs-lookup"><span data-stu-id="4da0a-109">Duplicating output</span></span>

<span data-ttu-id="4da0a-110">Una singola interfaccia, [**IDXGIOutput5**](/windows/win32/api/DXGI1_5/nn-dxgi1_5-idxgioutput5), con un solo metodo, [**DuplicateOutput1**](/windows/win32/api/DXGI1_5/nf-dxgi1_5-idxgioutput5-duplicateoutput1), è stata aggiunta a DXGI 1,5 per fornire una versione di prestazioni più flessibile e più elevata del metodo [**DuplicateOutput**](/windows/win32/api/DXGI1_2/nf-dxgi1_2-idxgioutput1-duplicateoutput) originale.</span><span class="sxs-lookup"><span data-stu-id="4da0a-110">A single interface, [**IDXGIOutput5**](/windows/win32/api/DXGI1_5/nn-dxgi1_5-idxgioutput5), with a single method, [**DuplicateOutput1**](/windows/win32/api/DXGI1_5/nf-dxgi1_5-idxgioutput5-duplicateoutput1), has been added to DXGI 1.5 to provide a more flexible and higher performance version of the original [**DuplicateOutput**](/windows/win32/api/DXGI1_2/nf-dxgi1_2-idxgioutput1-duplicateoutput) method.</span></span> <span data-ttu-id="4da0a-111">**DuplicateOutput1** consente di specificare un elenco di formati supportati per le superfici a schermo intero che possono essere restituite dall'oggetto [**IDXGIOutputDuplication**](/windows/win32/api/DXGI1_2/nn-dxgi1_2-idxgioutputduplication) e consente di acquisire contenuto HDR e WCG.</span><span class="sxs-lookup"><span data-stu-id="4da0a-111">**DuplicateOutput1** allows specifying a list of supported formats for fullscreen surfaces that can be returned by the [**IDXGIOutputDuplication**](/windows/win32/api/DXGI1_2/nn-dxgi1_2-idxgioutputduplication) object, and enables capturing HDR and WCG content.</span></span>

## <a name="offering-and-reclaiming-resources"></a><span data-ttu-id="4da0a-112">Offerta e richiesta di risorse</span><span class="sxs-lookup"><span data-stu-id="4da0a-112">Offering and Reclaiming Resources</span></span>

<span data-ttu-id="4da0a-113">I metodi aggiornati [**OfferResources1**](/windows/win32/api/dxgi1_5/nf-dxgi1_5-idxgidevice4-offerresources1) e [**ReclaimResources1**](/windows/win32/api/dxgi1_5/nf-dxgi1_5-idxgidevice4-reclaimresources1) sono stati aggiunti a una nuova interfaccia, [**IDXGIDevice4**](/windows/win32/api/dxgi1_5/nn-dxgi1_5-idxgidevice4), per consentire il decommit della memoria, oltre a rimuovere le risorse.</span><span class="sxs-lookup"><span data-stu-id="4da0a-113">Updated methods [**OfferResources1**](/windows/win32/api/dxgi1_5/nf-dxgi1_5-idxgidevice4-offerresources1) and [**ReclaimResources1**](/windows/win32/api/dxgi1_5/nf-dxgi1_5-idxgidevice4-reclaimresources1) have been added to a new interface, [**IDXGIDevice4**](/windows/win32/api/dxgi1_5/nn-dxgi1_5-idxgidevice4), to allow de-committing of memory in addition to discarding resources.</span></span> <span data-ttu-id="4da0a-114">Se si sceglie la nuova [**offerta DXGI flag di \_ \_ risorsa Consenti flag di \_ \_ \_ decommit**](/windows/win32/api/dxgi1_5/ne-dxgi1_5-dxgi_offer_resource_flags) , i nuovi risultati del nuovo reclamo devono essere gestiti correttamente.</span><span class="sxs-lookup"><span data-stu-id="4da0a-114">Opting in to the new [**DXGI\_OFFER\_RESOURCE\_FLAG\_ALLOW\_DECOMMIT**](/windows/win32/api/dxgi1_5/ne-dxgi1_5-dxgi_offer_resource_flags) flag means the new reclaim results must be properly handled.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4da0a-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4da0a-115">Related topics</span></span>

[<span data-ttu-id="4da0a-116">Guida per programmatori per DXGI</span><span class="sxs-lookup"><span data-stu-id="4da0a-116">Programming Guide for DXGI</span></span>](dx-graphics-dxgi-overviews.md)
