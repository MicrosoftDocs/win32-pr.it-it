---
title: Per configurare il VBR vincolato
description: Per configurare il VBR vincolato
ms.assetid: a39e7628-0211-48ad-94e5-5003203f30be
keywords:
- flussi, configurazione di flussi VBR
- flussi, velocità in bit variabile (VBR)
- velocità in bit variabile (VBR), flussi
- VBR (velocità in bit variabile), flussi
- flussi, configurazione di VBR vincolato
- velocità in bit variabile (VBR), configurazione vincolata
- VBR (velocità in bit variabile), configurazione vincolata
- profili, configurazione di VBR vincolato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98d4e2a1bbea1b724fdde1cc820f19caf9dd77be
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/25/2020
ms.locfileid: "104046432"
---
# <a name="to-configure-constrained-vbr"></a><span data-ttu-id="3fd51-111">Per configurare il VBR vincolato</span><span class="sxs-lookup"><span data-stu-id="3fd51-111">To Configure Constrained VBR</span></span>

<span data-ttu-id="3fd51-112">È possibile usare la codifica con velocità in bit variabile (VBR) vincolata in un flusso per specificare una velocità in bit media che verrà mantenuta nel contenuto codificato.</span><span class="sxs-lookup"><span data-stu-id="3fd51-112">You can use constrained variable bit rate (VBR) encoding on a stream to specify an average bit rate that will be maintained in the encoded content.</span></span> <span data-ttu-id="3fd51-113">È inoltre possibile specificare la velocità massima in bit del flusso e la finestra massima del buffer richiesta.</span><span class="sxs-lookup"><span data-stu-id="3fd51-113">You also specify the maximum bit rate of the stream and the maximum required buffer window.</span></span>

<span data-ttu-id="3fd51-114">Non è possibile conoscere la velocità in bit media per un flusso VBR vincolato prima della codifica, ma è possibile usare una stima approssimativa.</span><span class="sxs-lookup"><span data-stu-id="3fd51-114">You cannot know what the average bit rate will be for a constrained VBR stream before encoding, but you can use a rough estimate.</span></span> <span data-ttu-id="3fd51-115">Come regola generale, la velocità in bit massima specificata finirà da due a tre volte la velocità media in bit.</span><span class="sxs-lookup"><span data-stu-id="3fd51-115">As a general rule, the maximum bit rate you specify will end up being two to three times the average bit rate.</span></span>

<span data-ttu-id="3fd51-116">È necessario usare il VBR vincolato insieme alla codifica a due passaggi.</span><span class="sxs-lookup"><span data-stu-id="3fd51-116">Constrained VBR must be used in conjunction with two-pass encoding.</span></span> <span data-ttu-id="3fd51-117">La codifica a due passaggi non è impostata nel profilo.</span><span class="sxs-lookup"><span data-stu-id="3fd51-117">Two-pass encoding is not set in the profile.</span></span> <span data-ttu-id="3fd51-118">È necessario configurare il writer per eseguire un passaggio di pre-elaborazione prima di scrivere il flusso.</span><span class="sxs-lookup"><span data-stu-id="3fd51-118">You must configure the writer to perform a preprocessing pass before writing the stream.</span></span> <span data-ttu-id="3fd51-119">Per ulteriori informazioni sull'utilizzo della codifica a due passaggi, vedere [utilizzo della codifica Two-Pass](using-two-pass-encoding.md).</span><span class="sxs-lookup"><span data-stu-id="3fd51-119">For more information about using two-pass encoding, see [Using Two-Pass Encoding](using-two-pass-encoding.md).</span></span>

<span data-ttu-id="3fd51-120">Per configurare un flusso in un profilo per l'uso della codifica VBR vincolata, seguire questa procedura.</span><span class="sxs-lookup"><span data-stu-id="3fd51-120">To configure a stream in a profile to use constrained VBR encoding, perform the following steps.</span></span>

