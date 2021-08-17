---
description: Le routine WSPSend, WSPSendTo, WSPRecv e WSPRecvFrom accettano tutte una matrice di buffer client come parametri di input e pertanto possono essere usate per operazioni di I/O a dispersione/raccolta (o vettoriali).
ms.assetid: ecd3d2f1-74b1-42f7-8402-3170112e3aca
title: Supporto per input/output a dispersione/raccolta in SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b136898c1163ab298d8a177238f11239262b04306662b3f11b75bfb847f335d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117739998"
---
# <a name="support-for-scattergather-inputoutput-in-the-spi"></a>Supporto per input/output a dispersione/raccolta in SPI

Le routine [**WSPSend**](/previous-versions/windows/hardware/network/ff566316(v=vs.85)), [**WSPSendTo**](/previous-versions/windows/desktop/legacy/ms742291(v=vs.85)), [**WSPRecv**](/previous-versions/windows/hardware/network/ff566309(v=vs.85))e [**WSPRecvFrom**](/previous-versions/windows/desktop/legacy/ms742287(v=vs.85)) accettano tutte una matrice di buffer client come parametri di input e pertanto possono essere usate per l'I/O a dispersione/raccolta (o vettoriale). Ciò può essere molto utile nei casi in cui parti di ogni messaggio trasmesso sono costituite da uno o più componenti di intestazione a lunghezza fissa oltre a un corpo del messaggio. Tali componenti di intestazione non devono essere concatenati in un singolo buffer contiguo prima dell'invio. Analogamente alla ricezione, i componenti dell'intestazione possono essere suddivisi automaticamente in buffer separati, lasciando puro il corpo del messaggio.

L'utilizzo di elenchi di buffer anziché di un singolo buffer non modifica i limiti che si applicano alle operazioni di ricezione. Per i protocolli orientati ai messaggi, un'operazione di ricezione viene completata ogni volta che viene ricevuto un singolo messaggio, indipendentemente dal numero o dal numero di buffer forniti. Analogamente per i protocolli orientati al flusso, una ricezione viene completata quando una quantità non specificata di byte arriva in rete, non necessariamente quando tutti i buffer forniti sono completi.

 

 
