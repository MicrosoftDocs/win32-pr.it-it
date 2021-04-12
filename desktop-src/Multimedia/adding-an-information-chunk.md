---
title: Aggiunta di un blocco di informazioni
description: Aggiunta di un blocco di informazioni
ms.assetid: ebba5079-1f67-4236-9260-e36ff72ad51c
keywords:
- capFileSetInfoChunk (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bacb99fb29e4b1882b4f257c428315f42ee3a360
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221574"
---
# <a name="adding-an-information-chunk"></a><span data-ttu-id="7164b-104">Aggiunta di un blocco di informazioni</span><span class="sxs-lookup"><span data-stu-id="7164b-104">Adding an Information Chunk</span></span>

<span data-ttu-id="7164b-105">Se è necessario includere altre informazioni nell'applicazione oltre a audio e video, è possibile creare blocchi di informazioni e inserirli in un file di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="7164b-105">If you need to include other information in your application in addition to audio and video, you can create information chunks and insert them into a capture file.</span></span> <span data-ttu-id="7164b-106">I blocchi di informazioni possono contenere diversi tipi di informazioni, tra cui i dettagli di un avviso di copyright, l'identificazione dell'origine video o informazioni sulla temporizzazione esterna.</span><span class="sxs-lookup"><span data-stu-id="7164b-106">Information chunks can contain several types of information, including the details of a copyright notice, identification of the video source, or external timing information.</span></span> <span data-ttu-id="7164b-107">Nell'esempio seguente vengono archiviate le informazioni sulla temporizzazione esterna di un timecode SMPTE (Society of Motion Picture and Television Engineers) in un blocco di informazioni e il blocco viene aggiunto a un file di acquisizione utilizzando la macro [**capFileSetInfoChunk**](/windows/desktop/api/Vfw/nf-vfw-capfilesetinfochunk) .</span><span class="sxs-lookup"><span data-stu-id="7164b-107">The following example stores external timing information a SMPTE (Society of Motion Picture and Television Engineers) timecode in an information chunk and adds the chunk to a capture file using the [**capFileSetInfoChunk**](/windows/desktop/api/Vfw/nf-vfw-capfilesetinfochunk) macro.</span></span>


```C++
//  This example assumes the application controls 
//  the video source for preroll and postroll. 
CAPINFOCHUNK cic;
// . 
// . 
// . 
cic.fccInfoID = infotypeSMPTE_TIME;
cic.lpData = "00:20:30:12"; 
cic.cbData = strlen (cic.lpData) + 1;
capFileSetInfoChunk (hwndC, &cic); 
 
```



## <a name="related-topics"></a><span data-ttu-id="7164b-108">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7164b-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7164b-109">Uso di acquisizione video</span><span class="sxs-lookup"><span data-stu-id="7164b-109">Using Video Capture</span></span>](using-video-capture.md)
</dt> </dl>

 

 




