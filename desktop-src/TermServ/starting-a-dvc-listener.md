---
title: Avvio di un listener DVC
description: Per stabilire una connessione tra due moduli DVC (Dynamic Virtual Channel) in esecuzione nel client e nel server Connessione Desktop remoto (RDC), un listener DVC deve essere in esecuzione e in uno stato di ascolto.
ms.assetid: c9130375-eb60-4996-84f5-a1081144e130
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5d440069cb64597c16a14323a67926376bf1c425f5a29c77e451c52866a5399
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119000451"
---
# <a name="starting-a-dvc-listener"></a>Avvio di un listener DVC

Per stabilire una connessione tra due moduli DVC (Dynamic Virtual Channel) in esecuzione nel client e nel server Connessione Desktop remoto (RDC), un listener DVC deve essere in esecuzione e in uno stato di ascolto.

La creazione di un'istanza di un listener si verifica in genere nel [**metodo Initialize**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsplugin-initialize) del plug-in DVC. Tuttavia, la creazione di istanze non è limitata al **metodo Initialize** e può essere avviata in qualsiasi punto dell'esecuzione del plug-in. Il listener è descritto [**dall'interfaccia IWTSListener**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtslistener) di cui viene creata un'istanza da [**IWTSVirtualChannelManager.**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannelmanager) Un'istanza della gestione canali viene passata al plug-in nel punto di inizializzazione. Il plug-in può mantenere un riferimento interno all'istanza, purché sia necessario.

Un plug-in può creare un'istanza del numero di listener necessario. Qualsiasi connessione in ingresso verrà gestita da [**IWTSListenerCallback,**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtslistenercallback)fornito nel metodo [**CreateListener**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsvirtualchannelmanager-createlistener) di [**IWTSVirtualChannelManager.**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannelmanager) Per un esempio, vedere l'implementazione di **CDVCSamplePlugin::Initialize** nel codice di esempio di esempio del [plug-in client DVC.](dvc-client-plug-in-example.md)

 

 




