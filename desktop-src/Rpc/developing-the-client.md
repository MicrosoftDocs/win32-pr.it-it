---
title: Sviluppo del client
description: Lo sviluppo di un programma client RPC è simile allo sviluppo del programma server. Per informazioni sullo sviluppo di un programma server RPC, vedere sviluppo del server.
ms.assetid: 92276326-d478-479e-8fa4-02a2fce58eb6
keywords:
- RPC (Remote Procedure Call), attività, sviluppo del client
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10ceddedc4ccfd1d068e3452b64ed8c6b54a621d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103963363"
---
# <a name="developing-the-client"></a>Sviluppo del client

Lo sviluppo di un programma client RPC è simile allo sviluppo del programma server. Per informazioni sullo sviluppo di un programma server RPC, vedere [sviluppo del server](developing-the-server.md).

Come nello sviluppo di server, il programma client deve includere il file di intestazione generato dal compilatore MIDL dal file con estensione IDL. Il compilatore MIDL genera anche un file di origine C contenente lo stub client. È necessario compilare il file di origine C e collegarlo al programma client. Inoltre, il compilatore MIDL genera un file di origine C contenente lo stub del server, ma ciò non è pertinente per questa discussione.

Oltre a compilare e collegare lo stub client con i file di programma, è necessario collegare la libreria di importazione (e tutte le altre librerie necessarie al programma client) al programma client. Nel diagramma seguente viene illustrato il processo di creazione di un programma client RPC.

![processo di creazione di un programma client per un'applicazione distribuita](images/clntdev.png)

Nell'esempio riportato nella figura precedente viene illustrata la creazione di un programma client RPC denominato MyClnt.exe. Il primo passaggio consiste nel definire l'interfaccia nel file MyApp. idl. Il compilatore MIDL USA MyApp. idl per generare il file MyApp \_ c. c, che contiene lo stub client. Genera inoltre il file MyApp. h, che deve essere incluso nel programma client. Anche il programma client dovrà includere i file RPC. h e RPCNDR. h.

Il programma client viene creato nel file MyClnt. c. In un progetto reale, il programma client in genere è costituito da diversi file di origine C. Tutti questi elementi devono essere compilati e collegati tra loro. Tuttavia, in questo esempio viene usato un solo file per semplicità.

I file MyClnt. c e MyApp \_ c. c vengono compilati e collegati insieme alla libreria di runtime RPC e a qualsiasi altra libreria necessaria per il programma client. Il risultato è un programma client eseguibile denominato MyClnt.exe.

Se non si compila il file IDL in modalità di compatibilità OSF ([**/OSF**](/windows/desktop/Midl/-osf)), il programma client deve fornire una funzione per l'allocazione della memoria e una funzione per la deallocazione. Per Windows 2000 e versioni successive, la modalità consigliata è [**/Oicf**](/windows/desktop/Midl/-oi). Per informazioni dettagliate, vedere modalità di allocazione [e deallocazione della memoria](how-memory-is-allocated-and-deallocated.md)e [puntatori e allocazione di memoria](pointers-and-memory-allocation.md).

 

 