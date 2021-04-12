---
description: A partire da Windows Installer 3,0, gli autori possono aggiungere informazioni di sequenziazione delle patch al database del pacchetto di patch nella tabella MsiPatchSequence.
ms.assetid: 9cdcb25f-2c3d-411e-9aae-bdd52df38a97
title: Sequenziazione di patch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa9cbd9aead596abfaeb50d972915bf4d618440d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104234180"
---
# <a name="sequencing-patches"></a>Sequenziazione di patch

A partire da Windows Installer 3,0, gli autori possono aggiungere informazioni di sequenziazione delle patch al database del pacchetto di patch nella tabella [MsiPatchSequence](msipatchsequence-table.md) . Il programma di installazione può utilizzare queste informazioni per determinare quali patch sono applicabili a un pacchetto di installazione, per determinare la migliore sequenza di patch e per installare le patch in un ordine costante indipendentemente dall'ordine in cui vengono fornite al sistema.

**Windows Installer 2,0:** Non supportato. Windows Installer versioni precedenti a Windows Installer 3,0 installare le patch nell'ordine in cui sono fornite al sistema, indipendentemente dal fatto che contengano una tabella [MsiPatchSequence](msipatchsequence-table.md) .

Gli elementi seguenti sono necessari per usare la funzionalità di sequenziazione delle patch.

-   I [pacchetti di patch](patch-packages.md) (file con estensione msp) devono avere una tabella [MsiPatchSequence](msipatchsequence-table.md) contenente le informazioni di sequenziazione. Il programma di installazione installa le patch che non dispongono di una tabella MsiPatchSequence nell'ordine in cui sono fornite al sistema.
-   Le patch vengono installate con Windows Installer 3,0 o versioni successive.

Windows Installer versione 3,0 dispone delle funzioni seguenti che possono essere utilizzate dalle applicazioni per determinare la migliore sequenza di patch.

-   La funzione [**MsiDeterminePatchSequence**](/windows/desktop/api/Msi/nf-msi-msideterminepatchsequencea) accetta un elenco di patch e determina la sequenza che è possibile applicare a un prodotto installato. Questa funzione rappresenta le patch o i prodotti già installati nel sistema.
-   La funzione [**MsiDetermineApplicablePatches**](/windows/desktop/api/Msi/nf-msi-msidetermineapplicablepatchesa) accetta un elenco di patch e determina la sequenza che è possibile applicare a un prodotto installato. Questa funzione non tiene conto di eventuali patch o prodotti già installati nel sistema.

Windows Installer versione 3,0 può applicare più patch a un prodotto in un'unica installazione di patch. Il gruppo di patch può contenere patch che includono informazioni sulle sequenze di patch, ovvero una tabella [MsiPatchSequence](msipatchsequence-table.md) , e patch che non lo sono. Il Windows Installer installa i pacchetti di patch senza questa tabella nell'ordine in cui vengono forniti al sistema. Gli account del programma di installazione per i pacchetti di patch che non dispongono di una tabella MsiPatchSequence, ma che sono stati contrassegnati come patch obsoleti o sostituiti dal metodo descritto nella sezione seguente.

Quando Windows Installer versione 3,0 installa più patch, seguono questi passaggi per determinare la sequenza in cui vengono applicate le singole patch al prodotto:

1.  Le patch installate senza una tabella [MsiPatchSequence](msipatchsequence-table.md) vengono inserite nella sequenza nell'ordine in cui sono state applicate al prodotto. La prima patch applicata viene posizionata per prima nella sequenza.
2.  Le nuove patch senza una [tabella MsiPatchSequence](msipatchsequence-table.md) vengono inserite nella sequenza. Queste patch vengono applicate dall'installazione corrente delle patch. Vengono inserite nell'ordine in cui vengono fornite al sistema e inserite dopo tutte le patch nel passaggio 1.
3.  Le patch obsolete vengono eliminate dalla sequenza di patch.
    > [!Note]  
    > Un pacchetto di patch può specificare nella proprietà [**Riepilogo numero revisione**](revision-number-summary.md) un elenco esplicito di patch obsolete da rimuovere dalla patch. Questo elenco è destinato all'uso da parte di Windows Installer versioni precedenti alla versione 3,0. Windows Installer versione 3,0 rimuove le patch contrassegnate come obsolete dalla sequenza, solo se le patch non dispongono della [tabella MsiPatchSequence](msipatchsequence-table.md).

     

