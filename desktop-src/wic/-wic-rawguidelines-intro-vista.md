---
description: Formati di immagini non ELABORAte in Windows Vista
ms.assetid: e28b642c-03c8-4ecc-b5f5-e3911b8003a7
title: Formati di immagini non ELABORAte in Windows Vista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c48b4e3ab5b0d373dbc0313267e58177b189538
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232877"
---
# <a name="raw-image-formats-in-windows-vista"></a><span data-ttu-id="62d89-103">Formati di immagini non ELABORAte in Windows Vista</span><span class="sxs-lookup"><span data-stu-id="62d89-103">RAW Image Formats in Windows Vista</span></span>

<span data-ttu-id="62d89-104">Esplora risorse di Windows Vista, raccolta foto di Windows Vista, raccolta foto di Windows Live e Windows 7 Photo Viewer utilizzano Windows Imaging Component (WIC) e pertanto supportano i formati di immagine non ELABORAta quando nel computer sono installati codec appropriati.</span><span class="sxs-lookup"><span data-stu-id="62d89-104">Windows Vista Explorer , Windows Vista Photo Gallery, Window Live Photo Gallery, and the Windows 7 Photo Viewer all use Windows Imaging Component (WIC) and therefore support RAW image formats when appropriate codecs are installed on the computer.</span></span>

<span data-ttu-id="62d89-105">Poiché WIC è un'architettura di imaging estensibile, qualsiasi applicazione WIC può utilizzare nuovi formati di immagine non appena vengono installati nuovi codec nel sistema.</span><span class="sxs-lookup"><span data-stu-id="62d89-105">Because WIC is an extensible imaging architecture, any WIC application can consume new image formats as soon as new codecs are installed on the system.</span></span> <span data-ttu-id="62d89-106">In questo modo WIC è ideale come soluzione Plug and Play per i formati di immagine non ELABORAti prodotti dalle fotocamere digitali.</span><span class="sxs-lookup"><span data-stu-id="62d89-106">This makes WIC ideal as a Plug and Play solution for the RAW image formats that digital cameras produce.</span></span> <span data-ttu-id="62d89-107">Tramite WIC, le applicazioni Windows possono ottenere supporto per i nuovi modelli di fotocamera ogni volta che vengono resi disponibili codec aggiornati, idealmente con nuove fotocamere.</span><span class="sxs-lookup"><span data-stu-id="62d89-107">Through WIC, Windows applications can gain support for new camera models whenever updated codecs are made available (ideally in-box with new cameras).</span></span> <span data-ttu-id="62d89-108">Gli autori di codec possono supportare questi scenari implementando interfacce WIC comuni a tutti i tipi di immagine, come descritto in dettaglio in questo documento.</span><span class="sxs-lookup"><span data-stu-id="62d89-108">Codec authors can support these scenarios by implementing WIC interfaces that are common to all image types, as described in more detail in this document.</span></span>

<span data-ttu-id="62d89-109">Attualmente, la maggior parte delle applicazioni consumer mainstream non ha alcuna conoscenza speciale dei formati di immagine RAW e non espone un'interfaccia utente per la modifica delle impostazioni di elaborazione non ELABORAte.</span><span class="sxs-lookup"><span data-stu-id="62d89-109">Today, most mainstream consumer applications have no special knowledge of RAW image formats and do not expose a user interface for adjusting RAW processing settings.</span></span>

<span data-ttu-id="62d89-110">Tuttavia, per supportare applicazioni di imaging specializzate, gli autori di codec RAW devono implementare anche l'interfaccia [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) .</span><span class="sxs-lookup"><span data-stu-id="62d89-110">However, to support specialized imaging applications, RAW codec authors must also implement the [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) interface.</span></span> <span data-ttu-id="62d89-111">Questa interfaccia espone funzionalità speciali per le immagini non ELABORAte, ad esempio la possibilità di apportare modifiche di immagine comuni e di elaborare (sviluppare) immagini non ELABORAte in spazi dei colori di colore rosso-verde-blu (RGB) specificati.</span><span class="sxs-lookup"><span data-stu-id="62d89-111">This interface exposes special features for RAW images, such as the ability to make common image adjustments and to process (develop) RAW images into specified red-green-blue (RGB) color spaces.</span></span>

<span data-ttu-id="62d89-112">Molte altre interfacce WIC sono importanti per l'implementazione da autori di codec non ELABORAti.</span><span class="sxs-lookup"><span data-stu-id="62d89-112">Several other WIC interfaces are important for RAW codec authors to implement.</span></span> <span data-ttu-id="62d89-113">Questi argomenti sono illustrati in modo più dettagliato in questa serie di argomenti.</span><span class="sxs-lookup"><span data-stu-id="62d89-113">These are discussed in more detail in this series of topics.</span></span>

## <a name="related-topics"></a><span data-ttu-id="62d89-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="62d89-114">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="62d89-115">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="62d89-115">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="62d89-116">Panoramica del componente imaging Windows</span><span class="sxs-lookup"><span data-stu-id="62d89-116">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[<span data-ttu-id="62d89-117">Linee guida per WIC per i formati di immagine RAW della fotocamera</span><span class="sxs-lookup"><span data-stu-id="62d89-117">WIC Guidelines for Camera RAW Image Formats</span></span>](-wic-rawguidelines.md)
</dt> <dt>

[<span data-ttu-id="62d89-118">Come scrivere un CODEC WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="62d89-118">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> </dl>

 

 



