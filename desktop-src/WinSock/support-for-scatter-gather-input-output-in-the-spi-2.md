---
description: Le routine WSPSend, WSPSendTo, WSPRecv e WSPRecvFrom accettano una matrice di buffer client come parametri di input e quindi possono essere usate per operazioni di I/O a dispersione/raccolta (o vettoriali).
ms.assetid: ecd3d2f1-74b1-42f7-8402-3170112e3aca
title: Supporto per la dispersione/raccolta di input/output in SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c3f32e016c5c2e9f990c334716d4177d477c50f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310418"
---
# <a name="support-for-scattergather-inputoutput-in-the-spi"></a>Supporto per la dispersione/raccolta di input/output in SPI

Le routine [**WSPSend**](/previous-versions/windows/hardware/network/ff566316(v=vs.85)), [**WSPSendTo**](/previous-versions/windows/desktop/legacy/ms742291(v=vs.85)), [**WSPRecv**](/previous-versions/windows/hardware/network/ff566309(v=vs.85))e [**WSPRecvFrom**](/previous-versions/windows/desktop/legacy/ms742287(v=vs.85)) accettano una matrice di buffer client come parametri di input e quindi possono essere usate per operazioni di I/o a dispersione/raccolta (o vettoriali). Questo può essere molto utile in istanze in cui le parti di ogni messaggio trasmesso sono costituite da uno o più componenti di intestazione a lunghezza fissa oltre al corpo del messaggio. Questi componenti di intestazione non devono essere concatenati in un singolo buffer contiguo prima dell'invio. Analogamente alla ricezione, i componenti dell'intestazione possono essere suddivisi automaticamente in buffer distinti, lasciando pure il corpo del messaggio.

L'utilizzo di elenchi di buffer anziché di un singolo buffer non comporta la modifica dei limiti che si applicano alle operazioni di ricezione. Per i protocolli orientati ai messaggi, un'operazione di ricezione viene completata ogni volta che viene ricevuto un singolo messaggio, indipendentemente dal numero di buffer utilizzati. Analogamente, per i protocolli orientati al flusso, una ricezione viene completata quando arriva una quantità non specificata di byte sulla rete, non necessariamente quando tutti i buffer forniti sono pieni.

 

 
