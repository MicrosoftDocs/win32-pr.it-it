---
title: Vantaggi dell'uso di SIS
description: I vantaggi dell'uso di SIS e dell'architettura di backup SIS sono i seguenti.
ms.assetid: c72a14a1-92ae-4875-ae73-e277ed2b0c0d
keywords:
- Backup dell'archivio a istanza singola (SIS), vantaggi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4cc27eeefe8aa9a61566ea0a1d1e8fd1eca6c718c594ebf232572f16c44e3f7e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118173965"
---
# <a name="advantages-of-using-sis"></a>Vantaggi dell'uso di SIS

I vantaggi dell'uso di SIS e dell'architettura di backup SIS sono i seguenti:

-   Le connessioni tra i collegamenti SIS e i file di backup vengono gestite automaticamente dall'architettura SIS quando le applicazioni di backup chiamano le funzioni API di backup SIS.
-   Il contenuto dei reparse point SIS è opaco per le applicazioni di backup e ripristino, assicurando che gli aggiornamenti agli elementi interni DEL SIS non richiedano una modifica nell'API SIS o nelle applicazioni di backup e ripristino che chiamano funzioni API SIS. È necessario ricompilare l'applicazione solo con una nuova versione della DLL SIS, denominata Sisbkup.dll.
-   Poiché SIS viene implementato come driver file system filtro, tiene costantemente traccia delle connessioni tra i collegamenti SIS e i file di backup. Quando viene eseguito il backup e il ripristino dei file, il backup SIS garantisce che verrà eseguito il backup e il ripristino di una sola istanza del file di backup, indipendentemente dal numero di collegamenti SIS che vi puntano.

 

 




