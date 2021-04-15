---
description: Esempio di filtro del parser PSI
ms.assetid: e815d57f-25e5-4a71-8f40-e7abec0db236
title: Esempio di filtro del parser PSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1099375d2dbabf9ee6c8e891b0a1780bebbb599d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104569315"
---
# <a name="psi-parser-filter-sample"></a><span data-ttu-id="62305-103">Esempio di filtro del parser PSI</span><span class="sxs-lookup"><span data-stu-id="62305-103">PSI Parser Filter Sample</span></span>

## <a name="description"></a><span data-ttu-id="62305-104">Descrizione</span><span class="sxs-lookup"><span data-stu-id="62305-104">Description</span></span>

<span data-ttu-id="62305-105">Il filtro del parser PSI riceve informazioni specifiche del programma da un flusso di trasporto MPEG-2 ed estrae le informazioni sul programma dalla tabella di associazione di programma (PAT) e dalle tabelle della mappa dei programmi (PMT).</span><span class="sxs-lookup"><span data-stu-id="62305-105">The PSI Parser filter receives Program Specific Information (PSI) from an MPEG-2 transport stream and extracts program information from the Program Association Table (PAT) and Program Map Tables (PMT).</span></span> <span data-ttu-id="62305-106">Queste informazioni consentono a un'applicazione di configurare il Demultiplexer MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="62305-106">This information enables an application to configure the MPEG-2 Demultiplexer.</span></span> <span data-ttu-id="62305-107">Il filtro supporta un'interfaccia personalizzata, [**IMpeg2PsiParser**](impeg2psiparser.md), per il recupero delle informazioni psi.</span><span class="sxs-lookup"><span data-stu-id="62305-107">The filter supports a custom interface, [**IMpeg2PsiParser**](impeg2psiparser.md), for retrieving the PSI information.</span></span>

<span data-ttu-id="62305-108">Questo filtro è progettato per i dispositivi MPEG-2, ad esempio i camcorder IEEE 1394 MPEG-2 e i dispositivi D-VHS.</span><span class="sxs-lookup"><span data-stu-id="62305-108">This filter is designed for MPEG-2 devices, such as IEEE 1394 MPEG-2 camcorders and D-VHS devices.</span></span> <span data-ttu-id="62305-109">Per ulteriori informazioni, vedere il [driver MSTape](mstape-driver.md) .</span><span class="sxs-lookup"><span data-stu-id="62305-109">See [MSTape Driver](mstape-driver.md) for more information.</span></span> <span data-ttu-id="62305-110">Per ottenere informazioni sul programma, le origini broadcast della televisione digitale devono usare un filtro TIF.</span><span class="sxs-lookup"><span data-stu-id="62305-110">Digital television broadcast sources should use a TIF filter to get program information.</span></span>

## <a name="usage"></a><span data-ttu-id="62305-111">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="62305-111">Usage</span></span>

<span data-ttu-id="62305-112">È possibile testare il filtro del parser PSI in GraphEdit come segue:</span><span class="sxs-lookup"><span data-stu-id="62305-112">You can test the PSI Parser filter in GraphEdit as follows:</span></span>

1.  <span data-ttu-id="62305-113">Avviare GraphEdit.</span><span class="sxs-lookup"><span data-stu-id="62305-113">Launch GraphEdit.</span></span>
2.  <span data-ttu-id="62305-114">Inserire un'origine del trasporto MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="62305-114">Insert an MPEG-2 transport source.</span></span> <span data-ttu-id="62305-115">I camcorder MPEG-2 e i dispositivi D-VHS vengono visualizzati come "dispositivo unità secondaria nastro Microsoft AV/C" nella categoria origini acquisizione video.</span><span class="sxs-lookup"><span data-stu-id="62305-115">MPEG-2 camcorders and D-VHS devices appear as "Microsoft AV/C Tape Subunit Device" in the Video Capture Sources category.</span></span>
3.  <span data-ttu-id="62305-116">Connettere il filtro di origine al filtro MPEG-2 Demultiplexer.</span><span class="sxs-lookup"><span data-stu-id="62305-116">Connect the source filter to the MPEG-2 Demultiplexer filter.</span></span>
4.  <span data-ttu-id="62305-117">Usare la pagina delle proprietà in Demux per creare un pin di output con un tipo di supporto "MPEG-2 PSI".</span><span class="sxs-lookup"><span data-stu-id="62305-117">Use the property page on the demux to create an output pin with an "MPEG-2 PSI" media type.</span></span> <span data-ttu-id="62305-118">Questo pin fornirà le sezioni PAT e PMT.</span><span class="sxs-lookup"><span data-stu-id="62305-118">This pin will deliver the PAT and PMT sections.</span></span>
5.  <span data-ttu-id="62305-119">Utilizzare la pagina delle proprietà Demux per eseguire il mapping del PID 0x00 al pin di output.</span><span class="sxs-lookup"><span data-stu-id="62305-119">Use the demux property page to map PID 0x00 to the output pin.</span></span> <span data-ttu-id="62305-120">Impostare il tipo di contenuto su "MPEG2 PSI sections".</span><span class="sxs-lookup"><span data-stu-id="62305-120">Set the content type to "MPEG2 PSI Sections".</span></span>
6.  <span data-ttu-id="62305-121">Connettere il pin di output demux al parser PSI, come illustrato nella figura seguente.</span><span class="sxs-lookup"><span data-stu-id="62305-121">Connect the demux output pin to PSI Parser, as shown in the following diagram.</span></span>

    ![grafico del filtro del parser PSI](images/psi-parser.png)

