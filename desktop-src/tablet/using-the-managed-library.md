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
# <a name="using-the-managed-library"></a><span data-ttu-id="573a3-103">Uso della libreria gestita</span><span class="sxs-lookup"><span data-stu-id="573a3-103">Using the Managed Library</span></span>

<span data-ttu-id="573a3-104">Il Common Language Runtime costituisce la base del Framework di Microsoft .NET.</span><span class="sxs-lookup"><span data-stu-id="573a3-104">The common language runtime is the foundation of the Microsoft .NET Framework.</span></span> <span data-ttu-id="573a3-105">È possibile considerare il Common Language Runtime come un agente che gestisce il codice in fase di esecuzione, fornendo servizi di base quali gestione della memoria, gestione di thread e servizi remoti, applicando allo stesso tempo una rigida sicurezza del codice.</span><span class="sxs-lookup"><span data-stu-id="573a3-105">You can think of the common language runtime as an agent that manages code at execution time, providing core services such as memory management, thread management, and remoting, while also enforcing strict code safety.</span></span> <span data-ttu-id="573a3-106">Il concetto di gestione del codice è infatti un principio fondamentale del Common Language Runtime.</span><span class="sxs-lookup"><span data-stu-id="573a3-106">In fact, the concept of code management is a fundamental principle of the common language runtime.</span></span> <span data-ttu-id="573a3-107">Il codice destinato al Common Language Runtime è noto come codice gestito.</span><span class="sxs-lookup"><span data-stu-id="573a3-107">Code that targets the common language runtime is known as managed code.</span></span> <span data-ttu-id="573a3-108">Il codice che non è destinato alla Common Language Runtime è noto come codice nativo.</span><span class="sxs-lookup"><span data-stu-id="573a3-108">Code that does not target the common language runtime is known as native code.</span></span>

<span data-ttu-id="573a3-109">La libreria di classi del Framework è una raccolta completa orientata agli oggetti di classi riutilizzabili che è possibile usare per sviluppare applicazioni che vanno dalle applicazioni tradizionali della riga di comando o dell'interfaccia utente grafica (GUI) a quelle basate sulle più recenti innovazioni offerte da ASP.NET e dai servizi Web.</span><span class="sxs-lookup"><span data-stu-id="573a3-109">The Framework class library is a comprehensive, object-oriented collection of reusable classes that you can use to develop applications ranging from traditional command-line or graphical user interface (GUI) applications to applications based on the latest innovations provided by ASP.NET and Web Services.</span></span>

<span data-ttu-id="573a3-110">La libreria gestita da Tablet PC contiene un set di oggetti gestiti che estende il Framework per fornire supporto per l'input e l'output della grafia nei tablet PC e per l'interscambio dei dati con altri computer.</span><span class="sxs-lookup"><span data-stu-id="573a3-110">The Tablet PC Managed Library contains a set of managed objects that extends the Framework to provide support for input and output of handwriting on Tablet PC as well as data interchange with other computers.</span></span>

## <a name="exceptions"></a><span data-ttu-id="573a3-111">Eccezioni</span><span class="sxs-lookup"><span data-stu-id="573a3-111">Exceptions</span></span>

<span data-ttu-id="573a3-112">Gli oggetti libreria gestita nell'API Tablet PC incapsulano le implementazioni della libreria COM.</span><span class="sxs-lookup"><span data-stu-id="573a3-112">The managed library objects in the Tablet PC API wrap the COM library implementations.</span></span> <span data-ttu-id="573a3-113">Quando l'oggetto o il controllo della libreria COM sottostante restituisce un errore, l'API gestita genererà un'eccezione Marshal. ThrowExceptionForHR che fornisce i dettagli sull'eccezione COM interna.</span><span class="sxs-lookup"><span data-stu-id="573a3-113">When the underlying COM library object or control returns an error, the managed API's will throw a Marshal.ThrowExceptionForHR exception that provides the details on the inner COM exception.</span></span> <span data-ttu-id="573a3-114">Per informazioni dettagliate sui possibili errori che possono essere restituiti, è possibile fare riferimento ai valori HRESULT nei riferimenti alla libreria COM.</span><span class="sxs-lookup"><span data-stu-id="573a3-114">You can refer to the HRESULT values in the COM Library Reference for details on the possible errors that may be returned.</span></span>

