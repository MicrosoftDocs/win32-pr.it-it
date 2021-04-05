---
title: Per recuperare esempi di supporti con il Reader asincrono
description: Per recuperare esempi di supporti con il Reader asincrono
ms.assetid: 0d8c3099-f068-4074-b717-2f5b9ed9eeb8
keywords:
- Formato di sistemi avanzati (ASF), recupero di esempi di supporti
- ASF (Advanced Systems Format), recupero di esempi di supporti
- ASF (Advanced Systems Format), Reader asincroni
- ASF (formato avanzato dei sistemi), Reader asincroni
- Reader asincroni, recupero di esempi di supporti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb0419619ea99bd3734db67f8e658b1f3ff058a3
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104046293"
---
# <a name="to-retrieve-media-samples-with-the-asynchronous-reader"></a>Per recuperare esempi di supporti con il Reader asincrono

Dopo aver ricevuto il messaggio di \_ stato WMT aperto nell'implementazione di [**IWMStatusCallback:: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus), è possibile iniziare a ricevere esempi chiamando [**IWMReader:: Start**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-start). Il lettore asincrono recapita esempi all'implementazione di [**IWMReaderCallback:: OnSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample). Gli esempi vengono recapitati in ordine temporale di presentazione.

**Start** è una chiamata asincrona. Verrà restituito quasi immediatamente e continuerà a essere eseguito su thread separati. Il lettore asincrono usa più thread durante la decodifica del contenuto e la distribuzione di esempi. Quando viene raggiunta la fine del file, il lettore invia un \_ messaggio di stato WMT EOF all'implementazione del callback **OnStatus** . Quando \_ si invia WMT EOF, il lettore interrompe la propria elaborazione; non è necessario rispondere a WMT \_ EOF con una chiamata a [**IWMReader:: Stop**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-stop).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Interfaccia IWMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader)
</dt> <dt>

[**Per implementare i messaggi del lettore nel callback OnStatus**](to-implement-reader-messages-in-the-onstatus-callback.md)
</dt> <dt>

[**Per implementare il callback OnSample**](to-implement-the-onsample-callback.md)
</dt> </dl>

 

 




