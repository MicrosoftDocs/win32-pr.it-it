---
description: Questo esempio si basa sull'esempio modulo di attestazioni automatico integrando l'oggetto PenInputPanel. L'esempio si trova nella directory PIPanel di C \# nella cartella AutoClaims.
ms.assetid: 9a2c1565-fb24-4767-bfa5-0257129f4bd4
title: Esempio di PenInputPanel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c464be52fd08c6c461ba094428a1868fbb51fb328e1a3c88a2d0949a6ae581e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119934741"
---
# <a name="peninputpanel-sample"></a>Esempio di PenInputPanel

Questo esempio si basa sull'esempio modulo di attestazioni automatico integrando [l'oggetto PenInputPanel.](/previous-versions/aa514041(v=msdn.10)) L'esempio si trova nella directory PIPanel di C \# nella cartella AutoClaims.

> [!Note]  
> Questo esempio richiede che il sistema sia dotato di un dispositivo penna. Se si usa solo un mouse o un altro dispositivo di puntamento HID (Non-Human Interface Device), [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) non viene visualizzato.

 

Per altre informazioni sull'esempio auto claims form, vedere [Auto Claims Form Sample](auto-claims-form-sample.md). Per altre informazioni [sull'oggetto PenInputPanel,](/previous-versions/aa514041(v=msdn.10)) vedi [Programmazione del pannello di input usando la classe PenInputPanel.](programming-the-input-panel-using-the-peninputpanel-class.md)

Nell'esempio, il modulo di attestazioni auto contiene cinque campi in cui all'utente viene richiesto di inserire le informazioni rilevanti per l'attestazione: numero del criterio, nome assicurata, anno, make e modello dell'automobile. Un [oggetto PenInputPanel](/previous-versions/aa514041(v=msdn.10)) è associato a ogni campo di input per fornire un modo semplice per immettere valori con una penna.

Esistono due tecniche per collegare un [oggetto PenInputPanel](/previous-versions/aa514041(v=msdn.10)) ai campi di input nel form. La prima tecnica consiste nell'assegnare un'istanza separata dell'oggetto a ogni campo di input in fase di progettazione. Il secondo è creare una singola istanza dell'oggetto e quindi associare tale istanza dell'oggetto in fase di esecuzione a un campo quando riceve lo stato attivo. In questo esempio vengono illustrate entrambe le tecniche.

Esistono compromessi per decidere quale tecnica usare. La creazione di un'istanza univoca dell'oggetto per ogni campo del modulo richiede una quantità di memoria leggermente maggiore quando il modulo viene caricato. Consente tuttavia di risparmiare la necessità di gestire gli eventi di stato attivo per i campi per assegnare una singola istanza al campo corrente in fase di esecuzione.

Poiché [l'oggetto PenInputPanel](/previous-versions/aa514041(v=msdn.10)) è supportato solo in un Tablet PC, l'esempio crea gli oggetti PenInputPanel all'interno di un blocco di gestione delle eccezioni.

## <a name="one-object-per-field"></a>Un oggetto per campo

L'esempio illustra la prima tecnica (un oggetto [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) per campo) assegnando i campi di input per il numero di criteri ( ) e il nome assicurati ( ) un'istanza univoca `inkEdPolicyNumber` `inkEdName` dell'oggetto PenInputPanel. Un costruttore di overload per l'oggetto PenInputPanel può prendere il nome del controllo di input come argomento, associando così i controlli. Le righe seguenti del gestore dell'evento [Load](/dotnet/api/system.windows.forms.form.load?view=netcore-3.1) del form mostrano quanto segue:


```C++
pipPolicyNumber = new PenInputPanel(inkEdPolicyNumber);
pipName = new PenInputPanel(inkEdName);
```



## <a name="one-object-per-form"></a>Un oggetto per modulo

La seconda tecnica è illustrata anche nell'esempio: una singola istanza di un oggetto [PenInputPanel,](/previous-versions/aa514041(v=msdn.10)) , viene condivisa tra i campi `pipShared` di input Year, Make e Model. L'oggetto condiviso viene creato utilizzando il costruttore predefinito.


```C++
pipShared = new PenInputPanel();
```



L'uso di questa tecnica richiede che il modulo abbia una sola istanza [dell'oggetto PenInputPanel.](/previous-versions/aa514041(v=msdn.10)) Ciò consente di risparmiare memoria, ma è necessario aggiungere codice per gestire l'evento quando un campo di input riceve lo stato attivo. Quando un controllo che usa un'istanza condivisa di un oggetto PenInputPanel ottiene lo stato attivo, imposta la proprietà [AttachedEditControl](/previous-versions/aa514050(v=msdn.10)) dell'oggetto PenInputPanel su tale controllo. Il codice seguente mostra un gestore eventi per gli eventi dei campi Year, Make e `Enter` Model.


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