## <a name="object-comparison"></a><span data-ttu-id="573a3-115">Confronto di oggetti</span><span class="sxs-lookup"><span data-stu-id="573a3-115">Object Comparison</span></span>

<span data-ttu-id="573a3-116">Per tutti gli oggetti della libreria gestita della piattaforma Tablet PC, non viene eseguito l'override di [**Equals**](/previous-versions/windows/) per confrontare correttamente due oggetti uguali.</span><span class="sxs-lookup"><span data-stu-id="573a3-116">For all objects in the Tablet PC Platform Managed library, [**Equals**](/previous-versions/windows/) is not overridden to correctly compare two objects that are the same.</span></span> <span data-ttu-id="573a3-117">Il Application Programming Interface gestito (API) non supporta il confronto degli oggetti per verificarne l'uguaglianza, tramite la funzione **Equals** o tramite l'operatore Equals (= =).</span><span class="sxs-lookup"><span data-stu-id="573a3-117">The managed application programming interface (API) does not support the comparison of objects for equality, either through the **Equals** function or through the equals (==) operator.</span></span>

## <a name="binding-to-the-latest-microsoftinkdll"></a><span data-ttu-id="573a3-118">Associazione alla Microsoft.Ink.dll più recente</span><span class="sxs-lookup"><span data-stu-id="573a3-118">Binding to the Latest Microsoft.Ink.dll</span></span>

<span data-ttu-id="573a3-119">L'assembly Microsoft.Ink.dll più recente è una sostituzione compatibile per Microsoft.Ink.dll versione 1,0 e Microsoft.Ink.15.dll.</span><span class="sxs-lookup"><span data-stu-id="573a3-119">The latest Microsoft.Ink.dll assembly is a compatible replacement for Microsoft.Ink.dll version 1.0 and Microsoft.Ink.15.dll.</span></span> <span data-ttu-id="573a3-120">Nella maggior parte dei casi, non è necessario apportare modifiche alle applicazioni distribuite con gli assembly precedenti.</span><span class="sxs-lookup"><span data-stu-id="573a3-120">In most cases, you do not need to make any changes to your applications that are distributed with the older assemblies.</span></span> <span data-ttu-id="573a3-121">Tuttavia, in alcuni casi è necessario indicare all'Common Language Runtime Loader di utilizzare la libreria di collegamento dinamico (DLL) più recente, in cui è stato fatto riferimento alle DLL precedenti.</span><span class="sxs-lookup"><span data-stu-id="573a3-121">However, in some cases you need to instruct the common language runtime loader to use the newer dynamic-link library (DLL) wherever the older DLLs have been referenced.</span></span>

<span data-ttu-id="573a3-122">L'unico momento in cui è necessario eseguire l'associazione esplicita al nuovo assembly usando la tecnica seguente è se l'applicazione usa un componente che fa riferimento all'assembly versione 1,0 o 1,5 insieme a un componente che fa riferimento a un assembly di versione più recente, ad esempio 1,7, e se tali componenti possono scambiare dati.</span><span class="sxs-lookup"><span data-stu-id="573a3-122">The only time you need to explicitly bind to the new assembly by using the following technique is if your application uses a component that references the version 1.0 or 1.5 assembly in combination with a component that references a more recent version assembly,such as 1.7, and if those components may exchange data.</span></span>

<span data-ttu-id="573a3-123">Il modo migliore per indicare al caricatore Common Language Runtime di usare la DLL più recente consiste nel reindirizzare le versioni degli assembly a livello di applicazione.</span><span class="sxs-lookup"><span data-stu-id="573a3-123">The best way to instruct the common language runtime loader to use the newer DLL is to redirect assembly versions at the application level.</span></span> <span data-ttu-id="573a3-124">È possibile specificare che l'applicazione usi la versione più recente dell'assembly inserendo le informazioni di associazione dell'assembly nel file di configurazione dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="573a3-124">You can specify that your application use the newer version of the assembly by putting assembly binding information in your application's configuration file.</span></span> <span data-ttu-id="573a3-125">Per ulteriori informazioni sul reindirizzamento delle versioni di assembly a livello di applicazione, vedere [Reindirizzamento delle versioni di assembly](/documentation/?url=%2flibrary%2fcpguide%2fhtml%2fcpconassemblyversionredirection.asp%3fframe%3dtrue), in particolare la sezione "specifica dell'associazione di assembly nei file di configurazione".</span><span class="sxs-lookup"><span data-stu-id="573a3-125">For more information about redirecting assembly versions at the application level, see [Redirecting Assembly Versions](/documentation/?url=%2flibrary%2fcpguide%2fhtml%2fcpconassemblyversionredirection.asp%3fframe%3dtrue), specifically the section "Specifying Assembly Binding in Configuration Files."</span></span>

