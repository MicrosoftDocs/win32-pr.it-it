---
title: Operazioni asincrone
description: Quando RasDial viene richiamato come operazione asincrona, la funzione restituisce immediatamente .
ms.assetid: f165b4a7-00fb-4888-8225-8fd106e113f2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0db03b1d9d3c98e84bc9a2f4fd80ec7206d9a4524608cdbc96cca83f89d0ea00
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120030561"
---
# <a name="asynchronous-operations"></a>Operazioni asincrone

Quando [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) viene richiamato come operazione asincrona, la funzione restituisce immediatamente . In modalità asincrona, la chiamata [](notification-handlers.md) **RasDial** deve specificare un gestore di notifica che il Gestione connessioni di accesso remoto usa per informare il client ogni volta che l'operazione di connessione cambia stato o si verifica un errore.

Il gestore di notifica può essere una finestra per ricevere messaggi o una funzione di callback [**RasDialFunc,**](/windows/desktop/api/Ras/nc-ras-rasdialfunc) [**RasDialFunc1**](/windows/desktop/api/Ras/nc-ras-rasdialfunc1)o [**RasDialFunc2.**](/windows/desktop/api/Ras/nc-ras-rasdialfunc2) L'Gestione connessioni di accesso remoto effettua le notifiche asincrone nel contesto del thread che ha effettuato la [**chiamata RasDial.**](/windows/desktop/api/Ras/nf-ras-rasdiala) Per questo motivo, il thread chiamante non deve terminare fino a quando l'operazione di connessione non è stata stabilita correttamente o non si verifica un errore. Come in modalità sincrona, l'applicazione client può terminare in modo [](disconnecting.md) sicuro dopo aver stabilito la connessione e deve arrestare l'operazione di connessione in caso di errore.

 

 




