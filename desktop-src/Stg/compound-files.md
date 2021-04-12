---
title: file compositi
description: Sebbene sia possibile implementare le interfacce e gli oggetti di archiviazione strutturati, COM fornisce un'implementazione standard denominata file composti.
ms.assetid: 23b425e6-dfe5-403b-8f43-de6843a03dcd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62be79f09afd23e53a569b76ad3e0af46cae2f9e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221045"
---
# <a name="compound-files"></a>file compositi

Sebbene sia possibile implementare le interfacce e gli oggetti di archiviazione strutturati, COM fornisce un'implementazione standard denominata file composti. L'uso di file composti consente di evitare il lavoro di codifica della propria implementazione di archiviazione strutturata e conferisce diversi vantaggi aggiuntivi derivati dall'adesione a uno standard definito. Tra i vantaggi offerti è incluso quanto segue:

-   **Indipendenza dalla piattaforma e dal file System**. Poiché l'implementazione dei file composti di COM viene eseguita su sistemi file flat esistenti, i file composti archiviati nei file system FAT file system, NTFS file system o Macintosh possono essere aperti da applicazioni che utilizzano uno degli altri file System.
-   **Ricercabile**. Poiché gli oggetti separati in un file composto vengono salvati in un formato standard ed è possibile accedervi utilizzando interfacce COM e API standard, qualsiasi utilità browser che utilizza queste interfacce e API può elencare gli oggetti nel file, anche se i dati all'interno di un determinato oggetto possono essere in un formato proprietario.
-   **Accesso a determinati dati interni**. Poiché l'implementazione dei file composti fornisce metodi standard per la scrittura di determinati tipi di dati, ad esempio le informazioni di riepilogo, le applicazioni possono leggere questi dati usando le interfacce COM e le API.

 

 




