---
title: Scrittura di un modulo client DVC
description: Per scrivere un modulo client Dynamic Channel (DVC), è necessario innanzitutto implementare e registrare un plug-in client di Connessione Desktop remoto (RDC).
ms.assetid: b6f475d4-d2ad-41ce-b3b9-d844fbd23cf0
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcb881fd057132eb416066ffac050f75f4df1b12
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298414"
---
# <a name="writing-a-client-dvc-module"></a>Scrittura di un modulo client DVC

Per scrivere un modulo client Dynamic Channel (DVC), è necessario innanzitutto implementare e registrare un plug-in client di Connessione Desktop remoto (RDC). Il plug-in DVC è un'implementazione di [**IWTSPlugin**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin), registrato come oggetto Component Object Model (com).

> [!Note]  
> Il plug-in deve essere implementato in un modello a thread libero. L'implementazione del modello di Apartment non è supportata.

 

Di seguito è riportato un elenco di interfacce implementate da oggetti di cui viene creata un'istanza dal plug-in.



| Interfaccia                                                        | Descrizione                                                                                                                                                                                          |
|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IWTSPlugin**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin)                                 | Consente il caricamento del plug-in del client Connessione Desktop remoto (RDC) dal client di Connessione Desktop remoto (RDC).<br/>                                                                 |
| [**IWTSListenerCallback**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtslistenercallback)             | Notifica al plug-in del client Connessione Desktop remoto (RDC) informazioni sulle richieste in ingresso su un listener specifico.<br/>                                                                             |
| [**IWTSVirtualChannelCallback**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannelcallback) | Riceve le notifiche relative alle modifiche dello stato del canale o ai dati ricevuti. Ogni istanza di questa interfaccia è associata a un'istanza di [**IWTSVirtualChannel**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannel).<br/> |



 

Di seguito è riportato un elenco di interfacce implementate da oggetti di cui viene creata un'istanza dal client Connessione Desktop remoto (RDC) e che fanno parte del Framework.



| Interfaccia                                                      | Descrizione                                                                                                        |
|----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [**IWTSVirtualChannelManager**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannelmanager) | Gestisce tutti i plug-in del client Connessione Desktop remoto (RDC), i listener DVC o i canali virtuali statici.<br/> |
| [**IWTSListener**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtslistener)                           | Gestisce le impostazioni di configurazione per ogni listener per la connessione DVC.<br/>                                |
| [**IWTSVirtualChannel**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannel)               | Controlla lo stato del canale, nonché le Scritture sul canale.<br/>                                           |



 

Nella figura seguente viene illustrata la relazione tra il client di Connessione Desktop remoto (RDC) e il plug-in del client di Connessione Desktop remoto (RDC).

![relazione tra il client e il plug-in](images/tsclient.png)

 

 