7.  <span data-ttu-id="62305-123">Eseguire il grafo per inviare i dati PSI al filtro del parser PSI.</span><span class="sxs-lookup"><span data-stu-id="62305-123">Run the graph, in order to feed PSI data to the PSI Parser filter.</span></span> <span data-ttu-id="62305-124">Quando il filtro decodifica le sezioni PAT, esegue automaticamente il mapping dei PID PMT allo stesso pin di output in Demux, in modo che riceva le sezioni PMT.</span><span class="sxs-lookup"><span data-stu-id="62305-124">As the filter decodes the PAT sections, it automatically maps the PMT PIDs to the same output pin on the demux, so that it receives the PMT sections.</span></span>
8.  <span data-ttu-id="62305-125">Usare la pagina delle proprietà del parser PSI per selezionare un numero di programma.</span><span class="sxs-lookup"><span data-stu-id="62305-125">Use the PSI Parser property page to select a program number.</span></span> <span data-ttu-id="62305-126">Nell'elenco dei flussi elementari della pagina delle proprietà vengono visualizzati il PID e il tipo di flusso associati a ogni flusso elementare nel programma selezionato.</span><span class="sxs-lookup"><span data-stu-id="62305-126">The elementary stream list in the property page will show the PID and stream type associated with each elementary stream in the selected program.</span></span> <span data-ttu-id="62305-127">La pagina delle proprietà è progettata per riconoscere i tipi di flusso definiti in ISO/IEC 13818-1.</span><span class="sxs-lookup"><span data-stu-id="62305-127">The property page is designed to recognize stream types defined in ISO/IEC 13818-1.</span></span>
9.  <span data-ttu-id="62305-128">Immettere il numero PID audio nella casella di modifica **PID audio** e il numero PID video nella casella di modifica **PID video** .</span><span class="sxs-lookup"><span data-stu-id="62305-128">Enter the audio PID number in the **Audio PID** edit box, and the video PID number in the **Video PID** edit box.</span></span>
10. <span data-ttu-id="62305-129">Fare clic sul pulsante **Visualizza programma** .</span><span class="sxs-lookup"><span data-stu-id="62305-129">Click the **View Program** button.</span></span> <span data-ttu-id="62305-130">Il parser PSI configurerà i pin di output in Demux in modo che corrispondano alle informazioni sul flusso di programma e eseguano il rendering dei pin.</span><span class="sxs-lookup"><span data-stu-id="62305-130">The PSI Parser will configure the output pins on the demux to match the program stream information and render the pins.</span></span>

> [!Note]  
> <span data-ttu-id="62305-131">Viene fornita la pagina delle proprietà del parser PSI per semplificare i test e fornire codice di esempio per la configurazione del Demultiplexer MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="62305-131">The PSI Parser property page is provided to make testing easier, and to provide sample code that configures the MPEG-2 Demultiplexer.</span></span> <span data-ttu-id="62305-132">Non è consigliabile utilizzare le applicazioni.</span><span class="sxs-lookup"><span data-stu-id="62305-132">It is not recommended for applications to use.</span></span> <span data-ttu-id="62305-133">Le applicazioni devono configurare demux a livello di codice.</span><span class="sxs-lookup"><span data-stu-id="62305-133">Applications should configure the demux programmatically.</span></span>

 

<span data-ttu-id="62305-134">Per usare il filtro del parser PSI in un'applicazione, iniziare compilando il grafico di filtro dall'origine MPEG-2 al demux MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="62305-134">To use the PSI Parser filter in an application, start by building the filter graph from the MPEG-2 source to the MPEG-2 demux.</span></span> <span data-ttu-id="62305-135">Il codice per questo passaggio non è illustrato in questo articolo, perché la configurazione esatta del grafo dipende dall'origine.</span><span class="sxs-lookup"><span data-stu-id="62305-135">Code for this step is not shown here, because the exact graph configuration will depend on the source.</span></span>

