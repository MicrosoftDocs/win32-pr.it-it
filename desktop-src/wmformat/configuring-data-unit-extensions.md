---
title: Configurazione di estensioni delle unità dati
description: Configurazione di estensioni delle unità dati
ms.assetid: 5dc0a596-68ae-409a-9abc-15ca507d6ec7
keywords:
- flussi, configurazione di estensioni di unità dati
- flussi, estensioni di unità dati
- estensioni unità dati, configurazione
- profili, estensioni di unità dati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc7e6794b95128d180bc3922f9bf03a15a2749df
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/21/2020
ms.locfileid: "103724045"
---
# <a name="configuring-data-unit-extensions"></a><span data-ttu-id="0296e-107">Configurazione di estensioni delle unità dati</span><span class="sxs-lookup"><span data-stu-id="0296e-107">Configuring Data Unit Extensions</span></span>

<span data-ttu-id="0296e-108">Gli esempi scritti nei file ASF possono contenere informazioni aggiuntive oltre agli esempi di supporti.</span><span class="sxs-lookup"><span data-stu-id="0296e-108">Samples written to ASF files can contain additional information apart from the media samples themselves.</span></span> <span data-ttu-id="0296e-109">Queste informazioni vengono incluse utilizzando le estensioni di unità dati.</span><span class="sxs-lookup"><span data-stu-id="0296e-109">This information is included using data unit extensions.</span></span> <span data-ttu-id="0296e-110">Per ulteriori informazioni sulle estensioni dell'unità dati, vedere [estensioni di unità dati](data-unit-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="0296e-110">For more information about data unit extensions, see [Data Unit Extensions](data-unit-extensions.md).</span></span>

<span data-ttu-id="0296e-111">Per usare le estensioni dell'unità dati, è necessario configurare il flusso nel profilo per accettarle.</span><span class="sxs-lookup"><span data-stu-id="0296e-111">To use data unit extensions, you must configure the stream in the profile to accept them.</span></span> <span data-ttu-id="0296e-112">Per configurare un'estensione di unità dati per un flusso, seguire questa procedura.</span><span class="sxs-lookup"><span data-stu-id="0296e-112">To configure a data unit extension for a stream, perform the following steps.</span></span>

1.  <span data-ttu-id="0296e-113">Ottenere un puntatore all'interfaccia [**IWMStreamConfig2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig2) chiamando il metodo **QueryInterface** di [**IWMStreamConfig**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig).</span><span class="sxs-lookup"><span data-stu-id="0296e-113">Obtain a pointer to the [**IWMStreamConfig2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig2) interface by calling the **QueryInterface** method of [**IWMStreamConfig**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig).</span></span>
2.  <span data-ttu-id="0296e-114">Chiamare [**IWMStreamConfig2:: AddDataUnitExtension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-adddataunitextension) per registrare un tipo di estensione di unità dati per il flusso.</span><span class="sxs-lookup"><span data-stu-id="0296e-114">Call [**IWMStreamConfig2::AddDataUnitExtension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-adddataunitextension) to register a type of data unit extension for the stream.</span></span>

<span data-ttu-id="0296e-115">È possibile esaminare tutti i tipi di estensione dell'unità dati attualmente registrati per un flusso chiamando [**IWMStreamConfig2:: GetDataUnitExtensionCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-getdataunitextensioncount) per recuperare il numero di tipi di estensione di unità dati registrate.</span><span class="sxs-lookup"><span data-stu-id="0296e-115">You can examine all of the data unit extension types currently registered for a stream by calling [**IWMStreamConfig2::GetDataUnitExtensionCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-getdataunitextensioncount) to retrieve the number of registered data unit extension types.</span></span> <span data-ttu-id="0296e-116">È quindi possibile scorrere in ciclo tutti i tipi usando le chiamate a [**IWMStreamConfig2:: GetDataUnitExtension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-getdataunitextension) per ognuno di essi.</span><span class="sxs-lookup"><span data-stu-id="0296e-116">Then you can loop through all of the types using calls to [**IWMStreamConfig2::GetDataUnitExtension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-getdataunitextension) for each.</span></span>

