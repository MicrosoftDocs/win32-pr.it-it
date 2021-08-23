---
description: Un'installazione amministrativa crea un'immagine di origine di un'applicazione o di un prodotto in una rete.
ms.assetid: 40755461-317f-4764-aaa2-6b8471d52f55
title: Applicazione di piccoli aggiornamenti tramite l'applicazione di patch a un'immagine amministrativa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e02c8e3eb606dc92c60a86dd8e3216cbc99603200a87e5ee5dda0983fb7ad34d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119559161"
---
# <a name="applying-small-updates-by-patching-an-administrative-image"></a>Applicazione di piccoli aggiornamenti tramite l'applicazione di patch a un'immagine amministrativa

[Un'installazione amministrativa](administrative-installation.md) crea un'immagine di origine di un'applicazione o di un prodotto in una rete. Gli utenti di un gruppo di lavoro che hanno accesso a questa immagine amministrativa possono installare il prodotto da questa origine. L'aggiornamento dell'applicazione per questo gruppo di lavoro viene eseguito in due passaggi:

-   In primo luogo, la piccola patch di aggiornamento può essere applicata all'immagine amministrativa.
-   In secondo momento, le modifiche apportate al piccolo aggiornamento devono essere propagate agli utenti.

**Per applicare una piccola patch di aggiornamento a un'immagine amministrativa**

1.  Ottenere il piccolo aggiornamento sotto forma di un [pacchetto di patch](patch-packages.md). Ad esempio, il piccolo aggiornamento denominato Patch.msp.
2.  Ottenere il percorso dell'immagine amministrativa.
3.  Dalla riga di comando usare:

    **msiexec /a** *\[ percorso dell'immagine amministrativa .msi file \]* **/p** *patch.msp*

4.  In questo modo i file dell'applicazione e .msi file dell'immagine amministrativa. Per un elenco delle opzioni che possono essere usate con Msiexec.exe, vedere [Opzioni della riga di comando.](command-line-options.md) Windows Il programma di installazione determina automaticamente se l'immagine amministrativa usa nomi di file brevi e imposta la [**proprietà SHORTFILENAMES.**](shortfilenames.md)
5.  L'immagine amministrativa risultante è uguale a quella prodotta da un'installazione amministrativa usando un CD-ROM completo del prodotto che include l'aggiornamento. Quando i nuovi utenti installano l'applicazione da questa origine, ricevono l'applicazione aggiornata.

**Per propagare l'aggiornamento di piccole dimensioni al gruppo di lavoro**

-   I membri del gruppo di lavoro ottengono le modifiche reinstallando l'applicazione dall'immagine amministrativa usando la procedura descritta in Applicazione di piccoli aggiornamenti [reinstallando il prodotto](applying-small-updates-by-reinstalling-the-product.md).

 

 



