---
title: Accettazione di una connessione (Servizi Desktop remoto)
description: A un certo punto nel tempo, il client dinamico del canale virtuale (DVC) richiederà una connessione al listener di DVC.
ms.assetid: eab17aa9-590c-4da2-a1a9-6e50a11d1de7
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b13aa0b78e459c85e7ba07e043e3da313b3f6118
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104567730"
---
# <a name="accepting-a-connection-remote-desktop-services"></a>Accettazione di una connessione (Servizi Desktop remoto)

A un certo punto nel tempo, il client dinamico del canale virtuale (DVC) richiederà una connessione al listener di DVC. Quando si verifica questo problema, il listener può generare un canale di comunicazione univoco per il client, gestito dal metodo [**OnNewChannelConnection**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtslistenercallback-onnewchannelconnection) di [**IWTSListenerCallback**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannelcallback). Per un esempio, vedere l'implementazione di **CDVCSamplePlugin:: OnNewChannelConnection** nel codice di esempio relativo al [plug-in del client DVC](dvc-client-plug-in-example.md) .

Nella figura seguente viene illustrata la sequenza di eventi per stabilire una connessione DVC. Gli oggetti ombreggiati sono forniti dall'utente (applicazione/servizio DVC e [**IWTSListenerCallback**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtslistenercallback)), mentre gli oggetti non ombreggiati fanno parte di framework (host sessione Desktop remoto servizio host sessione Desktop remoto, listener e [**IWTSVirtualChannel**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannel)).

![sequenza di eventi per stabilire una connessione DVC](images/acceptingconnection.png)

> [!Note]  
> In questa figura si presuppone che sia stato creato un oggetto listener tramite una chiamata [**CreateListener**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsvirtualchannelmanager-createlistener) a [**IWTSVirtualChannelManager**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannelmanager)e che il plug-in abbia specificato [**IWTSListenerCallback**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtslistenercallback) come parametro.

 

 

 




