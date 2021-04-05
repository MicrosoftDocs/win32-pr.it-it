---
title: Come il client stabilisce una connessione
description: Per stabilire una sessione di comunicazione client/server con un programma server, è necessario che le applicazioni client con handle espliciti creino un handle di associazione.
ms.assetid: c67c9b1a-084f-4b85-ac6c-8cf25a6b0cca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70c5fd8437fb5821c2b52240256a1938e8de31c3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044831"
---
# <a name="how-the-client-establishes-a-connection"></a>Come il client stabilisce una connessione

Per stabilire una sessione di comunicazione client/server con un programma server, è necessario che le applicazioni client con handle espliciti creino un handle di associazione. Una volta eseguita questa operazione, la libreria di runtime RPC trova il computer che ospita il programma server. Trova quindi l'endpoint su cui il programma server è in ascolto e indirizza la chiamata. La figura seguente illustra questo processo.

![un client RPC stabilisce una connessione con un server RPC](images/clntcon.png)

In questa sezione vengono fornite informazioni sul modo in cui il client si connette al programma server ed esegue le procedure remote che offre. Sono disponibili molti approcci per completare questi passaggi. a seconda della progettazione scelta, un'applicazione può scegliere una serie diversa di passaggi. Questo esempio è semplicemente un modo per eseguire questa operazione.

La discussione è divisa nelle sezioni seguenti:

-   [Creazione di un handle di associazione](creating-a-binding-handle.md)
-   [Esecuzione di una chiamata di procedura remota](making-a-remote-procedure-call.md)
-   [Ricerca del programma server](finding-the-server-program.md)
-   [Invio della chiamata al programma server](sending-the-call-to-the-server-program.md)

 

 




