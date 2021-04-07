---
description: Impostazioni dei campi DVINFO nel driver MSDV
ms.assetid: f0723da5-4f53-4f83-a657-ae42815a784e
title: Impostazioni dei campi DVINFO nel driver MSDV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4205a680833b0e2f8c6be2dc4cb65faa60515867
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103746666"
---
# <a name="dvinfo-field-settings-in-the-msdv-driver"></a><span data-ttu-id="da7b6-103">Impostazioni dei campi DVINFO nel driver MSDV</span><span class="sxs-lookup"><span data-stu-id="da7b6-103">DVINFO Field Settings in the MSDV Driver</span></span>

<span data-ttu-id="da7b6-104">Questa sezione descrive il modo in cui il driver MSDV compila la struttura [**DVinfo**](/windows/desktop/api/strmif/ns-strmif-dvinfo) .</span><span class="sxs-lookup"><span data-stu-id="da7b6-104">This section describes how the MSDV driver fills in the [**DVINFO**](/windows/desktop/api/strmif/ns-strmif-dvinfo) structure.</span></span>

<span data-ttu-id="da7b6-105">La `DVINFO` struttura definisce il blocco di formato per le connessioni pin tra Msdv e altri filtri.</span><span class="sxs-lookup"><span data-stu-id="da7b6-105">The `DVINFO` structure defines the format block for pin connections between MSDV and other filters.</span></span> <span data-ttu-id="da7b6-106">Per impostazione predefinita, il filtro della barra di divisione DV viene usato durante l'acquisizione da un dispositivo DV e il filtro Mux DV viene usato durante la trasmissione al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="da7b6-106">By default, the DV Splitter filter is used when capturing from a DV device, and the DV Mux filter is used when transmitting to the device.</span></span> <span data-ttu-id="da7b6-107">Tuttavia, le applicazioni possono fornire filtri personalizzati, quindi è utile comprendere il modo in cui MSDV popola il `DVINFO` blocco di formato.</span><span class="sxs-lookup"><span data-stu-id="da7b6-107">However, applications may provide their own custom filters, so it is useful to understand how MSDV populates the `DVINFO` format block.</span></span>

<span data-ttu-id="da7b6-108">La `DVINFO` struttura contiene le informazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="da7b6-108">The `DVINFO` structure contains the following information:</span></span>

-   <span data-ttu-id="da7b6-109">Due pacchetti di origine audio ausiliari (AAUX), per il primo e il secondo blocco audio.</span><span class="sxs-lookup"><span data-stu-id="da7b6-109">Two audio auxiliary (AAUX) source packs, for the first and second audio blocks.</span></span>
-   <span data-ttu-id="da7b6-110">Due pacchetti di controllo del codice sorgente AAUX, per il primo e il secondo blocco audio.</span><span class="sxs-lookup"><span data-stu-id="da7b6-110">Two AAUX source control packs, for the first and second audio blocks.</span></span>
-   <span data-ttu-id="da7b6-111">Un pacchetto di origine video ausiliario (VAUX).</span><span class="sxs-lookup"><span data-stu-id="da7b6-111">A video auxiliary (VAUX) source pack.</span></span>
-   <span data-ttu-id="da7b6-112">Un pacchetto di controllo del codice sorgente VAUX.</span><span class="sxs-lookup"><span data-stu-id="da7b6-112">A VAUX source control pack.</span></span>

<span data-ttu-id="da7b6-113">Ogni frame in un flusso DV contiene i Pack AAUX e VAUX.</span><span class="sxs-lookup"><span data-stu-id="da7b6-113">Every frame in a DV stream contains AAUX and VAUX packs.</span></span> <span data-ttu-id="da7b6-114">Tuttavia, il `DVINFO` blocco di formato è statico e viene usato solo per stabilire la connessione del PIN.</span><span class="sxs-lookup"><span data-stu-id="da7b6-114">However, the `DVINFO` format block is static, and is only used to establish the pin connection.</span></span> <span data-ttu-id="da7b6-115">Quando il driver MSDV si connette, non esamina i pacchetti AAUX o VAUX nel flusso.</span><span class="sxs-lookup"><span data-stu-id="da7b6-115">When the MSDV driver connects, it does not examine any of the AAUX or VAUX packs in the stream.</span></span> <span data-ttu-id="da7b6-116">USA invece un set di valori predefiniti, in base alle caratteristiche seguenti del dispositivo DV:</span><span class="sxs-lookup"><span data-stu-id="da7b6-116">Instead, it uses a set of default values, based on the following characteristics of the DV device:</span></span>

