---
description: Esempio DMOEnum
ms.assetid: afd7853e-b0ab-42f6-8c2e-c2b0b40d989b
title: Esempio DMOEnum
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c413b7787ba12785758cffed89be15229373643d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104225475"
---
# <a name="dmoenum-sample"></a><span data-ttu-id="d5d53-103">Esempio DMOEnum</span><span class="sxs-lookup"><span data-stu-id="d5d53-103">DMOEnum Sample</span></span>

## <a name="description"></a><span data-ttu-id="d5d53-104">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d5d53-104">Description</span></span>

<span data-ttu-id="d5d53-105">Questa applicazione di esempio enumera tutti gli [oggetti multimediali DirectX](directx-media-objects.md) (DMOS) registrati nel sistema dell'utente e visualizza le relative informazioni.</span><span class="sxs-lookup"><span data-stu-id="d5d53-105">This sample application enumerates all of the [DirectX Media Objects](directx-media-objects.md) (DMOs) registered in the user's system, and displays information about them.</span></span>

<span data-ttu-id="d5d53-106">Nell'esempio vengono utilizzate la funzione [**DMOEnum**](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmoenum) e l'interfaccia [**IEnumDMO**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-ienumdmo) per enumerare DMOS.</span><span class="sxs-lookup"><span data-stu-id="d5d53-106">The sample uses the [**DMOEnum**](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmoenum) function and the [**IEnumDMO**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-ienumdmo) interface to enumerate the DMOs.</span></span> <span data-ttu-id="d5d53-107">Usa l'interfaccia [**IMediaObject**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediaobject) e altre interfacce DMO per recuperare le informazioni su ogni DMO.</span><span class="sxs-lookup"><span data-stu-id="d5d53-107">It uses the [**IMediaObject**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediaobject) interface and other DMO interfaces to retrieve information about each DMO.</span></span>

## <a name="usage"></a><span data-ttu-id="d5d53-108">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="d5d53-108">Usage</span></span>

<span data-ttu-id="d5d53-109">Quando l'applicazione viene avviata, enumera tutti i DMOs installati.</span><span class="sxs-lookup"><span data-stu-id="d5d53-109">When the application launches, it enumerates all of the installed DMOs.</span></span> <span data-ttu-id="d5d53-110">Se si seleziona una categoria DMO specifica, nell'applicazione vengono visualizzati solo i DMOs di tale categoria.</span><span class="sxs-lookup"><span data-stu-id="d5d53-110">If you select a specific DMO category, the application displays only the DMOs in that category.</span></span> <span data-ttu-id="d5d53-111">Per visualizzare le informazioni su un DMO, selezionare DMO dall'elenco.</span><span class="sxs-lookup"><span data-stu-id="d5d53-111">To view information about a DMO, select the DMO from the list.</span></span> <span data-ttu-id="d5d53-112">L'applicazione Visualizza il numero di flussi, i tipi di supporto preferiti, il server DLL per tale DMO e altre informazioni su DMO.</span><span class="sxs-lookup"><span data-stu-id="d5d53-112">The application displays the number of streams, the preferred media types, the DLL server for that DMO, and other information about the DMO.</span></span> <span data-ttu-id="d5d53-113">Per includere o escludere DMOs con chiave, impostare la casella di controllo **Includi DMOS?** .</span><span class="sxs-lookup"><span data-stu-id="d5d53-113">To include or exclude keyed DMOs, toggle the **Include Keyed DMOs?** checkbox.</span></span>

## <a name="downloading-the-sample"></a><span data-ttu-id="d5d53-114">Download dell'esempio</span><span class="sxs-lookup"><span data-stu-id="d5d53-114">Downloading the Sample</span></span>

<span data-ttu-id="d5d53-115">Per scaricare gli esempi di DirectShow SDK, installare la versione più recente del [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="d5d53-115">To download the DirectShow SDK samples, install the latest version of the [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span>

<span data-ttu-id="d5d53-116">Questo esempio viene installato nel percorso seguente: *\[ SDK \] radice* \\ esempi \\ multimediali \\ DirectShow \\ varie \\ DMOEnum.</span><span class="sxs-lookup"><span data-stu-id="d5d53-116">This sample is installed under the following path: *\[SDK Root\]*\\Samples\\Multimedia\\DirectShow\\Misc\\DMOEnum.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d5d53-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d5d53-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d5d53-118">Esempi di DirectShow</span><span class="sxs-lookup"><span data-stu-id="d5d53-118">DirectShow Samples</span></span>](directshow-samples.md)
</dt> </dl>

 

 



