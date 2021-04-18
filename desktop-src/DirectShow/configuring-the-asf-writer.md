---
description: Configurazione del writer ASF
ms.assetid: 5708c4a0-6197-4a42-adfd-01c6dfe86302
title: Configurazione del writer ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62a6dfc1827743dce946188ebf9e050226b5c484
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304122"
---
# <a name="configuring-the-asf-writer"></a>Configurazione del writer ASF

Quando il filtro del [writer ASF WM](wm-asf-writer-filter.md) viene creato, viene configurato automaticamente con il \_ profilo WMProfile \_ V80 256Video. Questo profilo usa i codec Windows Media Audio e Windows Media Video versione 8, che non sono recenti come i codec della serie Windows Media 9. Si consiglia di creare un profilo personalizzato che usa i codec della serie Windows Media 9 e di configurare il writer ASF WM con il profilo personalizzato, come descritto in [configurazione di profili e altre proprietà del file ASF](configuring-profiles-and-other-asf-file-properties.md). È necessario aggiungere il filtro del writer ASF WM al grafico filtro prima di configurare il filtro e configurare il filtro prima di connetterlo a tutti gli altri filtri.

Tutti i dati di input devono avere un timestamp e tutti i pin di input devono essere connessi prima di poter eseguire o sospendere il filtro. Se pertanto si configura il filtro con un profilo con un flusso audio e un flusso video, il filtro creerà un pin di input audio e video ed è necessario che entrambi i pin siano connessi prima di poter eseguire il filtro. Poiché Windows Media Format SDK richiede il funzionamento di un flusso audio, il writer ASF WM deve avere sempre un pin audio di input, anche se è per un flusso fittizio, ovvero un flusso audio a bassa velocità in bit disattivato.

Aggiunta di estensioni di unità dati

È possibile configurare un flusso del profilo per le estensioni dell'unità dati, ad esempio i codici temporali SMPTE, prima o dopo la connessione del filtro, purché si segua questo ordine di operazioni:

1.  Aggiungere una o più estensioni di unità dati al flusso usando **IWMStreamConfig2:: AddDataUnitExtension**.
2.  Chiamare **IWMProfile:: ReconfigStream** per aggiornare il profilo.
3.  Chiamare [**IConfigAsfWriter:: ConfigureFilterUsingProfile**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter-configurefilterusingprofile) con l'oggetto profilo aggiornato.
4.  Trovare il pin di input del video e chiamare il metodo [**IAMWMBufferPass:: senotify**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iamwmbufferpass-setnotify) per registrare l'interfaccia [**IAMWMBufferPassCallback**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iamwmbufferpasscallback) definita dall'applicazione.

Quando si esegue il grafo, viene chiamato il metodo [**IAMWMBufferPassCallback:: Notify**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iamwmbufferpasscallback-notify) per ogni frame e sarà possibile ottenere e impostare le proprietà nell'esempio usando i relativi metodi di interfaccia **INSSBuffer3** .

> [!Note]  
> In alcuni scenari con utilizzo intensivo del processore, ad esempio la telecine inversa, il writer ASF WM potrebbe richiedere un maggior numero di buffer di output rispetto ad alcuni filtri downstream che possono supportare. Il decodificatore DV, ad esempio, non accetterà più di un buffer per il pin di output e lo stesso vale per il decompressore AVI in determinate condizioni. Se si verificano problemi durante il tentativo di connessione a questi filtri o quando si esegue il grafo, potrebbe essere necessario scrivere un filtro intermediario che accetti un numero qualsiasi di buffer nel pin di output.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Creazione di file ASF in DirectShow](creating-asf-files-in-directshow.md)
</dt> </dl>

 

 



