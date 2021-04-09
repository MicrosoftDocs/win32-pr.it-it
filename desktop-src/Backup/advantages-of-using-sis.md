---
title: Vantaggi dell'uso di SIS
description: I vantaggi dell'utilizzo di SIS e dell'architettura di backup SIS sono i seguenti.
ms.assetid: c72a14a1-92ae-4875-ae73-e277ed2b0c0d
keywords:
- Backup dell'archivio a istanza singola (SIS), vantaggi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dcd1856ce54e817c25830f15f133c7d76c6a80fc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044169"
---
# <a name="advantages-of-using-sis"></a><span data-ttu-id="1cba1-104">Vantaggi dell'uso di SIS</span><span class="sxs-lookup"><span data-stu-id="1cba1-104">Advantages of Using SIS</span></span>

<span data-ttu-id="1cba1-105">I vantaggi dell'utilizzo di SIS e dell'architettura di backup SIS sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="1cba1-105">The advantages of using SIS and the SIS backup architecture are the following:</span></span>

-   <span data-ttu-id="1cba1-106">Le connessioni tra i collegamenti SIS e i file di supporto vengono gestite automaticamente dall'architettura SIS, perché le applicazioni di backup chiamano le funzioni API di backup SIS.</span><span class="sxs-lookup"><span data-stu-id="1cba1-106">The connections between the SIS links and the backing files are automatically maintained by the SIS architecture as your backup applications call the SIS backup API functions.</span></span>
-   <span data-ttu-id="1cba1-107">Il contenuto dei reparse point di SIS è opaco per le applicazioni di backup e ripristino, garantendo che gli aggiornamenti agli elementi interni SIS non richiedano una modifica nell'API SIS o nelle applicazioni di backup e ripristino che chiamano funzioni API SIS.</span><span class="sxs-lookup"><span data-stu-id="1cba1-107">The contents of the SIS reparse points are opaque to your backup and restore applications, ensuring that upgrades to the SIS internals will not require a change in the SIS API or your backup and restore applications that call SIS API functions.</span></span> <span data-ttu-id="1cba1-108">È necessario ricompilare l'applicazione solo con una nuova versione della DLL SIS, denominata Sisbkup.dll.</span><span class="sxs-lookup"><span data-stu-id="1cba1-108">You need only recompile your application with a new version of the SIS DLL, named Sisbkup.dll.</span></span>
-   <span data-ttu-id="1cba1-109">Poiché SIS viene implementato come un driver di filtro file system, tiene sempre traccia delle connessioni tra i collegamenti SIS e i file di supporto.</span><span class="sxs-lookup"><span data-stu-id="1cba1-109">Because SIS is implemented as a file system filter driver, it constantly tracks the connections between the SIS links and the backing files.</span></span> <span data-ttu-id="1cba1-110">Quando si esegue il backup e il ripristino dei file, il backup SIS garantisce che venga eseguito il backup e il ripristino di una sola istanza del file di backup, indipendentemente dal numero di collegamenti SIS che puntano a tale file.</span><span class="sxs-lookup"><span data-stu-id="1cba1-110">When the files are backed up and restored, SIS backup ensures that only one instance of the backing file will be backed up and restored, regardless of the number of SIS links that point to it.</span></span>

 

 




