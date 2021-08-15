---
title: Procedura di compilazione generale
description: Pagina di navigazione per il processo di creazione di un'applicazione client/server tramite RPC (Remote Procedure Call).
ms.assetid: 77fa9f30-c370-4ec2-8c23-6037ec520dc3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8402a14ceac3b34114e7b40998038a4e09fb7ba1a915c173f2062f7fab9e63d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118929634"
---
# <a name="general-build-procedure"></a>Procedura di compilazione generale

Il processo per la creazione di un'applicazione client/server tramite Rpc Microsoft è il seguente:

-   Sviluppare l'interfaccia .
-   Sviluppare il server che implementa l'interfaccia .
-   Sviluppare il client che usa l'interfaccia .

Nella figura seguente vengono illustrati questi passaggi.

![processo per la creazione di un'applicazione client-server tramite microsoft rpc](images/appdev.png)

È possibile e comune sviluppare contemporaneamente le applicazioni client e server. Poiché i programmi client e server dipendono dall'interfaccia, tuttavia, l'interfaccia tra di essi deve essere sviluppata prima che il client e il server siano sviluppati, come illustrato nel diagramma precedente.

In questa sezione vengono illustrati i passaggi necessari per la compilazione di un'applicazione client/server con RPC. Le informazioni vengono presentate negli argomenti seguenti:

-   [Sviluppo dell'interfaccia](developing-the-interface.md)
-   [Sviluppo del server](developing-the-server.md)
-   [Sviluppo del client](developing-the-client.md)

 

 




