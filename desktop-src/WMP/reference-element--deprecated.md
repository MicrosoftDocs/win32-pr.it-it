---
title: Elemento Reference (deprecato)
description: Elemento Reference (deprecato)
ms.assetid: 0a549750-abaa-43bf-8420-8fe00eb6feff
keywords:
- Metafile di Windows Media, elemento Reference
- Metafile, elemento Reference
- Reference-elemento
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6c521b080609bbe51470a2de960481a86e8264c0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298528"
---
# <a name="reference-element-deprecated"></a><span data-ttu-id="0b3e0-106">Elemento Reference (deprecato)</span><span class="sxs-lookup"><span data-stu-id="0b3e0-106">reference Element (deprecated)</span></span>

<span data-ttu-id="0b3e0-107">In questo argomento viene documentata una funzionalità che non viene più utilizzata nella versione corrente dei file di Windows Media.</span><span class="sxs-lookup"><span data-stu-id="0b3e0-107">This topic documents a feature that is no longer used in the current version of Windows Media Metafiles.</span></span>

<span data-ttu-id="0b3e0-108">L'elemento **Reference** contiene un elenco di riferimenti agli URL.</span><span class="sxs-lookup"><span data-stu-id="0b3e0-108">The **reference** element contains a list of references to URLs.</span></span> <span data-ttu-id="0b3e0-109">Ogni elemento nell'elenco ha il formato URL ref *XX*  =  , dove *XX* è un numero intero e *URL* è l'URL di un file di formato ASF (Advanced Systems Format).</span><span class="sxs-lookup"><span data-stu-id="0b3e0-109">Each item in the list has the form Ref *XX* = *URL*, where *XX* is an integer and *URL* is the URL of an Advanced Systems Format (ASF) file.</span></span>

<span data-ttu-id="0b3e0-110">**Sintassi**</span><span class="sxs-lookup"><span data-stu-id="0b3e0-110">**Syntax**</span></span>


```XML
[reference]
RefXX = URL
RefXX = URL
   
<entity type="hellip"/>
```



<span data-ttu-id="0b3e0-111">I numeri interi rappresentati da *XX* devono essere in ordine crescente.</span><span class="sxs-lookup"><span data-stu-id="0b3e0-111">The integers represented by *XX* must be in ascending order.</span></span> <span data-ttu-id="0b3e0-112">Ovvero il valore integer in ogni riga deve essere maggiore di quello della riga precedente.</span><span class="sxs-lookup"><span data-stu-id="0b3e0-112">That is, the integer in each line must be greater than the integer in the preceding line.</span></span>

<span data-ttu-id="0b3e0-113">Quando un programma client legge un elemento di riferimento, tenta di connettersi al file multimediale rappresentato dal primo URL nell'elenco.</span><span class="sxs-lookup"><span data-stu-id="0b3e0-113">When a client program reads a reference element, it attempts to connect to the media file represented by the first URL in the list.</span></span> <span data-ttu-id="0b3e0-114">Se l'operazione ha esito negativo, il programma client tenta di connettersi al file rappresentato dall'URL successivo nell'elenco.</span><span class="sxs-lookup"><span data-stu-id="0b3e0-114">If that fails, the client program attempts to connect to the file represented by the next URL in the list.</span></span> <span data-ttu-id="0b3e0-115">Il programma client continua a scorrere l'elenco fino a quando non riesce a connettersi o raggiunge la fine dell'elenco.</span><span class="sxs-lookup"><span data-stu-id="0b3e0-115">The client program continues down the list until it makes a successful connection or reaches the end of the list.</span></span> <span data-ttu-id="0b3e0-116">Si noti che se il programma client effettua una connessione, non legge alcun URL successivo nell'elenco.</span><span class="sxs-lookup"><span data-stu-id="0b3e0-116">Note that if the client program makes a successful connection, it does not read any of the subsequent URLs in the list.</span></span>

<span data-ttu-id="0b3e0-117">**Codice di esempio**</span><span class="sxs-lookup"><span data-stu-id="0b3e0-117">**Example Code**</span></span>

<span data-ttu-id="0b3e0-118">Nell'esempio seguente il programma client tenterà innanzitutto di connettersi al file rappresentato dall'URL di MMS.</span><span class="sxs-lookup"><span data-stu-id="0b3e0-118">In the following example, the client program would first attempt to connect to the file represented by the mms URL.</span></span> <span data-ttu-id="0b3e0-119">Se l'operazione non è riuscita, il programma client tenterà di connettersi al file rappresentato dall'URL http.</span><span class="sxs-lookup"><span data-stu-id="0b3e0-119">If that failed, the client program would attempt to connect to the file represented by the http URL.</span></span>


```XML
[reference]
Ref01 = mms://example.com/MusicFile.wma
Ref02 = https://example.com/MusicFile.wma

```



## <a name="remarks"></a><span data-ttu-id="0b3e0-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="0b3e0-120">Remarks</span></span>

<span data-ttu-id="0b3e0-121">Il formato di file ASF comprende un'ampia gamma di tipi di supporti, inclusi audio e video.</span><span class="sxs-lookup"><span data-stu-id="0b3e0-121">The ASF file format encompasses a wide variety of media types including audio and video.</span></span> <span data-ttu-id="0b3e0-122">I file ASF usano anche diverse estensioni di file, tra cui WMA e WMV.</span><span class="sxs-lookup"><span data-stu-id="0b3e0-122">ASF files also use several different file name extensions, including .wma and .wmv.</span></span>

<span data-ttu-id="0b3e0-123">I numeri interi rappresentati da *XX* devono essere in ordine crescente.</span><span class="sxs-lookup"><span data-stu-id="0b3e0-123">The integers represented by *XX* must be in ascending order.</span></span> <span data-ttu-id="0b3e0-124">Ovvero il valore integer in ogni riga deve essere maggiore di quello della riga precedente.</span><span class="sxs-lookup"><span data-stu-id="0b3e0-124">That is, the integer in each line must be greater than the integer in the preceding line.</span></span>

<span data-ttu-id="0b3e0-125">Quando un programma client legge un elemento di riferimento, tenta di connettersi al file multimediale rappresentato dal primo URL nell'elenco.</span><span class="sxs-lookup"><span data-stu-id="0b3e0-125">When a client program reads a reference element, it attempts to connect to the media file represented by the first URL in the list.</span></span> <span data-ttu-id="0b3e0-126">Se l'operazione ha esito negativo, il programma client tenta di connettersi al file rappresentato dall'URL successivo nell'elenco.</span><span class="sxs-lookup"><span data-stu-id="0b3e0-126">If that fails, the client program attempts to connect to the file represented by the next URL in the list.</span></span> <span data-ttu-id="0b3e0-127">Il programma client continua a scorrere l'elenco fino a quando non riesce a connettersi o raggiunge la fine dell'elenco.</span><span class="sxs-lookup"><span data-stu-id="0b3e0-127">The client program continues down the list until it makes a successful connection or reaches the end of the list.</span></span> <span data-ttu-id="0b3e0-128">Si noti che se il programma client effettua una connessione, non legge alcun URL successivo nell'elenco.</span><span class="sxs-lookup"><span data-stu-id="0b3e0-128">Note that if the client program makes a successful connection, it does not read any of the subsequent URLs in the list.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0b3e0-129">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0b3e0-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0b3e0-130">**Versioni precedenti dei file di Windows Media (deprecato)**</span><span class="sxs-lookup"><span data-stu-id="0b3e0-130">**Previous Versions of Windows Media Metafiles (deprecated)**</span></span>](previous-versions-of-windows-media-metafiles--deprecated.md)
</dt> </dl>

 

 




