---
title: Per configurare il VBR non vincolato
description: Per configurare il VBR non vincolato
ms.assetid: 69ef951f-d08b-401b-a285-2ffdf43ea35d
keywords:
- flussi, configurazione di flussi VBR
- flussi, velocità in bit variabile (VBR)
- velocità in bit variabile (VBR), flussi
- VBR (velocità in bit variabile), flussi
- flussi, configurazione di VBR non vincolato
- velocità in bit variabile (VBR), configurazione non vincolata
- VBR (velocità in bit variabile), configurazione non vincolata
- profili, configurazione di VBR non vincolato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b24c022c79bb38414ab201db11abd0cf260dfafe
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/25/2020
ms.locfileid: "104117450"
---
# <a name="to-configure-unconstrained-vbr"></a><span data-ttu-id="ce75e-111">Per configurare il VBR non vincolato</span><span class="sxs-lookup"><span data-stu-id="ce75e-111">To Configure Unconstrained VBR</span></span>

<span data-ttu-id="ce75e-112">È possibile utilizzare la codifica della velocità in bit variabile (VBR) non vincolata in un flusso per specificare una velocità in bit media che verrà mantenuta nel contenuto codificato.</span><span class="sxs-lookup"><span data-stu-id="ce75e-112">You can use unconstrained variable bit rate (VBR) encoding on a stream to specify an average bit rate that will be maintained in the encoded content.</span></span> <span data-ttu-id="ce75e-113">Il VBR non vincolato è diverso da quello normale in quanto la varianza nella velocità in bit nel flusso può essere maggiore.</span><span class="sxs-lookup"><span data-stu-id="ce75e-113">Unconstrained VBR differs from normal CBR in that the variance in bit rate throughout the stream can be greater.</span></span>

<span data-ttu-id="ce75e-114">La velocità in bit del flusso, impostata con [**IWMStreamConfig:: bitrate**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setbitrate), viene utilizzata come velocità in bit media desiderata.</span><span class="sxs-lookup"><span data-stu-id="ce75e-114">The bit rate of the stream, set with [**IWMStreamConfig::SetBitrate**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setbitrate), is used as the desired average bit rate.</span></span> <span data-ttu-id="ce75e-115">Quando la codifica del flusso è completa, è possibile usare [**IWMPropertyVault:: GetPropertyByName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-getpropertybyname) per recuperare due proprietà aggiuntive: **g \_ wszVBRPeak** e **g \_ wszBufferAverage**.</span><span class="sxs-lookup"><span data-stu-id="ce75e-115">When encoding of the stream is complete, you can use [**IWMPropertyVault::GetPropertyByName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-getpropertybyname) to retrieve two additional properties: **g\_wszVBRPeak** and **g\_wszBufferAverage**.</span></span> <span data-ttu-id="ce75e-116">Queste proprietà descrivono rispettivamente la velocità in bit massima del contenuto codificato e la finestra media del buffer del contenuto.</span><span class="sxs-lookup"><span data-stu-id="ce75e-116">These properties describe the peak bit rate of the encoded content and the average buffer window of the content, respectively.</span></span>

<span data-ttu-id="ce75e-117">È necessario usare il VBR non vincolato insieme alla codifica a due passaggi.</span><span class="sxs-lookup"><span data-stu-id="ce75e-117">Unconstrained VBR must be used in conjunction with two-pass encoding.</span></span> <span data-ttu-id="ce75e-118">La codifica a due passaggi non è impostata nel profilo.</span><span class="sxs-lookup"><span data-stu-id="ce75e-118">Two-pass encoding is not set in the profile.</span></span> <span data-ttu-id="ce75e-119">È necessario configurare il writer per eseguire un passaggio di pre-elaborazione prima di scrivere il flusso.</span><span class="sxs-lookup"><span data-stu-id="ce75e-119">You must configure the writer to perform a preprocessing pass before writing the stream.</span></span> <span data-ttu-id="ce75e-120">Per ulteriori informazioni sull'utilizzo della codifica a due passaggi, vedere [utilizzo della codifica Two-Pass](using-two-pass-encoding.md).</span><span class="sxs-lookup"><span data-stu-id="ce75e-120">For more information about using two-pass encoding, see [Using Two-Pass Encoding](using-two-pass-encoding.md).</span></span>

