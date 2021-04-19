---
description: Questo esempio si basa sull'esempio di modulo delle attestazioni automatiche integrando l'oggetto PenInputPanel. L'esempio si trova nella \# directory C PIPanel nella cartella Autoclaims.
ms.assetid: 9a2c1565-fb24-4767-bfa5-0257129f4bd4
title: Esempio di PenInputPanel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d60f33ff3f61e1a2930841e5fd3d3ce3f9fc5b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317916"
---
# <a name="peninputpanel-sample"></a>Esempio di PenInputPanel

Questo esempio si basa sull'esempio di modulo delle attestazioni automatiche integrando l'oggetto [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) . L'esempio si trova nella \# directory C PIPanel nella cartella Autoclaims.

> [!Note]  
> Per questo esempio è necessario che il sistema sia dotato di un dispositivo Pen. Se si usa solo un mouse (o un altro dispositivo di puntamento HID), l'oggetto [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) non viene visualizzato.

 

Per ulteriori informazioni sull'esempio relativo al modulo Auto Claims, vedere l'esempio relativo al [modulo Claims automatico](auto-claims-form-sample.md). Per ulteriori informazioni sull'oggetto [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) , vedere [Programming the input panel using the PenInputPanel class](programming-the-input-panel-using-the-peninputpanel-class.md).

Nell'esempio, il form auto Claims contiene cinque campi in cui all'utente viene richiesto di inserire le informazioni relative all'attestazione: numero di criteri, nome assicurato, anno, marca e modello dell'automobile. Un oggetto [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) è associato a ogni campo di input per fornire un metodo semplice per l'immissione di valori con una penna.

Esistono due tecniche per il fissaggio di un oggetto [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) ai campi di input nel form. La prima tecnica consiste nell'assegnare un'istanza separata dell'oggetto a ogni campo di input in fase di progettazione. Il secondo consiste nel creare una singola istanza dell'oggetto e quindi collegarla in fase di esecuzione a un campo quando riceve lo stato attivo. In questo esempio vengono illustrate entrambe le tecniche.

La scelta della tecnica da utilizzare comporta compromessi. La creazione di un'istanza univoca dell'oggetto per ogni campo del modulo richiede una quantità di memoria leggermente maggiore quando il modulo viene caricato. Tuttavia, salva la necessità di gestire gli eventi di attivazione per i campi per assegnare una singola istanza al campo corrente in fase di esecuzione.

Poiché l'oggetto [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) è supportato solo in un Tablet PC, l'esempio crea gli oggetti PenInputPanel all'interno di un blocco di gestione delle eccezioni.

## <a name="one-object-per-field"></a>Un oggetto per ogni campo

Nell'esempio viene illustrata la prima tecnica (un oggetto [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) per ogni campo) assegnando i campi di input per il numero di criteri ( `inkEdPolicyNumber` ) e il nome assicurato ( `inkEdName` ) un'istanza univoca dell'oggetto PenInputPanel. Un costruttore di overload per l'oggetto PenInputPanel può assumere il nome del controllo di input come argomento, associando così i controlli. Le righe seguenti del gestore dell'evento [Load](/dotnet/api/system.windows.forms.form.load?view=netcore-3.1) del form mostrano quanto segue:


```C++
pipPolicyNumber = new PenInputPanel(inkEdPolicyNumber);
pipName = new PenInputPanel(inkEdName);
```



## <a name="one-object-per-form"></a>Un oggetto per ogni form

La seconda tecnica è illustrata nell'esempio: una singola istanza di un oggetto [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) , `pipShared` , viene condivisa tra i campi anno, marca e input modello. L'oggetto condiviso viene creato utilizzando il costruttore predefinito.


```C++
pipShared = new PenInputPanel();
```



Per usare questa tecnica è necessario che il form disponga di una sola istanza dell'oggetto [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) . Questa operazione consente di risparmiare memoria, ma è necessario aggiungere il codice per gestire l'evento quando un campo di input riceve lo stato attivo. Quando un controllo che usa un'istanza condivisa di un oggetto PenInputPanel ottiene lo stato attivo, impostare la proprietà [AttachedEditControl](/previous-versions/aa514050(v=msdn.10)) dell'oggetto PenInputPanel su tale controllo. Il codice seguente illustra un gestore eventi per gli eventi year, make e Model Fields `Enter` .


