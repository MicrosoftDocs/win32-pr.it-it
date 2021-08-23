---
description: Il file di funzionalità Concert del prodotto originale, MNP2000, contiene un errore nel file Concert.txt.
ms.assetid: 4289bd0c-bdf3-4747-9287-94f737ce4f5c
title: Pianificazione di una patch di aggiornamento di piccole dimensioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0aed6c947ee278e7c4856281790a9c392af38734c475e3d40561d72d805f6011
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119519541"
---
# <a name="planning-a-small-update-patch"></a>Pianificazione di una patch di aggiornamento di piccole dimensioni

Il file di funzionalità Concert del prodotto originale, MNP2000, contiene un errore nel file Concert.txt. Poiché Windows programma di installazione è stato usato per l'installazione e l'installazione dell'applicazione, le correzioni secondarie per l'applicazione possono essere gestite installando un piccolo pacchetto di patch di aggiornamento. Un [piccolo aggiornamento](small-updates.md) apporta modifiche a uno o più file dell'applicazione troppo piccoli per modificare il codice del prodotto. L'esempio seguente illustra come creare un pacchetto di patch di Windows Installer in grado di applicare il piccolo aggiornamento e fornire una correzione rapida al prodotto MNP2000.

Per creare l'aggiornamento di piccole dimensioni, ottenere prima un'immagine completamente non compressa del prodotto MNP2000 che include l'errore Concert.txt. L'immagine deve includere MNP2000.msi e tutti i file di origine descritti in [Pianificazione dell'installazione di](planning-the-installation.md). Nella discussione seguente questa operazione è denominata Immagine di destinazione. L'immagine di destinazione deve essere completamente non compressa perché il processo di creazione della patch non è in grado di generare patch binarie per i file compressi in file CAB. Inserire il .msi e tutti i file di origine dell'immagine di destinazione in una cartella denominata Target.

Successivamente, ottenere un'immagine completamente non compressa del prodotto MNP2000 con un file Concert.txt che è stato corretto. Questa operazione è denominata immagine aggiornata nella discussione seguente. Usare uno strumento di modifica del database di installazione, ad esempio Orca, per aggiornare il .msi file. Ad esempio, se le dimensioni del Concert.txt corretto sono inferiori a quelle originali, assicurarsi di immettere le nuove dimensioni nel campo FileSize della tabella File dell'immagine aggiornata. Si noti che poiché il pacchetto è stato modificato, è necessario assegnare un nuovo codice del pacchetto nella [**proprietà Riepilogo numero revisione.**](revision-number-summary.md) Inserire il .msi e tutti i file di origine dell'immagine aggiornata in una cartella denominata Upgraded.

Ai fini di questo esempio, si supponga che le dimensioni del Concert.txt file cambino. Ciò significa che i campi FileSize nelle tabelle File del database di destinazione e aggiornato contengono dati diversi.

La tabella [file seguente identifica](file-table.md) il record dall'immagine di destinazione.



| File        | Componente\_ | FileName    | FileSize | Versione | Linguaggio | Attributi | Sequenza |
|-------------|-------------|-------------|----------|---------|----------|------------|----------|
| Concert.txt | Concerto     | Concert.txt | 1000     |         |          | 0          | 1        |



 

La tabella file seguente identifica il record dall'immagine aggiornata.



| File        | Componente\_ | FileName    | FileSize | Versione | Linguaggio | Attributi | Sequenza |
|-------------|-------------|-------------|----------|---------|----------|------------|----------|
| Concert.txt | Concerto     | Concert.txt | 900      |         |          | 0          | 1        |



 

> [!Note]
> Il file deve avere la stessa chiave nelle tabelle [file dell'immagine](file-table.md) di destinazione e dell'immagine aggiornata. I valori stringa nella colonna File di entrambe le tabelle devono essere identici. Anche le lettere maiuscole e minuscole devono essere identiche.
> 
> Seguire le linee guida descritte in [Creazione di un pacchetto di patch.](creating-a-patch-package.md) Non creare un pacchetto con chiavi tabella [file](file-table.md) che differiscono solo per maiuscole e minuscole, perché [Msimsp.exe](msimsp-exe.md) e [Patchwiz.dll](patchwiz-dll.md) chiamano Makecab.exe, senza distinzione tra maiuscole e minuscole e la generazione di patch ha esito negativo.

[Continua](creating-a-patch-creation-properties-file.md)

 

 



