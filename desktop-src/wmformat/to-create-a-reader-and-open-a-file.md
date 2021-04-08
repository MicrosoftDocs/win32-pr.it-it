---
title: Per creare un reader e aprire un file
description: Per creare un reader e aprire un file
ms.assetid: 82b194d6-7cb7-4b88-9ed7-944b8b43bc29
keywords:
- ASF (Advanced Systems Format), creazione di Reader
- ASF (formato avanzato dei sistemi), creazione di Reader
- ASF (Advanced Systems Format), apertura di file
- ASF (Advanced Systems Format), apertura di file
- Reader asincroni, creazione
- Reader asincroni, apertura di file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8e714f51b56a7d9f3b18a774cd3b8c74bf05352
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/25/2020
ms.locfileid: "103724092"
---
# <a name="to-create-a-reader-and-open-a-file"></a>Per creare un reader e aprire un file

Prima di poter eseguire qualsiasi operazione con il lettore, sarà necessario creare un oggetto Reader e caricare un file per la lettura. Per inizializzare il Reader e aprire un file, seguire questa procedura.

1.  Creare un oggetto Reader chiamando la funzione [**WMCreateReader**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatereader) . È necessario specificare il livello desiderato di Rights Management per il nuovo oggetto Reader. Le modalità disponibili sono elencate nel tipo di enumerazione [**WMT \_ Rights**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_rights) .
2.  Specificare un file da leggere chiamando [**IWMReader:: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open). È necessario specificare un'interfaccia di callback Reader per il lettore da usare. Per ulteriori informazioni sul callback del lettore, vedere [per implementare i messaggi del lettore nel callback OnStatus](to-implement-reader-messages-in-the-onstatus-callback.md).
3.  Attendere che il lettore Apra il file. Quando si chiama **Open** per caricare un file, viene restituito quasi immediatamente e continua l'elaborazione in un altro thread. È necessario attendere il completamento delle operazioni segnalando un evento quando il callback **OnStatus** riceve il \_ messaggio di stato WMT aperto.

Il lettore supporta inoltre l'utilizzo dell'interfaccia com **IStream** per l'apertura di file. È possibile implementare l'interfaccia **IStream** come desiderato. Una volta aperto il file desiderato in **IStream**, è possibile seguire la procedura sopra indicata, ad eccezione del fatto che è necessario chiamare [**IWMReaderAdvanced2:: OpenStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-openstream) anziché **IWMReader:: Open** nel passaggio 2.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Interfaccia IWMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader)
</dt> <dt>

[**Interfaccia IWMReaderAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2)
</dt> <dt>

[**Interfaccia IWMStatusCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback)
</dt> <dt>

[**Lettura di file con il lettore asincrono**](reading-files-with-the-asynchronous-reader.md)
</dt> <dt>

[**Utilizzo dei metodi di callback**](using-the-callback-methods.md)
</dt> </dl>

 

 




