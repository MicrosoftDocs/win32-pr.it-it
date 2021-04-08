---
description: Un modulo merge può essere applicato a un file con estensione msi per aggiungere directory all'installazione, ma non è possibile sostituire o rimuovere le directory esistenti.
ms.assetid: 5b808aa2-b2b2-4703-bd57-0b5e1e73b306
title: Creazione di tabelle di directory del modulo merge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98332f2c0bda10a5cc076f0ec80df3bf4b2e05aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881101"
---
# <a name="authoring-merge-module-directory-tables"></a>Creazione di tabelle di directory del modulo merge

Un modulo merge può essere applicato a un file con estensione msi per aggiungere directory all'installazione, ma non è possibile sostituire o rimuovere le directory esistenti. La [tabella directory](directory-table.md) specifica il layout delle directory fornite dal modulo merge all'installazione di destinazione. In ogni modulo merge è necessaria una tabella di directory.

Usare le linee guida seguenti durante la creazione della tabella di directory in un modulo merge. Per ulteriori informazioni, vedere [tabella directory](directory-table.md) e [utilizzo della tabella directory](using-the-directory-table.md).

-   La struttura di directory aggiunta dal modulo merge deve avere una singola directory radice. La radice deve essere denominata TARGETDIR. L'utente può modificare il valore di TARGETDIR durante il merge per specificare la posizione in cui alleghi la struttura di directory del modulo nell'albero di directory della destinazione.
-   Le tabelle del modulo merge diverse dalla tabella di directory non devono fare riferimento direttamente ai percorsi della directory a TARGETDIR. Il percorso di tale riferimento viene modificato se l'utente modifica il valore di TARGETDIR.
-   È necessario che le tabelle del modulo merge facciano riferimento al percorso di una directory figlio di TARGETDIR o a un'altra directory nell'albero del modulo merge. Eseguire le operazioni seguenti per specificare TARGETDIR come elemento padre di una directory nel modulo merge. Immettere la directory nella colonna directory e immettere TARGETDIR nella \_ colonna padre della directory. Usare la notazione "." nella colonna DefaultDir per indicare che questa directory si trova in TARGETDIR senza una sottodirectory. Per ulteriori informazioni, vedere [utilizzo della tabella directory](using-the-directory-table.md).
-   I nomi delle directory aggiunte dal modulo merge devono usare le convenzioni di denominazione descritte in [denominazione delle chiavi primarie nei database dei moduli di merge](naming-primary-keys-in-merge-module-databases.md). Sono incluse le directory predefinite da proprietà come la proprietà [**SystemFolder**](systemfolder.md) e la proprietà [**ProgramFilesFolder**](programfilesfolder.md) .
-   Aggiungere un [*GUID*](g-gly.md) a ogni voce nella tabella di directory (ad eccezione di TARGETDIR). Sono incluse le voci della tabella di directory che specificano Windows Installer proprietà [**SystemFolder**](systemfolder.md) , ad esempio SystemFolder. 00000000 \_ 0000 \_ 0000 \_ 0000 \_ 000000000000. La libreria Mergemod.dll aggiunge azioni personalizzate per impostare la proprietà **SystemFolder** .
-   Quando in un modulo merge viene inclusa una directory predefinita, lo strumento di merge aggiunge automaticamente al database di destinazione un' [azione personalizzata di tipo 51](custom-action-type-51.md) . L'autore del modulo merge deve verificare che sia inclusa anche una [tabella CustomAction](customaction-table.md) . La tabella CustomAction può essere vuota, ma la tabella deve esistere nel database di destinazione e garantisce che le directory predefinite modificate vengano scritte nei percorsi corretti. Ad esempio, quando una directory di sistema è inclusa in un modulo merge, l'autore del modulo merge deve verificare che sia presente una tabella delle azioni personalizzata.

    Si noti che l'algoritmo di corrispondenza per la generazione di queste azioni personalizzate di tipo 51 controlla solo che il nome di directory inizi con una delle proprietà [**SystemFolder**](systemfolder.md) predefinite. Non verifica che il nome di directory corrisponda esattamente alla proprietà della directory. Tutte le directory che iniziano con uno di questi nomi di cartella standard ottengono un'azione personalizzata di tipo 51, anche se il resto del nome non è un GUID. È necessario che gli autori si occupino di non generare corrispondenze false positive e la generazione di azioni personalizzate non intenzionali, su chiavi primarie derivate che iniziano con una delle proprietà **SystemFolder** .

Di seguito è riportato un esempio di tabella di directory in un modulo merge e le directory risolte previste.



| Directory                                              | \_Padre directory                                | DefaultDir  |
|--------------------------------------------------------|--------------------------------------------------|-------------|
| TARGETDIR                                              |                                                  | SourceDir   |
| Dir00. BC82E350 \_ C7FC \_ 11D1 \_ A848-006097ABDE17        | TARGETDIR                                        | .: \_ PROG mmm |
| SystemFolder. BC82E350 \_ C7FC \_ 11D1 \_ A848-006097ABDE17 | TARGETDIR                                        | \_Sys mmm    |
| Dir02. BC82E350 \_ C7FC \_ 11D1 \_ A848-006097ABDE17        | Dir00. BC82E350 \_ C7FC \_ 11D1 \_ A848 \_ 006097ABDE17 | \_ocx MFC    |



 

Si prevede che un modulo merge con la tabella di directory precedente provochi la seguente struttura di directory.



| Directory                                              | Destinazione                                     | Source (Sorgente)                                               |
|--------------------------------------------------------|--------------------------------------------|------------------------------------------------------|
| Dir00. BC82E350 \_ C7FC \_ 11D1 \_ A848-006097ABDE17        | \[Punto di installazione del modulo di merge\]\\         | \[\] \\ PROG mmm punto di origine del modulo di merge \_           |
| SystemFolder. BC82E350 \_ C7FC \_ 11D1 \_ A848-006097ABDE17 | \[SystemFolder\]\\                         | \[Il punto di origine del modulo di Unione \] \\ mmm \_ sys            |
| Dir02. BC82E350 \_ C7FC \_ 11D1 \_ A848-006097ABDE17        | \[OCX per il punto di installazione del modulo di merge \] \\ \_ | \[Punto di origine del modulo di merge- \] \\ \_ PROG \\ MFC \_ ocx |



 

 

 



