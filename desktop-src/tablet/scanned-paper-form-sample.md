---
description: In questo esempio di C \# , un modulo cartaceo è stato analizzato come file di Portable Network Graphics (png) e specificato come immagine di sfondo in fase di esecuzione per un controllo InkPicture. Nell'esempio viene utilizzata una finestra di messaggio per visualizzare i risultati del riconoscimento della grafia.
ms.assetid: fc9a39c2-9e4b-4d22-a118-3d24544897dd
title: Esempio di modulo cartaceo analizzato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d60e1d62a4e023ba38e9a1fd2c4890288a542d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314900"
---
# <a name="scanned-paper-form-sample"></a>Esempio di modulo cartaceo analizzato

In questo esempio di C \# , un modulo cartaceo è stato analizzato come file di Portable Network Graphics (png) e specificato come immagine di sfondo in fase di esecuzione per un controllo [InkPicture](/previous-versions/aa514604(v=msdn.10)) . Nell'esempio viene utilizzata una finestra di messaggio per visualizzare i risultati del riconoscimento della grafia.

Nell'esempio è incluso un file Extensible Markup Language (XML), Formdata.xml. Il file XML contiene il nome del file PNG. Contiene anche `FieldInfo` elementi che definiscono aree rettangolari sul form in cui un utente può immettere input penna. Le informazioni nell' `FieldInfo` elemento sono illustrate nell'esempio seguente:


```C++
    <FieldInfo>
        <Name>first name</Name>
        <Left>88</Left>
        <Top>65</Top>
        <Right>332</Right>
        <Bottom>94</Bottom>
    </FieldInfo>
```



Gli elementi sinistro, superiore, destro e inferiore sono definizioni delle coordinate dei pixel per ogni campo.

L'esempio Inizializza un nuovo [set](/dotnet/api/system.data.dataset?view=netcore-3.1) di dati con i dati contenuti in Formdata.xml:


```C++
    formData = new DataSet("FormData");
    formData.ReadXml("formdata.xml"); 
```



L'immagine del modulo specificata in Formdata.xml viene caricata come sfondo del controllo [InkPicture](/previous-versions/aa514604(v=msdn.10)) :


```C++
    inkPicture1.BackgroundImage = 
        System.Drawing.Image.FromFile(
        (string) formData.Tables["FormData"].Rows[0]["Image"]);
```



La raccolta di input penna viene quindi abilitata per il controllo [InkPicture](/previous-versions/aa514604(v=msdn.10)) :


```C++
    inkPicture1.InkEnabled = true;
```



## <a name="menu-event-handlers"></a>Gestori eventi di menu

L'applicazione include i gestori eventi Click per tutti i menu visualizzati nella parte superiore del form.

### <a name="recognize-menu-item"></a>Voce di menu riconosci

Il gestore dell'evento click del menu Recognize Disabilita la raccolta di input penna per il controllo e verifica la presenza di un riconoscimento della grafia. Se non è installato alcun riconoscimento, viene visualizzata una finestra di dialogo. Un utente deve quindi fare clic sull'opzione di menu input penna o penna per riabilitare il controllo per input penna.

Se è installato un riconoscimento, la `Recognize` funzione recupera i dati XML che specificano le coordinate dei pixel per ogni campo del modulo. Le coordinate vengono convertite in coordinate dello spazio di input penna e viene definito un rettangolo per ogni campo del modulo. Dopo aver definito i rettangoli, la funzione trova i tratti che si intersecano e si trovano all'interno di ogni rettangolo. Infine, esegue il riconoscimento sull'input penna e Visualizza i risultati in una finestra di messaggio.

### <a name="ink-menu-item"></a>Voce di menu input penna

Il gestore dell'evento clic del menu input penna Abilita il controllo [InkPicture](/previous-versions/aa514604(v=msdn.10)) .

### <a name="pen-menu-item"></a>Voce di menu penna

Il gestore eventi click del menu penna esegue le attività seguenti:

-   Disabilita la raccolta di input penna per il controllo [InkPicture](/previous-versions/aa514604(v=msdn.10)) (necessario prima di modificare la proprietà [EditingMode](/previous-versions/ms582189(v=vs.100)) ).
-   Imposta la proprietà [EditingMode](/previous-versions/ms582189(v=vs.100)) per la raccolta di input penna.
-   Riabilita la raccolta di input penna per il controllo [InkPicture](/previous-versions/aa514604(v=msdn.10)) e attiva o disattiva i menu penna, seleziona e Cancella per indicare la modalità attiva.

### <a name="edit-menu-item"></a>Modifica voce di menu

Il gestore eventi click del menu modifica è simile al gestore dell'evento del menu Pen. Esegue le attività seguenti:

-   Disabilita la raccolta di input penna.
-   Imposta la proprietà [EditingMode](/previous-versions/ms582189(v=vs.100)) su **SELECT**, che consente all'utente di eseguire la selezione dell'input penna.
-   Abilita nuovamente la raccolta di input penna e attiva o disattiva i menu di penna, modifica e gomma per indicare la modalità attiva.

### <a name="eraser-menu-item"></a>Voce di menu gomma

Il gestore eventi click del menu gomma imposta il [](/previous-versions/aa514604(v=msdn.10)) controllo InkPicture [EditingMode](/previous-versions/ms582189(v=vs.100)) su **Delete**, che consente a un utente di cancellare l'input penna. Consente inoltre di impostare le voci di menu penna, modifica e gomma.

### <a name="clear-menu-item"></a>Cancella voce di menu

Il gestore dell'evento click menu Clear elimina la raccolta [Strokes](/previous-versions/ms552701(v=vs.100)) corrente per il controllo [InkPicture](/previous-versions/aa514604(v=msdn.10)) , cancellando così tutto l'input penna nel form.

## <a name="closing-the-form"></a>Chiusura del modulo

Nel codice generato da Progettazione Windows Form, il controllo [InkPicture](/previous-versions/aa514604(v=msdn.10)) viene aggiunto all'elenco dei componenti del form quando il modulo viene inizializzato. Quando il form viene chiuso, il controllo InkPicture viene eliminato, così come gli altri componenti del form, dal metodo [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) del modulo.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Controllo InkEdit](inkedit-control.md)
</dt> <dt>

[Controllo InkPicture](inkpicture-control.md)
</dt> </dl>

 

 
