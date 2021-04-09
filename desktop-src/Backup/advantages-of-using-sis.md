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
# <a name="advantages-of-using-sis"></a>Vantaggi dell'uso di SIS

I vantaggi dell'utilizzo di SIS e dell'architettura di backup SIS sono i seguenti:

-   Le connessioni tra i collegamenti SIS e i file di supporto vengono gestite automaticamente dall'architettura SIS, perché le applicazioni di backup chiamano le funzioni API di backup SIS.
-   Il contenuto dei reparse point di SIS è opaco per le applicazioni di backup e ripristino, garantendo che gli aggiornamenti agli elementi interni SIS non richiedano una modifica nell'API SIS o nelle applicazioni di backup e ripristino che chiamano funzioni API SIS. È necessario ricompilare l'applicazione solo con una nuova versione della DLL SIS, denominata Sisbkup.dll.
-   Poiché SIS viene implementato come un driver di filtro file system, tiene sempre traccia delle connessioni tra i collegamenti SIS e i file di supporto. Quando si esegue il backup e il ripristino dei file, il backup SIS garantisce che venga eseguito il backup e il ripristino di una sola istanza del file di backup, indipendentemente dal numero di collegamenti SIS che puntano a tale file.

 

 




