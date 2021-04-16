---
description: I moduli merge sono essenzialmente file con estensione msi semplificati, ovvero l'estensione del nome file per un pacchetto di installazione Windows Installer. Un modulo merge standard ha un'estensione del nome di file MSM.
ms.assetid: 580fe58a-4636-4f9a-a68d-4fd0e281e949
title: Informazioni sui moduli merge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c70d416b89f0979d5651480a05052e95b4d32e2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104345171"
---
# <a name="about-merge-modules"></a>Informazioni sui moduli merge

I moduli merge sono essenzialmente file con estensione msi semplificati, ovvero l'estensione del nome file per un pacchetto di installazione Windows Installer. Un modulo merge standard ha un'estensione del nome di file MSM.

Un modulo merge non può essere installato da solo perché mancano alcune tabelle di database fondamentali presenti in un database di installazione. I moduli merge contengono anche tabelle aggiuntive univoche per se stesse. Per installare le informazioni fornite da un modulo merge con un'applicazione, è necessario innanzitutto eseguire il merge del modulo nel file con estensione msi dell'applicazione.

Un modulo merge è costituito dalle parti seguenti:

-   Un [database del modulo merge](merge-module-database.md) contenente le proprietà di installazione e la logica di installazione fornita dal modulo merge.
-   [Riferimento al flusso di informazioni di riepilogo del modulo merge](merge-module-summary-information-stream-reference.md) che descrive il modulo.
-   Un file CAB [MergeModule.CABinet](mergemodule-cabinet.md) archiviato come flusso all'interno del modulo merge. Questo cabinet contiene tutti i file necessari per i componenti forniti dal modulo merge.

I [moduli di Unione con più](multiple-language-merge-modules.md) lingue possono fornire componenti a un pacchetto di installazione in più linguaggi. In un modulo di Unione a più lingue il database contiene le proprietà di installazione e la logica per più di un linguaggio e il cabinet MergeModule.CABinet include tutti i file necessari per installare i componenti con tutte le lingue supportate dal modulo.

 

 



