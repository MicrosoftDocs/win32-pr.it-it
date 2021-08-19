---
title: Sviluppo del client
description: Lo sviluppo di un programma client RPC è simile allo sviluppo del programma server. Per informazioni sullo sviluppo di un programma server RPC, vedere Sviluppo del server.
ms.assetid: 92276326-d478-479e-8fa4-02a2fce58eb6
keywords:
- Chiamata di procedura remota RPC, attività, sviluppo del client
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fccc719d724ecdcc5631c5f72c5190870f864e06affd45bcce3e7f2da79fb709
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120021897"
---
# <a name="developing-the-client"></a>Sviluppo del client

Lo sviluppo di un programma client RPC è simile allo sviluppo del programma server. Per informazioni sullo sviluppo di un programma server RPC, vedere [Sviluppo del server](developing-the-server.md).

Come nello sviluppo server, il programma client deve includere il file di intestazione generato dal compilatore MIDL dal file con estensione idl. Il compilatore MIDL genera anche un file di origine C contenente lo stub client. È necessario compilare il file di origine C e collegarlo al programma client. Inoltre, il compilatore MIDL genera un file di origine C contenente lo stub del server, ma questo non è rilevante per questa discussione.

Oltre a compilare e collegare lo stub client con i file di programma, è necessario collegare la libreria di importazione (e qualsiasi altra libreria richiesta dal programma client) al programma client. Il processo di creazione di un programma client RPC è illustrato nel diagramma seguente.

![processo di creazione di un programma client per un'applicazione distribuita](images/clntdev.png)

L'esempio nella figura precedente illustra la creazione di un programma client RPC denominato MyClnt.exe. Il primo passaggio consiste nel definire l'interfaccia nel file MyApp.idl. Il compilatore MIDL usa MyApp.idl per generare il file MyApp \_ c.c, che contiene lo stub client. Genera anche il file MyApp.h, che deve essere incluso nel programma client. Il programma client dovrà anche includere i file RPC.h e RPCNDR.h.

Il programma client stesso viene creato nel file MyClnt.c. In un progetto reale, il programma client in genere è costituito da diversi file di origine C. Tutti questi elementi devono essere compilati e collegati tra loro. In questo esempio, tuttavia, viene utilizzato un solo file per semplicità.

I file MyClnt.c e MyApp c.c vengono compilati e collegati insieme alla libreria di runtime RPC e a qualsiasi altra libreria richiesta dal \_ programma client. Il risultato è un programma client eseguibile denominato MyClnt.exe.

Se non si compila il file IDL in modalità di compatibilità OSF ([**/osf**](/windows/desktop/Midl/-osf)), il programma client deve fornire una funzione per l'allocazione della memoria e una funzione per la deallocazione. Per Windows 2000 e versioni successive, la modalità consigliata è [**/Oicf**](/windows/desktop/Midl/-oi). Per informazioni dettagliate, vedere [Come viene allocata e deallocata la](how-memory-is-allocated-and-deallocated.md)memoria e [Puntatori e allocazione di memoria](pointers-and-memory-allocation.md).

 

 