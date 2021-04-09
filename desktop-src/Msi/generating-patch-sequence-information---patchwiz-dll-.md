---
description: La versione di PATCHWIZ.DLL rilasciata con Windows Installer&\# 160; 3.0 può generare automaticamente informazioni di sequenziazione delle patch e aggiungere alla tabella MsiPatchSequence una nuova patch.
ms.assetid: 03e7eea6-1a37-4c86-a9da-109fbaf20728
title: Generazione di informazioni sulla sequenza di patch (PATCHWIZ.DLL)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff82166f33266a58cd3ef299b2546b04a94ebb14
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967800"
---
# <a name="generating-patch-sequence-information-patchwizdll"></a>Generazione di informazioni sulla sequenza di patch (PATCHWIZ.DLL)

La versione di [PATCHWIZ.DLL](patchwiz-dll.md) rilasciata con Windows Installer 3,0 può generare automaticamente informazioni di sequenziazione delle patch e aggiungere alla [tabella MsiPatchSequence](msipatchsequence-table.md) una nuova patch.

Impostare la \_ \_ \_ Proprietà disabilitata generazione dati sequenza su 1 (uno) nella [tabella delle proprietà](properties-table-patchwiz-dll-.md) del file con estensione PCP per evitare la generazione automatica di informazioni di sequenziazione delle patch. Se questa proprietà è assente, le informazioni vengono generate e aggiunte automaticamente.

Quando il [PATCHWIZ.DLL](patchwiz-dll.md) rilasciato con Windows Installer 3,0 viene usato per generare automaticamente le informazioni di sequenziazione della patch, si verifica quanto segue:

-   Viene aggiunta una nuova riga alla [tabella MsiPatchSequence](msipatchsequence-table.md) per ogni codice prodotto di un'immagine di destinazione elencata nella [tabella TargetImages](targetimages-table-patchwiz-dll-.md).
-   I valori aggiunti alla colonna PatchFamily nelle nuove righe corrispondono ai codici prodotto di destinazione delle immagini di destinazione elencate nella [tabella TargetImages](targetimages-table-patchwiz-dll-.md).
-   I valori aggiunti alle colonne di sequenza nelle nuove righe vengono generati utilizzando la versione del prodotto più elevata di destinazione della patch e l'ora UTC in cui viene generata la patch. Il numero di sequenza è <Product Minor Version> . <Build Major Number> . <Time Stamp 1>. <timestamp 2>.
    -   Il primo campo è la versione del prodotto della versione più recente del prodotto a cui è destinata la patch.
    -   Il secondo campo è il numero di build principale della versione più recente del prodotto a cui è destinata la patch.

    I due campi timestamp rappresentano il timestamp di 32 bit necessario per conteggiare i secondi nell'ora UTC (Coordinated Universal Time).
    > [!Note]  
    > Le versioni del prodotto hanno il formato seguente: <Product Major Version> . <Product Minor Version> . <Build Major Number> . <Build Minor Number> e un prodotto con un numero di versione 2.1.0.0 è una versione successiva a un prodotto con numero di versione 1.2.0.0

     

-   L'attributo msidbPatchSequenceSupersedeEarlier viene immesso nella colonna Attribute delle nuove righe generate per i Service Pack (SP) o per le patch di aggiornamento secondarie. L'attributo msidbPatchSequenceSupersedeEarlier non viene aggiunto a una patch QFE o Small Update.
    > [!Note]  
    > Un Service Pack (SP) deve contenere le correzioni di tutti i QFE che sono stati rilasciati prima. Tuttavia, se un autore della patch imposta la \_ Proprietà Sequence Data \_ sostituzione su 0 (zero) o 1 (uno) nel file con estensione PCP, la colonna attributi di tutte le righe della tabella MsiPatchSequence viene impostata sul valore specificato per i dati di \_ sequenza \_ sostituzione. Gli autori delle patch che richiedono un maggiore controllo devono creare manualmente la colonna attributi.

     

Se si include una [tabella PatchSequence](patchsequence-table--patchwiz-dll-.md) nel file con estensione PCP, la \_ \_ \_ Proprietà disabilitata generazione dati sequenza viene ignorata e le informazioni fornite nella tabella PatchSequence possono essere aggiunte alla [tabella MsiPatchSequence](msipatchsequence-table.md) della patch.

 

 



