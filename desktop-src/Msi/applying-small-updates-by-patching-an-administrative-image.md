---
description: Un'installazione amministrativa crea un'immagine di origine di un'applicazione o di un prodotto in una rete.
ms.assetid: 40755461-317f-4764-aaa2-6b8471d52f55
title: Applicazione di piccoli aggiornamenti con l'applicazione di patch a un'immagine amministrativa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1dad22d91e101d79d2bf6ecc0efc8ea9358eda2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967286"
---
# <a name="applying-small-updates-by-patching-an-administrative-image"></a>Applicazione di piccoli aggiornamenti con l'applicazione di patch a un'immagine amministrativa

Un' [installazione amministrativa](administrative-installation.md) crea un'immagine di origine di un'applicazione o di un prodotto in una rete. Gli utenti di un gruppo di lavoro che hanno accesso a questa immagine amministrativa possono installare il prodotto da questa origine. L'aggiornamento dell'applicazione per questo gruppo di lavoro viene eseguito in due passaggi:

-   Per prima cosa, è possibile applicare la patch di aggiornamento di piccole dimensioni all'immagine amministrativa.
-   In secondo luogo, le modifiche apportate al piccolo aggiornamento devono essere propagate agli utenti.

**Per applicare una patch di aggiornamento di piccole dimensioni a un'immagine amministrativa**

1.  Ottenere il piccolo aggiornamento sotto forma di pacchetto di [patch](patch-packages.md). Ad esempio, il piccolo aggiornamento denominato patch. msp.
2.  Ottenere il percorso dell'immagine amministrativa.
3.  Dalla riga di comando usare:

    **msiexec/a** *\[ percorso del file \] di immagine amministrativa. msi* **/p** *patch. msp*

4.  Vengono aggiornati i file dell'applicazione e il file con estensione msi dell'immagine amministrativa. Per un elenco delle opzioni che è possibile usare con Msiexec.exe, vedere [Opzioni della riga di comando](command-line-options.md). Windows Installer determina automaticamente se l'immagine amministrativa utilizza nomi di file brevi e imposta la proprietà [**SHORTFILENAMES**](shortfilenames.md) .
5.  L'immagine amministrativa risultante è identica a quella generata da un'installazione amministrativa usando un CD-ROM di prodotto completo che include l'aggiornamento. Quando i nuovi utenti installano l'applicazione da questa origine ricevono l'applicazione aggiornata.

**Per propagare il piccolo aggiornamento al gruppo di lavoro**

-   I membri del gruppo di lavoro ottengono le modifiche reinstallando l'applicazione dall'immagine amministrativa utilizzando la procedura descritta in [applicazione di piccoli aggiornamenti tramite la reinstallazione del prodotto](applying-small-updates-by-reinstalling-the-product.md).

 

 



