---
title: Livelli di autenticazione
description: Microsoft RPC offre più livelli di autenticazione.
ms.assetid: d9ed938e-4cd4-4355-8d08-830f955dd00c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c5fd25efb84b4ee2834e6f79c7fdd21dd903d55
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221381"
---
# <a name="authentication-levels"></a>Livelli di autenticazione

Microsoft RPC offre più livelli di autenticazione. A seconda del livello di autenticazione, è possibile verificare l'origine del traffico (l'entità di sicurezza che ha inviato il traffico) quando viene stabilita la connessione, quando il client avvia una nuova chiamata di procedura remota o durante ogni scambio di pacchetti tra il client e il server.

Anche quando viene verificato il mittente del traffico, la protezione è ancora debole, dal momento che tale verifica non garantisce che il pacchetto non sia stato modificato o danneggiato in Route; verifica solo che il pacchetto provenga dal principale specificato. Per una maggiore sicurezza, le applicazioni distribuite possono impostare la libreria di runtime RPC per verificare che nessuno dei dati scambiati tra il client e il server venga modificato. La libreria RPC può inoltre crittografare il contenuto di ogni pacchetto prima di inviarlo. In generale, le applicazioni che vogliono proteggere il traffico devono usare solo gli ultimi due livelli: integrità e privacy.

Tenere presente che i livelli più elevati di autenticazione richiedono un sovraccarico computazionale più elevato. Gli sviluppatori devono decidere quale sia l'aspetto più importante per l'applicazione, ad esempio velocità o sicurezza. La maggior parte degli sviluppatori ritiene che, con alcuni test delle prestazioni, possano ottenere livelli di prestazioni accettabili mantenendo una sicurezza adeguata.

Il client e le parti del server dell'applicazione distribuita devono utilizzare lo stesso livello di autenticazione. Per un elenco dei livelli di autenticazione RPC, vedere [costanti a livello di autenticazione](authentication-level-constants.md).

 

 




