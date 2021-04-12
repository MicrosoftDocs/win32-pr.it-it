---
description: Un provider di rete è una DLL che supporta un protocollo di rete specifico.
ms.assetid: ebd47c1b-f427-4fa1-a2ec-1e73be297bef
title: Provider di rete
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30e3cc231f461d48e7ce71d908cb92f6cd06eabd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232822"
---
# <a name="network-providers"></a>Provider di rete

Un provider di rete è una DLL che supporta un protocollo di rete specifico. Implementa inoltre l' [API del provider di rete](network-provider-api.md). In questo modo è possibile interagire con il sistema operativo Windows per ricevere richieste di rete standard, ad esempio richieste di connessione o disconnessione. Per gestire queste richieste, il provider di rete chiama quindi l'API specifica della rete che è appropriata per il protocollo di rete supportato dal provider di rete. In altre parole, il provider di rete esegue il wrapping della funzionalità specifica della rete in una DLL, che espone un'interfaccia standard a Windows.

Utilizzando i provider di rete, Windows può supportare molti tipi diversi di protocolli di rete senza dover individuare i dettagli specifici della rete di ogni rete. Questa operazione è essenziale perché i nuovi protocolli di rete sono in fase di sviluppo. Con i provider di rete, il supporto di un nuovo protocollo richiede semplicemente la creazione e l'installazione di un nuovo provider di rete.

Per informazioni sulle funzioni e sulle strutture del provider di rete, vedere gli argomenti seguenti:

-   [Funzioni del provider di rete](authentication-functions.md)
-   [Strutture del provider di rete](authentication-structures.md)

 

 



