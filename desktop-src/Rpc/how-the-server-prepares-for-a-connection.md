---
title: Preparazione del server per una connessione
description: Quando un programma server inizia l'esecuzione, deve prima registrare l'interfaccia o le interfacce che contiene con la libreria di runtime RPC.
ms.assetid: 3e78e095-f4a4-4ce7-b4a9-936a6c10316b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9787cc0f4a10da99f1401843450a6e00073e135b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104330623"
---
# <a name="how-the-server-prepares-for-a-connection"></a>Preparazione del server per una connessione

Quando un programma server inizia l'esecuzione, deve prima registrare l'interfaccia o le interfacce che contiene con la libreria di runtime RPC. Vengono quindi create le informazioni di binding necessarie. Il programma server deve inoltre registrare l'endpoint o gli endpoint su cui è in ascolto. Può quindi iniziare ad ascoltare le chiamate del client. Questo processo è illustrato nella figura seguente.

![un'applicazione server RPC si prepara per le connessioni client](images/srvrcon.png)

A seconda della progettazione scelta, un'applicazione server può scegliere un set di passaggi diverso; Nell'esempio precedente viene illustrato un approccio.

In questa sezione vengono presentate informazioni sui passaggi che un processo server deve eseguire per preparare la connessione. La discussione è divisa nelle sezioni seguenti:

-   [Registrazione dell'interfaccia](registering-the-interface.md)
-   [Rendere disponibile il server in rete](making-the-server-available-on-the-network.md)
-   [Registrazione degli endpoint](registering-endpoints.md)
-   [Ascolto delle chiamate client](listening-for-client-calls.md)

 

 




