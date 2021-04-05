---
title: Implementazione di canali virtuali tramite script tramite Connessione Web Desktop remoto
description: Esempi di codice che illustrano i passaggi per l'implementazione di canali virtuali utilizzabili tramite script con Connessione Web Desktop remoto.
ms.assetid: a482b84d-96b6-4f42-8841-7039a1882789
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89a36f685de01312a93df67deb6be16ce031794c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103712217"
---
# <a name="implementing-scriptable-virtual-channels-by-using-remote-desktop-web-connection"></a>Implementazione di canali virtuali tramite script tramite Connessione Web Desktop remoto

Nella procedura e negli esempi di codice riportati di seguito vengono illustrati i passaggi per l'implementazione di canali virtuali tramite script con Connessione Web Desktop remoto. Gli esempi sono stati scritti in Visual Basic Scripting Edition e presuppongono che il controllo ActiveX Desktop remoto sia denominato "MsRdpClient".

**Per creare e distribuire canali virtuali tramite script**

1.  Distribuire il lato server dell'applicazione e assicurarsi che sia in esecuzione nel server host sessione Desktop remoto (host sessione Desktop remoto). Per informazioni sulla distribuzione di applicazioni di canali virtuali sul server, vedere [Virtual Channel Server Application](virtual-channel-server-application.md).
2.  Nello script client, chiamare [**IMsTscAx:: CreateVirtualChannels**](imstscax-createvirtualchannels.md), passando una stringa che contiene un elenco delimitato da virgole di nomi di canale virtuali.

    ```VB
    MsRdpClient.CreateVirtualChannels("mychan1,mychan2")
    ```

    

    Per informazioni sulle restrizioni di denominazione dei canali virtuali, vedere [registrazione client del canale virtuale](virtual-channel-client-registration.md).

3.  Chiamare [**IMsTscAx:: Connect**](imstscax-connect.md) per creare la connessione Servizi Desktop remoto.

    ```VB
    MsRdpClient.connect
    ```

    

4.  Usare il metodo [**IMsTscAx:: SendOnVirtualChannel**](imstscax-sendonvirtualchannel.md) per inviare dati al server, passando una stringa che contiene il nome del canale virtuale e una seconda stringa che contiene i dati da passare.

    ```VB
    MsRdpClient.SendOnVirtualChannel("mychan1","hello from the client")
    ```

    

5.  Ricevere i dati dal server nell'evento [**IMsTscAxEvents:: OnChannelReceivedData**](imstscaxevents-onchannelreceiveddata.md) .

    ```VB
    Sub MsRdpClient.OnChannelReceivedData(chanName,data)
    Msgbox("received data:" &data& "on virtual channel:" &chanName)
    End sub
    ```

    

 

 




