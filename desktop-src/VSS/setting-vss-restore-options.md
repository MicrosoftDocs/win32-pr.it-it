---
description: Le opzioni di ripristino consentono ai richiedenti di comunicare opzioni di ripristino personalizzate ai writer.
ms.assetid: 364550a1-070a-4f7e-bd62-84672959dc21
title: Impostazione delle opzioni di ripristino VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c814ffb94f25229e7f3e17f592c631f13b6717e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310667"
---
# <a name="setting-vss-restore-options"></a>Impostazione delle opzioni di ripristino VSS

Le opzioni di ripristino consentono ai richiedenti di comunicare opzioni di ripristino personalizzate ai writer.

## <a name="restore-options"></a>Opzioni di ripristino

La standardizzazione del formato delle opzioni di ripristino consente a writer e richiedenti di gestire richieste personalizzate comuni. Le opzioni di ripristino vengono impostate dal richiedente chiamando il metodo [**IVssBackupComponents:: SetRestoreOptions**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrestoreoptions) fino a una volta per ogni componente selezionato per il backup prima di chiamare il metodo [**rerestore IVssBackupComponents::P**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore) . La stringa passata nel parametro *wszRestoreOptions* al metodo **SetRestoreOptions** può contenere più valori, come descritto di seguito.

## <a name="format"></a>Formato

Il formato delle opzioni di ripristino è costituito da una o più coppie nome/valore separate da virgole e il nome è facoltativamente preceduto dal nome del sottocomponente a cui si applica. I nomi dei componenti e i nomi delle opzioni non fanno distinzione tra maiuscole e minuscole. La distinzione tra maiuscole e minuscole dei valori è determinata dal writer. Ad esempio:

``` syntax
"Child1":"Option1"="Value1","Option2"="Value2","Child2\Grandchild3":"Option3"="Value3"
```

In questo esempio "opzione1" si applica solo al sottocomponente "child1" e ai relativi discendenti, "opzione2" si applica a tutti i componenti e ai relativi discendenti e "Option3" si applica solo ai \\ sottocomponenti "child2 Grandchild3" e ai relativi discendenti.

Il metodo [**SetRestoreOptions**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrestoreoptions) può essere chiamato solo su componenti selezionabili per il backup, mentre i nodi discendenti non possono essere selezionati per il backup, possono essere selezionati per il ripristino.

## <a name="common-restore-options"></a>Opzioni di ripristino comuni

Queste opzioni di ripristino comuni sono state definite per aumentare l'interoperabilità tra writer e richiedenti.

-   Autorevole

    L'opzione "autorevole" supporta più valori "Item", ma solo un valore "All".

    Questo intero componente è autorevole.

    ``` syntax
    "Authoritative"="All"
    ```

    Solo l'elemento specificato è autorevole. Il formato dell'elemento denominato è definito dal writer. Le designazioni comuni sono " \* " per indicare tutti i file, "..." per indicare tutti i file e le sottodirectory del componente specificato.

    ``` syntax
    "Authoritative"="Item:XXX"
    ```

-   Rollforward

    Dopo il ripristino di un database, in genere i writer eseguono il rollforward dei log per rendere aggiornato il database. Nel caso di ripristini incrementali o differenziali, il richiedente usa il metodo [**IVssBackupComponents:: SetAdditionalRestores**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setadditionalrestores) per controllare parzialmente il comportamento di gestione dei log. questa opzione di ripristino consente un controllo più granulare.

    Non eseguire il rollup dei log.

    ``` syntax
    "Roll Forward"="None"
    ```

    Scorrere tutti i log.

    ``` syntax
    "Roll Forward"="All"
    ```

    Eseguire il rollup dei log fino al punto specificato. Il formato del punto specificato è definito dal writer.

    ``` syntax
    "Roll Forward"="Partial:XXX"
    ```

-   Nome nuovo componente

    Un writer potrebbe voler ripristinare un componente in un nuovo nome. Ad esempio, il ripristino di un database con un nome diverso per il ripristino di un singolo elemento. il ripristino con lo stesso nome richiederebbe a tutti i dati che i writer accettino un percorso logico e un nome di componente validi come valore di questa opzione. Questa operazione viene spesso usata con una [*destinazione diretta*](vssgloss-d.md).

    ``` syntax
    "New Component Name"="Logical Path\Component Name"
    ```

 

 



