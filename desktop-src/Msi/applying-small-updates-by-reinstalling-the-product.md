---
description: Un piccolo aggiornamento può essere applicato a un'applicazione eseguendo una reinstallazione completa o parziale dell'applicazione dalla riga di comando o da un programma.
ms.assetid: 6f8b68da-7748-436d-bc95-96e39cf42143
title: Applicazione di piccoli aggiornamenti con la reinstallazione del prodotto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a27b97ff0274baac5a4ec30df244394a609ed525
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967284"
---
# <a name="applying-small-updates-by-reinstalling-the-product"></a>Applicazione di piccoli aggiornamenti con la reinstallazione del prodotto

Un piccolo aggiornamento può essere applicato a un'applicazione eseguendo una reinstallazione completa o parziale dell'applicazione dalla riga di comando o da un programma.

**Per propagare il piccolo aggiornamento agli utenti correnti (si tratta di una reinstallazione completa) dalla riga di comando**

1.  Dalla riga di comando usare: **msiexec/fvomus \[** _percorso del file con estensione msi aggiornato_ *_\]_* o **msiexec/i \[** _percorso al file MSI aggiornato_ *_\] REINSTALL = ALL REINSTALLMODE = vomus_*.
2.  Il file con estensione msi aggiornato viene memorizzato nella cache nel computer dell'utente. Si noti che l'utente non può reinstallare il prodotto utilizzando Installazione applicazioni perché il file con estensione msi aggiornato non è ancora presente nel computer dell'utente.

**Per propagare un piccolo aggiornamento agli utenti correnti (si tratta di una reinstallazione completa) da un programma**

1.  Da un programma, chiamare [**MsiReinstallProduct**](/windows/desktop/api/Msi/nf-msi-msireinstallproducta) e specificare il \_ pacchetto REINSTALLMODE, REINSTALLMODE \_ FILEOLDERVERSION, REINSTALLMODE \_ MACHINEDATA, REINSTALLMODE \_ UserData e il \_ collegamento REINSTALLMODE
2.  Il file con estensione msi aggiornato viene memorizzato nella cache nel computer dell'utente.

Il metodo seguente avvia una reinstallazione solo delle funzionalità o dei componenti interessati dall'aggiornamento di piccole dimensioni.

**Per propagare un piccolo aggiornamento agli utenti correnti (si tratta di una reinstallazione parziale)**

1.  Ottenere un elenco dei nomi delle funzionalità e dei componenti interessati dall'aggiornamento di piccole dimensioni.
2.  Dal prompt dei comandi usare: **msiexec/i \[** _percorso di aggiornamento del file con estensione msi_ *_\] REINSTALL = \[_*_Feature List \]_ **REINSTALLMODE = vomus**.
3.  Il file con estensione msi aggiornato viene memorizzato nella cache nel computer dell'utente.

 

 



