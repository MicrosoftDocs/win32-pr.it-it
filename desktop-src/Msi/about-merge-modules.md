---
description: I moduli unione sono essenzialmente file .msi, ovvero l'estensione di file per un pacchetto Windows di installazione del programma di installazione. Un modulo unione standard ha un'estensione msm.
ms.assetid: 580fe58a-4636-4f9a-a68d-4fd0e281e949
title: Informazioni sui moduli unione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca3e6c0ec1d4d7073d85984539ce54b47de92885a64570bc1de709be64748b22
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118640163"
---
# <a name="about-merge-modules"></a>Informazioni sui moduli unione

I moduli unione sono essenzialmente file .msi, ovvero l'estensione di file per un pacchetto Windows di installazione del programma di installazione. Un modulo unione standard ha un'estensione msm.

Un modulo unione non può essere installato da solo perché manca di alcune tabelle di database essenziali presenti in un database di installazione. I moduli unione contengono anche tabelle aggiuntive univoche per se stessi. Per installare le informazioni fornite da un modulo unione con un'applicazione, il modulo deve prima essere unito nel file di .msi'applicazione.

Un modulo unione è costituito dalle parti seguenti:

-   Database [del modulo unione](merge-module-database.md) contenente le proprietà di installazione e la logica di installazione recapitate dal modulo unione.
-   Riferimento [al flusso di informazioni di riepilogo del modulo unione](merge-module-summary-information-stream-reference.md) che descrive il modulo.
-   Un [MergeModule.CABfile cab inet](mergemodule-cabinet.md) archiviato come flusso all'interno del modulo unione. Questo file cab contiene tutti i file richiesti dai componenti recapitati dal modulo unione.

[Più moduli di unione linguistici](multiple-language-merge-modules.md) possono distribuire componenti a un pacchetto di installazione in più lingue. In un modulo unione in più lingue il database contiene le proprietà di installazione e la logica per più lingue e l'archivio inet MergeModule.CABinclude tutti i file necessari per installare i componenti con tutte le lingue supportate dal modulo.

 

 



