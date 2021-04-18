---
description: Di seguito sono riportate alcune considerazioni relative al threading di Tablet PC per la libreria gestita.
ms.assetid: bcc398d3-22ea-466c-9206-92b0ac208def
title: Considerazioni sul threading della libreria gestita
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b8677375b8bbdb5f171329927d01e6178b5cb83
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314910"
---
# <a name="managed-library-threading-considerations"></a>Considerazioni sul threading della libreria gestita

Di seguito sono riportate alcune considerazioni relative al threading di Tablet PC per la libreria gestita.

-   [Thread-safety](#thread-safety)
-   [Applicazioni STA e MTA](#sta-and-mta-applications)
-   [Considerazioni sul threading di Windows Form](#windows-forms-threading-considerations)
-   [Considerazioni sugli Appunti](#clipboard-considerations)
-   [Eccezioni nei gestori eventi](#exceptions-within-event-handlers)
-   [Eliminazione di oggetti e controlli](#disposing-objects-and-controls)
-   [API StylusInput](#stylusinput-apis)

## <a name="thread-safety"></a>Thread-Safety

Le classi della libreria gestita della piattaforma Tablet PC non sono in genere thread-safe. Le raccolte seguenti sono thread-safe a livello di membro. Tuttavia, queste raccolte non garantiscono che un enumeratore sia protetto se un altro thread opera sulla raccolta contemporaneamente:

-   [CursorButtons](/previous-versions/ms839506(v=msdn.10))
-   [Cursori](/previous-versions/ms839493(v=msdn.10))
-   [DivisionUnits](/previous-versions/ms837954(v=msdn.10))
-   [RecognitionAlternates](/previous-versions/ms830115(v=msdn.10))
-   [Riconoscitori](/previous-versions/ms828520(v=msdn.10))
-   [Tablet](/previous-versions/ms827599(v=msdn.10))

## <a name="sta-and-mta-applications"></a>Applicazioni STA e MTA

Per impostazione predefinita, le applicazioni gestite create usando le procedure guidate contenute in Microsoft Visual Studio .NET sono Apartment a thread singolo (STA). È possibile modificare l'Apartment per l'applicazione impostando il thread STA o l'attributo thread dell'Apartment a thread multipli (MTA) nel punto di ingresso dell'applicazione.

Se l'applicazione viene eseguita in un MTA, è necessario scrivere codice thread-safe; Tuttavia, in questo modo è possibile migliorare determinati problemi di prestazioni di gestione degli eventi.

Per ulteriori informazioni sugli attributi thread STA e thread MTA, vedere classe [STAThreadAttribute](/dotnet/api/system.stathreadattribute?view=netcore-3.1) e classe [MTAThreadAttribute](/dotnet/api/system.mtathreadattribute?view=netcore-3.1) .

## <a name="windows-forms-threading-considerations"></a>Considerazioni sul threading di Windows Form

I controlli [InkPicture](/previous-versions/aa514604(v=msdn.10)) e [InkEdit](/previous-versions/ms552265(v=vs.100)) estendono Windows Form controlli. I controlli Windows Form usano il modello di Apartment a thread singolo (STA) perché Windows Form sono basati su finestre Win32 native che sono intrinsecamente a thread singolo. Nel codice gestito, i controlli Ink devono essere creati nello stesso thread del thread principale per il form.

In un'applicazione STA, si verificano determinati eventi in un thread diverso dal thread dell'interfaccia utente dell'applicazione. Quando si chiama un oggetto Windows Form o un controllo, inclusi i controlli [InkPicture](/previous-versions/aa514604(v=msdn.10)) e [InkEdit](/previous-versions/ms552265(v=vs.100)) , dall'interno di un gestore eventi di Tablet PC, utilizzare il metodo [Control. Invoke](/dotnet/api/system.windows.forms.control.invoke?view=netcore-3.1) ereditato dell'oggetto o del controllo. Per determinare se è necessario, è possibile usare la proprietà [InvokeRequired](/dotnet/api/system.windows.forms.control.invokerequired?view=netcore-3.1) , ereditata dalla classe Control.

Ad esempio, nel gestore eventi seguente per l'evento di [riconoscimento](/previous-versions/ms829424(v=msdn.10)) , la proprietà [InvokeRequired](/dotnet/api/system.windows.forms.control.invokerequired?view=netcore-3.1) viene verificata e, se **true**, il gestore eventi viene richiamato dal thread dell'interfaccia utente.


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



Se si inserisce un [UserControl](/dotnet/api/system.web.ui.usercontrol?view=netframework-4.8) in awebpagein in un browser (vedere [controlli Web](web-controls.md)), viene eseguito come applicazione sta. Per le applicazioni smart client (vedere [No Touch Deployment](no-touch-deployment.md)), lo sviluppatore ha il controllo completo sulla [ApartmentState](/dotnet/api/system.threading.apartmentstate?view=netcore-3.1). Il valore predefinito è in genere STA, ma può essere MTA, a seconda della versione di CLR. Per problemi di threading che coinvolgono il metodo [**RealTimeStylus**](realtimestylus-class.md), vedere [considerazioni relative al threading per le API StylusInput](threading-considerations-for-the-stylusinput-apis.md).

Per ulteriori informazioni sulla chiamata di Windows Form da un'applicazione MTA, vedere [esempio di controllo multithreading Windows Form](/previous-versions/dotnet/netframework-1.1/3s8xdz5c(v=vs.71)).

## <a name="clipboard-considerations"></a>Considerazioni sugli Appunti

L'oggetto [Appunti](../dataxchg/clipboard.md) funziona solo da un thread sta. Quando si tenta di copiare o incollare dagli Appunti da un thread che non è STA, si ottiene un [ThreadStateException](/previous-versions/windows/). Se l'applicazione è MTA, creare un thread STA per gestire le chiamate al metodo degli Appunti e alcuni degli altri aspetti dell'interfaccia utente dell'applicazione.

## <a name="exceptions-within-event-handlers"></a>Eccezioni nei gestori eventi

Le eccezioni non possono essere generate dall'interno dei gestori di eventi di Tablet PC. Se, ad esempio, un delegato del gestore eventi per un oggetto o una raccolta di Tablet PC ha tre gestori registrati e il primo genera un'eccezione, si verifica la sequenza seguente:

1.  Il primo gestore si chiude.
2.  L'eccezione viene persa.
3.  I gestori rimanenti non vengono richiamati.

## <a name="disposing-objects-and-controls"></a>Eliminazione di oggetti e controlli

Per evitare una perdita di memoria, è necessario chiamare in modo esplicito il metodo [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) su qualsiasi oggetto o controllo di Tablet PC a cui è stato collegato un gestore eventi prima che l'oggetto o il controllo esca dall'ambito.

Per migliorare le prestazioni nell'applicazione, eliminare manualmente qualsiasi oggetto o controllo di Tablet PC che implementi il metodo [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) quando l'oggetto o il controllo non è più necessario.

## <a name="stylusinput-apis"></a>API StylusInput

Per informazioni sulle considerazioni relative al threading per l'oggetto [**RealTimeStylus**](realtimestylus-class.md) e le API (Application Programming Interface) di StylusInput, vedere [considerazioni relative al threading per le API StylusInput](threading-considerations-for-the-stylusinput-apis.md).

 

 