-   <span data-ttu-id="da7b6-117">Indica se il dispositivo supporta un formato utente (DVCR) o un formato Professional (DVCPRO)</span><span class="sxs-lookup"><span data-stu-id="da7b6-117">Whether the device supports a consumer format (DVCR) or professional format (DVCPRO)</span></span>
-   <span data-ttu-id="da7b6-118">Tipo di segnale</span><span class="sxs-lookup"><span data-stu-id="da7b6-118">The signal type</span></span>
-   <span data-ttu-id="da7b6-119">Indica se il formato è NTSC o PAL.</span><span class="sxs-lookup"><span data-stu-id="da7b6-119">Whether the format is NTSC or PAL.</span></span> <span data-ttu-id="da7b6-120">Se il dispositivo non riporta queste informazioni, MSDV per impostazione predefinita è le impostazioni NTSC.</span><span class="sxs-lookup"><span data-stu-id="da7b6-120">(If the device does not report this information, MSDV defaults to the NTSC settings)</span></span>

<span data-ttu-id="da7b6-121">Una volta avviato il flusso, è responsabilità dei filtri in modalità utente, ad esempio la barra di divisione DV, esaminare il contenuto effettivo di ogni frame DV.</span><span class="sxs-lookup"><span data-stu-id="da7b6-121">Once streaming begins, it is the responsibility of the user-mode filters, such as the DV Splitter, to examine the actual contents of each DV frame.</span></span> <span data-ttu-id="da7b6-122">Poiché le informazioni possono essere modificate dal frame al frame, potrebbe essere necessario eseguire una modifica del formato dinamico per il filtro.</span><span class="sxs-lookup"><span data-stu-id="da7b6-122">Because the information can change from frame to frame, the filter may need to perform a dynamic format change.</span></span> <span data-ttu-id="da7b6-123">Se, ad esempio, la frequenza audio viene modificata, il filtro potrebbe dover rinegoziare il tipo audio.</span><span class="sxs-lookup"><span data-stu-id="da7b6-123">For example, if the audio rate changes, the filter might need to renegotiate the audio type.</span></span>

<span data-ttu-id="da7b6-124">Se si acquisisce un file DV di tipo 1, la `DVINFO` struttura viene scritta nel file come formato di flusso (' strF ').</span><span class="sxs-lookup"><span data-stu-id="da7b6-124">If you capture a type-1 DV file, the `DVINFO` structure is written into the file as the stream format ('strf') chunk.</span></span> <span data-ttu-id="da7b6-125">Questi dati vengono ricavati direttamente dal blocco di formato fornito da MSDV.</span><span class="sxs-lookup"><span data-stu-id="da7b6-125">This data is taken directly from the format block provided by MSDV.</span></span> <span data-ttu-id="da7b6-126">Come indicato, il contenuto effettivo del flusso potrebbe essere diverso.</span><span class="sxs-lookup"><span data-stu-id="da7b6-126">As noted, the actual content of the stream might be different.</span></span> <span data-ttu-id="da7b6-127">È responsabilità dell'applicazione esaminare i Pack AAUX e VAUX in ogni frame.</span><span class="sxs-lookup"><span data-stu-id="da7b6-127">It is the application's responsibility to examine the AAUX and VAUX packs in each frame.</span></span>

<span data-ttu-id="da7b6-128">Negli argomenti seguenti è possibile trovare le tabelle che elencano tutti i campi usati da MSDV.</span><span class="sxs-lookup"><span data-stu-id="da7b6-128">In the following topics, you can find tables listing all of the fields used by MSDV.</span></span>

-   [<span data-ttu-id="da7b6-129">Pacchetto di origine (AS) AAUX</span><span class="sxs-lookup"><span data-stu-id="da7b6-129">AAUX Source (AS) Pack</span></span>](aaux-source--as--pack.md)
-   [<span data-ttu-id="da7b6-130">Pack del controllo del codice sorgente AAUX (ASC)</span><span class="sxs-lookup"><span data-stu-id="da7b6-130">AAUX Source Control (ASC) Pack</span></span>](aaux-source-control--asc--pack.md)
-   [<span data-ttu-id="da7b6-131">Pacchetto di origine (VS) VAUX</span><span class="sxs-lookup"><span data-stu-id="da7b6-131">VAUX Source (VS) Pack</span></span>](vaux-source--vs--pack.md)
-   [<span data-ttu-id="da7b6-132">Pack del controllo del codice sorgente (VSC) di VAUX</span><span class="sxs-lookup"><span data-stu-id="da7b6-132">VAUX Source Control (VSC) Pack</span></span>](vaux-source-control--vsc--pack.md)

