---
description: La versione di PATCHWIZ.DLL rilasciata con Windows Installer&160;3.0 può generare automaticamente informazioni di sequenziazione delle patch e aggiungere alla tabella \# MsiPatchSequence una nuova patch.
ms.assetid: 03e7eea6-1a37-4c86-a9da-109fbaf20728
title: Generazione di informazioni sulla sequenza di patch (PATCHWIZ.DLL)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03094d9df26f4565db5b3a31c9a27c58a0bb45dac8aac93b2fefce34104d58c1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118947022"
---
# <a name="generating-patch-sequence-information-patchwizdll"></a>Generazione di informazioni sulla sequenza di patch (PATCHWIZ.DLL)

La versione di [PATCHWIZ.DLL](patchwiz-dll.md) rilasciata con Windows Installer 3.0 può generare automaticamente informazioni di sequenziazione delle patch e aggiungere una nuova patch alla tabella [MsiPatchSequence.](msipatchsequence-table.md)

Impostare la proprietà SEQUENCE DATA GENERATION DISABLED su \_ 1 (uno) nella tabella Delle proprietà del file con estensione pcp per impedire la generazione automatica delle informazioni di \_ \_ sequenziazione delle patch. [](properties-table-patchwiz-dll-.md) Se questa proprietà è assente, le informazioni vengono generate e aggiunte automaticamente.

Quando il [PATCHWIZ.DLL](patchwiz-dll.md) rilasciato con Windows Installer 3.0 viene usato per generare automaticamente le informazioni di sequenziazione delle patch, si verifica quanto segue:

-   Viene aggiunta una nuova riga alla tabella [MsiPatchSequence per](msipatchsequence-table.md) ogni codice prodotto di un'immagine di destinazione elencata nella tabella [TargetImages](targetimages-table-patchwiz-dll-.md).
-   I valori aggiunti alla colonna PatchFamily nelle nuove righe corrispondono ai codici prodotto di destinazione delle immagini di destinazione elencate nella [tabella TargetImages](targetimages-table-patchwiz-dll-.md).
-   I valori aggiunti alle colonne Sequenza nelle nuove righe vengono generati usando la versione più recente del prodotto di destinazione della patch e l'ora UTC in cui viene generata la patch. Il numero di sequenza è <Product Minor Version> <Build Major Number> . <timestamp 1>.<Timestamp 2>.
    -   Il primo campo è la versione del prodotto della versione più recente del prodotto di destinazione della patch.
    -   Il secondo campo è il numero principale della build della versione più recente del prodotto di destinazione della patch.

    I due campi timestamp account per il timestamp a 32 bit necessario per contare i secondi in Coordinated Universal Time (UTC).
    > [!Note]  
    > Le versioni del prodotto hanno il formato seguente: . . . e un prodotto con numero di versione 2.1.0.0 è una versione successiva rispetto a un prodotto con numero di versione <Product Major Version> <Product Minor Version> <Build Major Number> <Build Minor Number> 1.2.0.0

     

-   L'attributo msidbPatchSequenceSupersedeEarlier viene immesso nella colonna Attributo delle nuove righe generate per Service Pack (SP) o patch di aggiornamento secondarie. L'attributo msidbPatchSequenceSupersedeEarlier non viene aggiunto a una patch di aggiornamento QFE o di piccole dimensioni.
    > [!Note]  
    > Un Service Pack (SP) deve contenere le correzioni di tutti i QFE rilasciati prima di esso. Tuttavia, se un autore di patch imposta la proprietà SEQUENCE DATA SUPERSEDENCE su 0 (zero) o 1 (uno) nel file con estensione pcp, la colonna Attributes di tutte le righe della tabella MsiPatchSequence viene impostata sul valore specificato per \_ \_ SEQUENCE DATA \_ \_ SUPERSEDENCE. Gli autori di patch che richiedono un maggiore controllo devono creare manualmente la colonna Attributi.

     

Se si include una tabella [PatchSequence](patchsequence-table--patchwiz-dll-.md) nel file con estensione pcp, la proprietà SEQUENCE DATA GENERATION DISABLED viene ignorata e le informazioni fornite nella tabella PatchSequence possono essere aggiunte alla tabella \_ \_ \_ [MsiPatchSequence](msipatchsequence-table.md) della patch.

 

 



