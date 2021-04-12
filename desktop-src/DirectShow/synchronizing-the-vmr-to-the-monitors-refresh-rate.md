---
description: Sincronizzazione di VMR alla frequenza di aggiornamento del monitoraggio
ms.assetid: 73e73821-fb08-488a-956e-ef33f6651a26
title: Sincronizzazione di VMR alla frequenza di aggiornamento del monitoraggio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5a9550e96e6a2e35c196048d38dd5b6e5b536d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233714"
---
# <a name="synchronizing-the-vmr-to-the-monitors-refresh-rate"></a>Sincronizzazione di VMR alla frequenza di aggiornamento del monitoraggio

In rari scenari, è opportuno sincronizzare con precisione il rendering video con la frequenza di aggiornamento del monitoraggio, in modo che ogni volta che il monitoraggio venga aggiornato viene visualizzato esattamente un nuovo frame. Il modo più affidabile per eseguire questa operazione consiste nel creare un allocatore-Presenter personalizzato che usa un'operazione di capovolgimento anziché un'operazione blit per scrivere i bit video nell'area primaria. "Flip" viene chiamato ogni volta che il monitoraggio viene aggiornato, quindi se il flusso video non contiene timestamp, il VMR viene eseguito il rendering il più rapidamente possibile nell'area primaria, ma la superficie bloccherà il flusso fino al completamento dell'operazione di capovolgimento. Ciò significa che, finché la CPU non è sovraccarica, il fotogramma successivo sarà sempre in attesa nella superficie primaria ogni volta che il monitoraggio viene aggiornato. Tuttavia, se è in esecuzione un altro processo con utilizzo intensivo della CPU, è possibile che il thread di streaming DirectShow muoia in modo improprio, in modo che non sia in grado di recapitare i frame video in modo sufficientemente rapido

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Modalità di riproduzione con rendering VMR (allocatore personalizzato-Presenter)](vmr-renderless-playback-mode--custom-allocator-presenters.md)
</dt> </dl>

 

 



