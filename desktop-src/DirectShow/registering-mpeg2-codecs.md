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
# <a name="registering-mpeg2-codecs"></a>Registrazione di codec MPEG2

Questo argomento si applica solo a Windows XP Media Center Edition.

Windows XP Media Center Edition gestisce due chiavi del registro di sistema che utilizza per determinare quale codec utilizzare per riprodurre file audio e video MPEG2. La prima chiave del registro di sistema specifica il codec MPEG2 preferito del produttore del computer e il secondo elenca tutti i codec compatibili con Media Center attualmente installati nel computer. Quando Media Center deve riprodurre un file MPEG2, usa il codec preferito del produttore, se ne è stato specificato uno. In caso contrario, viene utilizzato il primo codec compatibile con Media Center elencato nel registro di sistema. Se il registro di sistema non specifica codec preferiti o compatibili, Media Center USA il merito standard del filtro DirectShow per scegliere un codec.

Per assicurarsi che Media Center usi sempre un codec MPEG2 compatibile, i produttori di computer Media Center devono specificare il codec MPEG2 preferito nel seguente percorso del registro di sistema:


```C++
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\Media Center\Service\Video
```



I dati della chiave dovrebbero essere i seguenti:


```C++
PreferredMPEG2VideoDecoder=REG_SZ "{MPEG2 Video CLSID GUID}"
PreferredMPEG2AudioDecoder=REG_SZ "{MPEG2 Audio CLSID GUID}"
```



Il programma di installazione di un codec MPEG2 compatibile con Media Center deve registrare il codec creando due istanze della chiave del registro di sistema seguente, una per il codec video e una per il codec audio:


```C++
[HKEY_CLASSES_ROOT\CLSID\{083863F1-70DE-11d0-BD40-00A0C911CE86}\Instance\<Your Codec CLSID here>\Capabilities]
```



I dati della chiave dovrebbero essere i seguenti:


```C++
"{374ac4df-7c98-4257-b13d-36087dbee458}"=dword:00000001
```



 

 



