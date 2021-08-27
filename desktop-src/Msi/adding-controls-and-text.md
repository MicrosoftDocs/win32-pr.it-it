---
description: I controlli e il testo inserito nelle finestre di dialogo e nei manifesti consentono all'utente di interagire con il processo di installazione.
ms.assetid: 2c6204c7-535d-4dda-8394-723ddbf46b96
title: Aggiunta di controlli e testo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58602c4d793b25e1670373773ac8d3f5be2399c6351e56ebe2de1579c78ddcc6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120046031"
---
# <a name="adding-controls-and-text"></a>Aggiunta di controlli e testo

I controlli e il testo inserito nelle finestre di dialogo e nei manifesti consentono all'utente di interagire con il processo di installazione. Aggiungere una finestra di dialogo all'interfaccia utente includendola nella tabella [Dialog](dialog-table.md) come descritto in [Using the Interfaccia utente](using-the-user-interface.md). Compilare le finestre di dialogo e i manifesti con i controlli popolando rispettivamente la tabella [Control](control-table.md) e la tabella [BBControl.](bbcontrol-table.md)

Gli attributi iniziali del controllo possono essere specificati nella colonna Attributi della [tabella Control](control-table.md). Vedere [Attributi del controllo](control-attributes.md).

Per rendere gli attributi del controllo dipendenti da una condizione, usare la tabella [ControlCondition](controlcondition-table.md) per disabilitare, abilitare, nascondere o visualizzare un controllo in base al valore di una proprietà o di un'istruzione condizionale. È anche possibile usare questa tabella per eseguire l'override della specifica del controllo predefinito immesso nella [tabella Dialog](dialog-table.md).

Per fare in modo che un evento cambi l'attributo di un controllo, sottoscrivere il controllo a un oggetto ControlEvent nella [tabella EventMapping](eventmapping-table.md). ControlEvent specifica un'azione che deve essere eseguita dal programma di installazione o una modifica negli attributi di uno o più controlli nella finestra di dialogo. Vedere [Cenni preliminari su ControlEvent](controlevent-overview.md). Immettere l'identificatore dell'attributo nella colonna Attributo e l'identificatore di ControlEvent nella colonna Event della [tabella EventMapping](eventmapping-table.md).

Alcuni controlli facilitano la raccolta di informazioni dell'utente. Ad esempio, una casella di controllo consente all'utente di impostare il valore di una proprietà. Vedere la [tabella CheckBox](checkbox-table.md), [la tabella ComboBox](combobox-table.md), la [tabella ListBox](listbox-table.md), la tabella [RadioButton](radiobutton-table.md)e la [tabella ListView](listview-table.md).

Si noti che per motivi di sicurezza, le proprietà private non possono essere modificate dall'utente che interagisce con l'interfaccia utente. Se una proprietà deve essere impostata dall'interfaccia utente, deve essere una proprietà pubblica e avere un nome in lettere maiuscole. Vedere [Informazioni sulle proprietà](about-properties.md).

È possibile fare in modo che la finestra di dialogo presenti informazioni all'utente o scriverla in un log in risposta alle azioni di installazione compilando la [tabella ActionText](actiontext-table.md).

I controlli possono avere uno stile del carattere predefinito. Per impostare il tipo di carattere e lo stile del carattere di una stringa di testo, antessare alla stringa di caratteri visualizzati { style} o \\ {&*style*}. Dove style è un identificatore elencato nella colonna TextStyle della [tabella TextStyle](textstyle-table.md). Se nessuna di queste proprietà è presente, ma la [**proprietà DefaultUIFont**](defaultuifont.md) è definita come stile di testo valido, verrà usato tale tipo di carattere.

È consigliabile impostare la [**proprietà DefaultUIFont**](defaultuifont.md) di ogni pacchetto di installazione con un'interfaccia utente nella tabella [Proprietà](property-table.md) su uno degli stili predefiniti elencati nella [tabella TextStyle](textstyle-table.md). Se questa proprietà non viene specificata, il programma di installazione usa il tipo di carattere System. Ciò può causare la visualizzazione non corretta delle stringhe di testo da parte del programma di installazione se la tabella codici del pacchetto è diversa dalla tabella codici predefinita dell'interfaccia utente dell'utente.

Per la maggior parte dei controlli, il testo viene visualizzato usando il set di caratteri specificato dalla tabella codici del database. In questo modo si garantisce che il set di caratteri corretto sia usato con le informazioni contenute nel database. Ad eccezione di questo sono i controlli [Edit](edit-control.md), [DirectoryList](directorylist-control.md), [PathEdit](pathedit-control.md)e [DirectoryCombo,](directorycombo-control.md) che visualizzano sempre il testo usando il set di caratteri predefinito dell'interfaccia utente dell'utente. I [controlli Text,](text-control.md) [ListBox](listbox-control.md)e [ComboBox](combobox-control.md) usano il set di caratteri dell'interfaccia utente predefinito dell'utente se è impostato [l'attributo Del controllo UserLanguage.](userslanguage-control-attribute.md)

In alcuni casi un controllo può essere ridisegnato in modo non corretto quando si annulla una finestra di dialogo. Questa operazione ha a che fare con l'ordine in cui i controlli ricevono messaggi WM PAINT dopo la rimozione della finestra \_ di dialogo Annulla.  Per risolvere questo problema, provare a modificare l'ordine dei controlli nella tabella Control.

I controlli devono essere sufficientemente grandi da contenere l'intero testo visualizzato con tutte le impostazioni relative alle dimensioni del carattere. I controlli devono essere sufficientemente grandi da contenere l'intero testo localizzato, se il testo nell'interfaccia utente può essere localizzato. Dimensioni del carattere maggiori o testo localizzato possono richiedere più spazio del testo originale e possono essere troncati da un controllo troppo piccolo. Per altre informazioni sulla localizzazione del testo dell'interfaccia utente, vedere la sezione [Esempio di localizzazione](a-localization-example.md).

 

 



