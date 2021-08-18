---
description: Un piccolo aggiornamento può essere applicato a un'applicazione reinstallando completamente o parzialmente l'applicazione dalla riga di comando o da un programma.
ms.assetid: 6f8b68da-7748-436d-bc95-96e39cf42143
title: Applicazione di piccoli aggiornamenti reinstallando il prodotto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6cb128ec3b62b3f81e8a1f9762bda715fa21e010fa4c16d16c8ca377aa4c5ce1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119145854"
---
# <a name="applying-small-updates-by-reinstalling-the-product"></a>Applicazione di piccoli aggiornamenti reinstallando il prodotto

Un piccolo aggiornamento può essere applicato a un'applicazione reinstallando completamente o parzialmente l'applicazione dalla riga di comando o da un programma.

**Per propagare il piccolo aggiornamento agli utenti correnti (si tratta di una reinstallazione completa) dalla riga di comando**

1.  Dalla riga di comando usare: **msiexec \[ /fvomus** path to _updated .msi file_ o *_\]_* **msiexec /I \[** path to updated .msi _file_ *_\] REINSTALL=ALL REINSTALLMODE=vomus_*.
2.  Il file .msi aggiornato viene memorizzato nella cache nel computer dell'utente. Si noti che non è possibile che l'utente reinstalli il prodotto usando Installazione applicazioni perché il file .msi aggiornato non è ancora presente nel computer dell'utente.

**Per propagare un piccolo aggiornamento agli utenti correnti (si tratta di una reinstallazione completa) da un programma**

1.  Da un programma chiamare [**MsiReinstallProduct**](/windows/desktop/api/Msi/nf-msi-msireinstallproducta) e specificare REINSTALLMODE \_ PACKAGE, REINSTALLMODE \_ FILEOLDERVERSION, REINSTALLMODE \_ MACHINEDATA, REINSTALLMODE \_ USERDATA e REINSTALLMODE \_ SHORTCUT
2.  Il file .msi aggiornato viene memorizzato nella cache nel computer dell'utente.

Il metodo seguente avvia una reinstallazione solo delle funzionalità o dei componenti interessati dal piccolo aggiornamento.

**Per propagare un piccolo aggiornamento agli utenti correnti (si tratta di una reinstallazione parziale)**

1.  Ottenere un elenco dei nomi delle funzionalità e dei componenti interessati dal piccolo aggiornamento.
2.  Dal prompt dei comandi usare: **msiexec /I \[** _path to updated .msi file_ *_\] REINSTALL= \[_* Feature _list \]_ **REINSTALLMODE=vomus**.
3.  Il file .msi aggiornato viene memorizzato nella cache nel computer dell'utente.

 

 



