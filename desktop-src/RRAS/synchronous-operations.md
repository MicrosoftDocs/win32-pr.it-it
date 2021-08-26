---
title: Operazioni sincrone
description: Quando RasDial viene richiamato come operazione sincrona, la funzione non restituisce un valore finché non viene stabilita la connessione o non si verifica un errore.
ms.assetid: 5333ca88-bcec-48bc-88d2-3c6c0701802e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80c923a22758e7d6b9563cde9e4c9b2ce6036afa47f85116c0c18ed523996e49
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120025611"
---
# <a name="synchronous-operations"></a>Operazioni sincrone

Quando [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) viene richiamato come operazione sincrona, la funzione non restituisce il controllo finché non viene stabilita la connessione o non si verifica un errore. La modalità sincrona consente a un client RAS di stabilire una connessione in modo semplice. Il client può semplicemente chiamare **RasDial,** attendere la restituzione della funzione e quindi chiamare la funzione [**RasGetConnectStatus**](/windows/desktop/api/Ras/nf-ras-rasgetconnectstatusa) per determinare se l'operazione di connessione è riuscita. Dopo aver stabilito la connessione, l'applicazione client può terminare senza interrompere la connessione. Se si verifica un errore, l'applicazione client deve [arrestare l'operazione di connessione](disconnecting.md) prima di terminare.

Lo svantaggio della modalità sincrona è che il client non riceve notifiche sullo stato di avanzamento durante l'operazione di connessione. Come soluzione alternativa per questa mancanza di notifiche di stato, un client in modalità sincrona può usare un thread separato che chiama [**RasGetConnectStatus**](/windows/desktop/api/Ras/nf-ras-rasgetconnectstatusa) per eseguire il polling e visualizzare lo stato corrente. Tuttavia, per i client RAS che vogliono ricevere informazioni sullo stato di avanzamento, la tecnica preferita consiste nel richiamare [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) in modo asincrono.

 

 




