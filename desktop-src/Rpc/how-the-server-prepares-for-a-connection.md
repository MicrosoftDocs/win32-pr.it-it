---
title: Preparazione del server per una connessione
description: Quando un programma server inizia l'esecuzione, deve prima registrare l'interfaccia o le interfacce contenute nella libreria di runtime RPC.
ms.assetid: 3e78e095-f4a4-4ce7-b4a9-936a6c10316b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66314c55ad8e78922f7afcc74c6de3b4afad8234293373cf0cd35a560a1942ec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118929494"
---
# <a name="how-the-server-prepares-for-a-connection"></a>Preparazione del server per una connessione

Quando un programma server inizia l'esecuzione, deve prima registrare l'interfaccia o le interfacce contenute nella libreria di runtime RPC. Crea quindi le informazioni di associazione necessarie. Il programma server deve anche registrare l'endpoint o gli endpoint a cui è in ascolto. Può quindi iniziare ad ascoltare le chiamate client. Questo processo è illustrato nel diagramma seguente.

![un'applicazione server rpc si prepara per le connessioni client](images/srvrcon.png)

A seconda della progettazione scelta, un'applicazione server può scegliere un set di passaggi diverso. L'esempio e l'illustrazione precedenti forniscono un approccio.

In questa sezione vengono fornite informazioni sui passaggi che un processo del server deve eseguire per preparare una connessione. La discussione è suddivisa nelle sezioni seguenti:

-   [Registrazione dell'interfaccia](registering-the-interface.md)
-   [Rendere disponibile il server nella rete](making-the-server-available-on-the-network.md)
-   [Registrazione degli endpoint](registering-endpoints.md)
-   [Ascolto di chiamate client](listening-for-client-calls.md)

 

 