```C++
private void inkEdYear_Enter(object sender, System.EventArgs e)
{
    // Attach the shared PenInputPanel to the Year field
    pipShared.AttachedEditControl = inkEdYear;

    // set the NUMBER factoid to bias recognition for numbers
    pipShared.Factoid = "NUMBER";

    // Enable correction UI on the inkEdYear field
    pipShared.EnableTsf(true);
}

private void inkEdMake_Enter(object sender, System.EventArgs e)
{
    // Attach the shared PenInputPanel to the Make field
    pipShared.AttachedEditControl = inkEdMake;

    // reset the factoid to bias recognition for general text
    pipShared.Factoid = "DEFAULT";

    // Enable correction UI on the inkEdMake field
    pipShared.EnableTsf(true);
}
private void inkEdModel_Enter(object sender, System.EventArgs e)
{
    // Attach the shared PenInputPanel to the Model field
    pipShared.AttachedEditControl = inkEdModel;

    // reset the factoid to bias recognition for general text
    pipShared.Factoid = "DEFAULT";

    // Enable correction UI on the inkEdModel field
    pipShared.EnableTsf(true);
}
```



Assicurarsi di impostare le proprietà che devono essere impostate quando lo stato attivo viene modificato in un nuovo controllo. Nei gestori eventi precedenti, ad esempio, la proprietà del controllo del controllo è impostata in [base alle esigenze](/previous-versions/ms571978(v=vs.100)) .

## <a name="usability-considerations"></a>Considerazioni sull'usabilità

Quando si usa l'oggetto [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) nell'applicazione, tenere presenti le seguenti considerazioni sull'usabilità.

### <a name="positioning-the-peninputpanel"></a>Posizionamento di PenInputPanel

Poiché i campi sono disposti verticalmente sul form in questo esempio, l'interfaccia utente [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) per ogni controllo di input è leggermente posizionata a destra del controllo di input per facilitarne l'uso. In questo modo si impedisce a PenInputPanel di coprire la successiva casella di modifica, rendendo più semplice la destinazione della successiva casella di modifica.


```C++
pipShared.HorizontalOffset = 32;
pipPolicyNumber.HorizontalOffset = 32;
pipName.HorizontalOffset = 32;
```



### <a name="selecting-input-panel-to-display"></a>Selezione del pannello di input da visualizzare

Poiché i numeri di criteri sono spesso combinazioni di numeri, lettere e altri caratteri, possono essere soggetti a errori di riconoscimento. Pertanto, l'esempio imposta il pannello predefinito visualizzato dall'oggetto [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) come tastiera quando viene collegato al campo numero di criteri.


```C++
pipPolicyNumber.DefaultPanel = PanelType.Keyboard;
```



Il comportamento predefinito dell'oggetto [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) consiste nell'usare il pannello selezionato per ultimo dall'utente.

### <a name="text-services-framework-correction-user-interface"></a>Interfaccia utente di correzione del Framework di servizi di testo

In questo esempio tutti i campi di input sono controlli [InkEdit](/previous-versions/ms552265(v=vs.100)) . Questa operazione è significativa perché il controllo InkEdit dispone del supporto incorporato per il [Framework di servizi di testo](../tsf/text-services-framework.md) (TSF) ed è quindi in grado di supportare l'interfaccia utente di correzione sul posto per l'input ricevuto dall'oggetto [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) .

Il valore predefinito per [EnableTsf](/previous-versions/ms569656(v=vs.100)) è **true**. In questo modo, l'oggetto [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) tenta di avviare il Framework dei servizi di testo (TSF) sul controllo associato. In caso di esito positivo, l'interfaccia utente di correzione viene visualizzata nel controllo e consente l'accesso alle alternative di riconoscimento. La chiamata di questo metodo con un parametro **false** tenta di arrestare TSF sul controllo associato.

Il controllo [InkEdit](/previous-versions/ms552265(v=vs.100)) fornisce già un'interfaccia utente di correzione, ma nell'esempio [EnableTsf](/previous-versions/ms569656(v=vs.100)) viene usato per consentire a [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) di usare il contesto del riconoscimento di inserimento di TSF anziché la funzione [**SendInput**](/windows/win32/api/winuser/nf-winuser-sendinput) per inviare i risultati del riconoscimento della grafia nel controllo. Il risultato è che il testo può essere inserito anche se il campo non ha più lo stato attivo.


```C++
  pipName.EnableTsf(true);
  pipPolicyNumber.EnableTsf(true);
```



## <a name="closing-the-form"></a>Chiusura del modulo

Nel codice generato da Progettazione Windows Form, i controlli [InkEdit](/previous-versions/ms552265(v=vs.100)) e [InkPicture](/previous-versions/aa514604(v=msdn.10)) vengono aggiunti all'elenco dei componenti del form quando il modulo viene inizializzato. Quando il form viene chiuso, i controlli InkEdit e InkPicture vengono eliminati, così come gli altri componenti del form, dal metodo [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) del modulo. Il metodo Dispose del modulo Elimina inoltre gli oggetti [Ink](/previous-versions/aa515768(v=msdn.10)) creati per il form.

 

 
