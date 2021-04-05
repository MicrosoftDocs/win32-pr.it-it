---
description: ICE17 verifica le situazioni illustrate nell'esempio alla fine di questo argomento.
ms.assetid: a1d9a6e9-4d21-4544-a813-dc82e11f5a26
title: ICE17
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c296273e1de5ae633b2708c92cf0376018e6d32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882945"
---
# <a name="ice17"></a>ICE17

ICE17 verifica le situazioni illustrate nell'esempio alla fine di questo argomento.

## <a name="result"></a>Risultato

ICE17 Visualizza un messaggio di errore o di avviso per ogni situazione nell'esempio. Gli esempi di tali messaggi sono riportati nella tabella seguente.



| Errore o avviso ICE17                                                                                                                                                                                                             | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Pulsante: Button1 della finestra di dialogo: la finestra di dialogo non ha un evento definito nella tabella ControlEvent. Errore <br/>                                                                                                                | È presente un [controllo pulsante](pushbutton-control.md) che non è elencato nella [tabella ControlEvent](controlevent-table.md). Se ICE17 restituisce questo errore in un pulsante per il quale l'attributo di **Abilitazione del controllo** o l'attributo del **controllo visibile** non è impostato nella colonna attributi della [tabella dei controlli](control-table.md), controllare se il controllo dispone anche di una voce nella [tabella ControlCondition](controlcondition-table.md). Il controllo può essere attivato in modo imprevisto, o visibile, se il valore nella colonna condizione diventa true, Enable o show.<br/>                                                                                                                                                                                                                                                                                                                                                    |
| Bitmap: bitmap1 del controllo: bitmap1 della finestra di dialogo: finestra di dialogo non presente nella tabella binaria. Errore <br/>                                                                                                                              | È presente un controllo [bitmap](bitmap-control.md) o un [controllo Icon](icon-control.md), ma la bitmap o l'icona corrispondente non è elencata nella [tabella binaria](binary-table.md). Aggiungere la bitmap o l'icona alla tabella binaria.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| RadioButtonGroup: RadioButton1 del controllo: RadioButton1 della finestra di dialogo: la finestra di dialogo non è presente nella tabella RadioButton. Avviso <br/>                                                                                                   | È presente un [controllo RadioButtonGroup](radiobuttongroup-control.md) con i valori nella colonna Property e la colonna Attribute della [tabella dei controlli](control-table.md); il bit [indiretto](indirect-control-attribute.md) non è impostato nella colonna Attributes. ICE17 pubblica un avviso perché il programma di installazione usa il valore della proprietà come chiave esterna nella tabella RadioButton, ma il valore non è presente nella chiave primaria della tabella. Se viene impostato il bit [indiretto](indirect-control-attribute.md) , la proprietà elencata per il controllo non viene utilizzata come proprietà. viene invece usato come nome della proprietà effettivamente usata.<br/> Questo avviso può essere ignorato se il controllo viene creato in fase di esecuzione. Il [controllo ListBox](listbox-control.md) per nella [finestra di dialogo filesinus](filesinuse-dialog.md) , ad esempio, viene creato solo in fase di esecuzione se durante l'installazione sono presenti file in uso.<br/> |
| ListBox: ListBox1 del controllo: ListBox1 della finestra di dialogo: la finestra di dialogo non è presente nella tabella ListBox. Avviso <br/>                                                                                                                        | È presente un [controllo ListBox](listbox-control.md) con un valore nella colonna Property della tabella dei [controlli](control-table.md) e per il quale il bit [indiretto](indirect-control-attribute.md) non è impostato nella colonna Attributes. ICE17 pubblica un avviso perché il programma di installazione usa il valore della proprietà come chiave esterna nella [tabella ListBox](listbox-table.md), ma il valore non è presente nella chiave primaria della tabella. Se viene impostato il bit [indiretto](indirect-control-attribute.md) , il controllo modifica il valore di una proprietà con un nome che corrisponde al valore della proprietà associata a questo controllo.<br/> Questo avviso può essere ignorato se il controllo viene creato in fase di esecuzione. Il [controllo ListBox](listbox-control.md) per nella [finestra di dialogo filesinus](filesinuse-dialog.md) , ad esempio, viene creato solo in fase di esecuzione se durante l'installazione sono presenti file in uso.<br/>                                |
| ComboBox: ComboBox1 del controllo: ComboBox1 della finestra di dialogo: ByDialog non è presente nell'avviso della tabella ComboBox <br/>                                                                                                                     | È presente un [controllo ComboBox](combobox-control.md) con un valore nella colonna Property della tabella dei [controlli](control-table.md) e per il quale il bit [indiretto](indirect-control-attribute.md) non è impostato nella colonna Attributes. ICE17 pubblica un avviso perché il programma di installazione usa il valore della proprietà come chiave esterna nella [tabella ComboBox](combobox-table.md), ma il valore non è presente nella chiave primaria della tabella. Se viene impostato il bit [indiretto](indirect-control-attribute.md) , il controllo modifica il valore di una proprietà con un nome che corrisponde al valore della proprietà associata a questo controllo.<br/> Questo avviso può essere ignorato se il controllo viene creato in fase di esecuzione. Il [controllo ListBox](listbox-control.md) per nella [finestra di dialogo filesinus](filesinuse-dialog.md) , ad esempio, viene creato solo in fase di esecuzione se durante l'installazione sono presenti file in uso.<br/>                            |
| ListView: ListView1 del controllo: ListView1 della finestra di dialogo: la finestra di dialogo non è presente nella tabella ListView. Avviso <br/>                                                                                                                    | È presente un [controllo ListView](listview-control.md) con un valore nella colonna Property della tabella dei [controlli](control-table.md) e per il quale il bit [indiretto](indirect-control-attribute.md) non è impostato nella colonna Attributes. ICE17 pubblica un avviso perché il programma di installazione usa il valore della proprietà come chiave esterna nella [tabella ListView](listview-table.md), ma il valore non è presente nella chiave primaria della tabella. Se viene impostato il bit [indiretto](indirect-control-attribute.md) , il controllo modifica il valore di una proprietà con un nome che corrisponde al valore della proprietà associata a questo controllo.<br/> Questo avviso può essere ignorato se il controllo viene creato in fase di esecuzione. Il [controllo ListBox](listbox-control.md) per nella [finestra di dialogo filesinus](filesinuse-dialog.md) , ad esempio, viene creato solo in fase di esecuzione se durante l'installazione sono presenti file in uso.<br/>                            |
| Bitmap: "Bitmap2" per il controllo: "Button2" della finestra di dialogo: "finestra di dialogo" non trovata nell'errore di tabella binaria <br/>                                                                                                                         | È disponibile un controllo [pulsante](pushbutton-control.md) o un [controllo CheckBox](checkbox-control.md) per il quale la colonna di testo della [tabella dei controlli](control-table.md) non contiene una chiave esterna nel record della [tabella binaria](binary-table.md) che contiene la bitmap o l'icona.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| Bitmap: "Bitmap3" per il controllo: "RadioButton2" della finestra di dialogo: "finestra di dialogo" non trovata nella tabella binaria o<br/> Icona:' icon1' per il controllo:' RadioButton3' della finestra di dialogo ' dialog ' non trovata nella tabella binaria<br/> Errore <br/> | È disponibile un [controllo RadioButtonGroup](radiobuttongroup-control.md) per il quale la colonna di testo della [tabella RadioButton](radiobutton-table.md) non contiene una chiave esterna nel record della [tabella binaria](binary-table.md) che contiene la bitmap o l'icona.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| Controllo immagine: "Button3" della finestra di dialogo: "finestra di dialogo" contiene l'errore di impostazione degli attributi Icon e bitmap <br/>                                                                                                                     | È presente un controllo [pulsante](pushbutton-control.md), [casella](checkbox-control.md)di controllo o [RadioButtonGroup](radiobuttongroup-control.md) con il bit [icona](icon-control-attribute.md) o bit [bitmap](bitmap-control-attribute.md) impostato nella colonna attributi della tabella dei [controlli](control-table.md). Non è possibile impostare entrambi gli attributi insieme.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |



 

