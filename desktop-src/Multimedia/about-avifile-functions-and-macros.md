---
title: Informazioni sulle funzioni e le macro AVIFile
description: Informazioni sulle funzioni e le macro AVIFile
ms.assetid: 877f6759-8271-47eb-8a7f-540393e5ae89
keywords:
- AVIFileInit (funzione)
- AVIFileExit (funzione)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f66bbac900b69841fd7cba814aad339731b75727
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045326"
---
# <a name="about-avifile-functions-and-macros"></a>Informazioni sulle funzioni e le macro AVIFile

Le funzioni e le macro AVIFile gestiscono le informazioni nei file basati sul tempo come uno o più *flussi di dati* anziché blocchi di dati contrassegnati, detti blocchi. I flussi di dati fanno riferimento ai componenti di un file basato sul tempo. Un file AVI può contenere diversi tipi di dati, ad esempio una sequenza video, una colonna musicale inglese e una colonna musicale francese. Utilizzando AVIFile, un'applicazione può accedere separatamente a ognuno di questi componenti.

> [!Note]  
> Sebbene le funzioni e le macro AVIFile funzionino con qualsiasi file di RIFF, questa panoramica ne illustra l'uso solo con i file AVI. I file AVI sono in genere i file basati sul tempo usati con le macro e le funzioni di AVIFile.

 

Le funzioni e le macro AVIFile sono contenute in una libreria a collegamento dinamico. Per inizializzare la libreria, usare la funzione [**AVIFileInit**](/windows/desktop/api/Vfw/nf-vfw-avifileinit) . Dopo aver inizializzato la libreria, è possibile usare qualsiasi funzione o macro AVIFile. Per rilasciare la libreria, usare la funzione [**AVIFileExit**](/windows/desktop/api/Vfw/nf-vfw-avifileexit) . AVIFile gestisce un conteggio dei riferimenti delle applicazioni che usano la libreria, ma non quelle che lo hanno rilasciato. Le applicazioni devono bilanciare ogni uso di **AVIFileInit** con una chiamata a **AVIFileExit** per rilasciare completamente la libreria al termine dell'uso di ogni applicazione.

 

 




