---
title: Sviluppo del server
description: Quando si crea un programma server per un'applicazione distribuita, è necessario usare il file di intestazione e lo stub del server generati dal compilatore MIDL.
ms.assetid: 2b7b14f5-5692-41b8-bb98-7edd36309d21
keywords:
- RPC (Remote Procedure Call), attività, sviluppo del server
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0fc3405c52c48f531572ab159ad083bad93f95e0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338727"
---
# <a name="developing-the-server"></a>Sviluppo del server

Quando si crea un programma server per un'applicazione distribuita, è necessario usare il file di intestazione e lo stub del server generati dal compilatore MIDL. Per informazioni dettagliate, vedere [sviluppo dell'interfaccia](developing-the-interface.md). Includere il file di intestazione nel file di programma del server C. Compilare lo stub del server con i file di origine C che compongono l'applicazione. Collegare i file oggetto risultanti insieme alla libreria di importazione. Questo processo è illustrato nella figura seguente.

![processo di creazione di un programma server per un'applicazione distribuita](images/srvrdev.png)

Come si può notare dall'esempio nell'illustrazione, per definire l'interfaccia è stato usato un file MIDL denominato MyApp. idl. Il compilatore MIDL ha usato MyApp. idl per produrre MyApp \_ s. c e MyApp. h. Genera inoltre un file di origine C per lo stub client, ma ciò non è pertinente per questa discussione particolare. Il file di origine C per il programma server (in questo caso, Mysrvr. C) deve includere il file MyApp. h. Sarà inoltre necessario includere i file RPC. h e Rpcndr. h.

L'applicazione server è stata sviluppata in due file, Mysrvr. c e Rprocs. c. Il file Mysrvr. c contiene le funzioni necessarie per rendere operativo il programma server. Le procedure remote offerte dal programma server sono contenute nel file Rprocs. c.

I file Mysrvr. c e Rprocs. c sono stati compilati insieme a MyApp \_ s. c per produrre file oggetto. I file oggetto sono stati quindi collegati con la libreria di runtime RPC e con tutte le altre librerie che potrebbero essere necessarie. Il risultato è un programma server eseguibile denominato Mysrvr.exe.

Se non si compila il file IDL con la modalità di compatibilità Open Software Foundation (OSF) ([**/OSF**](/windows/desktop/Midl/-osf)), il programma server deve fornire una funzione per l'allocazione della memoria e una funzione per la deallocazione. Per Windows 2000 e versioni successive di Windows, la modalità consigliata è [**/Oicf**](/windows/desktop/Midl/-oi). Per informazioni dettagliate, vedere modalità di allocazione [e deallocazione della memoria](how-memory-is-allocated-and-deallocated.md)e [puntatori e allocazione di memoria](pointers-and-memory-allocation.md).

 

 