<span data-ttu-id="da7b6-133">Quando si leggono queste tabelle, consultare le specifiche seguenti:</span><span class="sxs-lookup"><span data-stu-id="da7b6-133">When reading these tables, please consult the following specifications:</span></span>

-   <span data-ttu-id="da7b6-134">IEC 61834</span><span class="sxs-lookup"><span data-stu-id="da7b6-134">IEC 61834</span></span>
-   <span data-ttu-id="da7b6-135">314M SMPTE</span><span class="sxs-lookup"><span data-stu-id="da7b6-135">SMPTE 314M</span></span>
-   <span data-ttu-id="da7b6-136">SMPTE 370</span><span class="sxs-lookup"><span data-stu-id="da7b6-136">SMPTE 370</span></span>

<span data-ttu-id="da7b6-137">In ogni tabella la prima colonna restituisce il codice del campo, seguito dal numero di bit (tra parentesi).</span><span class="sxs-lookup"><span data-stu-id="da7b6-137">In each table, the first column gives the field code, followed by the number of bits (in parentheses).</span></span> <span data-ttu-id="da7b6-138">Le colonne rimanenti forniscono i valori dei campi.</span><span class="sxs-lookup"><span data-stu-id="da7b6-138">The remaining columns give the field values.</span></span> <span data-ttu-id="da7b6-139">Molti dei campi AAUX e VAUX non sono rilevanti per la connessione pin, nel qual caso MSDV imposta un valore fittizio.</span><span class="sxs-lookup"><span data-stu-id="da7b6-139">Many of the AAUX and VAUX fields are not relevant for the pin connection, in which case MSDV sets a dummy value.</span></span> <span data-ttu-id="da7b6-140">Il valore numerico dell'intero Pack è elencato nella parte inferiore di ogni tabella.</span><span class="sxs-lookup"><span data-stu-id="da7b6-140">The numeric value of the entire pack is listed at the bottom of each table.</span></span>

<span data-ttu-id="da7b6-141">Le note successive a ogni tabella forniscono ulteriori informazioni sui campi selezionati.</span><span class="sxs-lookup"><span data-stu-id="da7b6-141">The notes after each table give more information about selected fields.</span></span> <span data-ttu-id="da7b6-142">Per descrizioni complete, vedere le specifiche.</span><span class="sxs-lookup"><span data-stu-id="da7b6-142">For complete descriptions, refer to the specifications.</span></span> <span data-ttu-id="da7b6-143">Inoltre, alcuni campi non hanno lo stesso significato in SMPTE 314M/SMPTE 370, come avviene in IEC 61834.</span><span class="sxs-lookup"><span data-stu-id="da7b6-143">Also, some fields do not have the same meaning in SMPTE 314M/SMPTE 370 as they do in IEC 61834.</span></span>

> [!Note]  
> <span data-ttu-id="da7b6-144">Attualmente, DirectShow non supporta i formati DVCPRO.</span><span class="sxs-lookup"><span data-stu-id="da7b6-144">Currently, DirectShow does not support DVCPRO formats.</span></span> <span data-ttu-id="da7b6-145">I valori elencati per i formati DVCPRO sono definiti per un uso futuro.</span><span class="sxs-lookup"><span data-stu-id="da7b6-145">The values listed for the DVCPRO formats are defined for future use.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="da7b6-146">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="da7b6-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="da7b6-147">Video digitale in DirectShow</span><span class="sxs-lookup"><span data-stu-id="da7b6-147">Digital Video in DirectShow</span></span>](digital-video-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="da7b6-148">Dati DV nel formato di file AVI</span><span class="sxs-lookup"><span data-stu-id="da7b6-148">DV Data in the AVI File Format</span></span>](dv-data-in-the-avi-file-format.md)
</dt> <dt>

[<span data-ttu-id="da7b6-149">Driver MSDV</span><span class="sxs-lookup"><span data-stu-id="da7b6-149">MSDV Driver</span></span>](msdv-driver.md)
</dt> </dl>

 

 



