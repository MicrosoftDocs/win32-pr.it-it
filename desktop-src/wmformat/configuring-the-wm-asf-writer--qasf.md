---
title: Configurazione del writer ASF WM (QASF)
description: Configurazione del writer ASF WM (QASF)
ms.assetid: 0f49ed5a-c228-456a-9551-8d277adccd0e
keywords:
- Windows Media Format SDK, configurazione di WM ASF Writer (QASF)
- Windows Media Format SDK, DirectShow
- Windows Media Format SDK, WM ASF Writer
- Windows Media Format SDK, QASF
- Advanced Systems Format (ASF), configurazione di WM ASF Writer (QASF)
- ASF (Advanced Systems Format), configurazione di WM ASF Writer (QASF)
- ASF (Advanced Systems Format), writer ASF WM
- ASF (formato avanzato dei sistemi), writer ASF WM
- ASF (Advanced Systems Format), DirectShow
- ASF (Advanced Systems Format), DirectShow
- Formato Advanced Systems (ASF), QASF
- ASF (formato avanzato dei sistemi), QASF
- DirectShow, configurazione di WM ASF Writer (QASF)
- DirectShow, WM-writer ASF
- DirectShow, QASF
- Writer ASF WM, configurazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72f954522c4acae89e6f6dd001561811088c2a9e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104118258"
---
# <a name="configuring-the-wm-asf-writer-qasf"></a>Configurazione del writer ASF WM (QASF)

Quando il filtro del [writer ASF WM](wm-asf-writer-filter.md) viene creato, viene configurato automaticamente con il \_ profilo WMProfile \_ V80 256Video come valore predefinito. Poiché questo profilo usa i codec Windows Media Audio e Windows Media Video versione 8, è consigliabile creare un profilo personalizzato che usa i codec della serie Windows Media 9, quindi passare il puntatore [**IWMProfile**](iwmprofile.md) al filtro usando il metodo [**IConfigAsfWriter:: ConfigureFilterUsingProfile**](iconfigasfwriter-configurefilterusingprofile.md) . Il filtro deve essere aggiunto al grafico prima che il filtro possa essere configurato e deve essere configurato prima di poter essere connesso ai filtri upstream. Il filtro usa il profilo per determinare il tipo di file di formato Windows Media da scrivere, il numero di pin di input da configurare e i tipi di supporti che i pin possono accettare.

Il filtro consente di reimpostare i profili mentre i pin di input sono connessi, purché il nuovo profilo non richieda pin di input aggiuntivi. Ad esempio, se si modifica il profilo da un profilo audio di input singolo a un profilo audio e video di due input, solo il pin audio sarà reconnectedAll i dati di input devono essere timestamp e tutti i pin di input devono essere connessi prima che il filtro possa essere eseguito o sospeso. Ciò significa che se si configura il filtro con un profilo con un flusso audio e un flusso video, il filtro creerà un pin di input audio e video ed è necessario che entrambi i pin siano connessi prima di poter eseguire il filtro.

Aggiunta di estensioni di unità dati

È possibile configurare un flusso del profilo per le estensioni dell'unità dati, ad esempio i codici temporali SMPTE, prima o dopo la connessione del filtro, purché si segua questo ordine di operazioni:

1.  Aggiungere una o più estensioni di unità dati al flusso usando [**IWMStreamConfig2:: AddDataUnitExtension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-adddataunitextension).
2.  Chiamare [**WMProfile:: ReconfigStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-reconfigstream) per aggiornare il profilo.
3.  Chiamare [**IConfigAsfWriter:: ConfigureFilterUsingProfile**](iconfigasfwriter-configurefilterusingprofile.md) con l'oggetto profilo aggiornato.
4.  Trovare il pin di input del video e chiamare il metodo [**IAMWMBufferPass:: senotify**](iamwmbufferpass-setnotify.md) per registrare l'interfaccia [**IAMWMBufferPassCallback**](/previous-versions/windows/desktop/api/dshowasf/nn-dshowasf-iamwmbufferpasscallback) definita dall'applicazione.

Quando si esegue il grafo, viene chiamato il metodo [**IAMWMBufferPassCallback:: Notify**](iamwmbufferpasscallback-notify.md) per ogni frame e sarà possibile ottenere e impostare le proprietà nell'esempio usando i relativi metodi di interfaccia [**INSSBuffer3**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer3) .

> [!Note]  
> In alcuni scenari con utilizzo intensivo del processore, ad esempio la telecine inversa, il writer ASF WM potrebbe richiedere un maggior numero di buffer di output rispetto ad alcuni filtri downstream che possono supportare. Il decodificatore DV, ad esempio, non accetterà più di un buffer per il pin di output e lo stesso vale per il decompressore AVI in determinate condizioni. Se si verificano problemi durante il tentativo di connessione a questi filtri o quando si esegue il grafo, potrebbe essere necessario scrivere un filtro intermediario che accetti un numero qualsiasi di buffer nel pin di output.

 

 

 