---
title: Operazioni asincrone
description: Quando RasDial viene richiamato come operazione asincrona, la funzione restituisce immediatamente.
ms.assetid: f165b4a7-00fb-4888-8225-8fd106e113f2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db434b7e6d080933e7e21de056f9af5ea7d57dfe
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396210"
---
# <a name="asynchronous-operations"></a>Operazioni asincrone

Quando [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) viene richiamato come operazione asincrona, la funzione restituisce immediatamente. In modalità asincrona la chiamata **RasDial** deve specificare un [gestore di notifiche](notification-handlers.md) usato dalla gestione connessione di accesso remoto per informare il client ogni volta che l'operazione di connessione cambia Stati o si verifica un errore.

Il gestore delle notifiche può essere una finestra per la ricezione di messaggi o una funzione di callback [**RasDialFunc**](/windows/desktop/api/Ras/nc-ras-rasdialfunc), [**RasDialFunc1**](/windows/desktop/api/Ras/nc-ras-rasdialfunc1)o [**RasDialFunc2**](/windows/desktop/api/Ras/nc-ras-rasdialfunc2) . La gestione connessione di accesso remoto esegue le notifiche asincrone nel contesto del thread che ha effettuato la chiamata a [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) . Per questo motivo, il thread chiamante non deve terminare fino a quando l'operazione di connessione non è stata stabilita correttamente o si verifica un errore. In modalità sincrona, l'applicazione client può terminare in modo sicuro una volta stabilita la connessione e [arrestare l'operazione di connessione](disconnecting.md) se si verifica un errore.

 

 




