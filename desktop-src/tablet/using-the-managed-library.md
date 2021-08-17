---
description: Panoramica della libreria gestita e note sull'uso della libreria gestita della piattaforma Tablet PC.
ms.assetid: d283ea1c-faf3-4222-a9a7-c67087636b86
title: Uso della libreria gestita
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d1241787b680045d6c84b440717ced5426e4352d8c280ef58c1bb7f75c9fc66
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118449248"
---
# <a name="using-the-managed-library"></a>Uso della libreria gestita

Common Language Runtime è alla base di Microsoft .NET Framework. È possibile pensare a Common Language Runtime come a un agente che gestisce il codice in fase di esecuzione, fornendo servizi di base, ad esempio la gestione della memoria, la gestione dei thread e la comunicazione remota, e allo stesso tempo forzando la rigorosa sicurezza del codice. In realtà, il concetto di gestione del codice è un principio fondamentale di Common Language Runtime. Il codice destinato a Common Language Runtime è noto come codice gestito. Il codice che non ha come destinazione Common Language Runtime è noto come codice nativo.

La libreria di classi Framework è una raccolta completa e orientata a oggetti di classi riutilizzabili che è possibile usare per sviluppare applicazioni che vanno dalle tradizionali applicazioni della riga di comando o dell'interfaccia utente grafica (GUI) alle applicazioni basate sulle innovazioni più recenti fornite da ASP.NET e servizi Web.

La libreria gestita di Tablet PC contiene un set di oggetti gestiti che estende framework per fornire il supporto per l'input e l'output della grafia in Tablet PC, nonché l'interscambio dei dati con altri computer.

## <a name="exceptions"></a>Eccezioni

Gli oggetti della libreria gestita nell'API Tablet PC esegono il wrapping delle implementazioni della libreria COM. Quando l'oggetto o il controllo della libreria COM sottostante restituisce un errore, l'API gestita genererà un'eccezione Marshal.ThrowExceptionForHR che fornisce i dettagli sull'eccezione COM interna. È possibile fare riferimento ai valori HRESULT nelle informazioni di riferimento sulla libreria COM per informazioni dettagliate sui possibili errori che possono essere restituiti.

## <a name="object-comparison"></a>Confronto tra oggetti

Per tutti gli oggetti nella libreria gestita della piattaforma Tablet PC, [**equals**](/previous-versions/windows/) non viene sottoposto a override per confrontare correttamente due oggetti uguali. L'API (Application Programming Interface) gestita non supporta il confronto di oggetti per l'uguaglianza, tramite la funzione **Equals** o tramite l'operatore uguale a (==).

## <a name="binding-to-the-latest-microsoftinkdll"></a>Associazione alla versione più recente Microsoft.Ink.dll

L'assembly Microsoft.Ink.dll più recente è una sostituzione compatibile con Microsoft.Ink.dll versione 1.0 e Microsoft.Ink.15.dll. Nella maggior parte dei casi, non è necessario apportare modifiche alle applicazioni distribuite con gli assembly meno recenti. Tuttavia, in alcuni casi è necessario indicare al caricatore di Common Language Runtime di usare la libreria di collegamento dinamico (DLL) più recente, ovunque sia stato fatto riferimento alle DLL meno recenti.

L'unica volta che è necessario eseguire l'associazione in modo esplicito al nuovo assembly usando la tecnica seguente è se l'applicazione usa un componente che fa riferimento all'assembly della versione 1.0 o 1.5 in combinazione con un componente che fa riferimento a un assembly della versione più recente, ad esempio 1.7, e se tali componenti possono scambiare dati.

Il modo migliore per indicare al caricatore di Common Language Runtime di usare la DLL più recente è reindirizzare le versioni degli assembly a livello di applicazione. È possibile specificare che l'applicazione usi la versione più recente dell'assembly inserendo le informazioni di associazione dell'assembly nel file di configurazione dell'applicazione. Per altre informazioni sul reindirizzamento delle versioni degli assembly a livello di applicazione, vedere Reindirizzamento delle versioni degli [assembly,](/documentation/?url=%2flibrary%2fcpguide%2fhtml%2fcpconassemblyversionredirection.asp%3fframe%3dtrue)in particolare la sezione "Specifica dell'associazione di assembly nei file di configurazione".

