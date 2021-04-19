---
description: I controlli e il testo posizionati nelle finestre di dialogo e nei tabelloni consentono all'utente di interagire con il processo di installazione.
ms.assetid: 2c6204c7-535d-4dda-8394-723ddbf46b96
title: Aggiunta di controlli e testo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 706d071741d742205d0df2b19c4416acf355fd7f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311082"
---
# <a name="adding-controls-and-text"></a>Aggiunta di controlli e testo

I controlli e il testo posizionati nelle finestre di dialogo e nei tabelloni consentono all'utente di interagire con il processo di installazione. Aggiungere una finestra di dialogo all'interfaccia utente, inserendola nella [tabella della finestra di dialogo](dialog-table.md) come descritto in [utilizzo dell'interfaccia utente](using-the-user-interface.md). Riempire le finestre di dialogo e i tabelloni con i controlli popolando rispettivamente la [tabella di controllo](control-table.md) e la [tabella BBControl](bbcontrol-table.md).

Gli attributi iniziali del controllo possono essere specificati nella colonna attributi della tabella dei [controlli](control-table.md). Vedere [attributi del controllo](control-attributes.md).

Per fare in modo che gli attributi del controllo dipendano da una condizione, usare la [tabella ControlCondition](controlcondition-table.md) per disabilitare, abilitare, nascondere o mostrare un controllo in base al valore di una proprietà o di un'istruzione condizionale. È inoltre possibile utilizzare questa tabella per eseguire l'override della specifica del controllo predefinito immesso nella [tabella della finestra di dialogo](dialog-table.md).

Per fare in modo che un evento modifichi un attributo di controllo, sottoscrivere il controllo in un ControlEvent nella [tabella EventMapping](eventmapping-table.md). Un ControlEvent specifica un'azione che deve essere eseguita dal programma di installazione o una modifica negli attributi di uno o più controlli nella finestra di dialogo. Vedere [Panoramica di ControlEvent](controlevent-overview.md). Immettere l'identificatore dell'attributo nella colonna Attribute e l'identificatore di ControlEvent nella colonna Event della [tabella EventMapping](eventmapping-table.md).

Alcuni controlli facilitano la raccolta di informazioni da parte dell'utente. Ad esempio, una casella di controllo consente all'utente di impostare il valore di una proprietà. Vedere la tabella [CheckBox](checkbox-table.md), la tabella [ComboBox](combobox-table.md), la [tabella ListBox](listbox-table.md), la [tabella RadioButton](radiobutton-table.md)e la [tabella ListView](listview-table.md).

Si noti che, per motivi di sicurezza, le proprietà private non possono essere modificate dall'utente che interagisce con l'interfaccia utente. Se una proprietà deve essere impostata dall'interfaccia utente, deve essere una proprietà pubblica e avere un nome in lettere maiuscole. Vedere [informazioni sulle proprietà](about-properties.md).

È possibile fare in modo che la finestra di dialogo presenti informazioni sull'utente o scriverla in un log in risposta alle azioni di installazione compilando la [tabella ActionText](actiontext-table.md).

I controlli possono avere uno stile del carattere predefinito. Per impostare il tipo di carattere e lo stile del carattere di una stringa di testo, anteporre alla stringa dei caratteri visualizzati lo stile { \\ Style} o {&*Style*}. Dove Style è un identificatore elencato nella colonna TextStyle della [tabella TextStyle](textstyle-table.md). Se nessuna di queste è presente, ma la proprietà [**DefaultUIFont**](defaultuifont.md) è definita come uno stile di testo valido, verrà usato tale tipo di carattere.

È consigliabile impostare la proprietà [**DefaultUIFont**](defaultuifont.md) di ogni pacchetto di installazione con un'interfaccia utente nella tabella delle [Proprietà](property-table.md) su uno degli stili predefiniti elencati nella [tabella TextStyle](textstyle-table.md). Se questa proprietà non è specificata, il programma di installazione utilizza il tipo di carattere di sistema. Questo può causare la visualizzazione non corretta delle stringhe di testo del programma di installazione se la tabella codici del pacchetto è diversa dalla tabella codici dell'interfaccia utente predefinita dell'utente.

Per la maggior parte dei controlli, il testo viene visualizzato utilizzando il set di caratteri specificato dalla tabella codici del database. In questo modo si garantisce che il set di caratteri corretto venga utilizzato con le informazioni contenute nel database. Le eccezioni sono i controlli [Edit](edit-control.md), [directory](directorylist-control.md), [PathEdit](pathedit-control.md)e [DirectoryCombo](directorycombo-control.md) , che visualizzano sempre il testo utilizzando il set di caratteri dell'interfaccia utente predefinito dell'utente. I controlli [Text](text-control.md), [ListBox](listbox-control.md)e [ComboBox](combobox-control.md) utilizzano il set di caratteri dell'interfaccia utente predefinito dell'utente se è impostato l' [attributo del controllo UsersLanguage](userslanguage-control-attribute.md) .

In alcuni casi è possibile che un controllo non venga ridisegnato correttamente quando si annulla una finestra di dialogo. Questa operazione deve essere eseguita con l'ordine in cui i controlli ricevono i \_ messaggi di disegno WM dopo che la finestra di dialogo **Annulla** è stata rimossa. Per risolvere il problema, provare a modificare l'ordine dei controlli nella tabella del controllo.

I controlli devono essere sufficientemente grandi da contenere l'intero testo visualizzato in tutte le impostazioni relative alle dimensioni del carattere. I controlli devono essere sufficientemente grandi da contenere l'intero testo localizzato, se è possibile localizzare il testo nell'interfaccia utente. Dimensioni del carattere maggiori o testo localizzato possono richiedere più spazio rispetto al testo originale e possono essere troncati da un controllo troppo piccolo. Per ulteriori informazioni sulla localizzazione del testo dell'interfaccia utente, vedere la sezione [esempio di localizzazione](a-localization-example.md).

 

 



