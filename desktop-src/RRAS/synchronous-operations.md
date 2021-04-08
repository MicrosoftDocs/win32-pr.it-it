---
title: Operazioni sincrone
description: Quando RasDial viene richiamato come operazione sincrona, la funzione non viene restituita fino a quando non viene stabilita la connessione o si verifica un errore.
ms.assetid: 5333ca88-bcec-48bc-88d2-3c6c0701802e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2463e3112c3faac4d7601023ea73f0182e2d5b73
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045198"
---
# <a name="synchronous-operations"></a>Operazioni sincrone

Quando [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) viene richiamato come operazione sincrona, la funzione non viene restituita fino a quando non viene stabilita la connessione o si verifica un errore. La modalità sincrona consente a un client RAS di stabilire una connessione in modo semplice. Il client può semplicemente chiamare **RasDial**, attendere la restituzione della funzione e quindi chiamare la funzione [**RasGetConnectStatus**](/windows/desktop/api/Ras/nf-ras-rasgetconnectstatusa) per determinare se l'operazione di connessione è stata eseguita correttamente. Una volta stabilita la connessione, l'applicazione client può terminare senza interrompere la connessione. Se si verifica un errore, l'applicazione client deve [arrestare l'operazione di connessione](disconnecting.md) prima di terminare.

Lo svantaggio della modalità sincrona è che il client non riceve le notifiche di stato durante l'operazione di connessione. Come soluzione alternativa per questa mancanza di notifiche di stato, un client in modalità sincrona può usare un thread separato che chiama [**RasGetConnectStatus**](/windows/desktop/api/Ras/nf-ras-rasgetconnectstatusa) per eseguire il polling e visualizzare lo stato corrente. Tuttavia, per i client RAS che desiderano ricevere informazioni sullo stato di avanzamento, la tecnica preferita consiste nel richiamare [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) in modo asincrono.

 

 