Sarà necessario creare un file di configurazione nella stessa directory del file eseguibile. Il file di configurazione deve avere lo stesso nome dell'eseguibile, seguito dall'.config file. Ad esempio, per un'applicazione, MyApp.exe, il file di configurazione deve essere il file MyApp.exe.config. Il file di configurazione usa un [elemento bindingRedirect](/previous-versions/dotnet/netframework-1.1/eftw1fys(v=vs.71)) per forzare il mapping di tutte le versioni precedenti alla versione più recente, come illustrato nell'esempio seguente:

`<bindingRedirect oldVersion="0.0.0.0-1.7.2600.xxxx" newVersion="1.7.2600.xxxx" />`

Per altre informazioni sui file di configurazione, inclusi esempi di come costruire il Extensible Markup Language (XML) per il file di configurazione, vedere [bindingRedirect](/previous-versions/dotnet/netframework-1.1/eftw1fys(v=vs.71)) e Reindirizzamento delle versioni [degli assembly.](/documentation/?url=%2flibrary%2fcpguide%2fhtml%2fcpconassemblyversionredirection.asp%3fframe%3dtrue)

Le applicazioni create con Microsoft Windows XP Tablet PC Edition Development Kit 1.7 e versioni successive vengono associate automaticamente alla nuova versione dell'assembly Microsoft.Ink. Per altre informazioni sull'associazione di assembly, vedere [How the Runtime Locates Assemblies](/documentation/?url=%2flibrary%2fcpguide%2fhtml%2fcpconHowRuntimeLocatesAssemblies.asp).

> [!Note]  
> L'uso dei criteri dell'applicazione per l'associazione all'assembly aggiornato non funziona per le applicazioni che usano la [classe Divider](/previous-versions/ms583616(v=vs.100)) o [PenInputPanel.](/previous-versions/aa514041(v=msdn.10)) Le applicazioni che usano una di queste classi devono continuare a usare Microsoft.Ink.15.dll o essere ricompilate dopo aver fatto riferimento all'assembly aggiornato.

 

## <a name="working-with-events"></a>Uso degli eventi

Se il codice all'interno di un gestore eventi per uno degli oggetti gestiti genera un'eccezione, l'eccezione non viene recapitata all'utente. Per assicurarsi che le eccezioni siano recapitate, usare blocchi try-catch nei gestori eventi per gli eventi gestiti.

## <a name="managing-forms"></a>Gestione dei moduli

La [classe Form](/dotnet/api/system.windows.forms.form?view=netcore-3.1) e le relative classi base non definiscono un finalizzatore. Per pulire le risorse in un form, scrivere una sottoclasse che fornisce un finalizzatore (ad esempio, il distruttore C usando ~) che \# chiama [Dispose.](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) Per eseguire la pulizia, il finalizzatore esegue l'override di Dispose e quindi chiama la classe di base Dispose. Non fare riferimento ad altri oggetti che richiedono il metodo [Finalize](/previous-versions/windows/) nel metodo Dispose quando il parametro booleano è **FALSE,** perché tali oggetti potrebbero essere già stati finalizzati. Per altre informazioni sul rilascio delle risorse, vedere [Metodi Finalize e distruttori.](/documentation/?url=%2flibrary%2fcpguide%2fhtml%2fcpconfinalizemethodscdestructors.asp)

## <a name="forms-and-the-recognizercontext"></a>Moduli e RecognizerContext

