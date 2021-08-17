---
title: Gestione connessione
description: I clienti che intendono sviluppare dialer personalizzati usando l'API del servizio di accesso remoto potrebbero voler esaminare Microsoft Gestione connessioni e il Connection Manager Administration Kit.
ms.assetid: c3227aea-ba36-44f6-b69d-2c6aa4be360e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc20979ecd99f904aef158738d49ce1e5bc5a25309288db83dfc99de05959234
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117791585"
---
# <a name="connection-manager"></a>Gestione connessione

I clienti che intendono sviluppare dialer personalizzati usando l'API del servizio di accesso remoto potrebbero voler esaminare Microsoft Gestione connessioni e il Connection Manager Administration Kit. Gestione connessioni è il client di accesso remoto gestito di Microsoft. Consente a un amministratore di creare un pacchetto di configurazione di accesso remoto da distribuire agli utenti remoti dell'amministratore. Per altre informazioni sui Gestione connessioni e sul Connection Manager Administration Kit, vedere la Guida online per Microsoft Windows 2000 Server e sistemi operativi successivi.

È possibile trovare il codice sorgente per un esempio Gestione connessioni'azione personalizzata nell'SDK (Platform Software Development Kit) completo. Platform SDK può essere scaricato dal [sito Web Microsoft](https://msdn.microsoft.com/windowsserver/bb980924.aspx). Dopo l'installazione, il percorso del codice di esempio è %Install Path% Microsoft SDK Samples netds Ras ConnectionManager, dove %Install Path% definisce la directory di installazione di base di \\ \\ Platform SDK \\ \\ \\ (ad esempio, C: \\ Programmi).

Le azioni personalizzate rendono possibile per il client di accesso remoto eseguire azioni specifiche in vari punti del processo di connessione. L'azione personalizzata illustrata nell'esempio regola automaticamente la configurazione del server proxy per una connessione in base all'indirizzo del server della connessione. I clienti possono usare questo esempio come punto di partenza per la creazione di azioni personalizzate.

 

 




