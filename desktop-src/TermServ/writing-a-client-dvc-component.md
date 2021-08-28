---
title: Scrittura di un modulo DVC client
description: Per scrivere un modulo client DVC (Dynamic Virtual Channel), è prima necessario implementare e registrare un plug-in client Connessione Desktop remoto (RDC).
ms.assetid: b6f475d4-d2ad-41ce-b3b9-d844fbd23cf0
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: faa9f365034ff7771baf8eaeca102d7156f592e71d0cedffc97cef6d75b81fae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120008266"
---
# <a name="writing-a-client-dvc-module"></a>Scrittura di un modulo DVC client

Per scrivere un modulo client DVC (Dynamic Virtual Channel), è prima necessario implementare e registrare un plug-in client Connessione Desktop remoto (RDC). Il plug-in DVC è un'implementazione di [**IWTSPlugin,**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin)registrata come oggetto Component Object Model (COM).

> [!Note]  
> Il plug-in deve essere implementato in un modello di threading free. L'implementazione del modello di apartment non è supportata.

 

Di seguito è riportato un elenco di interfacce implementate dagli oggetti di cui viene creata un'istanza dal plug-in.



| Interfaccia                                                        | Descrizione                                                                                                                                                                                          |
|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IWTSPlugin**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin)                                 | Consente il Connessione Desktop remoto plug-in client (RDC) da caricare dal client Connessione Desktop remoto (RDC).<br/>                                                                 |
| [**IWTSListenerCallback**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtslistenercallback)             | Notifica al plug-in Connessione Desktop remoto (RDC) le richieste in ingresso in un listener specifico.<br/>                                                                             |
| [**IWTSVirtualChannelCallback**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannelcallback) | Riceve notifiche sulle modifiche dello stato del canale o sui dati ricevuti. Ogni istanza di questa interfaccia è associata a un'istanza di [**IWTSVirtualChannel.**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannel)<br/> |



 

Di seguito è riportato un elenco di interfacce implementate da oggetti di cui viene creata un'istanza dal client Connessione Desktop remoto (RDC) e fanno parte del framework.



| Interfaccia                                                      | Descrizione                                                                                                        |
|----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [**IWTSVirtualChannelManager**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannelmanager) | Gestisce tutti Connessione Desktop remoto plug-in client (RDC), listener DVC o canali virtuali statici.<br/> |
| [**IWTSListener**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtslistener)                           | Gestisce le impostazioni di configurazione per ogni listener per la connessione DVC.<br/>                                |
| [**IWTSVirtualChannel**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannel)               | Controlla lo stato del canale, nonché le scritture sul canale.<br/>                                           |



 

La figura seguente illustra la relazione tra il client Connessione Desktop remoto (RDC) e il plug-in client Connessione Desktop remoto (RDC).

![relazione tra client e plug-in](images/tsclient.png)

 

 





