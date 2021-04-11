---
description: Vantaggi dello streaming multimediale
ms.assetid: 01020ad5-430d-4b4d-8de3-bcc81270e132
title: Vantaggi dello streaming multimediale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd907d9b8e91cb61709479a2d600323d6d420958
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "104132158"
---
# <a name="advantages-of-multimedia-streaming"></a><span data-ttu-id="1148a-103">Vantaggi dello streaming multimediale</span><span class="sxs-lookup"><span data-stu-id="1148a-103">Advantages of Multimedia Streaming</span></span>

> [!Note]  
> <span data-ttu-id="1148a-104">Queste API sono deprecate.</span><span class="sxs-lookup"><span data-stu-id="1148a-104">These APIs are deprecated.</span></span> <span data-ttu-id="1148a-105">Le applicazioni devono usare il filtro [**grabber di esempio**](sample-grabber-filter.md) o implementare un filtro personalizzato per ottenere i dati da un grafico filtro DirectShow.</span><span class="sxs-lookup"><span data-stu-id="1148a-105">Applications should use the [**Sample Grabber**](sample-grabber-filter.md) filter or implement a custom filter to get data from a DirectShow filter graph.</span></span>

 

<span data-ttu-id="1148a-106">Quando gli sviluppatori usano lo streaming multimediale nelle proprie applicazioni, riduce notevolmente la quantità di programmazione specifica del formato necessario.</span><span class="sxs-lookup"><span data-stu-id="1148a-106">When developers use multimedia streaming in their applications, it greatly reduces the amount of format-specific programming needed.</span></span> <span data-ttu-id="1148a-107">In genere, un'applicazione che deve ottenere i dati multimediali da un file o da un'origine hardware deve conoscere tutte le informazioni sul formato dei dati e sul dispositivo hardware.</span><span class="sxs-lookup"><span data-stu-id="1148a-107">Typically, an application that must obtain media data from a file or hardware source must know everything about the data format and the hardware device.</span></span> <span data-ttu-id="1148a-108">L'applicazione deve gestire la connessione, il trasferimento dei dati, qualsiasi conversione di dati necessaria e l'archiviazione di file o il rendering dei dati effettivi.</span><span class="sxs-lookup"><span data-stu-id="1148a-108">The application must handle the connection, transfer of data, any necessary data conversion, and the actual data rendering or file storage.</span></span> <span data-ttu-id="1148a-109">Poiché ogni formato e dispositivo è leggermente diverso, questo processo è spesso complesso e ingombrante.</span><span class="sxs-lookup"><span data-stu-id="1148a-109">Because each format and device is slightly different, this process is often complex and cumbersome.</span></span> <span data-ttu-id="1148a-110">Il flusso multimediale, d'altra parte, negozia automaticamente il trasferimento e la conversione dei dati dall'origine all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="1148a-110">Multimedia streaming, on the other hand, automatically negotiates the transfer and conversion of data from the source to the application.</span></span> <span data-ttu-id="1148a-111">Le interfacce di flusso offrono un metodo uniforme e prevedibile di accesso ai dati e controllo, che consente a un'applicazione di riprodurre i dati, indipendentemente dall'origine o dal formato originale.</span><span class="sxs-lookup"><span data-stu-id="1148a-111">The streaming interfaces provide a uniform and predictable method of data access and control, which makes it easy for an application to play back the data, regardless of its original source or format.</span></span>

<span data-ttu-id="1148a-112">I passaggi seguenti illustrano come implementare lo streaming, dal dispositivo hardware alla riproduzione di cui è stato eseguito il rendering.</span><span class="sxs-lookup"><span data-stu-id="1148a-112">The following steps show how to implement streaming, from hardware device to rendered playback.</span></span>

1.  <span data-ttu-id="1148a-113">Un'origine di dati video, ad esempio DirectShow, espone le interfacce di streaming.</span><span class="sxs-lookup"><span data-stu-id="1148a-113">A source of video data, such as DirectShow, exposes the streaming interfaces.</span></span>
2.  <span data-ttu-id="1148a-114">Lo sviluppatore di applicazioni usa le interfacce di streaming multimediali per gestire la conversione del formato dati.</span><span class="sxs-lookup"><span data-stu-id="1148a-114">The application developer uses the multimedia streaming interfaces to handle data format conversion.</span></span>
3.  <span data-ttu-id="1148a-115">Lo sviluppatore di applicazioni utilizza le interfacce DirectDraw per eseguire il rendering dei dati risultanti.</span><span class="sxs-lookup"><span data-stu-id="1148a-115">The application developer uses the DirectDraw interfaces to render the resulting data.</span></span>

<span data-ttu-id="1148a-116">La specifica per i flussi multimediali comprende diverse interfacce. ogni interfaccia include metodi che controllano un determinato aspetto del processo di streaming o gestiscono un determinato tipo di dati.</span><span class="sxs-lookup"><span data-stu-id="1148a-116">The specification for multimedia streams comprises several interfaces; each interface includes methods that control a certain aspect of the streaming process or handle a certain type of data.</span></span> <span data-ttu-id="1148a-117">Per ulteriori informazioni, vedere l' [elenco delle interfacce di streaming multimediali](list-of-multimedia-streaming-interfaces.md) .</span><span class="sxs-lookup"><span data-stu-id="1148a-117">See [List of Multimedia Streaming Interfaces](list-of-multimedia-streaming-interfaces.md) for additional information.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1148a-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1148a-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1148a-119">Informazioni sull'architettura di streaming multimediale</span><span class="sxs-lookup"><span data-stu-id="1148a-119">About the Multimedia Streaming Architecture</span></span>](about-the-multimedia-streaming-architecture.md)
</dt> </dl>

 

 



