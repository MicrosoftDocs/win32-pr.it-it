---
description: Cenni preliminari sulla libreria gestita e sulle note sull'utilizzo della libreria gestita della piattaforma Tablet PC.
ms.assetid: d283ea1c-faf3-4222-a9a7-c67087636b86
title: Uso della libreria gestita
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b1a1050705a6d74e6b183d04ec1c8f82d3954f0
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "106320265"
---
# <a name="using-the-managed-library"></a>Uso della libreria gestita

Il Common Language Runtime costituisce la base del Framework di Microsoft .NET. È possibile considerare il Common Language Runtime come un agente che gestisce il codice in fase di esecuzione, fornendo servizi di base quali gestione della memoria, gestione di thread e servizi remoti, applicando allo stesso tempo una rigida sicurezza del codice. Il concetto di gestione del codice è infatti un principio fondamentale del Common Language Runtime. Il codice destinato al Common Language Runtime è noto come codice gestito. Il codice che non è destinato alla Common Language Runtime è noto come codice nativo.

La libreria di classi del Framework è una raccolta completa orientata agli oggetti di classi riutilizzabili che è possibile usare per sviluppare applicazioni che vanno dalle applicazioni tradizionali della riga di comando o dell'interfaccia utente grafica (GUI) a quelle basate sulle più recenti innovazioni offerte da ASP.NET e dai servizi Web.

La libreria gestita da Tablet PC contiene un set di oggetti gestiti che estende il Framework per fornire supporto per l'input e l'output della grafia nei tablet PC e per l'interscambio dei dati con altri computer.

## <a name="exceptions"></a>Eccezioni

Gli oggetti libreria gestita nell'API Tablet PC incapsulano le implementazioni della libreria COM. Quando l'oggetto o il controllo della libreria COM sottostante restituisce un errore, l'API gestita genererà un'eccezione Marshal. ThrowExceptionForHR che fornisce i dettagli sull'eccezione COM interna. Per informazioni dettagliate sui possibili errori che possono essere restituiti, è possibile fare riferimento ai valori HRESULT nei riferimenti alla libreria COM.

## <a name="object-comparison"></a>Confronto di oggetti

Per tutti gli oggetti della libreria gestita della piattaforma Tablet PC, non viene eseguito l'override di [**Equals**](/previous-versions/windows/) per confrontare correttamente due oggetti uguali. Il Application Programming Interface gestito (API) non supporta il confronto degli oggetti per verificarne l'uguaglianza, tramite la funzione **Equals** o tramite l'operatore Equals (= =).

## <a name="binding-to-the-latest-microsoftinkdll"></a>Associazione alla Microsoft.Ink.dll più recente

L'assembly Microsoft.Ink.dll più recente è una sostituzione compatibile per Microsoft.Ink.dll versione 1,0 e Microsoft.Ink.15.dll. Nella maggior parte dei casi, non è necessario apportare modifiche alle applicazioni distribuite con gli assembly precedenti. Tuttavia, in alcuni casi è necessario indicare all'Common Language Runtime Loader di utilizzare la libreria di collegamento dinamico (DLL) più recente, in cui è stato fatto riferimento alle DLL precedenti.

L'unico momento in cui è necessario eseguire l'associazione esplicita al nuovo assembly usando la tecnica seguente è se l'applicazione usa un componente che fa riferimento all'assembly versione 1,0 o 1,5 insieme a un componente che fa riferimento a un assembly di versione più recente, ad esempio 1,7, e se tali componenti possono scambiare dati.

Il modo migliore per indicare al caricatore Common Language Runtime di usare la DLL più recente consiste nel reindirizzare le versioni degli assembly a livello di applicazione. È possibile specificare che l'applicazione usi la versione più recente dell'assembly inserendo le informazioni di associazione dell'assembly nel file di configurazione dell'applicazione. Per ulteriori informazioni sul reindirizzamento delle versioni di assembly a livello di applicazione, vedere [Reindirizzamento delle versioni di assembly](/documentation/?url=%2flibrary%2fcpguide%2fhtml%2fcpconassemblyversionredirection.asp%3fframe%3dtrue), in particolare la sezione "specifica dell'associazione di assembly nei file di configurazione".

Sarà necessario creare un file di configurazione nella stessa directory del file eseguibile. Il file di configurazione deve avere lo stesso nome del file eseguibile, seguito dall'estensione config. Ad esempio, per un'applicazione MyApp.exe, il file di configurazione deve essere il file di MyApp.exe.config. Il file di configurazione usa un elemento [bindingRedirect](/previous-versions/dotnet/netframework-1.1/eftw1fys(v=vs.71)) per forzare il mapping di tutte le versioni precedenti alla versione più recente, come illustrato nell'esempio seguente:

`<bindingRedirect oldVersion="0.0.0.0-1.7.2600.xxxx" newVersion="1.7.2600.xxxx" />`

Per ulteriori informazioni sui file di configurazione, inclusi esempi di come costruire il Extensible Markup Language (XML) per il file di configurazione, vedere [bindingRedirect](/previous-versions/dotnet/netframework-1.1/eftw1fys(v=vs.71)) e [Reindirizzamento delle versioni degli assembly](/documentation/?url=%2flibrary%2fcpguide%2fhtml%2fcpconassemblyversionredirection.asp%3fframe%3dtrue).