<span data-ttu-id="573a3-126">Sarà necessario creare un file di configurazione nella stessa directory del file eseguibile.</span><span class="sxs-lookup"><span data-stu-id="573a3-126">You will need to create a configuration file in the same directory as your executable file.</span></span> <span data-ttu-id="573a3-127">Il file di configurazione deve avere lo stesso nome del file eseguibile, seguito dall'estensione config.</span><span class="sxs-lookup"><span data-stu-id="573a3-127">The configuration file must have the same name as your executable, followed by the .config file extension.</span></span> <span data-ttu-id="573a3-128">Ad esempio, per un'applicazione MyApp.exe, il file di configurazione deve essere il file di MyApp.exe.config.</span><span class="sxs-lookup"><span data-stu-id="573a3-128">For example, for an application, MyApp.exe, the configuration file must be the MyApp.exe.config file.</span></span> <span data-ttu-id="573a3-129">Il file di configurazione usa un elemento [bindingRedirect](/previous-versions/dotnet/netframework-1.1/eftw1fys(v=vs.71)) per forzare il mapping di tutte le versioni precedenti alla versione più recente, come illustrato nell'esempio seguente:</span><span class="sxs-lookup"><span data-stu-id="573a3-129">The configuration file uses a [bindingRedirect](/previous-versions/dotnet/netframework-1.1/eftw1fys(v=vs.71)) element to force all prior versions to be mapped to the latest version, as shown in the following example:</span></span>

`<bindingRedirect oldVersion="0.0.0.0-1.7.2600.xxxx" newVersion="1.7.2600.xxxx" />`

<span data-ttu-id="573a3-130">Per ulteriori informazioni sui file di configurazione, inclusi esempi di come costruire il Extensible Markup Language (XML) per il file di configurazione, vedere [bindingRedirect](/previous-versions/dotnet/netframework-1.1/eftw1fys(v=vs.71)) e [Reindirizzamento delle versioni degli assembly](/documentation/?url=%2flibrary%2fcpguide%2fhtml%2fcpconassemblyversionredirection.asp%3fframe%3dtrue).</span><span class="sxs-lookup"><span data-stu-id="573a3-130">For more information about configuration files, including examples of how to construct the Extensible Markup Language (XML) for the configuration file, see both [bindingRedirect](/previous-versions/dotnet/netframework-1.1/eftw1fys(v=vs.71)) and [Redirecting Assembly Versions](/documentation/?url=%2flibrary%2fcpguide%2fhtml%2fcpconassemblyversionredirection.asp%3fframe%3dtrue).</span></span>

<span data-ttu-id="573a3-131">Le applicazioni create con Microsoft Windows XP Tablet PC Edition Development Kit 1,7 e versioni successive vengono associate automaticamente alla nuova versione dell'assembly Microsoft. Ink.</span><span class="sxs-lookup"><span data-stu-id="573a3-131">Applications created with Microsoft Windows XP Tablet PC Edition Development Kit 1.7 and later versions are automatically bound to the new version of the Microsoft.Ink assembly.</span></span> <span data-ttu-id="573a3-132">Per ulteriori informazioni sull'associazione di assembly [, vedere come il runtime individua gli assembly](/documentation/?url=%2flibrary%2fcpguide%2fhtml%2fcpconHowRuntimeLocatesAssemblies.asp).</span><span class="sxs-lookup"><span data-stu-id="573a3-132">For more information about assembly binding see [How the Runtime Locates Assemblies](/documentation/?url=%2flibrary%2fcpguide%2fhtml%2fcpconHowRuntimeLocatesAssemblies.asp).</span></span>

