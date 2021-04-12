---
title: Avvio di un listener DVC
description: Per stabilire una connessione corretta tra due moduli DVC (Dynamic Virtual Channel) in esecuzione nel client e nel server Connessione Desktop remoto (RDC), è necessario che un listener DVC sia in esecuzione e in stato di ascolto.
ms.assetid: c9130375-eb60-4996-84f5-a1081144e130
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b625d5547facd0487af170af9d59eddd6bfed87
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104332388"
---
# <a name="starting-a-dvc-listener"></a>Avvio di un listener DVC

Per stabilire una connessione corretta tra due moduli DVC (Dynamic Virtual Channel) in esecuzione nel client e nel server Connessione Desktop remoto (RDC), è necessario che un listener DVC sia in esecuzione e in stato di ascolto.

La creazione di istanze di un listener si verifica in genere nel metodo [**Initialize**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsplugin-initialize) del plug-in DVC. Tuttavia, la creazione di istanze non è limitata al metodo **Initialize** e può essere avviata in qualsiasi punto dell'esecuzione del plug-in. Il listener viene descritto dall'interfaccia [**IWTSListener**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtslistener) di cui viene creata un'istanza da [**IWTSVirtualChannelManager**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannelmanager). Un'istanza di al gestore del canale viene passata al plug-in nel punto di inizializzazione. Il plug-in è in grado di mantenere un riferimento interno all'istanza a condizione che sia necessario.

Un plug-in può creare un'istanza di un numero di listener sufficiente. Tutte le connessioni in ingresso verranno gestite da [**IWTSListenerCallback**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtslistenercallback), fornito nel metodo [**CreateListener**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsvirtualchannelmanager-createlistener) di [**IWTSVirtualChannelManager**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannelmanager). Per un esempio, vedere l'implementazione di **CDVCSamplePlugin:: Initialize** nell'esempio di codice del [plug-in del client DVC](dvc-client-plug-in-example.md) .

 

 




