---
title: Scrittura di dati tramite un canale DVC
description: La scrittura di dati del canale tramite un canale virtuale dinamico (DVC) è simmetrica sia per il server host sessione Desktop remoto (Host sessione Desktop remoto) che per il client.
ms.assetid: 33bacbf0-c558-497a-a08a-95eb398fad97
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58e3f73b8e7a3d7db8ac109e84c9c638845af441b58568156782710fdac0968a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119058245"
---
# <a name="writing-data-by-using-a-dvc-channel"></a>Scrittura di dati tramite un canale DVC

La scrittura di dati del canale tramite un canale virtuale dinamico (DVC) è simmetrica sia per il server host sessione Desktop remoto (Host sessione Desktop remoto) che per il client. La scrittura dei dati del canale viene [**implementata dal metodo Write**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsvirtualchannel-write) dell'interfaccia [**IWTSVirtualChannel.**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannel)

La figura seguente illustra l'invio e la ricezione del pacchetto di dati tra il client e il server DVC (plug-in DVC).

![invio e ricezione di un pacchetto di dati tra il client e il server dvc](images/writedvcchannel.png)

 

 




