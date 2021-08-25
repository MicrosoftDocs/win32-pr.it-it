---
description: Configurazione di ASF Writer
ms.assetid: 5708c4a0-6197-4a42-adfd-01c6dfe86302
title: Configurazione di ASF Writer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e3d28b3b6178a383909f53a98fef98a5c3e69297f71615010f505d28b77375a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119871701"
---
# <a name="configuring-the-asf-writer"></a>Configurazione di ASF Writer

Quando viene creato, il filtro [WM ASF Writer](wm-asf-writer-filter.md) viene configurato automaticamente con il profilo WMProfile \_ V80 \_ 256Video. Questo profilo usa i codec Windows Media Audio e Windows Media Video versione 8, che non sono recenti come i codec Windows Media 9 Series. È consigliabile creare un profilo personalizzato che usa i codec Windows Media 9 Series e configurare WM ASF Writer con il profilo personalizzato, come descritto in [Configuring Profiles and Other ASF File Properties](configuring-profiles-and-other-asf-file-properties.md). È necessario aggiungere il filtro WM ASF Writer al grafico dei filtri prima di configurare il filtro e configurare il filtro prima di connetterlo a qualsiasi altro filtro.

Tutti i dati di input devono essere contrassegnati con un timestamp e tutti i pin di input devono essere connessi prima di poter eseguire o sospendere il filtro. Pertanto, se si configura il filtro con un profilo con un flusso audio e un flusso video, il filtro creerà un pin di input audio e video ed entrambi i pin devono essere connessi prima di poter eseguire il filtro. Poiché Windows Media Format SDK richiede il funzionamento di un flusso audio, WM ASF Writer deve avere sempre un pin audio di input, anche se è per un flusso fittizio, ovvero un flusso audio disattivato e a bassa velocità in bit.

Aggiunta di estensioni per unità dati

È possibile configurare un flusso del profilo per le estensioni di unità dati, ad esempio i codici temporizzato SMPTE, prima o dopo la connessione del filtro, purché si segua questo ordine di operazioni:

1.  Aggiungere una o più estensioni di unità dati al flusso **usando IWMStreamConfig2::AddDataUnitExtension.**
2.  Chiamare **IWMProfile::ReconfigStream** per aggiornare il profilo.
3.  Chiamare [**IConfigAsfWriter::ConfigureFilterUsingProfile con**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter-configurefilterusingprofile) l'oggetto profilo aggiornato.
4.  Trovare il pin di input video e chiamare il relativo [**metodo IAMWMBufferPass::SetNotify**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iamwmbufferpass-setnotify) per registrare l'interfaccia [**IAMWMBufferPassCallback**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iamwmbufferpasscallback) definita dall'applicazione.

Quando il grafo viene eseguito, il metodo [**IAMWMBufferPassCallback::Notify**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iamwmbufferpasscallback-notify) verrà chiamato per ogni frame e sarà possibile ottenere e impostare le proprietà nell'esempio usando i relativi metodi di interfaccia **INSSBuffer3.**

> [!Note]  
> In alcuni scenari con utilizzo intensivo del processore, ad esempio il telefono inverso, WM ASF Writer può richiedere più buffer di output di quelli supportati da alcuni filtri downstream. Il decodificatore DV, ad esempio, non accetterà più di un buffer per il pin di output e lo stesso vale per il decompressore AVI in determinate condizioni. Se si verificano problemi durante il tentativo di connessione a questi filtri o eventualmente durante l'esecuzione del grafo, potrebbe essere necessario scrivere un filtro intermedio che accetta un numero qualsiasi di buffer sul pin di output.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Creazione di file ASF in DirectShow](creating-asf-files-in-directshow.md)
</dt> </dl>

 

 



