---
title: Per configurare Quality-Based VBR
description: Per configurare Quality-Based VBR
ms.assetid: 077a18c5-1895-4241-8c31-5f7caf38b22e
keywords:
- flussi, configurazione di flussi VBR
- flussi, velocità in bit variabile (VBR)
- velocità in bit variabile (VBR), flussi
- VBR (velocità in bit variabile), flussi
- flussi, configurazione di VBR basato sulla qualità
- velocità in bit variabile (VBR), configurazione basata sulla qualità
- VBR (velocità in bit variabile), configurazione basata sulla qualità
- profili, configurazione di VBR basato sulla qualità
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d0b7a6ecb83c7242f82f5626a086c8aba23881f
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/25/2020
ms.locfileid: "103956262"
---
# <a name="to-configure-quality-based-vbr"></a><span data-ttu-id="7f175-111">Per configurare Quality-Based VBR</span><span class="sxs-lookup"><span data-stu-id="7f175-111">To Configure Quality-Based VBR</span></span>

<span data-ttu-id="7f175-112">È possibile usare la codifica di velocità in bit variabile (VBR) basata sulla qualità in un flusso per specificare un livello di qualità che verrà mantenuto per l'intero flusso, indipendentemente dai requisiti di velocità in bit che risultano.</span><span class="sxs-lookup"><span data-stu-id="7f175-112">You can use quality-based variable bit rate (VBR) encoding on a stream to specify a quality level that will be maintained for the entire stream, regardless of the bit-rate requirements that result.</span></span>

<span data-ttu-id="7f175-113">Per i flussi video VBR basati sulla qualità, è necessario specificare un livello di qualità compreso tra 1 e 100, con 100 che rappresentano la qualità più elevata.</span><span class="sxs-lookup"><span data-stu-id="7f175-113">For quality-based VBR video streams, you must specify a quality level from 1 to 100, with 100 representing the highest quality.</span></span> <span data-ttu-id="7f175-114">Al momento sono disponibili solo 30 impostazioni di qualità discrete.</span><span class="sxs-lookup"><span data-stu-id="7f175-114">At present there are only 30 discrete quality settings.</span></span> <span data-ttu-id="7f175-115">I livelli di qualità seguenti equivalgono a impostazioni di qualità discrete: 1, 4, 8, 11, 15, 18, 22, 25, 29, 33, 36, 40, 43, 47, 50, 54, 58, 61, 65, 68, 72, 75, 79, 83, 86, 90, 93, 97, 100.</span><span class="sxs-lookup"><span data-stu-id="7f175-115">The following quality levels equate to discrete quality settings: 1, 4, 8, 11, 15, 18, 22, 25, 29, 33, 36, 40, 43, 47, 50, 54, 58, 61, 65, 68, 72, 75, 79, 83, 86, 90, 93, 97, 100.</span></span> <span data-ttu-id="7f175-116">I numeri tra due valori consecutivi nell'elenco precedente corrispondono alla stessa impostazione di qualità del numero inferiore.</span><span class="sxs-lookup"><span data-stu-id="7f175-116">Numbers between two consecutive values in the preceding list equate to the same quality setting as the lower number.</span></span> <span data-ttu-id="7f175-117">Ad esempio, 1 e 4 sono elencati, quindi 2 e 3 generano entrambe la stessa impostazione di qualità di 1.</span><span class="sxs-lookup"><span data-stu-id="7f175-117">For example, 1 and 4 are listed, so 2 and 3 both result in the same quality setting as 1.</span></span>

<span data-ttu-id="7f175-118">Per i flussi audio, è possibile enumerare le modalità disponibili e recuperare un oggetto di configurazione del flusso.</span><span class="sxs-lookup"><span data-stu-id="7f175-118">For audio streams, you can enumerate the available modes and retrieve a stream configuration object.</span></span> <span data-ttu-id="7f175-119">Per ulteriori informazioni, vedere [per enumerare i formati di codec](to-enumerate-codec-formats.md).</span><span class="sxs-lookup"><span data-stu-id="7f175-119">For more information, see [To Enumerate Codec Formats](to-enumerate-codec-formats.md).</span></span>

<span data-ttu-id="7f175-120">Quando si usa il video VBR basato sulla qualità, è necessario impostare il membro **dwBitrate** della struttura [**WMVIDEOINFOHEADER**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmvideoinfoheader) su un valore positivo.</span><span class="sxs-lookup"><span data-stu-id="7f175-120">When using quality-based VBR video, you must set the **dwBitrate** member of the [**WMVIDEOINFOHEADER**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmvideoinfoheader) structure to a positive value.</span></span> <span data-ttu-id="7f175-121">Questo valore non viene utilizzato dal writer, ma il passaggio a zero o a un numero negativo può causare errori durante la scrittura.</span><span class="sxs-lookup"><span data-stu-id="7f175-121">This value is not used by the writer, but passing zero or a negative number can cause errors when writing.</span></span>

