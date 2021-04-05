---
title: Per eseguire ricerche in base al tempo tramite il Reader asincrono
description: Per eseguire ricerche in base al tempo tramite il Reader asincrono
ms.assetid: 731b0a6e-1472-45a7-998c-e395be86036f
keywords:
- Formato Advanced Systems (ASF), ricerca per ora
- ASF (Advanced Systems Format), ricerca per ora
- ASF (Advanced Systems Format), Reader asincroni
- ASF (formato avanzato dei sistemi), Reader asincroni
- lettori asincroni, ricerca per ora
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06f3e24c04d75d762aef6bac498d4b4c8dfa9552
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "103723566"
---
# <a name="to-seek-by-time-using-the-asynchronous-reader"></a><span data-ttu-id="f5edd-108">Per eseguire ricerche in base al tempo tramite il Reader asincrono</span><span class="sxs-lookup"><span data-stu-id="f5edd-108">To Seek By Time Using the Asynchronous Reader</span></span>

<span data-ttu-id="f5edd-109">Se si desidera eseguire la ricerca di un'ora di presentazione specifica in un file ASF, il file deve essere configurato correttamente.</span><span class="sxs-lookup"><span data-stu-id="f5edd-109">If you want to seek to a specific presentation time in an ASF file, the file must be properly configured.</span></span> <span data-ttu-id="f5edd-110">Per impostazione predefinita, è possibile cercare solo nei file audio, ma è necessario indicizzare i file video prima di cercare.</span><span class="sxs-lookup"><span data-stu-id="f5edd-110">You can seek in audio only files by default, but video files need to be indexed before seeking.</span></span> <span data-ttu-id="f5edd-111">Se non si è certi della modalità di creazione di un file, è possibile controllare l' \_ attributo g wszWMSeekable nell'intestazione del file chiamando [**IWMHeaderInfo:: GetAttributeByName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getattributebyname).</span><span class="sxs-lookup"><span data-stu-id="f5edd-111">If you are not sure about how a file has been created, you can check the g\_wszWMSeekable attribute in the header of the file by calling [**IWMHeaderInfo::GetAttributeByName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getattributebyname).</span></span>

<span data-ttu-id="f5edd-112">Per cercare i dati in un file ASF in base all'ora di presentazione utilizzando il lettore asincrono, chiamare [**IWMReader:: Start**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-start), passando il tempo e la durata desiderati della parte del file che si desidera leggere rispettivamente come *cnsStart* e *cnsDuration* .</span><span class="sxs-lookup"><span data-stu-id="f5edd-112">To seek to data in an ASF file by presentation time using the asynchronous reader, call [**IWMReader::Start**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-start), passing the desired time and duration of the part of the file you want to read as *cnsStart* and *cnsDuration* respectively.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f5edd-113">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f5edd-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f5edd-114">**Interfaccia IWMReader**</span><span class="sxs-lookup"><span data-stu-id="f5edd-114">**IWMReader Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader)
</dt> <dt>

[<span data-ttu-id="f5edd-115">**Lettura di file con il lettore asincrono**</span><span class="sxs-lookup"><span data-stu-id="f5edd-115">**Reading Files with the Asynchronous Reader**</span></span>](reading-files-with-the-asynchronous-reader.md)
</dt> <dt>

[<span data-ttu-id="f5edd-116">**Lettura dei metadati durante la riproduzione**</span><span class="sxs-lookup"><span data-stu-id="f5edd-116">**Reading Metadata at Playback**</span></span>](reading-metadata-at-playback.md)
</dt> <dt>

[<span data-ttu-id="f5edd-117">**Operazioni con gli indici**</span><span class="sxs-lookup"><span data-stu-id="f5edd-117">**Working with Indexes**</span></span>](working-with-indexes.md)
</dt> </dl>

 

 




