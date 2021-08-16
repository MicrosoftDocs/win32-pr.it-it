---
description: Le considerazioni seguenti sul threading per Tablet PC sono specifiche della libreria gestita.
ms.assetid: bcc398d3-22ea-466c-9206-92b0ac208def
title: Considerazioni sul threading della libreria gestita
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60908618fe3b566a552167f3448ee1d4269f9246c7b08f9bb1acf3269cf2ae77
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119031709"
---
# <a name="managed-library-threading-considerations"></a>Considerazioni sul threading della libreria gestita

Le considerazioni seguenti sul threading per Tablet PC sono specifiche della libreria gestita.

-   [Thread safety](#thread-safety)
-   [Applicazioni STA e MTA](#sta-and-mta-applications)
-   [Windows Considerazioni sul threading dei moduli](#windows-forms-threading-considerations)
-   [Considerazioni sugli Appunti](#clipboard-considerations)
-   [Eccezioni all'interno di gestori eventi](#exceptions-within-event-handlers)
-   [Eliminazione di oggetti e controlli](#disposing-objects-and-controls)
-   [API StylusInput](#stylusinput-apis)

## <a name="thread-safety"></a>Thread-Safety

Le classi della libreria gestita della piattaforma Tablet PC non sono in genere thread-safe. Le raccolte seguenti sono thread-safe a livello di membro. Tuttavia, queste raccolte non garantiscono che un enumeratore sia protetto se un altro thread opera contemporaneamente sulla raccolta:

-   [CursorButtons](/previous-versions/ms839506(v=msdn.10))
-   [Cursori](/previous-versions/ms839493(v=msdn.10))
-   [Divisionunits](/previous-versions/ms837954(v=msdn.10))
-   [Recognitionalternates](/previous-versions/ms830115(v=msdn.10))
-   [Riconoscitori](/previous-versions/ms828520(v=msdn.10))
-   [Tablet](/previous-versions/ms827599(v=msdn.10))

## <a name="sta-and-mta-applications"></a>Applicazioni STA e MTA

Le applicazioni gestite create usando le procedure guidate contenute in Microsoft Visual Studio .NET sono apartment a thread singolo (STA) per impostazione predefinita. È possibile modificare l'apartment per l'applicazione impostando l'attributo thread STA o thread apartment multithreading (MTA) nel punto di ingresso dell'applicazione.

Se l'applicazione viene eseguita in un MTA, è necessario scrivere codice thread-safe. Tuttavia, in questo modo è possibile migliorare determinati problemi di prestazioni di gestione degli eventi.

Per altre informazioni sugli attributi del thread STA e del thread MTA, vedere [Classe STAThreadAttribute](/dotnet/api/system.stathreadattribute?view=netcore-3.1) e [Classe MTAThreadAttribute.](/dotnet/api/system.mtathreadattribute?view=netcore-3.1)

## <a name="windows-forms-threading-considerations"></a>Windows Considerazioni sul threading dei moduli

I [controlli InkPicture](/previous-versions/aa514604(v=msdn.10)) [e InkEdit](/previous-versions/ms552265(v=vs.100)) estendono Windows form. Windows I controlli form usano il modello apartment a thread singolo (STA, Single-Threaded Apartment) perché Windows Form si basano su finestre Win32 native intrinsecamente a thread singolo. Nel codice gestito i controlli input penna devono essere creati nello stesso thread del thread principale per il form.

In un'applicazione STA alcuni eventi si verificano in un thread diverso dal thread dell'interfaccia utente dell'applicazione. Quando si chiama qualsiasi oggetto o controllo di Windows Forms, inclusi i controlli [InkPicture](/previous-versions/aa514604(v=msdn.10)) e [InkEdit,](/previous-versions/ms552265(v=vs.100)) dall'interno di un gestore eventi di Tablet PC, usare il metodo [Control.Invoke](/dotnet/api/system.windows.forms.control.invoke?view=netcore-3.1) ereditato dell'oggetto o del controllo. La [proprietà InvokeRequired,](/dotnet/api/system.windows.forms.control.invokerequired?view=netcore-3.1) ereditata dalla classe Control, può essere usata per determinare se è necessario.

Ad esempio, nel gestore eventi seguente per l'evento [Recognition](/previous-versions/ms829424(v=msdn.10)) viene testata la proprietà [InvokeRequired](/dotnet/api/system.windows.forms.control.invokerequired?view=netcore-3.1) e, se **TRUE,** il gestore eventi viene richiamato nuovamente dal thread dell'interfaccia utente.


```C++
void recoContext_Recognition(object sender, 
        RecognizerContextRecognitionEventArgs e)
{
    if (InvokeRequired)
    {
        Invoke( new RecognizerContextRecognitionEventHandler(  
                     recoContext_Recognition ),
                    new object[] { sender, e } );
        return;
    }
     // Use the recognition result here.
}
```



Se si mette un [UserControl](/dotnet/api/system.web.ui.usercontrol?view=netframework-4.8) in awebpage in un browser (vedere [Controlli Web),](web-controls.md)viene eseguito come applicazione STA. Per le applicazioni smart client (vedere [Nessuna distribuzione touch),](no-touch-deployment.md)lo sviluppatore ha il controllo completo su [ApartmentState.](/dotnet/api/system.threading.apartmentstate?view=netcore-3.1) L'impostazione predefinita è in genere STA, ma può essere MTA, a seconda della versione di CLR. Per problemi di threading relativi a [**RealTimeStylus,**](realtimestylus-class.md)vedere [Threading Considerations for the StylusInput APIs](threading-considerations-for-the-stylusinput-apis.md)( Considerazioni sul threading per le API StylusInput).

Per altre informazioni sulla chiamata Windows Form da un'applicazione MTA, vedere [Multithreaded Windows Forms Control Sample](/previous-versions/dotnet/netframework-1.1/3s8xdz5c(v=vs.71)).

## <a name="clipboard-considerations"></a>Considerazioni sugli Appunti

[L'oggetto Clipboard](../dataxchg/clipboard.md) funziona solo da un thread STA. Quando si tenta di copiare o incollare dagli Appunti da un thread diverso da STA, si ottiene [un'eccezione ThreadStateException.](/previous-versions/windows/) Se l'applicazione è MTA, creare un thread STA per gestire le chiamate al metodo degli Appunti e alcuni degli altri aspetti dell'interfaccia utente dell'applicazione.

## <a name="exceptions-within-event-handlers"></a>Eccezioni all'interno di gestori eventi

Non è possibile generare eccezioni dall'interno dei gestori eventi di Tablet PC. Ad esempio, se un delegato del gestore eventi per un oggetto o una raccolta di Tablet PC ha tre gestori registrati e il primo genera un'eccezione, si verifica la sequenza seguente:

1.  Il primo gestore viene chiuso.
2.  L'eccezione viene persa.
3.  I gestori rimanenti non vengono richiamati.

## <a name="disposing-objects-and-controls"></a>Eliminazione di oggetti e controlli

Per evitare una perdita di memoria, è necessario chiamare in modo esplicito il metodo [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) su qualsiasi oggetto o controllo Tablet PC a cui è stato associato un gestore eventi prima che l'oggetto o il controllo eserne l'ambito.

Per migliorare le prestazioni nell'applicazione, eliminare manualmente qualsiasi oggetto o controllo Tablet PC che implementa il [metodo Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) quando l'oggetto o il controllo non è più necessario.

## <a name="stylusinput-apis"></a>API StylusInput

Per informazioni sulle considerazioni sul threading per l'oggetto [**RealTimeStylus**](realtimestylus-class.md) e le API (Application Programming Interface) StylusInput, vedere Considerazioni sul threading per le [API StylusInput](threading-considerations-for-the-stylusinput-apis.md).

 

 