4.  Il programma di installazione esegue la sequenza di patch e determina quali patch sono applicabili nella sequenza specificata. Quando si applicano più patch a un prodotto, ogni patch nella sequenza trasforma anche il database di installazione del prodotto (file con estensione msi). Una patch è applicabile in una determinata sequenza solo se la trasformazione del database è in grado di accettare il [codice del prodotto](product-codes.md), la [**versione**](productversion.md), la [**lingua**](productlanguage.md)e il [**UpgradeCode**](upgradecode.md) risultante dall'applicazione delle trasformazioni di tutti i [pacchetti di patch](patch-packages.md) precedenti al database del prodotto. Il programma di installazione Elimina eventuali patch non applicabili dalla sequenza.
5.  Il programma di installazione inizia a inserire patch con informazioni di sequenziazione nella tabella [MsiPatchSequence](msipatchsequence-table.md) . Le patch di [aggiornamento secondarie](minor-upgrades.md) che includono la tabella MsiPatchSequence vengono inserite nella sequenza dopo le patch sequenziate nei passaggi precedenti e nell'ordine in cui si trovano più a una versione più recente del prodotto dopo l'aggiornamento. Windows Installer Elimina quindi eventuali patch di aggiornamento secondarie non applicabili in questa sequenza.
6.  Le patch di [aggiornamento di piccole dimensioni](small-updates.md) destinate a [aggiornamenti secondari](minor-upgrades.md) con una tabella [MsiPatchSequence](msipatchsequence-table.md) vengono assegnate alla versione più recente della patch di aggiornamento secondaria nella sequenza.
7.  Tutte le patch di [aggiornamento di piccole dimensioni](small-updates.md) che rimangono non assegnate dopo i passaggi precedenti e con la tabella [MsiPatchSequence](msipatchsequence-table.md) vengono inserite nella sequenza prima del primo [aggiornamento secondario](minor-upgrades.md) con la tabella MsiPatchSequence e dopo il database di installazione con estensione msi e le eventuali patch senza la tabella MsiPatchSequence. Windows Installer Elimina quindi eventuali patch di aggiornamento di piccole dimensioni non applicabili in questa sequenza.
8.  Windows Installer versione 3,0 Elimina le patch sostituite dalla sequenza. Quando una patch sostituisce le patch che si verificano prima nella sequenza di patch, la patch contiene tutte le correzioni nelle patch precedenti. Le patch precedenti non sono più necessarie. Per eliminare le patch sostituite, il Windows Installer richiede le informazioni nella tabella [MsiPatchSequence](msipatchsequence-table.md) .
    > [!Note]  
    > Le patch destinate a sostituire un set di patch precedente devono essere create per sostituire le patch precedenti in tutte le famiglie di patch. Le patch di [aggiornamento di piccole dimensioni](small-updates.md) possono sostituire solo piccoli aggiornamenti. Gli aggiornamenti [secondari](minor-upgrades.md) possono sostituire sia gli aggiornamenti di piccole dimensioni che altri aggiornamenti secondari.

     

9.  Patch di [aggiornamento di piccole dimensioni](small-updates.md) che contengono tabelle [MsiPatchSequence](msipatchsequence-table.md) , vengono sequenziate nelle versioni del prodotto in base alle informazioni di sequenziazione nelle tabelle MsiPatchSequence. Questa operazione determina la sequenza di patch finale.

Una patch che non dovrebbe più essere utilizzata può essere eliminata dalla sequenza di patch. Per ulteriori informazioni su come eliminare le patch dalla sequenza di patch, vedere [eliminazione di patch](eliminating-patches.md).

Per un esempio di come la tabella [MsiPatchSequence](msipatchsequence-table.md) può essere usata per applicare le patch nell'ordine in cui sono state create, vedere l'esempio relativo a [più patch](multiple-patching-example.md).

 

 