<span data-ttu-id="7f175-122">Per configurare un flusso in un profilo da codificare con VBR basato sulla qualità, seguire questa procedura.</span><span class="sxs-lookup"><span data-stu-id="7f175-122">To configure a stream in a profile to be encoded with quality-based VBR, perform the following steps.</span></span>

1.  <span data-ttu-id="7f175-123">Creare un oggetto di gestione del profilo chiamando la funzione [**WMCreateProfileManager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) .</span><span class="sxs-lookup"><span data-stu-id="7f175-123">Create a profile manager object by calling the [**WMCreateProfileManager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) function.</span></span>
2.  <span data-ttu-id="7f175-124">Aprire un profilo esistente a cui si desidera aggiungere il supporto per VBR.</span><span class="sxs-lookup"><span data-stu-id="7f175-124">Open an existing profile to which you want to add VBR support.</span></span> <span data-ttu-id="7f175-125">Per ulteriori informazioni sull'apertura di profili, vedere [utilizzo dei profili](working-with-profiles.md).</span><span class="sxs-lookup"><span data-stu-id="7f175-125">For more information about opening profiles, see [Working with Profiles](working-with-profiles.md).</span></span>
3.  <span data-ttu-id="7f175-126">Ottenere un oggetto di configurazione del flusso per il flusso che si vuole usare chiamando [**IWMProfile:: GetStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream) o [**IWMProfile:: GetStreamByNumber**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-getstreambynumber).</span><span class="sxs-lookup"><span data-stu-id="7f175-126">Get a stream configuration object for the stream you want to use by calling either [**IWMProfile::GetStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream) or [**IWMProfile::GetStreamByNumber**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-getstreambynumber).</span></span>
4.  <span data-ttu-id="7f175-127">Ottenere un puntatore all'interfaccia [**IWMPropertyVault**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault) dell'oggetto di configurazione del flusso chiamando **IWMStreamConfig:: QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="7f175-127">Get a pointer to the [**IWMPropertyVault**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault) interface of the stream configuration object by calling **IWMStreamConfig::QueryInterface**.</span></span>
5.  <span data-ttu-id="7f175-128">Abilitare VBR per il flusso chiamando [**IWMPropertyVault:: SetProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-setproperty) per la proprietà **g \_ wszVBREnabled** .</span><span class="sxs-lookup"><span data-stu-id="7f175-128">Enable VBR for the stream by calling [**IWMPropertyVault::SetProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-setproperty) for the **g\_wszVBREnabled** property.</span></span>
6.  <span data-ttu-id="7f175-129">Impostare il livello di qualità per il flusso VBR chiamando **IWMPropertyVault:: SetProperty** per la proprietà **g \_ wszVBRQuality** .</span><span class="sxs-lookup"><span data-stu-id="7f175-129">Set the quality level for the VBR stream by calling **IWMPropertyVault::SetProperty** for the **g\_wszVBRQuality** property.</span></span>
7.  <span data-ttu-id="7f175-130">Impostare **g \_ wszVBRBitrateMax** e **g \_ wszVBRBufferWindowMax** su zero con **IWMPropertyVault:: SetProperty**.</span><span class="sxs-lookup"><span data-stu-id="7f175-130">Set **g\_wszVBRBitrateMax** and **g\_wszVBRBufferWindowMax** both to zero with **IWMPropertyVault::SetProperty**.</span></span>
8.  <span data-ttu-id="7f175-131">Salvare le modifiche apportate al flusso chiamando [**IWMProfile:: ReconfigStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-reconfigstream).</span><span class="sxs-lookup"><span data-stu-id="7f175-131">Save the changes made to the stream by calling [**IWMProfile::ReconfigStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-reconfigstream).</span></span>
9.  <span data-ttu-id="7f175-132">Salvare il profilo o passarlo all'oggetto writer e iniziare a scrivere.</span><span class="sxs-lookup"><span data-stu-id="7f175-132">Save the profile, or pass it to the writer object and start writing.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7f175-133">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7f175-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7f175-134">**Configurazione di flussi VBR**</span><span class="sxs-lookup"><span data-stu-id="7f175-134">**Configuring VBR Streams**</span></span>](configuring-vbr-streams.md)
</dt> </dl>

 

 




