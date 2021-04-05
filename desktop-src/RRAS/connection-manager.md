---
title: Gestione connessione
description: I clienti che intendono sviluppare dialer personalizzati mediante l'API del servizio di accesso remoto potrebbero voler analizzare gestione connessione Microsoft e Connection Manager Administration Kit.
ms.assetid: c3227aea-ba36-44f6-b69d-2c6aa4be360e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7959482542630b6dc90149971df08f7944f83fc
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/20/2020
ms.locfileid: "104046372"
---
# <a name="connection-manager"></a>Gestione connessione

I clienti che intendono sviluppare dialer personalizzati mediante l'API del servizio di accesso remoto potrebbero voler analizzare gestione connessione Microsoft e Connection Manager Administration Kit. Gestione connessione è il client di accesso remoto gestito da Microsoft. Consente a un amministratore di creare un pacchetto di configurazione di accesso remoto da distribuire agli utenti remoti dell'amministratore. Per ulteriori informazioni su gestione connessione e Connection Manager Administration Kit, vedere la Guida in linea per Microsoft Windows Server 2000 e sistemi operativi successivi.

È possibile trovare il codice sorgente per un'azione personalizzata di gestione connessione di esempio nel Software Development Kit (SDK) completo della piattaforma. Platform SDK può essere scaricato dal [sito Web Microsoft](https://msdn.microsoft.com/windowsserver/bb980924.aspx). Al termine dell'installazione, il percorso del codice di esempio è% install path% \\ Microsoft SDK \\ Samples \\ netds \\ RAS \\ ConnectionManager, dove% install path% designa la directory di installazione di base di Platform SDK, ad esempio C: \\ Program Files.

Le azioni personalizzate consentono al client di accesso remoto di eseguire azioni specifiche in diversi punti del processo di connessione. L'azione personalizzata illustrata nell'esempio regola automaticamente la configurazione del server proxy per una connessione in base all'indirizzo del server della connessione. I clienti possono usare questo esempio come punto di partenza per la creazione di azioni personalizzate.

 

 




