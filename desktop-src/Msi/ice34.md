---
description: ICE34 verifica che ogni pulsante di opzione in ogni controllo RadioButtonGroup disponga di una proprietà nella colonna proprietà della tabella RadioButton che specifica il gruppo di pulsanti di opzione.
ms.assetid: 23a88a5a-89e9-47bc-9c0a-6101ce03123c
title: ICE34
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7723cb530397eae66374b0f218db9ad8505195a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314220"
---
# <a name="ice34"></a>ICE34

ICE34 verifica che ogni pulsante di opzione in ogni [controllo RadioButtonGroup](radiobuttongroup-control.md) disponga di una proprietà nella colonna proprietà della [tabella RadioButton](radiobutton-table.md) che specifica il gruppo di pulsanti di opzione. ICE34 verifica che questa proprietà esista e che sia impostata su un valore predefinito nella [tabella delle proprietà](property-table.md) , che è uguale a uno dei valori dei pulsanti di opzione del gruppo nella colonna valore della tabella RadioButton.

Un gruppo di pulsanti di opzione deve avere un valore predefinito per consentire agli utenti di selezionare una scelta usando il tasto TAB. Questa operazione è necessaria per l'accessibilità utente corretta.

ICE34 segnala le tabelle mancanti.

## <a name="result"></a>Risultato

ICE34 pubblica un messaggio di errore se è presente un pulsante di opzione che specifica una proprietà non valida.

## <a name="example"></a>Esempio

ICE34 segnala gli errori seguenti per l'esempio illustrato.



| Errore ICE34                                                                                                                                                                | Descrizione                                                                                                                                                                                                                                                                  |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Il controllo dialoga. Controllo2 deve avere una proprietà perché è di tipo RadioButtonGroup.                                                                                      | È presente un [controllo RadioButtonGroup](radiobuttongroup-control.md), senza il bit del [controllo indiretto](indirect-control-attribute.md) impostato nella colonna attributi della [tabella dei controlli](control-table.md), che non dispone di una proprietà elencata nella colonna proprietà. |
| Probabilmente non è un valore predefinito valido per RadioButtonGroup usando la proprietà Property3. Il valore deve essere elencato come opzione nella tabella RadioButtonGroup.                 | È presente un valore predefinito per una proprietà specificata nella colonna valore della tabella delle [Proprietà](property-table.md) che non è uno dei valori per il gruppo di pulsanti di opzione specificato nella colonna valore della [tabella RadioButton](radiobutton-table.md).                  |
| È necessario definire la proprietà PropertyB perché si tratta di una proprietà indiretta di un controllo RadioButtonGroup dialoga. Control4                                                       | La proprietà a cui fa riferimento questo gruppo RadioButton è una proprietà indiretta e il valore della proprietà indiretta non è una delle scelte per il gruppo RadioButton.                                                                                                       |
| Probabilmente non è un valore predefinito valido per la proprietà PropertyA. La proprietà è una proprietà RadioButtonGroup indiretta del controllo dialoga. Control5 (tramite la proprietà property5). | Il valore della proprietà indiretta a cui viene fatto riferimento tramite il controllo non è uno dei valori predefiniti per tale RadioButtonGroup.                                                                                                                                                    |



 

[Tabella di controllo](control-table.md) (parziale)



| Finestra di dialogo  | Control  | Tipo             | Attributi | Proprietà  |
|---------|----------|------------------|------------|-----------|
| Finestra di dialogo | Control1 | RadioButtonGroup | 0          | Property1 |
| Finestra di dialogo | Controllo2 | RadioButtonGroup | 0          |           |
| Finestra di dialogo | Control3 | RadioButtonGroup | 0          | Property3 |
| Finestra di dialogo | Control4 | RadioButtonGroup | 8          | Property4 |
| Finestra di dialogo | Control5 | RadioButtonGroup | 8          | Property5 |



 

[Tabella delle proprietà](property-table.md) (parziale)



| Proprietà  | Valore     |
|-----------|-----------|
| Property1 | Sì       |
| Property3 | È possibile     |
| Property4 | PropertyB |
| Property5 | PropertyA |
| PropertyA | È possibile     |



 

[Tabella RadioButton](radiobutton-table.md) (parziale)



| Proprietà  | JSON | Valore |
|-----------|-------|-------|
| Property1 | 1     | Sì   |
| Property1 | 2     | Adesso   |
| Property2 | 1     | Sì   |
| Property2 | 2     | No    |
| Property3 | 1     | Sì   |
| Property3 | 2     | No    |
| Property4 | 1     | Sì   |
| Property4 | 2     | No    |
| PropertyA | 1     | Sì   |
| PropertyA | 2     | No    |
| PropertyB | 1     | Sì   |
| PropertyB | 2     | No    |



 

Per correggere gli errori segnalati da questo ICE, controllare quanto segue:

-   Che ogni voce di controllo RadioButton senza il set di attributi indiretto disponga di una proprietà elencata nella colonna proprietà:
-   Ogni proprietà di questo tipo contiene almeno una voce corrispondente nella tabella RadioButton.
-   Ogni proprietà di questo tipo è definita nella tabella delle proprietà, con un valore che corrisponde a una delle scelte della tabella RadioButton.
-   Ogni proprietà a cui viene fatto riferimento nella colonna delle proprietà di un controllo RadioButton con il set di attributi indiretto viene definita nella tabella delle proprietà.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento ghiaccio](ice-reference.md)
</dt> </dl>

 

 



