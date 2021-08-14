---
title: API client DVC
description: Le API client DVC (Dynamic Virtual Channel) vengono implementate in modo specifico per il client Connessione Desktop remoto (RDC) della connessione.
ms.assetid: 976a6cc2-7bbe-4ecc-91b4-b7c659eca5ba
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 557f51adbf10562465f93a101e502632a791d5c272b278c5a8b7ea6124637913
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118130817"
---
# <a name="dvc-client-apis"></a>API client DVC

Le API client DVC (Dynamic Virtual Channel) vengono implementate in modo specifico per il client Connessione Desktop remoto (RDC) della connessione. Alcune API vengono implementate dal framework DVC e altre dallo sviluppatore di plug-in. Alcune API vengono usate per supportare il plug-in client Connessione Desktop remoto (RDC) e non sono direttamente correlate al trasporto dei dati.

## <a name="in-this-section"></a>Contenuto della sezione

<dl> <dt>

[**IWTSPlugin**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin)
</dt> <dd>

Consente al plug-in Connessione Desktop remoto (RDC) di essere caricato dal client Connessione Desktop remoto (RDC).

</dd> <dt>

[**IWTSListener**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtslistener)
</dt> <dd>

Gestisce le impostazioni di configurazione per ogni listener per la connessione DVC (Dynamic Virtual Channel).

</dd> <dt>

[**IWTSListenerCallback**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtslistenercallback)
</dt> <dd>

Usato per notificare al plug-in del client Connessione Desktop remoto (RDC) le richieste in ingresso in un listener specifico.

</dd> <dt>

[**IWTSVirtualChannelManager**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannelmanager)
</dt> <dd>

Gestisce tutti Connessione Desktop remoto plug-in client (RDC) e listener DVC (Dynamic Virtual Channel).

</dd> <dt>

[**IWTSVirtualChannel**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannel)
</dt> <dd>

Utilizzato per controllare lo stato del canale e scrive sul canale.

</dd> <dt>

[**IWTSVirtualChannelCallback**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannelcallback)
</dt> <dd>

Riceve notifiche sulle modifiche dello stato del canale o sui dati ricevuti.

</dd> <dt>

[**IWTSVirtualChannelCallback2**](iwtsvirtualchannelcallback2.md)
</dt> <dd>

Questa interfaccia non è supportata.

</dd> <dt>

[**VirtualChannelGetInstance**](virtualchannelgetinstance.md)
</dt> <dd>

Chiamato per fare in modo che il plug-in crei un'istanza [**dell'interfaccia IWTSPlugin**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin) per tutti i plug-in implementati dalla DLL.

</dd> </dl>

 

 




