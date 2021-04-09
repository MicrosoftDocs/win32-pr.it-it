---
title: Linee guida sull'applicazione di servizio nome
description: Quando si sviluppa l'applicazione distribuita, è necessario fornire agli utenti dell'applicazione un metodo per specificare il nome con cui è possibile registrare l'applicazione nel database del servizio nome.
ms.assetid: cda997b3-6031-4c0f-affc-c766ba4b7fd5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c67af441da7a51917ae92751345e860e6b0fc92b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955654"
---
# <a name="name-service-application-guidelines"></a>Linee guida sull'applicazione di servizio nome

Quando si sviluppa l'applicazione distribuita, è necessario fornire agli utenti dell'applicazione un metodo per specificare il nome con cui è possibile registrare l'applicazione nel database del servizio nome. Questo metodo può essere costituito da un file di dati, dall'input della riga di comando o dalla finestra di dialogo.

Sebbene l'architettura del servizio nome RPC supporti diversi metodi per organizzare le voci del server di un'applicazione, è ottimizzata per le ricerche. Di conseguenza, gli aggiornamenti frequenti possono compromettere le prestazioni del servizio nome e dell'applicazione. Per evitare di esportare le informazioni inutilmente, scegliere una progettazione che consenta al server di determinare se le relative informazioni si trovino nel database del servizio nome. Inoltre, ogni istanza del server deve essere esportata nel nome della propria voce. In caso contrario, sarà difficile per un'istanza modificare gli UUID degli oggetti supportati o le sequenze di protocollo senza compromettere le informazioni di un'altra istanza.

Il metodo seguente consente di evitare questi problemi e fornisce prestazioni ottimali, indipendentemente dal servizio dei nomi usato dalla rete.

Per iniziare, progettare l'applicazione in modo che la prima volta che viene avviata un'istanza del server specificata selezioni un nome univoco per la voce del server e salva il nome nel registro di sistema insieme alle altre informazioni di configurazione dell'applicazione. Quindi, fare in modo che esporti gli handle di binding e gli UUID degli oggetti, se presenti, alla relativa voce di servizio del nome.

Le chiamate successive dell'istanza del server devono verificare che la voce del servizio del nome sia presente e che contenga il set corretto di UUID degli oggetti e degli handle di associazione. Una voce mancante può indicare che un amministratore l'ha rimossa o che un'interruzione dell'alimentazione ha causato la perdita delle informazioni sul servizio del nome. È importante verificare che gli handle di associazione nella voce siano corretti; Se un amministratore aggiunge il supporto TCP/IP a un computer, ad esempio, i server RPC saranno in ascolto su tale sequenza di protocollo quando chiamano [**RpcServerUseAllProtSeqs**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseallprotseqs). Tuttavia, se il server non aggiorna la voce del servizio del nome, i client non saranno informati che TCP è supportato.

Quando il client importa, deve specificare **null** come nome di voce. Se si specifica **null** , le funzioni della libreria RPC di Microsoft cercano l'interfaccia in tutte le voci del servizio nome del dominio o del gruppo di lavoro del computer client, individuando quindi le informazioni per ogni istanza.

Se si utilizzano UUID di oggetti per rappresentare oggetti noti, ad esempio stampanti, è possibile utilizzare una variante di questo metodo. Anziché esportare i binding in una voce, progettare l'applicazione in modo che ogni istanza crei una voce per ogni oggetto supportato, ad esempio "/.:/ stampanti/laser1 "e"/.:/ stampanti/Laser2 ". Quindi, fare in modo che il server esporti gli handle di binding a ogni voce del server, insieme all'UUID dell'oggetto pertinente per tale voce.

In questo caso, un client può cercare una risorsa in base al nome importando dalla voce del server pertinente. non richiede l'UUID dell'oggetto della risorsa. Se ha l'UUID della risorsa ma non il nome, può importare dalla voce **null** .

 

 




