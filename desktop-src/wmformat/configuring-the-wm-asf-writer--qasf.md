---
title: Configurazione di WM ASF Writer (QASF)
description: Configurazione di WM ASF Writer (QASF)
ms.assetid: 0f49ed5a-c228-456a-9551-8d277adccd0e
keywords:
- Windows MEDIA Format SDK, configurazione di WM ASF Writer (QASF)
- Windows Media Format SDK,DirectShow
- Windows Media Format SDK,WM ASF Writer
- Windows Media Format SDK,QASF
- Advanced Systems Format (ASF), configurazione di WM ASF Writer (QASF)
- ASF (Advanced Systems Format), configurazione di WM ASF Writer (QASF)
- Advanced Systems Format (ASF),WM ASF Writer
- ASF (Advanced Systems Format),WM ASF Writer
- Advanced Systems Format (ASF), DirectShow
- ASF (Advanced Systems Format), DirectShow
- Advanced Systems Format (ASF),QASF
- ASF (Advanced Systems Format),QASF
- DirectShow,configurazione di WM ASF Writer (QASF)
- DirectShow,WM ASF Writer
- DirectShow,QASF
- WM ASF Writer, configurazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ba4559fc1780bdb9a9b398471cc842e2f3cf46f9c84a483229b01b3b6fa4a1c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118199177"
---
# <a name="configuring-the-wm-asf-writer-qasf"></a>Configurazione di WM ASF Writer (QASF)

Quando viene creato, il filtro [WM ASF Writer](wm-asf-writer-filter.md) viene configurato automaticamente con il profilo WMProfile \_ V80 \_ 256Video come impostazione predefinita. Poiché questo profilo usa i codec Windows Media Audio e Windows Media Video versione 8, è consigliabile creare un profilo personalizzato che usa i codec della serie Windows Media 9 e quindi passare il relativo puntatore [**IWMProfile**](iwmprofile.md) al filtro usando il metodo [**IConfigAsfWriter::ConfigureFilterUsingProfile.**](iconfigasfwriter-configurefilterusingprofile.md) Il filtro deve essere aggiunto al grafico prima di poter essere configurato e deve essere configurato prima di poter essere connesso ai filtri upstream. Il filtro usa il profilo per determinare il tipo di file Windows Media Format da scrivere, il numero di pin di input da configurare e i tipi di supporti che i pin possono accettare.

Il filtro consente la reimpostazione dei profili mentre i pin di input sono connessi, purché il nuovo profilo non richieda pin di input aggiuntivi. Ad esempio, se si modifica il profilo da un profilo con un solo input audio a un profilo audio e video a due input, solo il pin audio verrà riconnessoTutti i dati di input devono essere contrassegnati con un timestamp e tutti i pin di input devono essere connessi prima di poter eseguire o sospendere il filtro. Ciò significa che se si configura il filtro con un profilo con un flusso audio e un flusso video, il filtro creerà un pin di input audio e video ed entrambi i pin devono essere connessi prima di poter eseguire il filtro.

Aggiunta di estensioni per unità dati

È possibile configurare un flusso del profilo per le estensioni di unità dati, ad esempio i codici temporizzato SMPTE, prima o dopo la connessione del filtro, purché si segua questo ordine di operazioni:

1.  Aggiungere una o più estensioni di unità dati al flusso [**usando IWMStreamConfig2::AddDataUnitExtension.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-adddataunitextension)
2.  Chiamare [**WMProfile::ReconfigStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-reconfigstream) per aggiornare il profilo.
3.  Chiamare [**IConfigAsfWriter::ConfigureFilterUsingProfile con**](iconfigasfwriter-configurefilterusingprofile.md) l'oggetto profilo aggiornato.
4.  Trovare il pin di input video e chiamare il relativo [**metodo IAMWMBufferPass::SetNotify**](iamwmbufferpass-setnotify.md) per registrare l'interfaccia [**IAMWMBufferPassCallback**](/previous-versions/windows/desktop/api/dshowasf/nn-dshowasf-iamwmbufferpasscallback) definita dall'applicazione.

Quando il grafo viene eseguito, il metodo [**IAMWMBufferPassCallback::Notify**](iamwmbufferpasscallback-notify.md) verrà chiamato per ogni frame e sarà possibile ottenere e impostare le proprietà nell'esempio usando i relativi metodi di interfaccia [**INSSBuffer3.**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer3)

> [!Note]  
> In alcuni scenari con utilizzo intensivo del processore, ad esempio il telefono inverso, WM ASF Writer può richiedere più buffer di output di quelli supportati da alcuni filtri downstream. Il decodificatore DV, ad esempio, non accetterà più di un buffer per il pin di output e lo stesso vale per il decompressore AVI in determinate condizioni. Se si verificano problemi durante il tentativo di connessione a questi filtri o eventualmente durante l'esecuzione del grafo, potrebbe essere necessario scrivere un filtro intermedio che accetta un numero qualsiasi di buffer sul pin di output.

 

 

 