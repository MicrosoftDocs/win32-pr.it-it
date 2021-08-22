---
description: ICE17 verifica le situazioni illustrate nell'esempio alla fine di questo argomento.
ms.assetid: a1d9a6e9-4d21-4544-a813-dc82e11f5a26
title: ICE17
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b5e9714edebd666173a82c75fc6e8fed54a511c64adaa387013648b2f190e88
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119529201"
---
# <a name="ice17"></a>ICE17

ICE17 verifica le situazioni illustrate nell'esempio alla fine di questo argomento.

## <a name="result"></a>Risultato

ICE17 visualizza un messaggio di errore o di avviso per ognuna delle situazioni dell'esempio. Gli esempi di questi messaggi sono illustrati nella tabella seguente.



| Errore o avviso ICE17                                                                                                                                                                                                             | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| PushButton: Button1 della finestra di dialogo: MyDialog non ha un evento definito nella tabella ControlEvent. Errore <br/>                                                                                                                | È presente un [controllo Pushbutton](pushbutton-control.md) non elencato nella [tabella ControlEvent](controlevent-table.md). Se ICE17 restituisce questo errore in un controllo PushButton per cui l'attributo Enable **Control** o **Visible Control** non è impostato nella colonna Attributi della tabella [Control](control-table.md), controllare se il controllo include anche una voce nella [tabella ControlCondition](controlcondition-table.md). Il controllo può diventare in modo imprevisto abilitato o visibile se il valore nella colonna Condizione diventa True, Abilita o Mostra.<br/>                                                                                                                                                                                                                                                                                                                                                    |
| Bitmap: Bitmap1 del controllo: Bitmap1 della finestra di dialogo: MyDialog non si trova nella tabella Binary. Errore <br/>                                                                                                                              | È presente un [controllo Bitmap o](bitmap-control.md) Un controllo [Icona](icon-control.md), ma la bitmap o l'icona corrispondente non è elencata nella [tabella Binaria](binary-table.md). Aggiungere la bitmap o l'icona alla tabella Binary.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| RadioButtonGroup: RadioButton1 del controllo: RadioButton1 della finestra di dialogo: MyDialog non si trova nella tabella RadioButton. Avviso <br/>                                                                                                   | È presente un [controllo RadioButtonGroup](radiobuttongroup-control.md) con valori nella colonna Proprietà e nella colonna Attributo della [tabella Control](control-table.md). Il bit [indiretto](indirect-control-attribute.md) non è impostato nella colonna Attributi. ICE17 invia un avviso perché il programma di installazione usa il valore della proprietà come chiave esterna nella tabella RadioButton, ma il valore non è presente nella chiave primaria della tabella. Se il bit [indiretto](indirect-control-attribute.md) è impostato, la proprietà elencata per il controllo non viene utilizzata come proprietà . viene invece usato come nome della proprietà effettivamente usata.<br/> Questo avviso può essere ignorato se il controllo viene creato in fase di esecuzione. Ad esempio, il [controllo ListBox](listbox-control.md) per nella [finestra di dialogo FilesInUse](filesinuse-dialog.md) viene creato solo in fase di esecuzione se sono presenti file in uso durante l'installazione.<br/> |
| ListBox: ListBox1 del controllo: ListBox1 della finestra di dialogo: MyDialog non si trova nella tabella ListBox. Avviso <br/>                                                                                                                        | È presente un [controllo ListBox](listbox-control.md) con un valore nella colonna Proprietà della tabella [Control](control-table.md) e per il quale il [bit](indirect-control-attribute.md) indiretto non è impostato nella colonna Attributi. ICE17 invia un avviso perché il programma di installazione usa il valore della proprietà come chiave esterna nella tabella [ListBox](listbox-table.md), ma il valore non è presente nella chiave primaria di tale tabella. Se il bit [indiretto](indirect-control-attribute.md) è impostato, il controllo modifica il valore di una proprietà con un nome che è il valore della proprietà associata a questo controllo.<br/> Questo avviso può essere ignorato se il controllo viene creato in fase di esecuzione. Ad esempio, il [controllo ListBox](listbox-control.md) per nella [finestra di dialogo FilesInUse](filesinuse-dialog.md) viene creato solo in fase di esecuzione se sono presenti file in uso durante l'installazione.<br/>                                |
| ComboBox: ComboBox1 of Control: ComboBox1 of Dialog: ByDialog is not in the ComboBox table Warning <br/>                                                                                                                     | È presente un [controllo ComboBox](combobox-control.md) con un valore nella colonna Proprietà della tabella [Control](control-table.md) e per il quale il [bit](indirect-control-attribute.md) indiretto non è impostato nella colonna Attributi. ICE17 invia un avviso perché il programma di installazione usa il valore della proprietà come chiave esterna nella tabella [ComboBox](combobox-table.md), ma il valore non è presente nella chiave primaria della tabella. Se il bit [indiretto](indirect-control-attribute.md) è impostato, il controllo modifica il valore di una proprietà con un nome che è il valore della proprietà associata a questo controllo.<br/> Questo avviso può essere ignorato se il controllo viene creato in fase di esecuzione. Ad esempio, il [controllo ListBox](listbox-control.md) per nella [finestra di dialogo FilesInUse](filesinuse-dialog.md) viene creato solo in fase di esecuzione se sono presenti file in uso durante l'installazione.<br/>                            |
| ListView: ListView1 del controllo: ListView1 della finestra di dialogo: MyDialog non si trova nella tabella ListView. Avviso <br/>                                                                                                                    | È presente un [controllo ListView](listview-control.md) con un valore nella colonna Proprietà della tabella [Control](control-table.md) e per il quale il [bit](indirect-control-attribute.md) indiretto non è impostato nella colonna Attributi. ICE17 invia un avviso perché il programma di installazione usa il valore della proprietà come chiave esterna nella [tabella ListView](listview-table.md), ma il valore non è presente nella chiave primaria della tabella. Se il bit [indiretto](indirect-control-attribute.md) è impostato, il controllo modifica il valore di una proprietà con un nome che è il valore della proprietà associata a questo controllo.<br/> Questo avviso può essere ignorato se il controllo viene creato in fase di esecuzione. Ad esempio, il [controllo ListBox](listbox-control.md) per nella [finestra di dialogo FilesInUse](filesinuse-dialog.md) viene creato solo in fase di esecuzione se sono presenti file in uso durante l'installazione.<br/>                            |
| Bitmap: 'Bitmap2' for Control: 'Button2' of Dialog: 'MyDialog' not found in Binary table Error <br/>                                                                                                                         | È presente un [controllo Pushbutton o](pushbutton-control.md) [Un](checkbox-control.md) controllo Casella di controllo per cui la colonna Text della tabella [Control](control-table.md) non contiene una chiave esterna nel record della tabella [Binary](binary-table.md) contenente la bitmap o l'icona.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| Bitmap: 'Bitmap3' per il controllo: 'RadioButton2' della finestra di dialogo: 'MyDialog' non trovato nella tabella binaria o<br/> Icona: 'Icon1' for Control: 'RadioButton3' of Dialog: 'MyDialog' not found in Binary table (Icona1 per il controllo: 'RadioButton3' del dialogo: 'MyDialog' non trovato nella tabella binaria<br/> Errore <br/> | È presente un [controllo RadioButtonGroup](radiobuttongroup-control.md) per cui la colonna Text della tabella [RadioButton](radiobutton-table.md) non contiene una chiave esterna nel record della tabella [Binary](binary-table.md) contenente la bitmap o l'icona.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| Controllo immagine: 'Button3' della finestra di dialogo: 'MyDialog' ha entrambi gli attributi Icon e Bitmap impostati su Error <br/>                                                                                                                     | È presente un [controllo PushButton,](pushbutton-control.md) [CheckBox](checkbox-control.md)o [RadioButtonGroup](radiobuttongroup-control.md) con il bit [Icon](icon-control-attribute.md) o il bit [Bitmap](bitmap-control-attribute.md) impostato nella colonna Attributi della [tabella Control](control-table.md). Non è possibile impostare entrambi gli attributi insieme.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |



 