<span data-ttu-id="62305-136">Creare quindi un pin di output nel Demux per i dati PSI.</span><span class="sxs-lookup"><span data-stu-id="62305-136">Next, create an output pin on the demux for the PSI data.</span></span> <span data-ttu-id="62305-137">Map PID 0x00, che è riservato per le sezioni PAT, a questo pin, come illustrato nel codice seguente:</span><span class="sxs-lookup"><span data-stu-id="62305-137">Map PID 0x00, which is reserved for PAT sections, to this pin, as shown in the following code:</span></span>


```C++
// Set the media type to MPEG-2 table sections.
AM_MEDIA_TYPE mt;
ZeroMemory(&mt, sizeof(AM_MEDIA_TYPE));
mt.majortype = KSDATAFORMAT_TYPE_MPEG2_SECTIONS;

// Create the pin.
IPin *pPsiPin;
hr = pDemux->CreateOutputPin(&mt, L"PSI", &pPsiPin);
if (SUCCEEDED(hr))
{
    // Map to PID 0.
    ULONG Pid = 0x00;
    hr = pPid->MapPID(1, &Pid, MEDIA_MPEG2_PSI);
}
```



<span data-ttu-id="62305-138">Per ulteriori informazioni, vedere [utilizzo di MPEG-2 Demultiplexer](using-the-mpeg-2-demultiplexer.md).</span><span class="sxs-lookup"><span data-stu-id="62305-138">For more information, see [Using the MPEG-2 Demultiplexer](using-the-mpeg-2-demultiplexer.md).</span></span>

<span data-ttu-id="62305-139">Aggiungere il filtro del parser PSI al grafo e connetterlo al pin di output in demux.</span><span class="sxs-lookup"><span data-stu-id="62305-139">Add the PSI Parser filter to the graph and connect it to the output pin on the demux.</span></span> <span data-ttu-id="62305-140">Eseguire una query sul parser PSI per l'interfaccia [**IMpeg2PsiParser**](impeg2psiparser.md) .</span><span class="sxs-lookup"><span data-stu-id="62305-140">Query the PSI Parser for the [**IMpeg2PsiParser**](impeg2psiparser.md) interface.</span></span> <span data-ttu-id="62305-141">A questo punto, eseguire il grafo e \_ attendere \_ gli eventi di modifica del programma EC, che segnalano una nuova sezione Pat o PMT.</span><span class="sxs-lookup"><span data-stu-id="62305-141">Now run the graph and wait for EC\_PROGRAM\_CHANGED events, which signal a new PAT or PMT section.</span></span> <span data-ttu-id="62305-142">Questo evento è un evento personalizzato definito dal filtro del parser PSI.</span><span class="sxs-lookup"><span data-stu-id="62305-142">This event is a custom event defined by the PSI Parser filter.</span></span> <span data-ttu-id="62305-143">Quando si riceve un \_ \_ evento di modifica del programma EC, è possibile ottenere le informazioni PSI disponibili chiamando i metodi **IMpeg2PsiParser** .</span><span class="sxs-lookup"><span data-stu-id="62305-143">When you receive an EC\_PROGRAM\_CHANGED event, you can get the available PSI information by calling **IMpeg2PsiParser** methods.</span></span> <span data-ttu-id="62305-144">In questa sezione vengono descritti i metodi necessari più di frequente.</span><span class="sxs-lookup"><span data-stu-id="62305-144">This section describes the methods you will need most often.</span></span>

<span data-ttu-id="62305-145">Per ottenere il numero di programmi, usare il metodo [**IMpeg2PsiParser:: GetCountOfPrograms**](impeg2psiparser-getcountofprograms.md) :</span><span class="sxs-lookup"><span data-stu-id="62305-145">To get the number of programs, use the [**IMpeg2PsiParser::GetCountOfPrograms**](impeg2psiparser-getcountofprograms.md) method:</span></span>


```C++
int NumProgs = 0;
hr = pPsi->GetCountOfPrograms(&NumProgs);
```



<span data-ttu-id="62305-146">Per ottenere il numero di programma per un programma specifico, usare il metodo [**IMpeg2PsiParser:: GetRecordProgramNumber**](impeg2psiparser-getrecordprogramnumber.md) :</span><span class="sxs-lookup"><span data-stu-id="62305-146">To get the program number for a specific program, use the [**IMpeg2PsiParser::GetRecordProgramNumber**](impeg2psiparser-getrecordprogramnumber.md) method:</span></span>


```C++
WORD ProgNum = 0;
for (int i = 0; i < NumProgs; i++)
{
    hr = pPsi->GetRecordProgramNumber(i, &ProgNum);
    ...
}
```