<span data-ttu-id="ce75e-121">Per configurare un flusso in un profilo da codificare con VBR non vincolato, seguire questa procedura:</span><span class="sxs-lookup"><span data-stu-id="ce75e-121">To configure a stream in a profile to be encoded with unconstrained VBR, perform the following steps:</span></span>

1.  <span data-ttu-id="ce75e-122">Creare un oggetto di gestione del profilo chiamando la funzione [**WMCreateProfileManager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) .</span><span class="sxs-lookup"><span data-stu-id="ce75e-122">Create a profile manager object by calling the [**WMCreateProfileManager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) function.</span></span>
2.  <span data-ttu-id="ce75e-123">Aprire un profilo esistente a cui si desidera aggiungere il supporto per VBR.</span><span class="sxs-lookup"><span data-stu-id="ce75e-123">Open an existing profile to which you want to add VBR support.</span></span> <span data-ttu-id="ce75e-124">Per ulteriori informazioni sull'apertura di profili, vedere [utilizzo dei profili](working-with-profiles.md).</span><span class="sxs-lookup"><span data-stu-id="ce75e-124">For more information about opening profiles, see [Working with Profiles](working-with-profiles.md).</span></span>
3.  <span data-ttu-id="ce75e-125">Ottenere un oggetto di configurazione del flusso per il flusso che si vuole usare chiamando [**IWMProfile:: GetStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream) o [**IWMProfile:: GetStreamByNumber**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-getstreambynumber).</span><span class="sxs-lookup"><span data-stu-id="ce75e-125">Get a stream configuration object for the stream you want to use by calling either [**IWMProfile::GetStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream) or [**IWMProfile::GetStreamByNumber**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-getstreambynumber).</span></span>
4.  <span data-ttu-id="ce75e-126">Ottenere un puntatore all'interfaccia [**IWMPropertyVault**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault) dell'oggetto di configurazione del flusso chiamando **IWMStreamConfig:: QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="ce75e-126">Get a pointer to the [**IWMPropertyVault**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault) interface of the stream configuration object by calling **IWMStreamConfig::QueryInterface**.</span></span>
5.  <span data-ttu-id="ce75e-127">Abilitare la codifica VBR per il flusso chiamando [**IWMPropertyVault:: SetProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-setproperty) per la proprietà **g \_ wszVBREnabled** .</span><span class="sxs-lookup"><span data-stu-id="ce75e-127">Enable VBR encoding for the stream by calling [**IWMPropertyVault::SetProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-setproperty) for the **g\_wszVBREnabled** property.</span></span>
6.  <span data-ttu-id="ce75e-128">Impostare **g \_ wszVBRBitrateMax** e **g \_ wszVBRBufferWindowMax** su zero con **IWMPropertyVault:: SetProperty**.</span><span class="sxs-lookup"><span data-stu-id="ce75e-128">Set **g\_wszVBRBitrateMax** and **g\_wszVBRBufferWindowMax** both to zero with **IWMPropertyVault::SetProperty**.</span></span>
7.  <span data-ttu-id="ce75e-129">Salvare le modifiche apportate al flusso chiamando [**IWMProfile:: ReconfigStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-reconfigstream).</span><span class="sxs-lookup"><span data-stu-id="ce75e-129">Save the changes made to the stream by calling [**IWMProfile::ReconfigStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-reconfigstream).</span></span>
8.  <span data-ttu-id="ce75e-130">Salvare il profilo o passarlo all'oggetto writer.</span><span class="sxs-lookup"><span data-stu-id="ce75e-130">Save the profile, or pass it to the writer object.</span></span>
9.  <span data-ttu-id="ce75e-131">Configurare il writer per eseguire un passaggio di pre-elaborazione.</span><span class="sxs-lookup"><span data-stu-id="ce75e-131">Configure the writer to perform a preprocessing pass.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ce75e-132">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ce75e-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ce75e-133">**Configurazione di flussi VBR**</span><span class="sxs-lookup"><span data-stu-id="ce75e-133">**Configuring VBR Streams**</span></span>](configuring-vbr-streams.md)
</dt> </dl>

 

 