## <a name="example"></a>Esempio

[Tabella di controllo](control-table.md) (parziale)



| Finestra di dialogo\_ | Control      | Tipo             | Attributi | Proprietà     | Testo       |
|----------|--------------|------------------|------------|--------------|------------|
| MyDialog | Button1      | Pulsante       | 0          |              | OK         |
| MyDialog | Bitmap1      | Bitmap           | 0          |              | Bitmap1    |
| MyDialog | Pulsante di opzione1 | RadioButtonGroup | 0          | Pulsante di opzione1 |            |
| MyDialog | ListBox1     | ListBox          | 0          | ListBox1     |            |
| MyDialog | ComboBox1    | ComboBox         | 0          | ComboBox1    |            |
| MyDialog | ListView1    | ListView         | 0          | ListView1    |            |
| MyDialog | Button2      | Pulsante       | 262144     |              | Bitmap2    |
| MyDialog | Pulsante di opzione2 | RadioButtonGroup | 262144     |              | Proprietà2  |
| MyDialog | Pulsante di opzione3 | RadioButtonGroup | 524288     |              | Proprietà3  |
| MyDialog | Pulsante3      | Pulsante       | 786432     |              | Ambiguo1 |



 

[Tabella RadioButton](radiobutton-table.md) (parziale)



| Proprietà\_ | JSON | Testo    |
|------------|-------|---------|
| Proprietà2  | 1     | Bitmap3 |
| Proprietà3  | 2     | Icona1   |



 

Le tabelle seguenti sono vuote:

-   [Tabella ControlEvent](controlevent-table.md)
-   [Tabella ListBox](listbox-table.md)
-   [Tabella ComboBox](combobox-table.md)
-   [Tabella ListView](listview-table.md)
-   [Tabella binaria](binary-table.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento su ICE](ice-reference.md)
</dt> </dl>

 

 