<span data-ttu-id="62305-147">Il numero di programma viene usato per ottenere le voci PMT per i singoli programmi.</span><span class="sxs-lookup"><span data-stu-id="62305-147">The program number is used to obtain the PMT entries for individual programs.</span></span> <span data-ttu-id="62305-148">Per ottenere il numero di flussi elementari in un programma, usare il metodo [**GetCountOfElementaryStreams**](impeg2psiparser-getcountofelementarystreams.md) :</span><span class="sxs-lookup"><span data-stu-id="62305-148">To get the number of elementary streams in a program, use the [**GetCountOfElementaryStreams**](impeg2psiparser-getcountofelementarystreams.md) method:</span></span>


```C++
WORD cElemStreams = 0;
hr = pPsi->GetCountOfElementaryStreams(ProgNum, &cElemStreams);
```



<span data-ttu-id="62305-149">Per ogni flusso elementare, il metodo [**IMpeg2PsiParser:: GetRecordElementaryPid**](/previous-versions/windows/desktop/legacy/dd376623(v=vs.85)) restituisce il PID e il metodo [**IMpeg2PsiParser:: GetRecordStreamType**](/previous-versions/windows/desktop/legacy/dd376626(v=vs.85)) restituisce il tipo di flusso:</span><span class="sxs-lookup"><span data-stu-id="62305-149">For each elementary stream, the [**IMpeg2PsiParser::GetRecordElementaryPid**](/previous-versions/windows/desktop/legacy/dd376623(v=vs.85)) method returns the PID, and the [**IMpeg2PsiParser::GetRecordStreamType**](/previous-versions/windows/desktop/legacy/dd376626(v=vs.85)) method returns the stream type:</span></span>


```C++
BYTE ESType = 0;
WORD ESPid = 0;
for (WORD j = 0; j < cElemStreams; j++)
{
    hr = pPsi->GetRecordElementaryPid(ProgNum, j, &ESPid);
    hr = pPsi->GetRecordStreamType(ProgNum, j, &ESType);
}
```



<span data-ttu-id="62305-150">Il PID e il tipo di flusso consentono di configurare nuovi PIN di output in MPEG-2 Demultiplexer.</span><span class="sxs-lookup"><span data-stu-id="62305-150">The PID and the stream type enable you to configure new output pins on the MPEG-2 Demultiplexer.</span></span> <span data-ttu-id="62305-151">Questo potrebbe richiedere una certa conoscenza dell'origine originale.</span><span class="sxs-lookup"><span data-stu-id="62305-151">This may require some knowledge of the original source.</span></span> <span data-ttu-id="62305-152">Ad esempio, ISO/IEC 13818-1 definisce i tipi di flusso 0x80 tramite 0xFF come "utente privato", ma altri standard basati su MPEG-2 possono assegnare altri significati a questi tipi.</span><span class="sxs-lookup"><span data-stu-id="62305-152">For example, ISO/IEC 13818-1 defines stream types 0x80 through 0xFF as "user private," but other standards that are based on MPEG-2 may assign other meanings to these types.</span></span>

<span data-ttu-id="62305-153">Il Demultiplexer MPEG-2 può creare nuovi PIN e nuovi mapping PID durante l'esecuzione del grafo, ma è necessario arrestare il grafo per la connessione dei pin.</span><span class="sxs-lookup"><span data-stu-id="62305-153">The MPEG-2 Demultiplexer can create new pins and new PID mappings while the graph is running, but you must stop the graph to connect pins.</span></span>

## <a name="downloading-the-sample"></a><span data-ttu-id="62305-154">Download dell'esempio</span><span class="sxs-lookup"><span data-stu-id="62305-154">Downloading the Sample</span></span>

<span data-ttu-id="62305-155">Per scaricare gli esempi di DirectShow SDK, installare la versione più recente del [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="62305-155">To download the DirectShow SDK samples, install the latest version of the [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span>

<span data-ttu-id="62305-156">Questo esempio viene installato nel percorso seguente: esempi *\[ radice \] SDK* \\ \\ \\ filtri DirectShow multimediali \\ \\ PSIParser.</span><span class="sxs-lookup"><span data-stu-id="62305-156">This sample is installed under the following path: *\[SDK Root\]*\\Samples\\Multimedia\\DirectShow\\Filters\\PSIParser.</span></span>

## <a name="related-topics"></a><span data-ttu-id="62305-157">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="62305-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="62305-158">Esempi di DirectShow</span><span class="sxs-lookup"><span data-stu-id="62305-158">DirectShow Samples</span></span>](directshow-samples.md)
</dt> <dt>

[<span data-ttu-id="62305-159">**Interfaccia IMpeg2PsiParser**</span><span class="sxs-lookup"><span data-stu-id="62305-159">**IMpeg2PsiParser Interface**</span></span>](impeg2psiparser.md)
</dt> </dl>

 

 