> [!Note]  
> <span data-ttu-id="573a3-133">L'uso di criteri di applicazione per l'associazione all'assembly aggiornato non funziona per le applicazioni che usano la classe [divisore](/previous-versions/ms583616(v=vs.100)) o la classe [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="573a3-133">Using application policy to bind to the updated assembly does not work for applications that use the [Divider](/previous-versions/ms583616(v=vs.100)) class or the [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) class.</span></span> <span data-ttu-id="573a3-134">Le applicazioni che usano una di queste classi devono continuare a usare Microsoft.Ink.15.dll o essere ricompilate dopo aver fatto riferimento all'assembly aggiornato.</span><span class="sxs-lookup"><span data-stu-id="573a3-134">Applications that use either of those classes must either continue to use Microsoft.Ink.15.dll or be recompiled after referencing the updated assembly.</span></span>

 

## <a name="working-with-events"></a><span data-ttu-id="573a3-135">Utilizzo degli eventi</span><span class="sxs-lookup"><span data-stu-id="573a3-135">Working with Events</span></span>

<span data-ttu-id="573a3-136">Se il codice all'interno di un gestore eventi per uno degli oggetti gestiti genera un'eccezione, l'eccezione non viene recapitata all'utente.</span><span class="sxs-lookup"><span data-stu-id="573a3-136">If the code within an event handler for any of the managed objects throws an exception, the exception is not delivered to the user.</span></span> <span data-ttu-id="573a3-137">Per assicurarsi che le eccezioni vengano recapitate, usare blocchi try-catch nei gestori eventi per gli eventi gestiti.</span><span class="sxs-lookup"><span data-stu-id="573a3-137">To ensure that exceptions are delivered, use try-catch blocks in your event handlers for managed events.</span></span>

## <a name="managing-forms"></a><span data-ttu-id="573a3-138">Gestione dei moduli</span><span class="sxs-lookup"><span data-stu-id="573a3-138">Managing Forms</span></span>

