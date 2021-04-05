---
description: Il file di funzionalità del concerto del prodotto originale, MNP2000, contiene un errore nel file di Concert.txt.
ms.assetid: 4289bd0c-bdf3-4747-9287-94f737ce4f5c
title: Pianificazione di una patch di aggiornamento di piccole dimensioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f15f3667c6a18ab7a71e86997091bd76d4b15577
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "103886044"
---
# <a name="planning-a-small-update-patch"></a>Pianificazione di una patch di aggiornamento di piccole dimensioni

Il file di funzionalità del concerto del prodotto originale, MNP2000, contiene un errore nel file di Concert.txt. Poiché Windows Installer è stato usato per l'installazione e la configurazione dell'applicazione, è possibile che le correzioni minime per l'applicazione vengano gestite installando un pacchetto di patch di aggiornamento di piccole dimensioni. Un [piccolo aggiornamento](small-updates.md) apporta modifiche a uno o più file di applicazione troppo piccoli per modificare il codice del prodotto. Nell'esempio seguente viene illustrato come creare un pacchetto di patch Windows Installer in grado di applicare l'aggiornamento di piccole dimensioni e fornire una correzione rapida al prodotto MNP2000.

Per creare il piccolo aggiornamento, ottenere prima di tutto un'immagine completamente non compressa del prodotto MNP2000 che include l'errore in Concert.txt. L'immagine deve includere MNP2000.msi e tutti i file di origine descritti in [pianificazione dell'installazione](planning-the-installation.md). Nella discussione seguente viene chiamato immagine di destinazione. L'immagine di destinazione deve essere completamente decompressa perché il processo di creazione della patch non è in grado di generare patch binarie per i file compressi nei file CAB. Inserire il file con estensione msi e tutti i file di origine dell'immagine di destinazione in una cartella denominata target.

Ottenere quindi un'immagine completamente non compressa del prodotto MNP2000 con un file di Concert.txt fisso. Questa operazione è denominata immagine aggiornata nella discussione seguente. Usare uno strumento di modifica del database di installazione, ad esempio ORCA, per aggiornare il file con estensione msi. Se, ad esempio, le dimensioni del Concert.txt con correzione sono inferiori a quelle originali, assicurarsi di immettere le nuove dimensioni nel campo FileSize della tabella file dell'immagine aggiornata. Si noti che poiché il pacchetto è stato modificato, è necessario assegnare un nuovo codice del pacchetto nella proprietà [**Riepilogo numero revisione**](revision-number-summary.md) . Inserire il file con estensione msi e tutti i file di origine dell'immagine aggiornata in una cartella denominata aggiornato.

Ai fini di questo esempio, si supponga che le dimensioni del Concert.txt file cambino. Ciò significa che i campi Filesize nelle tabelle di file della destinazione e del database aggiornato contengono dati diversi.

La [tabella file](file-table.md) seguente identifica il record dall'immagine di destinazione.



| File        | Componente\_ | FileName    | FileSize | Versione | Linguaggio | Attributi | Sequenza |
|-------------|-------------|-------------|----------|---------|----------|------------|----------|
| Concert.txt | Concerto     | Concert.txt | 1000     |         |          | 0          | 1        |



 

La tabella file seguente identifica il record dall'immagine aggiornata.



| File        | Componente\_ | FileName    | FileSize | Versione | Linguaggio | Attributi | Sequenza |
|-------------|-------------|-------------|----------|---------|----------|------------|----------|
| Concert.txt | Concerto     | Concert.txt | 900      |         |          | 0          | 1        |



 

> [!Note]
> Il file deve avere la stessa chiave nelle [tabelle di file](file-table.md) dell'immagine di destinazione e dell'immagine aggiornata. I valori stringa nella colonna file di entrambe le tabelle devono essere identici. I caratteri maiuscoli e minuscoli devono essere anch ' essi identici.
> 
> Seguire le linee guida descritte in [creazione di un pacchetto di patch](creating-a-patch-package.md). Non creare un pacchetto con chiavi della [tabella file](file-table.md) che differiscono solo per le maiuscole/minuscole, perché [Msimsp.exe](msimsp-exe.md) e [Patchwiz.dll](patchwiz-dll.md) chiamano Makecab.exe, che non fa distinzione tra maiuscole e minuscole e la generazione della patch non riesce.

[Continua](creating-a-patch-creation-properties-file.md)

 

 