<span data-ttu-id="0296e-117">Alle estensioni delle unità dati viene assegnata una dimensione se configurata per un flusso.</span><span class="sxs-lookup"><span data-stu-id="0296e-117">Data unit extensions are assigned a size when configured for a stream.</span></span> <span data-ttu-id="0296e-118">Molti sistemi di estensione di unità dati utilizzano dati di dimensioni costanti (in genere una struttura).</span><span class="sxs-lookup"><span data-stu-id="0296e-118">Many data unit extension systems use data that is a constant size (usually a structure).</span></span> <span data-ttu-id="0296e-119">Tuttavia, è anche possibile configurare le estensioni dell'unità dati in modo che siano di dimensioni variabili impostando la dimensione su 0xFFFF.</span><span class="sxs-lookup"><span data-stu-id="0296e-119">However, you can also configure your data unit extensions to be of variable size by setting the size to 0xFFFF.</span></span> <span data-ttu-id="0296e-120">Ogni estensione dell'unità dati assegnata in fase di codifica può quindi avere dimensioni comprese tra 1 byte e 65534 byte.</span><span class="sxs-lookup"><span data-stu-id="0296e-120">Each data unit extension assigned at encoding time can then be of any size between 1 byte and 65534 bytes.</span></span> <span data-ttu-id="0296e-121">Le estensioni di unità dati di dimensioni variabili sono denominate anche estensioni di unità dati dinamiche.</span><span class="sxs-lookup"><span data-stu-id="0296e-121">Variably sized data unit extensions are also called dynamic data unit extensions.</span></span>

<span data-ttu-id="0296e-122">Il vantaggio dell'utilizzo delle estensioni di unità dati dinamiche è che è possibile alleghi i dati di estensione in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="0296e-122">The advantage of using dynamic data unit extensions is that you can attach extension data as needed.</span></span> <span data-ttu-id="0296e-123">Se si definisce un'estensione di unità dati con una dimensione impostata, ogni esempio per il flusso deve contenere dati di estensione di tale dimensione, anche se non sono presenti dati per alcuni esempi.</span><span class="sxs-lookup"><span data-stu-id="0296e-123">If you define a data unit extension with a set size, every sample for the stream must contain extension data of that size, even if you have no data for some samples.</span></span> <span data-ttu-id="0296e-124">Con le estensioni dell'unità dati dinamica è possibile omettere le estensioni dell'unità dati da alcuni esempi, per risparmiare spazio e ridurre i requisiti di larghezza di banda.</span><span class="sxs-lookup"><span data-stu-id="0296e-124">With dynamic data unit extensions, you can omit data unit extensions from some samples, which saves space and reduces bandwidth requirements.</span></span> <span data-ttu-id="0296e-125">Tuttavia, se le estensioni dell'unità dati sono di dimensioni variabili, l'oggetto di lettura non è in grado di verificare i dati di estensione ricevuti in base a una dimensione statica.</span><span class="sxs-lookup"><span data-stu-id="0296e-125">However, if data unit extensions are of variable size, the reading object cannot verify the received extension data against a static size.</span></span> <span data-ttu-id="0296e-126">È necessario verificare che i dati dell'estensione ricevuti siano validi e non la distorsione dannosa del flusso di bit.</span><span class="sxs-lookup"><span data-stu-id="0296e-126">You must verify that the extension data that you receive is valid, and not malicious distortion of the bit stream.</span></span>

<span data-ttu-id="0296e-127">Le singole estensioni di unità dati devono essere impostate per gli esempi tramite il metodo [**INSSBuffer3:: SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty) .</span><span class="sxs-lookup"><span data-stu-id="0296e-127">Individual data unit extensions must be set on samples by using the [**INSSBuffer3::SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty) method.</span></span> <span data-ttu-id="0296e-128">Per altre informazioni, vedere [Setting Data Unit Extensions](setting-data-unit-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="0296e-128">For more information, see [Setting Data Unit Extensions](setting-data-unit-extensions.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="0296e-129">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0296e-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0296e-130">**Configurazione di flussi**</span><span class="sxs-lookup"><span data-stu-id="0296e-130">**Configuring Streams**</span></span>](configuring-streams.md)
</dt> </dl>

 

 




