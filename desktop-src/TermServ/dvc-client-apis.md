---
title: API client DVC
description: Le API client dinamiche del canale virtuale (DVC) sono implementate in modo specifico per il client Connessione Desktop remoto (RDC) della connessione.
ms.assetid: 976a6cc2-7bbe-4ecc-91b4-b7c659eca5ba
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25c29d360fb0ad4d6e31e828f9c62f42f64fb311
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104329484"
---
# <a name="dvc-client-apis"></a>API client DVC

Le API client dinamiche del canale virtuale (DVC) sono implementate in modo specifico per il client Connessione Desktop remoto (RDC) della connessione. Alcune API sono implementate dal Framework DVC e alcune sono implementate dallo sviluppatore di plug-in. Alcune API vengono utilizzate per supportare il plug-in client di Connessione Desktop remoto (RDC) e non sono direttamente correlate al trasporto dati.

## <a name="in-this-section"></a>Contenuto della sezione

<dl> <dt>

[**IWTSPlugin**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin)
</dt> <dd>

Consente il caricamento del plug-in del client Connessione Desktop remoto (RDC) dal client di Connessione Desktop remoto (RDC).

</dd> <dt>

[**IWTSListener**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtslistener)
</dt> <dd>

Gestisce le impostazioni di configurazione per ogni listener per la connessione del canale virtuale dinamico (DVC).

</dd> <dt>

[**IWTSListenerCallback**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtslistenercallback)
</dt> <dd>

Utilizzato per notificare al plug-in del client Connessione Desktop remoto (RDC) informazioni sulle richieste in ingresso su un listener specifico.

</dd> <dt>

[**IWTSVirtualChannelManager**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannelmanager)
</dt> <dd>

Gestisce tutti i plug-in del client Connessione Desktop remoto (RDC) e i listener del canale virtuale dinamico (DVC).

</dd> <dt>

[**IWTSVirtualChannel**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannel)
</dt> <dd>

Utilizzato per controllare lo stato del canale e scrivere sul canale.

</dd> <dt>

[**IWTSVirtualChannelCallback**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannelcallback)
</dt> <dd>

Riceve le notifiche relative alle modifiche dello stato del canale o ai dati ricevuti.

</dd> <dt>

[**IWTSVirtualChannelCallback2**](iwtsvirtualchannelcallback2.md)
</dt> <dd>

Questa interfaccia non è supportata.

</dd> <dt>

[**VirtualChannelGetInstance**](virtualchannelgetinstance.md)
</dt> <dd>

Chiamato per fare in modo che il plug-in crei un'istanza dell'interfaccia [**IWTSPlugin**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin) per tutti i plug-in implementati dalla dll.

</dd> </dl>

 

 




