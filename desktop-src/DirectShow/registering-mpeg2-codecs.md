---
description: Registrazione di codec MPEG2
ms.assetid: f730a7df-af8f-4dce-9bfe-6ee1eca8fd90
title: Registrazione di codec MPEG2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7aaf683d03f529e394fe7e01af8ccae0e0fd009ad7a90b608c8bbebf834c5ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118952140"
---
# <a name="registering-mpeg2-codecs"></a>Registrazione di codec MPEG2

Questo argomento si applica solo Windows XP Media Center Edition.

Windows XP Media Center Edition gestisce due chiavi del Registro di sistema usate per determinare quale codec usare per riprodurre i file audio e video MPEG2. La prima chiave del Registro di sistema specifica il codec MPEG2 preferito del produttore del computer e la seconda elenca tutti i codec compatibili con Media Center attualmente installati nel computer. Quando Media Center deve riprodurre un file MPEG2, usa il codec preferito del produttore, se specificato. In caso contrario, usa il primo codec compatibile con Media Center elencato nel Registro di sistema. Se il Registro di sistema non specifica codec preferiti o compatibili, Media Center usa lo standard DirectShow filtro preferito per scegliere un codec.

Per assicurarsi che Media Center usi sempre un codec MPEG2 compatibile, i produttori di computer Media Center devono specificare il codec MPEG2 preferito nel percorso del Registro di sistema seguente:


```C++
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\Media Center\Service\Video
```



I dati della chiave devono essere i seguenti:


```C++
PreferredMPEG2VideoDecoder=REG_SZ "{MPEG2 Video CLSID GUID}"
PreferredMPEG2AudioDecoder=REG_SZ "{MPEG2 Audio CLSID GUID}"
```



Il programma di installazione per un codec MPEG2 compatibile con Media Center deve registrare il codec creando due istanze della chiave del Registro di sistema seguente, una per il codec video e una per il codec audio:


```C++
[HKEY_CLASSES_ROOT\CLSID\{083863F1-70DE-11d0-BD40-00A0C911CE86}\Instance\<Your Codec CLSID here>\Capabilities]
```



I dati della chiave devono essere i seguenti:


```C++
"{374ac4df-7c98-4257-b13d-36087dbee458}"=dword:00000001
```



 

 