## <a name="example"></a>Esempio

[Tabella di controllo](control-table.md) (parziale)



| Finestra di dialogo\_ | Control      | Tipo             | Attributi | Proprietà     | Testo       |
|----------|--------------|------------------|------------|--------------|------------|
| MyDialog | Button1      | Pulsante       | 0          |              | OK         |
| MyDialog | Bitmap1      | Bitmap           | 0          |              | Bitmap1    |
| MyDialog | RadioButton1 | RadioButtonGroup | 0          | RadioButton1 |            |
| MyDialog | ListBox1     | ListBox          | 0          | ListBox1     |            |
| MyDialog | ComboBox1    | ComboBox         | 0          | ComboBox1    |            |
| MyDialog | ListView1    | ListView         | 0          | ListView1    |            |
| MyDialog | Button2      | Pulsante       | 262144     |              | Bitmap2    |
| MyDialog | RadioButton2 | RadioButtonGroup | 262144     |              | Property2  |
| MyDialog | RadioButton3 | RadioButtonGroup | 524288     |              | Property3  |
| MyDialog | Button3      | Pulsante       | 786432     |              | Ambiguous1 |



 

[Tabella RadioButton](radiobutton-table.md) (parziale)



| Proprietà\_ | JSON | Testo    |
|------------|-------|---------|
| Property2  | 1     | Bitmap3 |
| Property3  | 2     | Icon1   |



 

Le tabelle seguenti sono vuote:

-   [Tabella ControlEvent](controlevent-table.md)
-   [Tabella ListBox](listbox-table.md)
-   [Tabella ComboBox](combobox-table.md)
-   [Tabella ListView](listview-table.md)
-   [Tabella binaria](binary-table.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento ghiaccio](ice-reference.md)
</dt> </dl>

 

 




