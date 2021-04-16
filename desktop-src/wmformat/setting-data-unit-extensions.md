---
title: Impostazione delle estensioni delle unità dati
description: Impostazione delle estensioni delle unità dati
ms.assetid: 28328c9e-8590-48b8-92b6-1c0475978246
keywords:
- ASF (Advanced Systems Format), estensioni di unità dati
- ASF (formato di sistemi avanzati), estensioni di unità dati
- estensioni unità dati, impostazione
- flussi, estensioni di unità dati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 822a05a6e6bcbb9f0101d32eed05f2b6c5c68dc8
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/25/2020
ms.locfileid: "104516663"
---
# <a name="setting-data-unit-extensions"></a><span data-ttu-id="e6101-107">Impostazione delle estensioni delle unità dati</span><span class="sxs-lookup"><span data-stu-id="e6101-107">Setting Data Unit Extensions</span></span>

<span data-ttu-id="e6101-108">Alcuni flussi sono configurati per l'uso di estensioni di unità dati per associare dati supplementari a singoli esempi.</span><span class="sxs-lookup"><span data-stu-id="e6101-108">Some streams are configured to use data unit extensions to associate supplementary data with individual samples.</span></span> <span data-ttu-id="e6101-109">Per ulteriori informazioni sugli esempi estesi, vedere [estensioni di unità dati](data-unit-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="e6101-109">For more information about extended samples, see [Data Unit Extensions](data-unit-extensions.md).</span></span>

<span data-ttu-id="e6101-110">Per la maggior parte dei sistemi di estensione dell'unità dati è necessaria un'estensione per ogni esempio nel flusso.</span><span class="sxs-lookup"><span data-stu-id="e6101-110">Most data unit extension systems require an extension on every sample in the stream.</span></span> <span data-ttu-id="e6101-111">Se non si specifica un'estensione della dimensione corretta, il writer rifiuterà l'esempio.</span><span class="sxs-lookup"><span data-stu-id="e6101-111">If you do not provide an extension of the correct size, the writer will reject the sample.</span></span>

<span data-ttu-id="e6101-112">Per aggiungere dati estesi a un esempio, usare il metodo [**INSSBuffer3:: SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty) .</span><span class="sxs-lookup"><span data-stu-id="e6101-112">To add extended data to a sample, use the [**INSSBuffer3::SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty) method.</span></span> <span data-ttu-id="e6101-113">Per ottenere informazioni sulle estensioni dell'unità dati configurate in un flusso, è possibile usare i metodi [**IWMStreamConfig2:: GetDataUnitExtensionCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-getdataunitextensioncount) e [**IWMStreamConfig2:: GetDataUnitExtension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-getdataunitextension) .</span><span class="sxs-lookup"><span data-stu-id="e6101-113">You can get information about the data unit extensions configured on a stream by using the [**IWMStreamConfig2::GetDataUnitExtensionCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-getdataunitextensioncount) and [**IWMStreamConfig2::GetDataUnitExtension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-getdataunitextension) methods.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e6101-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e6101-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e6101-115">**Configurazione di estensioni delle unità dati**</span><span class="sxs-lookup"><span data-stu-id="e6101-115">**Configuring Data Unit Extensions**</span></span>](configuring-data-unit-extensions.md)
</dt> <dt>

[<span data-ttu-id="e6101-116">**Scrittura di file ASF**</span><span class="sxs-lookup"><span data-stu-id="e6101-116">**Writing ASF Files**</span></span>](writing-asf-files.md)
</dt> </dl>

 

 




