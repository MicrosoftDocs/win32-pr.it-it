---
description: I programmi per la lettura dello schermo possono solo leggere il testo di un controllo RadioButtonGroup che è stato creato nella colonna di testo della tabella RadioButton.
ms.assetid: 92ad70ec-a3a4-4ea7-8888-40c78d73e58a
title: Aggiunta di testo aggiuntivo ai pulsanti di opzione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1e73ac55e300ddee603449e9ea7ce5e10f4e0be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967298"
---
# <a name="adding-extra-text-to-radio-buttons"></a>Aggiunta di testo aggiuntivo ai pulsanti di opzione

I programmi per la lettura dello schermo possono solo leggere il testo di un [controllo RadioButtonGroup](radiobuttongroup-control.md) che è stato creato nella colonna di testo della [tabella RadioButton](radiobutton-table.md). Se questo testo è una descrizione insufficiente dei pulsanti di opzione, è possibile aggiungere [controlli testo](text-control.md) sovrapposti per fornire testo descrittivo aggiuntivo. Questi controlli testo devono sovrapporsi tra loro nella finestra di dialogo e hanno le condizioni impostate nella [tabella ControlCondition](controlcondition-table.md) , in modo che venga visualizzato un solo controllo testo alla volta. I controlli di testo non devono sovrapporsi al controllo RadioButtonGroup o ad altri controlli della finestra di dialogo perché rendono i controlli invisibili per le utilità per la lettura dello schermo. Quando l'utente passa il cursore sul controllo di testo, il programma di lettura dello schermo legge il testo aggiuntivo.

Nell'esempio seguente la finestra di dialogo di esempio include un controllo RadioButtonGroup denominato colori con due opzioni per il valore della proprietà TheColor. Per ogni scelta è presente un controllo di testo con una condizione da nascondere o mostrare, a seconda della scelta corrente selezionata per TheColor. Un valore TheColor iniziale viene definito nella tabella delle proprietà. I controlli di testo hanno il testo descrittivo aggiuntivo creato nel campo di testo della tabella RadioButton. Quando un utente posiziona il cursore del mouse sul controllo di testo nella finestra di dialogo, l'lettore dello schermo può leggere la descrizione aggiuntiva della scelta corrente.

[Tabella finestra di dialogo](dialog-table.md)



| Finestra di dialogo   | HCentering | VCenter | Larghezza | Altezza | Attributi | Titolo                    | \_Primo controllo | Controllo \_ predefinito | \_Annulla controllo |
|----------|------------|------------|-------|--------|------------|--------------------------|----------------|------------------|-----------------|
| MySample | 50         | 50         | 200   | 180    | 3          | Pulsanti di opzione accessibili | Colori         | Prossima             |                 |



 

[Tabella di controllo](control-table.md)



| Finestra di dialogo\_ | Control    | Tipo             | X   | S   | Larghezza | Altezza | Attributi | Proprietà | Testo                               | Controllo \_ successivo | Help |
|----------|------------|------------------|-----|-----|-------|--------|------------|----------|------------------------------------|---------------|------|
| MySample | Colori     | RadioButtonGroup | 2   | 20  | 100   | 50     | 3          | TheColor |                                    | Prossima          |      |
| MySample | HowIsBlue  | Testo             | 20  | 80  | 150   | 15     | 2          |          | È come il cielo in un giorno chiaro. |               |      |
| MySample | HowIsGreen | Testo             | 20  | 80  | 150   | 15     | 2          |          | È come erba in primavera.    |               |      |



 

[RadioButton (tabella)](radiobutton-table.md)



| Proprietà | JSON | Valore | X   | S   | Larghezza | Altezza | Testo   | Help |
|----------|-------|-------|-----|-----|-------|--------|--------|------|
| TheColor | 1     | Blu  | 10  | 10  | 80    | 15     | &blu  |      |
| TheColor | 2     | Green | 10  | 30  | 80    | 15     | Verde & |      |



 

[Tabella delle proprietà](property-table.md)



| Proprietà | Valore |
|----------|-------|
| TheColor | Blu  |



 

[Tabella ControlCondition](controlcondition-table.md)



| Finestra di dialogo\_ | controllo\_  | Azione | Condizione                 |
|----------|------------|--------|---------------------------|
| MySample | HowIsBlue  | Nascondi   | TheColor <>  "blu"  |
| MySample | HowIsBlue  | Mostra   | TheColor = "blu"         |
| MySample | HowIsGreen | Nascondi   | TheColor <>  "verde" |
| MySample | HowIsGreen | Mostra   | TheColor = "verde"        |



 

Per ulteriori informazioni, vedere [accessibilità](accessibility.md).

 

 