Le applicazioni create con Microsoft Windows XP Tablet PC Edition Development Kit 1,7 e versioni successive vengono associate automaticamente alla nuova versione dell'assembly Microsoft. Ink. Per ulteriori informazioni sull'associazione di assembly [, vedere come il runtime individua gli assembly](/documentation/?url=%2flibrary%2fcpguide%2fhtml%2fcpconHowRuntimeLocatesAssemblies.asp).

> [!Note]  
> L'uso di criteri di applicazione per l'associazione all'assembly aggiornato non funziona per le applicazioni che usano la classe [divisore](/previous-versions/ms583616(v=vs.100)) o la classe [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) . Le applicazioni che usano una di queste classi devono continuare a usare Microsoft.Ink.15.dll o essere ricompilate dopo aver fatto riferimento all'assembly aggiornato.

 

## <a name="working-with-events"></a>Utilizzo degli eventi

Se il codice all'interno di un gestore eventi per uno degli oggetti gestiti genera un'eccezione, l'eccezione non viene recapitata all'utente. Per assicurarsi che le eccezioni vengano recapitate, usare blocchi try-catch nei gestori eventi per gli eventi gestiti.

## <a name="managing-forms"></a>Gestione dei moduli

La classe del [form](/dotnet/api/system.windows.forms.form?view=netcore-3.1) e le relative classi base non definiscono un finalizzatore. Per pulire le risorse in un form, scrivere una sottoclasse che fornisca un finalizzatore (ad esempio, il \# distruttore C usando il ~) che chiama [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1). Per eseguire la pulizia, il finalizzatore esegue l'override di Dispose e quindi chiama la classe di base Dispose. Non fare riferimento ad altri oggetti che richiedono il metodo [Finalize](/previous-versions/windows/) nel metodo Dispose quando il parametro booleano è **false**, perché tali oggetti potrebbero essere già stati finalizzati. Per ulteriori informazioni sul rilascio di risorse, vedere [Finalize Methods and destructrs](/documentation/?url=%2flibrary%2fcpguide%2fhtml%2fcpconfinalizemethodscdestructors.asp).

## <a name="forms-and-the-recognizercontext"></a>Form e RecognizerContext

Gli eventi [RecognizerContext](/previous-versions/ms552546(v=vs.100)) vengono eseguiti in un thread diverso rispetto al thread su cui si trova il form. I controlli in Windows Form sono associati a un thread specifico e non sono thread-safe. Pertanto, è necessario utilizzare uno dei metodi Invoke del controllo per effettuare il marshalling della chiamata al thread appropriato. Quattro metodi su un controllo sono thread-safe: i metodi [Invoke](/dotnet/api/system.windows.forms.control.invoke?view=netcore-3.1), [BeginInvoke](/dotnet/api/system.windows.forms.control.begininvoke?view=netcore-3.1), [EndInvoke](/dotnet/api/system.windows.forms.control.endinvoke?view=netcore-3.1)e [CreateGraphics](/dotnet/api/system.windows.forms.control.creategraphics?view=netcore-3.1) . Per tutte le altre chiamate al metodo, usare uno di questi metodi Invoke quando si chiama da un thread diverso. Per altre informazioni sull'uso di questi metodi, vedere [manipolazione dei controlli dai thread](/previous-versions/757y83z4(v=vs.140)).

## <a name="waiting-for-events"></a>In attesa di eventi

L'ambiente Tablet PC è multithreading. Usare la funzione [**CoWaitForMultipleHandles**](/windows/win32/api/combaseapi/nf-combaseapi-cowaitformultiplehandles) anziché altri metodi di attesa per consentire alle chiamate Component Object Model (com) rientranti di immettere l'Apartment a thread multipli (MTA) mentre l'applicazione è in attesa di un evento.

## <a name="using-ink-strokes-collections"></a>Uso delle raccolte di tratti di input penna

Le istanze delle raccolte [Strokes](/previous-versions/ms552701(v=vs.100)) ottenute da un oggetto [Ink](/previous-versions/aa515768(v=msdn.10)) non vengono sottoposte al Garbage Collector. Per evitare una perdita di memoria, ogni volta che si utilizza una di queste raccolte, utilizzare l'istruzione "using" come illustrato di seguito.


```C++
using (Strokes strokes = myInk.Strokes)
{
    int i = strokes.Count;
}
```



## <a name="disposing-managed-objects-and-controls"></a>Eliminazione di oggetti e controlli gestiti

Per evitare una perdita di memoria, è necessario chiamare in modo esplicito il metodo [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) su qualsiasi oggetto o controllo di Tablet PC a cui è stato collegato un gestore eventi prima che l'oggetto o il controllo esca dall'ambito.

Per migliorare le prestazioni dell'applicazione, eliminare manualmente gli oggetti, i controlli e la raccolta seguenti quando non sono più necessari.

-   [Divisore](/previous-versions/ms583616(v=vs.100))
-   [Input penna](/previous-versions/aa515768(v=msdn.10))
-   [InkCollector](/previous-versions/ms583683(v=vs.100))
-   [InkEdit](/previous-versions/ms552265(v=vs.100))
-   [InkOverlay](/previous-versions/ms552322(v=vs.100))
-   [InkPicture](/previous-versions/aa514604(v=msdn.10))
-   [PenInputPanel](/previous-versions/aa514041(v=msdn.10))
-   [RecognizerContext](/previous-versions/ms552546(v=vs.100))
-   [Tratti](/previous-versions/ms552701(v=vs.100))

Nell'esempio C riportato \# di seguito vengono illustrati alcuni scenari in cui viene utilizzato il metodo [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) .


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



 

 