Assicurarsi di impostare le proprietà che devono essere impostate quando lo stato attivo cambia in un nuovo controllo. Nei gestori eventi precedenti, ad esempio, la proprietà [Factoid](/previous-versions/ms571978(v=vs.100)) viene impostata nel modo appropriato.

## <a name="usability-considerations"></a>Considerazioni sull'usabilità

Quando si usa l'oggetto [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) nell'applicazione, tenere presenti le considerazioni seguenti sull'usabilità.

### <a name="positioning-the-peninputpanel"></a>Posizionamento di PenInputPanel

Poiché i campi sono disposti verticalmente nel form in questo esempio, l'interfaccia utente [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) per ogni controllo di input viene posizionata leggermente a destra del controllo di input per semplificarne l'uso. Ciò impedisce a PenInputPanel di coprire la casella di modifica successiva, semplificando la selezione della casella di modifica successiva come destinazione.


```C++
pipShared.HorizontalOffset = 32;
pipPolicyNumber.HorizontalOffset = 32;
pipName.HorizontalOffset = 32;
```



### <a name="selecting-input-panel-to-display"></a>Selezione del pannello di input da visualizzare

Poiché i numeri dei criteri sono spesso combinazioni di numeri, lettere e altri caratteri, possono essere increscibili a errori di riconoscimento. Pertanto, l'esempio imposta il pannello predefinito visualizzato dall'oggetto [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) come tastiera quando è collegato al campo del numero di criteri.


```C++
pipPolicyNumber.DefaultPanel = PanelType.Keyboard;
```



Il comportamento predefinito [dell'oggetto PenInputPanel](/previous-versions/aa514041(v=msdn.10)) è usare il pannello selezionato per ultimo dall'utente.

### <a name="text-services-framework-correction-user-interface"></a>Framework servizi di testo correzione Interfaccia utente

In questo esempio tutti i campi di input sono [controlli InkEdit.](/previous-versions/ms552265(v=vs.100)) Questo è significativo perché il controllo InkEdit include il supporto incorporato per [il Framework servizi di testo](../tsf/text-services-framework.md) (TSF) ed è quindi in grado di supportare l'interfaccia utente di correzione sul posto per l'input ricevuto dall'oggetto [PenInputPanel.](/previous-versions/aa514041(v=msdn.10))

Il valore predefinito per [EnableTsf](/previous-versions/ms569656(v=vs.100)) è **TRUE.** In questo modo [l'oggetto PenInputPanel](/previous-versions/aa514041(v=msdn.10)) tenta di avviare il Framework servizi di testo (TSF) nel controllo associato. Se l'operazione riesce, l'interfaccia utente di correzione viene visualizzata nel controllo e consente l'accesso alle alternative di riconoscimento. La chiamata di questo metodo con **un parametro FALSE** tenta di arrestare TSF nel controllo associato.

Il controllo [InkEdit](/previous-versions/ms552265(v=vs.100)) fornisce già un'interfaccia utente di correzione, ma nell'esempio [EnableTsf](/previous-versions/ms569656(v=vs.100)) viene usato per consentire a [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) di usare il contesto del riconoscitore di inserimento TSF anziché la funzione [**SendInput**](/windows/win32/api/winuser/nf-winuser-sendinput) per inviare i risultati del riconoscimento della grafia nel controllo. Il risultato è che il testo può essere inserito anche se il campo non ha più lo stato attivo.


```C++
  pipName.EnableTsf(true);
  pipPolicyNumber.EnableTsf(true);
```



## <a name="closing-the-form"></a>Chiusura del modulo

Nel codice Windows generato da Progettazione form, i controlli [InkEdit](/previous-versions/ms552265(v=vs.100)) e [InkPicture](/previous-versions/aa514604(v=msdn.10)) vengono aggiunti all'elenco dei componenti del form quando il form viene inizializzato. Quando il form viene chiuso, i controlli InkEdit e InkPicture vengono eliminati, così come gli altri componenti del form, dal metodo [Dispose del](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) form. Il metodo Dispose del form elimina anche gli oggetti [Ink](/previous-versions/aa515768(v=msdn.10)) creati per il form.

 

 
