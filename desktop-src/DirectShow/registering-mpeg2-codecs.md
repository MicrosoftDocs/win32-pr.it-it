---
description: Registrazione di codec MPEG2
ms.assetid: f730a7df-af8f-4dce-9bfe-6ee1eca8fd90
title: Registrazione di codec MPEG2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6de007cebdd0a911f6b43f21003ed3ede0bc1723
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124134"
---
# <a name="registering-mpeg2-codecs"></a><span data-ttu-id="6ce51-103">Registrazione di codec MPEG2</span><span class="sxs-lookup"><span data-stu-id="6ce51-103">Registering MPEG2 Codecs</span></span>

<span data-ttu-id="6ce51-104">Questo argomento si applica solo a Windows XP Media Center Edition.</span><span class="sxs-lookup"><span data-stu-id="6ce51-104">This topic applies to Windows XP Media Center Edition only.</span></span>

<span data-ttu-id="6ce51-105">Windows XP Media Center Edition gestisce due chiavi del registro di sistema che utilizza per determinare quale codec utilizzare per riprodurre file audio e video MPEG2.</span><span class="sxs-lookup"><span data-stu-id="6ce51-105">Windows XP Media Center Edition maintains two registry keys that it uses to determine which codec to use to play back MPEG2 video and audio files.</span></span> <span data-ttu-id="6ce51-106">La prima chiave del registro di sistema specifica il codec MPEG2 preferito del produttore del computer e il secondo elenca tutti i codec compatibili con Media Center attualmente installati nel computer.</span><span class="sxs-lookup"><span data-stu-id="6ce51-106">The first registry key specifies the computer manufacturer's preferred MPEG2 codec, and the second lists all of the Media Center compatible codecs that are currently installed on the computer.</span></span> <span data-ttu-id="6ce51-107">Quando Media Center deve riprodurre un file MPEG2, usa il codec preferito del produttore, se ne è stato specificato uno.</span><span class="sxs-lookup"><span data-stu-id="6ce51-107">When Media Center needs to play back an MPEG2 file, it uses the manufacturer's preferred codec, if one is specified.</span></span> <span data-ttu-id="6ce51-108">In caso contrario, viene utilizzato il primo codec compatibile con Media Center elencato nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="6ce51-108">If not, it uses the first Media Center compatible codec listed in the registry.</span></span> <span data-ttu-id="6ce51-109">Se il registro di sistema non specifica codec preferiti o compatibili, Media Center USA il merito standard del filtro DirectShow per scegliere un codec.</span><span class="sxs-lookup"><span data-stu-id="6ce51-109">If the registry specifies no preferred or compatible codecs, Media Center uses the standard DirectShow filter merit to choose a codec.</span></span>

<span data-ttu-id="6ce51-110">Per assicurarsi che Media Center usi sempre un codec MPEG2 compatibile, i produttori di computer Media Center devono specificare il codec MPEG2 preferito nel seguente percorso del registro di sistema:</span><span class="sxs-lookup"><span data-stu-id="6ce51-110">To ensure that Media Center always uses a compatible MPEG2 codec, manufacturers of Media Center computers should specify the preferred MPEG2 codec at the following registry location:</span></span>


```C++
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\Media Center\Service\Video
```



<span data-ttu-id="6ce51-111">I dati della chiave dovrebbero essere i seguenti:</span><span class="sxs-lookup"><span data-stu-id="6ce51-111">The key data should be as follows:</span></span>


```C++
PreferredMPEG2VideoDecoder=REG_SZ "{MPEG2 Video CLSID GUID}"
PreferredMPEG2AudioDecoder=REG_SZ "{MPEG2 Audio CLSID GUID}"
```



<span data-ttu-id="6ce51-112">Il programma di installazione di un codec MPEG2 compatibile con Media Center deve registrare il codec creando due istanze della chiave del registro di sistema seguente, una per il codec video e una per il codec audio:</span><span class="sxs-lookup"><span data-stu-id="6ce51-112">The setup program for a Media Center compatible MPEG2 codec should register the codec by creating two instances of the following registry key—one for the video codec and one for the audio codec:</span></span>


```C++
[HKEY_CLASSES_ROOT\CLSID\{083863F1-70DE-11d0-BD40-00A0C911CE86}\Instance\<Your Codec CLSID here>\Capabilities]
```



<span data-ttu-id="6ce51-113">I dati della chiave dovrebbero essere i seguenti:</span><span class="sxs-lookup"><span data-stu-id="6ce51-113">The key data should be as follows:</span></span>


```C++
"{374ac4df-7c98-4257-b13d-36087dbee458}"=dword:00000001
```



 

 



