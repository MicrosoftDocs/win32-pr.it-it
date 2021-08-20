---
description: Le opzioni di ripristino consentono ai richiedenti di comunicare opzioni di ripristino personalizzate ai writer.
ms.assetid: 364550a1-070a-4f7e-bd62-84672959dc21
title: Impostazione delle opzioni di ripristino vss
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58f3ca56a516148bcc11a12fc72aaa6941b0436236525c06c63142107bd18b59
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118121996"
---
# <a name="setting-vss-restore-options"></a>Impostazione delle opzioni di ripristino vss

Le opzioni di ripristino consentono ai richiedenti di comunicare opzioni di ripristino personalizzate ai writer.

## <a name="restore-options"></a>Opzioni di ripristino

La standardizzazione del formato delle opzioni di ripristino consente a writer e richiedenti di gestire le richieste personalizzate comuni. Le opzioni di ripristino vengono impostate dal richiedente chiamando il metodo [**IVssBackupComponents::SetRestoreOptions**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrestoreoptions) fino a una volta per ogni componente selected-for-backup prima di chiamare il metodo [**IVssBackupComponents::P restore.**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore) La stringa passata nel *parametro wszRestoreOptions* al **metodo SetRestoreOptions** può contenere più valori, come descritto di seguito.

## <a name="format"></a>Formato

Il formato delle opzioni di ripristino è una o più coppie nome/valore delimitate da virgole e il nome è preceduto facoltativamente dal nome del sottocomponente a cui si applica. Per i nomi dei componenti e delle opzioni non viene fatto distinzione tra maiuscole e minuscole. La distinzione tra maiuscole e minuscole dei valori è determinata dal writer. Esempio:

``` syntax
"Child1":"Option1"="Value1","Option2"="Value2","Child2\Grandchild3":"Option3"="Value3"
```

In questo esempio, "Option1" si applica solo al sottocomponente "Child1" e ai relativi discendenti, "Option2" si applica a tutti i componenti e ai relativi discendenti e "Option3" si applica solo ai sottocomponenti "Child2 Grandchild3" e ai relativi \\ discendenti.

Il [**metodo SetRestoreOptions**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrestoreoptions) può essere chiamato solo su componenti selezionabili per il backup, mentre i nodi discendenti potrebbero non essere selezionabili per il backup, ma possono essere selezionabili per il ripristino.

## <a name="common-restore-options"></a>Opzioni di ripristino comuni

Queste opzioni di ripristino comuni sono state definite per aumentare l'interoperabilità tra writer e richiedenti.

-   Autorevole

    L'opzione "Autorevole" supporta più valori "Item", ma solo un valore "All".

    L'intero componente è autorevole.

    ``` syntax
    "Authoritative"="All"
    ```

    Solo l'elemento specificato è autorevole. Il formato dell'elemento denominato è definito dal writer. Le designazioni comuni sono " \* " per indicare tutti i file, "..." per indicare tutti i file e le sottodirectory del componente specificato.

    ``` syntax
    "Authoritative"="Item:XXX"
    ```

-   Roll Forward

    Dopo il ripristino di un database, i writer in genere esere il roll forward dei log per il database aggiornato. Nel caso di ripristini incrementali o differenziali, il richiedente usa il metodo [**IVssBackupComponents::SetAdditionalRestores**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setadditionalrestores) per controllare parzialmente il comportamento di gestione dei log. Questa opzione di ripristino consente un controllo più granulare.

    Non eseguire il roll-through dei log.

    ``` syntax
    "Roll Forward"="None"
    ```

    Eseguire il roll-through di tutti i log.

    ``` syntax
    "Roll Forward"="All"
    ```

    Eseguire il roll through dei log fino al punto specificato. Il formato del punto specificato è definito dal writer.

    ``` syntax
    "Roll Forward"="Partial:XXX"
    ```

-   Nome nuovo componente

    Un writer potrebbe voler ripristinare un componente con un nuovo nome. Ad esempio, il ripristino di un database con un nome diverso per ripristinare un singolo elemento. il ripristino con lo stesso nome potrebbe essere necessario per tutti i dati È consigliabile che i writer accettino un percorso logico valido e un nome di componente come valore di queste opzioni. Questo verrà spesso usato con una [*destinazione diretta*](vssgloss-d.md).

    ``` syntax
    "New Component Name"="Logical Path\Component Name"
    ```

 

 



