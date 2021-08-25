---
title: file compositi
description: Sebbene sia possibile implementare interfacce e oggetti di archiviazione strutturati personalizzati, COM fornisce un'implementazione standard denominata File compositi.
ms.assetid: 23b425e6-dfe5-403b-8f43-de6843a03dcd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 302f7587817f07ec18900f537189a2571c883b0fc43a58eddb823a40fe1c0db3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119867461"
---
# <a name="compound-files"></a>file compositi

Sebbene sia possibile implementare interfacce e oggetti di archiviazione strutturati personalizzati, COM fornisce un'implementazione standard denominata File compositi. L'uso di file compositi consente di risparmiare il lavoro di codifica della propria implementazione dell'archiviazione strutturata e offre diversi vantaggi aggiuntivi derivanti dall'aderenza a uno standard definito. Tra i vantaggi offerti è incluso quanto segue:

-   **Indipendenza dal file system e dalla piattaforma**. Poiché l'implementazione dei file compositi com viene eseguita su file system flat esistenti, i file compositi archiviati nei file system FAT file system, NTFS file system o Macintosh possono essere aperti da applicazioni che usano uno qualsiasi degli altri file system.
-   **Ricercabile.** Poiché gli oggetti separati in un file composto vengono salvati in un formato standard ed è possibile accedervi usando api e interfacce COM standard, qualsiasi utilità browser che usa queste interfacce e API può elencare gli oggetti nel file, anche se i dati all'interno di un determinato oggetto possono essere in un formato proprietario.
-   **Accesso a determinati dati interni.** Poiché l'implementazione di file compositi offre modalità standard di scrittura di determinati tipi di dati, ad esempio informazioni di riepilogo, le applicazioni possono leggere questi dati usando interfacce COM e API.

 

 




