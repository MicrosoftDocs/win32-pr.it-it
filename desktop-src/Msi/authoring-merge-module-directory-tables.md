---
description: Un modulo unione può essere applicato a un file .msi per aggiungere directory all'installazione, ma non può sostituire o rimuovere directory esistenti.
ms.assetid: 5b808aa2-b2b2-4703-bd57-0b5e1e73b306
title: Creazione di tabelle di directory del modulo merge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f90768dff191b729d482f8ddd58a821a6ed440e79fcd1453ff412aaf7b8a76fb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120086271"
---
# <a name="authoring-merge-module-directory-tables"></a>Creazione di tabelle di directory del modulo merge

Un modulo unione può essere applicato a un file .msi per aggiungere directory all'installazione, ma non può sostituire o rimuovere directory esistenti. La [tabella Directory](directory-table.md) specifica il layout delle directory fornite dal modulo di merge all'installazione di destinazione. In ogni modulo di unione è necessaria una tabella Directory.

Quando si crea la tabella directory in un modulo di merge, usare le linee guida seguenti. Per altre informazioni, vedere [Tabella di directory](directory-table.md) e Uso della tabella di [directory.](using-the-directory-table.md)

-   La struttura di directory aggiunta dal modulo merge deve avere una singola directory radice. La radice deve essere denominata TARGETDIR. L'utente può modificare il valore di TARGETDIR durante l'unione per specificare dove collegare la struttura di directory del modulo all'albero di directory della destinazione.
-   Le tabelle del modulo merge diverse dalla tabella Directory non devono fare riferimento direttamente ai percorsi di directory a TARGETDIR. La posizione di tale riferimento cambia se il valore di TARGETDIR viene modificato dall'utente.
-   Le tabelle nel modulo di merge devono fare riferimento al percorso di una directory figlio di TARGETDIR o di un'altra directory nell'albero del modulo di merge. Eseguire le operazioni seguenti per specificare TARGETDIR come padre di una directory nel modulo di unione. Immettere la directory nella colonna Directory e targetDIR nella colonna Directory \_ padre. Usare la notazione "." nella colonna DefaultDir per indicare che questa directory si trova in TARGETDIR senza una sottodirectory. Per altre informazioni, vedere [Uso della tabella directory.](using-the-directory-table.md)
-   I nomi delle directory aggiunte dal modulo di merge devono usare le convenzioni di denominazione descritte in [Naming Primary Keys in Merge Module Databases](naming-primary-keys-in-merge-module-databases.md). Sono incluse le directory predefinite dalle proprietà, ad esempio [**la proprietà SystemFolder**](systemfolder.md) e [**la proprietà ProgramFilesFolder.**](programfilesfolder.md)
-   Aggiungere un [*GUID*](g-gly.md) a ogni voce della tabella Directory (ad eccezione di TARGETDIR). Sono incluse le voci della tabella Directory che specificano le proprietà [**systemFolder**](systemfolder.md) di Windows Installer, ad esempio SystemFolder.00000000 \_ 0000 \_ 0000 \_ 0000 \_ 000000000000000. La libreria Mergemod.dll aggiunge azioni personalizzate per impostare la **proprietà SystemFolder.**
-   Quando una directory predefinita viene inclusa in un modulo unione, lo strumento di merge aggiunge automaticamente un tipo di azione [personalizzata 51](custom-action-type-51.md) al database di destinazione. L'autore del modulo unione deve assicurarsi che sia inclusa anche una tabella [CustomAction.](customaction-table.md) La tabella CustomAction può essere vuota, ma questa tabella deve esistere nel database di destinazione e garantisce che le directory predefinite modificate siano scritte nei percorsi corretti. Ad esempio, quando una directory di sistema viene inclusa in un modulo merge, l'autore del modulo di merge deve assicurarsi che esista una tabella Azione personalizzata.

    Si noti che l'algoritmo di corrispondenza per la generazione di queste azioni personalizzate di tipo 51 controlla solo che il nome della directory inizi con una delle proprietà [**SystemFolder**](systemfolder.md) predefinite. Non verifica che il nome della directory sia esattamente uguale alla proprietà della directory. Qualsiasi directory che inizia con uno di questi nomi di cartella standard ottiene un'azione personalizzata di tipo 51, anche se il resto del nome non è un GUID. Gli autori devono fare attenzione a non generare corrispondenze false positive e la generazione di azioni personalizzate impreviste sulle chiavi primarie derivate che iniziano con una **delle proprietà SystemFolder.**

Di seguito è riportato un esempio di tabella Directory in un modulo unione e delle directory risolte previste.



| Directory                                              | Directory \_ Parent                                | DefaultDir  |
|--------------------------------------------------------|--------------------------------------------------|-------------|
| Targetdir                                              |                                                  | SourceDir   |
| Dir00.BC82E350 \_ C7FC \_ 11d1 \_ A848-006097ABDE17        | Targetdir                                        | Prog .:MMM \_ |
| SystemFolder.BC82E350 \_ C7FC \_ 11d1 \_ A848-006097ABDE17 | Targetdir                                        | MMM \_ Sys    |
| Dir02.BC82E350 \_ C7FC \_ 11d1 \_ A848-006097ABDE17        | Dir00.BC82E350 \_ C7FC \_ 11d1 \_ A848 \_ 006097ABDE17 | MFC \_ OCX    |



 

È previsto che un modulo unione con la tabella Directory precedente dia come risultato la struttura di directory seguente.



| Directory                                              | Destinazione                                     | Source (Sorgente)                                               |
|--------------------------------------------------------|--------------------------------------------|------------------------------------------------------|
| Dir00.BC82E350 \_ C7FC \_ 11d1 \_ A848-006097ABDE17        | \[Punto di installazione del modulo di merge\]\\         | \[Prog MMM del punto di \] \\ origine del modulo di \_ merge           |
| SystemFolder.BC82E350 \_ C7FC \_ 11d1 \_ A848-006097ABDE17 | \[Cartella Di sistema\]\\                         | \[Merge Module's Source Point \] \\ MMM \_ Sys            |
| Dir02.BC82E350 \_ C7FC \_ 11d1 \_ A848-006097ABDE17        | \[Punto di installazione del modulo \] \\ unione MFC \_ OCX | \[Punto di origine del modulo unione \] \\ MMM \_ Prog \\ MFC \_ OCX |



 

 

 



