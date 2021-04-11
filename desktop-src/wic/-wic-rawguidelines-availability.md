---
description: Disponibilità di codec e supporto della piattaforma
ms.assetid: 6b3d09c9-e91f-4c62-92f7-c2643e51987f
title: Disponibilità di codec e supporto della piattaforma
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dcc485c5f8db9ff7883263cd614578705eccd3fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232879"
---
# <a name="codec-availability-and-platform-support"></a><span data-ttu-id="8a5c1-103">Disponibilità di codec e supporto della piattaforma</span><span class="sxs-lookup"><span data-stu-id="8a5c1-103">Codec Availability and Platform Support</span></span>

<span data-ttu-id="8a5c1-104">È consigliabile che i fornitori di fotocamere includano codec non ELABORAti di Windows Imaging Component (WIC) nella distribuzione del software con nuove fotocamere e che il codec aggiornato venga installato con l'installazione del software fornitore predefinita Windows 7, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="8a5c1-104">Microsoft recommends that camera vendors include updated RAW Windows Imaging Component (WIC) codecs in the software distribution with new cameras and that the updated codec be installed with the default vendor software installation Windows 7, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="8a5c1-105">I fornitori di fotocamere devono inoltre fornire il codec WIC più recente come download dai rispettivi siti di supporto tecnico.</span><span class="sxs-lookup"><span data-stu-id="8a5c1-105">Camera vendors should also provide the latest WIC codec as a download from their support sites.</span></span>

## <a name="codec-discovery"></a><span data-ttu-id="8a5c1-106">Individuazione codec</span><span class="sxs-lookup"><span data-stu-id="8a5c1-106">Codec Discovery</span></span>

<span data-ttu-id="8a5c1-107">Microsoft sta effettuando le seguenti operazioni per consentire agli utenti di fare riferimento ai siti Web dei fornitori per i download di codec:</span><span class="sxs-lookup"><span data-stu-id="8a5c1-107">Microsoft is doing the following to help point users to vendors' Web sites for codec downloads:</span></span>

-   <span data-ttu-id="8a5c1-108">In Esplora risorse, se un utente fa doppio clic su un file non riconosciuto (il caso predefinito quando un file non elaborato si trova nel computer, ma il codec non è ancora installato), una finestra di dialogo indica che il file non è stato riconosciuto e chiede se l'utente vuole trovare un programma che riconosce il file.</span><span class="sxs-lookup"><span data-stu-id="8a5c1-108">In Windows Explorer, if a user double-clicks a file that is not recognized (the default case when a RAW file is on the computer, but the codec is not installed yet), a dialog box reports that the file is not recognized and asks whether the user wants to find a program that understands the file.</span></span> <span data-ttu-id="8a5c1-109">Microsoft gestisce un servizio di reindirizzamento esistente per l'invio di utenti ai siti Web dei fornitori in grado di fornire il programma per la comprensione del file.</span><span class="sxs-lookup"><span data-stu-id="8a5c1-109">Microsoft maintains an existing redirection service to forward users to vendors' Web sites that can supply the program to understand the file.</span></span> <span data-ttu-id="8a5c1-110">Questa funzionalità è disponibile in Windows XP e in Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="8a5c1-110">This facility exists in Windows XP and in Windows Vista.</span></span>
-   <span data-ttu-id="8a5c1-111">La raccolta foto di Windows, la raccolta foto di Windows Live e il Visualizzatore foto di Windows 7 riconoscono un set di estensioni di file come file non ELABORAti.</span><span class="sxs-lookup"><span data-stu-id="8a5c1-111">The Windows Photo Gallery, Windows Live Photo Gallery, and the Windows 7 Photo Viewer recognize a set of file extensions as RAW files.</span></span> <span data-ttu-id="8a5c1-112">Se i file di tale set si trovano nelle cartelle esaminate da una di queste applicazioni e non è ancora installato un codec per il file, viene visualizzata una finestra di dialogo, come descritto nel paragrafo precedente.</span><span class="sxs-lookup"><span data-stu-id="8a5c1-112">If files from that set are found in folders that any of these applications are looking at, and a codec for the file is not already installed, then a dialog box appears, as described in the preceding paragraph.</span></span>

<span data-ttu-id="8a5c1-113">Per ulteriori informazioni sull'individuazione dei codec, vedere disponibilità di codec e supporto della piattaforma.</span><span class="sxs-lookup"><span data-stu-id="8a5c1-113">For more information about codec discovery, see Codec Availability and Platform Support.</span></span>

## <a name="windows-xp-platform-support"></a><span data-ttu-id="8a5c1-114">Supporto della piattaforma Windows XP</span><span class="sxs-lookup"><span data-stu-id="8a5c1-114">Windows XP Platform Support</span></span>

<span data-ttu-id="8a5c1-115">Microsoft ha rilasciato Windows XP SP3 con WIC e un programma di installazione WIC autonomo per Windows XP SP2.</span><span class="sxs-lookup"><span data-stu-id="8a5c1-115">Microsoft has released Windows XP SP3 with WIC, and a standalone WIC installer for Windows XP SP2.</span></span> <span data-ttu-id="8a5c1-116">Questi utilizzano codec WIC per abilitare il supporto per anteprime e anteprime su tali piattaforme.</span><span class="sxs-lookup"><span data-stu-id="8a5c1-116">These use WIC codecs to enable support for thumbnails and previews on those platforms.</span></span> <span data-ttu-id="8a5c1-117">È pertanto importante che il download e l'installazione di codec siano supportati e testati in Windows 7, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="8a5c1-117">Therefore, it is important that codec download and installation be supported and tested on the Windows 7, Windows Vista, and Windows XP.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8a5c1-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8a5c1-118">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="8a5c1-119">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="8a5c1-119">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="8a5c1-120">Panoramica del componente imaging Windows</span><span class="sxs-lookup"><span data-stu-id="8a5c1-120">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[<span data-ttu-id="8a5c1-121">Linee guida per WIC per i formati di immagine RAW della fotocamera</span><span class="sxs-lookup"><span data-stu-id="8a5c1-121">WIC Guidelines for Camera RAW Image Formats</span></span>](-wic-rawguidelines.md)
</dt> <dt>

[<span data-ttu-id="8a5c1-122">Come scrivere un CODEC WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="8a5c1-122">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> </dl>

 

 