[Gli eventi RecognizerContext](/previous-versions/ms552546(v=vs.100)) vengono eseguiti in un thread diverso da quello in cui si trova il modulo. I controlli Windows form sono associati a un thread specifico e non sono thread-safe. Pertanto, è necessario usare uno dei metodi invoke del controllo per effettuare il marshalling della chiamata al thread appropriato. Quattro metodi in un controllo sono thread-safe: [i](/dotnet/api/system.windows.forms.control.invoke?view=netcore-3.1)metodi Invoke , [BeginInvoke](/dotnet/api/system.windows.forms.control.begininvoke?view=netcore-3.1), [EndInvoke](/dotnet/api/system.windows.forms.control.endinvoke?view=netcore-3.1)e [CreateGraphics.](/dotnet/api/system.windows.forms.control.creategraphics?view=netcore-3.1) Per tutte le altre chiamate al metodo, usare uno di questi metodi invoke quando si chiama da un thread diverso. Per altre informazioni sull'uso di questi metodi, vedere [Modifica di controlli da thread.](/previous-versions/757y83z4(v=vs.140))

## <a name="waiting-for-events"></a>In attesa di eventi

L'ambiente Tablet PC è multithreading. Usare la funzione [**CoWaitForMultipleHandles**](/windows/win32/api/combaseapi/nf-combaseapi-cowaitformultiplehandles) invece di altri metodi di attesa per consentire alle chiamate Component Object Model (COM) di entrare nell'apartment multithreading (MTA) mentre l'applicazione è in attesa di un evento.

## <a name="using-ink-strokes-collections"></a>Uso delle raccolte di tratti input penna

Le istanze [delle raccolte Strokes](/previous-versions/ms552701(v=vs.100)) ottenute da un [oggetto Ink](/previous-versions/aa515768(v=msdn.10)) non vengono garbage collection. Per evitare una perdita di memoria, ogni volta che si usa una di queste raccolte, usare l'istruzione "using", come illustrato di seguito.


```C++
using (Strokes strokes = myInk.Strokes)
{
    int i = strokes.Count;
}
```



## <a name="disposing-managed-objects-and-controls"></a>Eliminazione di oggetti e controlli gestiti

Per evitare una perdita di memoria, è necessario chiamare in modo esplicito il metodo [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) su qualsiasi oggetto o controllo Tablet PC a cui è stato associato un gestore eventi prima che l'oggetto o il controllo eserne l'ambito.

Per migliorare le prestazioni dell'applicazione, eliminare manualmente gli oggetti, i controlli e la raccolta seguenti quando non sono più necessari.

-   [Divisore](/previous-versions/ms583616(v=vs.100))
-   [Input penna](/previous-versions/aa515768(v=msdn.10))
-   [Inkcollector](/previous-versions/ms583683(v=vs.100))
-   [Inkedit](/previous-versions/ms552265(v=vs.100))
-   [Inkoverlay](/previous-versions/ms552322(v=vs.100))
-   [Inkpicture](/previous-versions/aa514604(v=msdn.10))
-   [Peninputpanel](/previous-versions/aa514041(v=msdn.10))
-   [Recognizercontext](/previous-versions/ms552546(v=vs.100))
-   [Tratti](/previous-versions/ms552701(v=vs.100))

Nell'esempio C \# seguente vengono illustrati alcuni scenari in cui viene usato il metodo [Dispose.](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1)


```C++
// A field for a Divider object
private Microsoft.Ink.Divider theDivider;

// A method that creates a Divider object
public void CreateDivider()
{
    // Make sure any previous Divider object was disposed of.
    if (null != theDivider)
    {
        theDivider.Dispose();
        theDivider = null;
    }
    // Create the Divider object.
    theDivider = new Microsoft.Ink.Divider();

    // The remainder of the method
}

// A method that disposes of the Divider object
public void DisposeDivider()
{
    // The remainder of the method

    // Dispose of the Divider object.
    if (null != theDivider)
    {
        theDivider.Dispose();
        theDivider = null;
    }
}

// A method that uses a local PenInputPanel object.
public void UsePenInputPanel()
{
    // Create the PenInputPanel object.
    Microsoft.Ink.PenInputPanel thePenInputPanel =
        new Microsoft.Ink.PenInputPanel();

    // The remainder of the method

    // Dispose of the PenInputPanel object before exiting.
    thePenInputPanel.Dispose();
    thePenInputPanel = null;
}
```



 

 