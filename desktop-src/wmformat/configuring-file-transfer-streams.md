---
title: Configurazione di flussi di trasferimento di file
description: Configurazione di flussi di trasferimento di file
ms.assetid: faed54ae-9e80-492a-9602-e726bdb3b54a
keywords:
- flussi, configurazione di flussi di trasferimento di file
- codec, configurazione di flussi di trasferimento di file
- flussi di trasferimento di file
- flussi, estensioni di unità dati
- codec, estensioni di unità dati
- estensioni unità dati, flussi di trasferimento file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75fac7d2270da82f1f9e82ed9123611ae608dd3c
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104046345"
---
# <a name="configuring-file-transfer-streams"></a><span data-ttu-id="dcd03-109">Configurazione di flussi di trasferimento di file</span><span class="sxs-lookup"><span data-stu-id="dcd03-109">Configuring File Transfer Streams</span></span>

<span data-ttu-id="dcd03-110">Per i flussi di trasferimento di file non è necessaria alcuna impostazione speciale nella struttura del [**\_ \_ tipo di supporto WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) .</span><span class="sxs-lookup"><span data-stu-id="dcd03-110">File transfer streams do not require any special settings in the [**WM\_MEDIA\_TYPE**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) structure.</span></span> <span data-ttu-id="dcd03-111">Per l'associazione di un nome file a ogni esempio, è necessario disporre di un'estensione di unità dati.</span><span class="sxs-lookup"><span data-stu-id="dcd03-111">They do require a data unit extension to associate a file name with each sample.</span></span> <span data-ttu-id="dcd03-112">Per inviare un nome con esempi di trasferimento di file, è necessario implementare un sistema di estensione dell'unità dati per il flusso.</span><span class="sxs-lookup"><span data-stu-id="dcd03-112">To send a name with file transfer samples, you must implement a data unit extension system for the stream.</span></span>

<span data-ttu-id="dcd03-113">Per impostare un'estensione di unità dati per il flusso, seguire questa procedura:</span><span class="sxs-lookup"><span data-stu-id="dcd03-113">To set a data unit extension for the stream, perform the following steps:</span></span>

1.  <span data-ttu-id="dcd03-114">Ottenere un puntatore all'interfaccia [**IWMStreamConfig2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig2) dell'oggetto di configurazione del flusso chiamando **IWMStreamConfig:: QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="dcd03-114">Obtain a pointer to the [**IWMStreamConfig2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig2) interface of the stream configuration object by calling **IWMStreamConfig::QueryInterface**.</span></span>
2.  <span data-ttu-id="dcd03-115">Aggiungere un'estensione per le unità dati per il flusso chiamando [**IWMStreamConfig2:: AddDataUnitExtension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-adddataunitextension) come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="dcd03-115">Add a data unit extension for the stream by calling [**IWMStreamConfig2::AddDataUnitExtension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-adddataunitextension) as follows:</span></span>
    ```C++
    hr = pStreamConfig2->AddDataUnitExtension(CLSID_WMTPropertyFileName,
                                              -1, NULL, 0);
    ```

    

## <a name="related-topics"></a><span data-ttu-id="dcd03-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="dcd03-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dcd03-117">**Configurazione comune a tutti i flussi**</span><span class="sxs-lookup"><span data-stu-id="dcd03-117">**Configuration Common to All Streams**</span></span>](configuration-common-to-all-streams.md)
</dt> <dt>

[<span data-ttu-id="dcd03-118">**Configurazione di tipi di flusso arbitrari**</span><span class="sxs-lookup"><span data-stu-id="dcd03-118">**Configuring Arbitrary Stream Types**</span></span>](configuring-arbitrary-stream-types.md)
</dt> <dt>

[<span data-ttu-id="dcd03-119">**Flussi di file**</span><span class="sxs-lookup"><span data-stu-id="dcd03-119">**File Streams**</span></span>](file-streams.md)
</dt> </dl>

 

 




