---
title: Linee guida per l'applicazione del servizio dei nomi
description: Quando si sviluppa l'applicazione distribuita, è necessario fornire agli utenti dell'applicazione un metodo per specificare il nome con cui possono registrare l'applicazione nel database del servizio dei nomi.
ms.assetid: cda997b3-6031-4c0f-affc-c766ba4b7fd5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7e0e79f8ddb9e2076da8d7b8d2c275cb1b1941f6867bfea68dd46bc6c352d49
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118927830"
---
# <a name="name-service-application-guidelines"></a>Linee guida per l'applicazione del servizio dei nomi

Quando si sviluppa l'applicazione distribuita, è necessario fornire agli utenti dell'applicazione un metodo per specificare il nome con cui possono registrare l'applicazione nel database del servizio dei nomi. Questo metodo può essere costituito da un file di dati, da un input della riga di comando o da una finestra di dialogo.

Sebbene l'architettura del servizio dei nomi RPC supporti vari metodi per organizzare le voci del server di un'applicazione, è ottimizzata per le ricerche. Di conseguenza, aggiornamenti frequenti possono ostacolare le prestazioni del servizio dei nomi e dell'applicazione. Per evitare di esportare le informazioni inutilmente, scegliere una progettazione che consenta al server di determinare se le informazioni sono contenute nel database del servizio dei nomi. Inoltre, ogni istanza del server deve esportare nel proprio nome di voce. In caso contrario, sarà difficile per un'istanza modificare i relativi UUID oggetto supportati o le sequenze di protocollo senza intasare le informazioni di un'altra istanza.

Il metodo seguente evita questi problemi e offre prestazioni ottimali, indipendentemente dal servizio dei nomi utilizzato dalla rete.

Per iniziare, progettare l'applicazione in modo che, al primo avvio di una determinata istanza del server, preleva un nome univoco per la voce del server e lo salva nel Registro di sistema insieme alle altre informazioni di configurazione dell'applicazione. Fare quindi in modo che esporti gli eventuali handle di associazione e gli UUID dell'oggetto nella voce del servizio dei nomi.

Le chiamate successive dell'istanza del server devono verificare che la voce del servizio dei nomi sia presente e contenga il set corretto di UUID oggetto e handle di associazione. Una voce mancante può indicare che un amministratore l'ha rimossa o che un'interruzione dell'alimentazione ha causato la perdita delle informazioni del servizio del nome. È importante verificare che gli handle di associazione nella voce siano corretti. se un amministratore aggiunge il supporto TCP/IP a un computer, ad esempio, i server RPC saranno in ascolto su tale sequenza di protocollo quando chiamano [**RpcServerUseAllProtseqs**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseallprotseqs). Tuttavia, se il server non aggiorna la voce del servizio dei nomi, i client non verranno informati che TCP è supportato.

Quando il client importa, deve specificare **NULL** come nome della voce. Se si specifica **NULL,** le funzioni della libreria RPC Microsoft ricercano l'interfaccia in tutte le voci del servizio dei nomi nel dominio o nel gruppo di lavoro del computer client, trovando così le informazioni per ogni istanza.

Se si usano UUID oggetto per rappresentare oggetti noti, ad esempio stampanti, è possibile utilizzare una variante di questo metodo. Anziché esportare le associazioni in una voce, progettare l'applicazione in modo che ogni istanza crei una voce per ogni oggetto supportato, ad esempio "/.:/ printers/Tutto1" e "/.:/ printers/Fax2." Fare in modo che il server esporti i relativi handle di associazione in ogni voce del server, insieme all'UUID dell'oggetto pertinente a tale voce.

In questo caso, un client può cercare una risorsa in base al nome importando dalla voce del server pertinente. non richiede l'UUID dell'oggetto della risorsa. Se ha l'UUID della risorsa ma non il nome, può importare dalla **voce** Null.

 

 




