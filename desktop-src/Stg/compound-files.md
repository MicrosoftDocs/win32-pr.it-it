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
# <a name="compound-files"></a><span data-ttu-id="82c2a-103">file compositi</span><span class="sxs-lookup"><span data-stu-id="82c2a-103">Compound Files</span></span>

<span data-ttu-id="82c2a-104">Sebbene sia possibile implementare le interfacce e gli oggetti di archiviazione strutturati, COM fornisce un'implementazione standard denominata file composti.</span><span class="sxs-lookup"><span data-stu-id="82c2a-104">Although you can implement your own structured storage objects and interfaces, COM provides a standard implementation called Compound Files.</span></span> <span data-ttu-id="82c2a-105">L'uso di file composti consente di evitare il lavoro di codifica della propria implementazione di archiviazione strutturata e conferisce diversi vantaggi aggiuntivi derivati dall'adesione a uno standard definito.</span><span class="sxs-lookup"><span data-stu-id="82c2a-105">Using Compound Files saves you the work of coding your own implementation of structured storage and confers several additional benefits derived from adhering to a defined standard.</span></span> <span data-ttu-id="82c2a-106">Tra i vantaggi offerti è incluso quanto segue:</span><span class="sxs-lookup"><span data-stu-id="82c2a-106">These benefits include the following:</span></span>

-   <span data-ttu-id="82c2a-107">**Indipendenza dalla piattaforma e dal file System**.</span><span class="sxs-lookup"><span data-stu-id="82c2a-107">**File-system and platform independence**.</span></span> <span data-ttu-id="82c2a-108">Poiché l'implementazione dei file composti di COM viene eseguita su sistemi file flat esistenti, i file composti archiviati nei file system FAT file system, NTFS file system o Macintosh possono essere aperti da applicazioni che utilizzano uno degli altri file System.</span><span class="sxs-lookup"><span data-stu-id="82c2a-108">Because COM's Compound Files implementation runs on top of existing flat-file systems, compound files stored in the FAT file system, NTFS file system, or Macintosh file systems can be opened by applications using any one of the other file systems.</span></span>
-   <span data-ttu-id="82c2a-109">**Ricercabile**.</span><span class="sxs-lookup"><span data-stu-id="82c2a-109">**Searchable**.</span></span> <span data-ttu-id="82c2a-110">Poiché gli oggetti separati in un file composto vengono salvati in un formato standard ed è possibile accedervi utilizzando interfacce COM e API standard, qualsiasi utilità browser che utilizza queste interfacce e API può elencare gli oggetti nel file, anche se i dati all'interno di un determinato oggetto possono essere in un formato proprietario.</span><span class="sxs-lookup"><span data-stu-id="82c2a-110">Because the separate objects in a compound file are saved in a standard format and can be accessed using standard COM interfaces and APIs, any browser utility using these interfaces and APIs can list the objects in the file, even though data within a given object may be in a proprietary format.</span></span>
-   <span data-ttu-id="82c2a-111">**Accesso a determinati dati interni**.</span><span class="sxs-lookup"><span data-stu-id="82c2a-111">**Access to certain internal data**.</span></span> <span data-ttu-id="82c2a-112">Poiché l'implementazione dei file composti fornisce metodi standard per la scrittura di determinati tipi di dati, ad esempio le informazioni di riepilogo, le applicazioni possono leggere questi dati usando le interfacce COM e le API.</span><span class="sxs-lookup"><span data-stu-id="82c2a-112">Because the Compound Files implementation provides standard ways of writing certain types of data—summary information, for example—applications can read this data using COM interfaces and APIs.</span></span>

 

 