1.  <span data-ttu-id="3fd51-121">Creare un oggetto di gestione del profilo chiamando la funzione [**WMCreateProfileManager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) .</span><span class="sxs-lookup"><span data-stu-id="3fd51-121">Create a profile manager object by calling the [**WMCreateProfileManager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) function.</span></span>
2.  <span data-ttu-id="3fd51-122">Aprire un profilo esistente a cui si desidera aggiungere il supporto per VBR.</span><span class="sxs-lookup"><span data-stu-id="3fd51-122">Open an existing profile to which you want to add VBR support.</span></span> <span data-ttu-id="3fd51-123">Per ulteriori informazioni sull'apertura di profili, vedere [utilizzo dei profili](working-with-profiles.md).</span><span class="sxs-lookup"><span data-stu-id="3fd51-123">For more information about opening profiles, see [Working with Profiles](working-with-profiles.md).</span></span>
3.  <span data-ttu-id="3fd51-124">Ottenere un oggetto di configurazione del flusso per il flusso che si vuole usare chiamando [**IWMProfile:: GetStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream) o [**IWMProfile:: GetStreamByNumber**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-getstreambynumber).</span><span class="sxs-lookup"><span data-stu-id="3fd51-124">Get a stream configuration object for the stream you want to use by calling either [**IWMProfile::GetStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream) or [**IWMProfile::GetStreamByNumber**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-getstreambynumber).</span></span>
4.  <span data-ttu-id="3fd51-125">Ottenere un puntatore all'interfaccia [**IWMPropertyVault**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault) dell'oggetto di configurazione del flusso chiamando **IWMStreamConfig:: QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="3fd51-125">Get a pointer to the [**IWMPropertyVault**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault) interface of the stream configuration object by calling **IWMStreamConfig::QueryInterface**.</span></span>
5.  <span data-ttu-id="3fd51-126">Abilitare la codifica VBR per il flusso chiamando [**IWMPropertyVault:: SetProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-setproperty) per la proprietà **g \_ wszVBREnabled** .</span><span class="sxs-lookup"><span data-stu-id="3fd51-126">Enable VBR encoding for the stream by calling [**IWMPropertyVault::SetProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-setproperty) for the **g\_wszVBREnabled** property.</span></span>
6.  <span data-ttu-id="3fd51-127">Usare le chiamate a **IWMPropertyVault:: SetProperty** per impostare i valori massimi desiderati per le proprietà **g \_ wszVBRBitrateMax** e **g \_ wszVBRBufferWindowMax** .</span><span class="sxs-lookup"><span data-stu-id="3fd51-127">Use calls to **IWMPropertyVault::SetProperty** to set the desired maximum values for the **g\_wszVBRBitrateMax** and **g\_wszVBRBufferWindowMax** properties.</span></span>
7.  <span data-ttu-id="3fd51-128">Salvare le modifiche apportate al flusso chiamando [**IWMProfile:: ReconfigStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-reconfigstream).</span><span class="sxs-lookup"><span data-stu-id="3fd51-128">Save the changes made to the stream by calling [**IWMProfile::ReconfigStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-reconfigstream).</span></span>
8.  <span data-ttu-id="3fd51-129">Salvare il profilo o passarlo all'oggetto writer.</span><span class="sxs-lookup"><span data-stu-id="3fd51-129">Save the profile, or pass it to the writer object.</span></span>
9.  <span data-ttu-id="3fd51-130">Configurare il writer per eseguire un passaggio di pre-elaborazione.</span><span class="sxs-lookup"><span data-stu-id="3fd51-130">Configure the writer to perform a preprocessing pass.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3fd51-131">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3fd51-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3fd51-132">**Configurazione di flussi VBR**</span><span class="sxs-lookup"><span data-stu-id="3fd51-132">**Configuring VBR Streams**</span></span>](configuring-vbr-streams.md)
</dt> </dl>

 

 




