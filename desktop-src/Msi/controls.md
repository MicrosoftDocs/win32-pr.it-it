---
description: Gli sviluppatori di pacchetti di installazione possono creare un'interfaccia utente contenente i controlli descritti in questo argomento.
ms.assetid: ed9fa158-9dad-4d2d-8153-78122b19a34e
title: Controlli (Windows Installer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ec286adf25c0642ae044bfd0b89e66182ef6839
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104350246"
---
# <a name="controls-windows-installer"></a>Controlli (Windows Installer)

Gli sviluppatori di pacchetti di installazione possono creare un'interfaccia utente contenente i controlli descritti in questo argomento. Per informazioni su come aggiungere un particolare controllo a una finestra di dialogo, vedere l'argomento relativo a tale controllo e leggere la sezione [aggiunta di controlli e testo](adding-controls-and-text.md).

Alcuni controlli, ad esempio CheckBox e ComboBox, sono associati a una proprietà specificata nella colonna proprietà della tabella dei [controlli](control-table.md). Un utente modifica il valore di questa proprietà interagendo con il controllo. I controlli passivi, ad esempio Billboard e bitmap, non sono associati a tale proprietà.

Per la sicurezza, le proprietà private non possono essere modificate da un utente che interagisce con l'interfaccia utente. Affinché una proprietà venga impostata dall'interfaccia utente, deve essere una proprietà pubblica e in maiuscolo. Vedere anche [informazioni sulle proprietà](about-properties.md).

In alcuni casi è possibile che un controllo non venga ridisegnato correttamente quando si annulla la finestra di dialogo. Questa operazione deve essere eseguita con l'ordine in cui i controlli ricevono i \_ messaggi di disegno WM dopo che la finestra di dialogo Annulla è stata rimossa. Per risolvere il problema, provare a modificare l'ordine dei controlli nella tabella del controllo.



| Nome del controllo                                       | Proprietà associata | Breve descrizione del controllo                                                                                                                                                          |
|----------------------------------------------------|---------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Billboard](billboard-control.md)                 | No                  | Visualizza i tabelloni in base ai messaggi di stato.                                                                                                                                       |
| [Bitmap](bitmap-control.md)                       | No                  | Visualizza un'immagine statica di una bitmap.                                                                                                                                                |
| [CheckBox](checkbox-control.md)                   | Sì                 | Casella di controllo A due Stati.                                                                                                                                                                |
| [ComboBox](combobox-control.md)                   | Sì                 | Elenco a discesa con un campo di modifica.                                                                                                                                                  |
| [DirectoryCombo](directorycombo-control.md)       | Sì                 | Selezionare tutti tranne l'ultimo segmento del percorso.                                                                                                                                       |
| [Elenco di directory](directorylist-control.md)         | Sì                 | Visualizza le cartelle sotto la parte principale del percorso.                                                                                                                                         |
| [Modifica](edit-control.md)                           | Sì                 | Un campo di modifica regolare per qualsiasi stringa o intero.                                                                                                                                       |
| [GroupBox](groupbox-control.md)                   | No                  | Visualizza un rettangolo che raggruppa altri controlli.                                                                                                                             |
| [Collegamento ipertestuale](hyperlink-control.md)                 | No                  | Visualizza un collegamento HTML a un indirizzo, che viene aperto nel browser predefinito. **[Windows Installer 4,5 e versioni precedenti](not-supported-in-windows-installer-4-5.md):** Non supportato.<br/> |
| [Icona](icon-control.md)                           | No                  | Visualizza un'immagine statica di un'icona.                                                                                                                                                 |
| [Linea](line-control.md)                           | No                  | Consente di visualizzare una linea orizzontale.                                                                                                                                                           |
| [ListBox](listbox-control.md)                     | Sì                 | Elenco A discesa senza campo di modifica.                                                                                                                                               |
| [ListView](listview-control.md)                   | Sì                 | Consente di visualizzare una colonna di valori con le icone per la selezione.                                                                                                                                 |
| [MaskedEdit](maskededit-control.md)               | Sì                 | Campo di modifica con una maschera nel campo di testo.                                                                                                                                          |
| [PathEdit](pathedit-control.md)                   | Sì                 | Visualizza il nome della cartella o l'intero percorso in un campo di modifica.                                                                                                                                 |
| [Controllo ProgressBar](progressbar-control.md)     | No                  | Grafico a barre che modifica la lunghezza durante la ricezione dei messaggi di stato.                                                                                                                       |
| [Pulsante](pushbutton-control.md)               | No                  | Visualizza un pulsante di push di base.                                                                                                                                                         |
| [RadioButtonGroup](radiobuttongroup-control.md)   | Sì                 | Gruppo di pulsanti di opzione.                                                                                                                                                             |
| [ScrollableText](scrollabletext-control.md)       | No                  | Visualizza una stringa di testo lungo.                                                                                                                                                       |
| [SelectionTree](selectiontree-control.md)         | Sì                 | Visualizza le informazioni dalla tabella delle funzionalità e consente all'utente di modificare lo stato di selezione.                                                                                     |
| [Text](text-control.md)                           | No                  | Consente di visualizzare il testo statico.                                                                                                                                                                 |
| [VolumeCostList](volumecostlist-control.md)       | No                  | Visualizza le informazioni sui costi su volumi diversi.                                                                                                                                    |
| [VolumeSelectCombo](volumeselectcombo-control.md) | Sì                 | Seleziona il volume da un elenco in ordine alfabetico.                                                                                                                                             |



 

 

 




