---
title: Sviluppo del server
description: Quando si crea un programma server per un'applicazione distribuita, è necessario usare il file di intestazione e lo stub del server generati dal compilatore MIDL.
ms.assetid: 2b7b14f5-5692-41b8-bb98-7edd36309d21
keywords:
- RPC Remote Procedure Call , attività, sviluppo del server
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efeba77168abe53e1df823f416c80a015cc63bc7b89c79a0a86d79174a7c78fb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120073406"
---
# <a name="developing-the-server"></a>Sviluppo del server

Quando si crea un programma server per un'applicazione distribuita, è necessario usare il file di intestazione e lo stub del server generati dal compilatore MIDL. Per informazioni dettagliate, vedere [Sviluppo dell'interfaccia](developing-the-interface.md). Includere il file di intestazione nel file di programma C del server. Compilare lo stub del server con i file di origine C che costituiscono l'applicazione. Collegare i file oggetto risultanti insieme alla libreria di importazione. Questo processo è illustrato nel diagramma seguente.

![processo di creazione di un programma server per un'applicazione distribuita](images/srvrdev.png)

Come si può vedere dall'esempio nella figura, per definire l'interfaccia è stato usato un file MIDL denominato MyApp.idl. Il compilatore MIDL ha usato MyApp.idl per produrre MyApp \_ s.c e MyApp.h. Produce anche un file di origine C per lo stub del client, ma questo non è rilevante per questa discussione specifica. Il file di origine C per il programma server (in questo caso Mysrvr.c) deve includere il file Myapp.h. Sarà inoltre necessario includere i file Rpc.h e Rpcndr.h.

L'applicazione server è stata sviluppata in due file, Mysrvr.c e Rprocs.c. Il file Mysrvr.c contiene le funzioni necessarie per l'esecuzione del programma server. Le procedure remote offerte dal programma server sono contenute nel file Rprocs.c.

I file Mysrvr.c e Rprocs.c sono stati compilati insieme a Myapp \_ s.c per produrre file oggetto. I file oggetto sono stati quindi collegati alla libreria di runtime RPC e a tutte le altre librerie che potrebbero essere necessarie. Il risultato è un programma server eseguibile denominato Mysrvr.exe.

Se non si compila il file IDL in modalità di compatibilità Open Software Foundation (OSF) ([**/osf**](/windows/desktop/Midl/-osf)), il programma server deve fornire una funzione per l'allocazione della memoria e una funzione per la deallocazione. Per Windows 2000 e versioni successive di Windows, la modalità consigliata è [**/Oicf**](/windows/desktop/Midl/-oi). Per informazioni dettagliate, vedere [Come viene allocata e deallocata la](how-memory-is-allocated-and-deallocated.md)memoria e [Puntatori e allocazione di memoria.](pointers-and-memory-allocation.md)

 

 