<span data-ttu-id="573a3-139">La classe del [form](/dotnet/api/system.windows.forms.form?view=netcore-3.1) e le relative classi base non definiscono un finalizzatore.</span><span class="sxs-lookup"><span data-stu-id="573a3-139">The [Form](/dotnet/api/system.windows.forms.form?view=netcore-3.1) class and its base classes do not define a finalizer.</span></span> <span data-ttu-id="573a3-140">Per pulire le risorse in un form, scrivere una sottoclasse che fornisca un finalizzatore (ad esempio, il \# distruttore C usando il ~) che chiama [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1).</span><span class="sxs-lookup"><span data-stu-id="573a3-140">To clean up your resources on a form, write a subclass that provides a finalizer (for example, the C\# destructor using the ~) that calls [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1).</span></span> <span data-ttu-id="573a3-141">Per eseguire la pulizia, il finalizzatore esegue l'override di Dispose e quindi chiama la classe di base Dispose.</span><span class="sxs-lookup"><span data-stu-id="573a3-141">To do the cleanup the finalizer overrides Dispose and then calls the base class Dispose.</span></span> <span data-ttu-id="573a3-142">Non fare riferimento ad altri oggetti che richiedono il metodo [Finalize](/previous-versions/windows/) nel metodo Dispose quando il parametro booleano è **false**, perché tali oggetti potrebbero essere già stati finalizzati.</span><span class="sxs-lookup"><span data-stu-id="573a3-142">Do not refer to other objects that require the [Finalize](/previous-versions/windows/) method in the Dispose method when the Boolean parameter is **FALSE**, because those objects may already have been finalized.</span></span> <span data-ttu-id="573a3-143">Per ulteriori informazioni sul rilascio di risorse, vedere [Finalize Methods and destructrs](/documentation/?url=%2flibrary%2fcpguide%2fhtml%2fcpconfinalizemethodscdestructors.asp).</span><span class="sxs-lookup"><span data-stu-id="573a3-143">For more information about releasing resources see [Finalize Methods and Destructors](/documentation/?url=%2flibrary%2fcpguide%2fhtml%2fcpconfinalizemethodscdestructors.asp).</span></span>

## <a name="forms-and-the-recognizercontext"></a><span data-ttu-id="573a3-144">Form e RecognizerContext</span><span class="sxs-lookup"><span data-stu-id="573a3-144">Forms and the RecognizerContext</span></span>

<span data-ttu-id="573a3-145">Gli eventi [RecognizerContext](/previous-versions/ms552546(v=vs.100)) vengono eseguiti in un thread diverso rispetto al thread su cui si trova il form.</span><span class="sxs-lookup"><span data-stu-id="573a3-145">[RecognizerContext](/previous-versions/ms552546(v=vs.100)) events run in a different thread than the thread that the form is on.</span></span> <span data-ttu-id="573a3-146">I controlli in Windows Form sono associati a un thread specifico e non sono thread-safe.</span><span class="sxs-lookup"><span data-stu-id="573a3-146">Controls in Windows Forms are bound to a specific thread and are not thread safe.</span></span> <span data-ttu-id="573a3-147">Pertanto, è necessario utilizzare uno dei metodi Invoke del controllo per effettuare il marshalling della chiamata al thread appropriato.</span><span class="sxs-lookup"><span data-stu-id="573a3-147">Therefore, you must use one of the control's invoke methods to marshal the call to the proper thread.</span></span> <span data-ttu-id="573a3-148">Quattro metodi su un controllo sono thread-safe: i metodi [Invoke](/dotnet/api/system.windows.forms.control.invoke?view=netcore-3.1), [BeginInvoke](/dotnet/api/system.windows.forms.control.begininvoke?view=netcore-3.1), [EndInvoke](/dotnet/api/system.windows.forms.control.endinvoke?view=netcore-3.1)e [CreateGraphics](/dotnet/api/system.windows.forms.control.creategraphics?view=netcore-3.1) .</span><span class="sxs-lookup"><span data-stu-id="573a3-148">Four methods on a control are thread safe: the [Invoke](/dotnet/api/system.windows.forms.control.invoke?view=netcore-3.1), [BeginInvoke](/dotnet/api/system.windows.forms.control.begininvoke?view=netcore-3.1), [EndInvoke](/dotnet/api/system.windows.forms.control.endinvoke?view=netcore-3.1), and [CreateGraphics](/dotnet/api/system.windows.forms.control.creategraphics?view=netcore-3.1) methods.</span></span> <span data-ttu-id="573a3-149">Per tutte le altre chiamate al metodo, usare uno di questi metodi Invoke quando si chiama da un thread diverso.</span><span class="sxs-lookup"><span data-stu-id="573a3-149">For all other method calls, use one of these invoke methods when calling from a different thread.</span></span> <span data-ttu-id="573a3-150">Per altre informazioni sull'uso di questi metodi, vedere [manipolazione dei controlli dai thread](/previous-versions/757y83z4(v=vs.140)).</span><span class="sxs-lookup"><span data-stu-id="573a3-150">For more information on using these methods, see [Manipulating Controls from Threads](/previous-versions/757y83z4(v=vs.140)).</span></span>

## <a name="waiting-for-events"></a><span data-ttu-id="573a3-151">In attesa di eventi</span><span class="sxs-lookup"><span data-stu-id="573a3-151">Waiting for Events</span></span>

<span data-ttu-id="573a3-152">L'ambiente Tablet PC è multithreading.</span><span class="sxs-lookup"><span data-stu-id="573a3-152">The Tablet PC environment is multithreaded.</span></span> <span data-ttu-id="573a3-153">Usare la funzione [**CoWaitForMultipleHandles**](/windows/win32/api/combaseapi/nf-combaseapi-cowaitformultiplehandles) anziché altri metodi di attesa per consentire alle chiamate Component Object Model (com) rientranti di immettere l'Apartment a thread multipli (MTA) mentre l'applicazione è in attesa di un evento.</span><span class="sxs-lookup"><span data-stu-id="573a3-153">Use the [**CoWaitForMultipleHandles**](/windows/win32/api/combaseapi/nf-combaseapi-cowaitformultiplehandles) function instead of other wait methods to allow re-entrant Component Object Model (COM) calls to enter your multithreaded apartment (MTA) while your application is waiting on an event.</span></span>

## <a name="using-ink-strokes-collections"></a><span data-ttu-id="573a3-154">Uso delle raccolte di tratti di input penna</span><span class="sxs-lookup"><span data-stu-id="573a3-154">Using Ink Strokes Collections</span></span>

<span data-ttu-id="573a3-155">Le istanze delle raccolte [Strokes](/previous-versions/ms552701(v=vs.100)) ottenute da un oggetto [Ink](/previous-versions/aa515768(v=msdn.10)) non vengono sottoposte al Garbage Collector.</span><span class="sxs-lookup"><span data-stu-id="573a3-155">Instances of [Strokes](/previous-versions/ms552701(v=vs.100)) collections which are obtained from an [Ink](/previous-versions/aa515768(v=msdn.10)) object are not garbage collected.</span></span> <span data-ttu-id="573a3-156">Per evitare una perdita di memoria, ogni volta che si utilizza una di queste raccolte, utilizzare l'istruzione "using" come illustrato di seguito.</span><span class="sxs-lookup"><span data-stu-id="573a3-156">In order to avoid a memory leak, any time that you are working with one of these collections, make use of the "using" statement as shown below.</span></span>


```C++
using (Strokes strokes = myInk.Strokes)
{
    int i = strokes.Count;
}
```



## <a name="disposing-managed-objects-and-controls"></a><span data-ttu-id="573a3-157">Eliminazione di oggetti e controlli gestiti</span><span class="sxs-lookup"><span data-stu-id="573a3-157">Disposing Managed Objects and Controls</span></span>

<span data-ttu-id="573a3-158">Per evitare una perdita di memoria, è necessario chiamare in modo esplicito il metodo [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) su qualsiasi oggetto o controllo di Tablet PC a cui è stato collegato un gestore eventi prima che l'oggetto o il controllo esca dall'ambito.</span><span class="sxs-lookup"><span data-stu-id="573a3-158">To avoid a memory leak you must explicitly call the [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) method on any Tablet PC object or control to which an event handler has been attached before the object or control goes out of scope.</span></span>

<span data-ttu-id="573a3-159">Per migliorare le prestazioni dell'applicazione, eliminare manualmente gli oggetti, i controlli e la raccolta seguenti quando non sono più necessari.</span><span class="sxs-lookup"><span data-stu-id="573a3-159">To improve the performance of your application, manually dispose of the following objects, controls, and collection when they are no longer needed.</span></span>

-   <span data-ttu-id="573a3-160">[Divisore](/previous-versions/ms583616(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="573a3-160">[Divider](/previous-versions/ms583616(v=vs.100))</span></span>
-   <span data-ttu-id="573a3-161">[Input penna](/previous-versions/aa515768(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="573a3-161">[Ink](/previous-versions/aa515768(v=msdn.10))</span></span>
-   <span data-ttu-id="573a3-162">[InkCollector](/previous-versions/ms583683(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="573a3-162">[InkCollector](/previous-versions/ms583683(v=vs.100))</span></span>
-   <span data-ttu-id="573a3-163">[InkEdit](/previous-versions/ms552265(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="573a3-163">[InkEdit](/previous-versions/ms552265(v=vs.100))</span></span>
-   <span data-ttu-id="573a3-164">[InkOverlay](/previous-versions/ms552322(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="573a3-164">[InkOverlay](/previous-versions/ms552322(v=vs.100))</span></span>
-   <span data-ttu-id="573a3-165">[InkPicture](/previous-versions/aa514604(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="573a3-165">[InkPicture](/previous-versions/aa514604(v=msdn.10))</span></span>
-   <span data-ttu-id="573a3-166">[PenInputPanel](/previous-versions/aa514041(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="573a3-166">[PenInputPanel](/previous-versions/aa514041(v=msdn.10))</span></span>
-   <span data-ttu-id="573a3-167">[RecognizerContext](/previous-versions/ms552546(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="573a3-167">[RecognizerContext](/previous-versions/ms552546(v=vs.100))</span></span>
-   <span data-ttu-id="573a3-168">[Tratti](/previous-versions/ms552701(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="573a3-168">[Strokes](/previous-versions/ms552701(v=vs.100))</span></span>

<span data-ttu-id="573a3-169">Nell'esempio C riportato \# di seguito vengono illustrati alcuni scenari in cui viene utilizzato il metodo [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) .</span><span class="sxs-lookup"><span data-stu-id="573a3-169">The following C\# example demonstrates some scenarios in which the [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) method is used.</span></span>


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



 

 